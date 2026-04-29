# Ejercicio 12 de JavaScript — Proyecto integrador

## Enunciado

Vamos a crear un buscador de usuarios de GitHub que combine todo lo aprendido en el capítulo: fetch, async/await, DOM, eventos, localStorage e Intl.

## Solución

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Buscador de GitHub</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Buscador de usuarios de GitHub</h1>

    <div class="buscador">
      <input type="text" id="campo-busqueda" placeholder="Nombre de usuario..." />
      <button id="btn-buscar">Buscar</button>
    </div>

    <div id="busquedas-recientes"></div>
    <div id="resultado"></div>

    <script src="app.js"></script>
  </body>
</html>
```

**app.js**

```javascript
const campoBusqueda = document.querySelector('#campo-busqueda');
const btnBuscar = document.querySelector('#btn-buscar');
const resultado = document.querySelector('#resultado');
const busquedasRecientes = document.querySelector('#busquedas-recientes');

// Guardar búsqueda en localStorage
function guardarBusqueda(username) {
  const recientes = JSON.parse(localStorage.getItem('busquedasRecientes') || '[]');

  // Evitar duplicados
  const sinDuplicados = recientes.filter(u => u !== username);

  // Mantener solo los últimos 5
  const actualizados = [username, ...sinDuplicados].slice(0, 5);

  localStorage.setItem('busquedasRecientes', JSON.stringify(actualizados));
  mostrarBusquedasRecientes();
}

// Mostrar búsquedas recientes
function mostrarBusquedasRecientes() {
  const recientes = JSON.parse(localStorage.getItem('busquedasRecientes') || '[]');

  if (recientes.length === 0) {
    busquedasRecientes.innerHTML = '';
    return;
  }

  busquedasRecientes.innerHTML = `
    <h2>Búsquedas recientes</h2>
    <ul>
      ${recientes.map(u => `<li><button class="btn-reciente">${u}</button></li>`).join('')}
    </ul>
  `;

  // Añadir eventos a los botones de búsquedas recientes
  document.querySelectorAll('.btn-reciente').forEach(btn => {
    btn.addEventListener('click', () => {
      campoBusqueda.value = btn.textContent;
      buscarUsuario(btn.textContent);
    });
  });
}

// Buscar usuario en la API de GitHub
async function buscarUsuario(username) {
  resultado.innerHTML = '<p>Buscando...</p>';

  try {
    const response = await fetch(`https://api.github.com/users/${username}`);

    if (response.status === 404) {
      resultado.innerHTML = `<p class="error">No se ha encontrado ningún usuario con el nombre "${username}"</p>`;
      return;
    }

    if (!response.ok) {
      throw new Error(`Error HTTP: ${response.status}`);
    }

    const {
      name,
      login,
      bio,
      avatar_url,
      public_repos,
      followers,
      html_url,
      created_at
    } = await response.json();

    const fechaRegistro = new Intl.DateTimeFormat('es-ES', {
      dateStyle: 'long'
    }).format(new Date(created_at));

    resultado.innerHTML = `
      <article class="tarjeta-usuario">
        <img src="${avatar_url}" alt="Avatar de ${login}" />
        <div class="info">
          <h2>${name || login}</h2>
          <p class="username">@${login}</p>
          ${bio ? `<p class="bio">${bio}</p>` : ''}
          <ul class="stats">
            <li>📦 ${public_repos} repositorios</li>
            <li>👥 ${followers} seguidores</li>
            <li>📅 Miembro desde ${fechaRegistro}</li>
          </ul>
          <a href="${html_url}" target="_blank" rel="noopener noreferrer">
            Ver perfil en GitHub
          </a>
        </div>
      </article>
    `;

    guardarBusqueda(login);

  } catch (error) {
    resultado.innerHTML = `<p class="error">Ha ocurrido un error: ${error.message}</p>`;
  }
}

// Evento del botón buscar
btnBuscar.addEventListener('click', () => {
  const username = campoBusqueda.value.trim();
  if (username) buscarUsuario(username);
});

// Buscar al pulsar Enter
campoBusqueda.addEventListener('keydown', (e) => {
  if (e.key === 'Enter') {
    const username = campoBusqueda.value.trim();
    if (username) buscarUsuario(username);
  }
});

// Mostrar búsquedas recientes al cargar
document.addEventListener('DOMContentLoaded', mostrarBusquedasRecientes);
```

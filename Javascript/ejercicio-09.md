# Ejercicio 9 de JavaScript

## Enunciado

En este ejercicio practicaremos fetch y async/await consumiendo datos de la API pública JSONPlaceholder.

## Solución

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 9 JavaScript</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>API JSONPlaceholder</h1>
    <div class="botones">
      <button id="btn-usuarios">Cargar usuarios</button>
      <button id="btn-posts">Cargar posts</button>
    </div>
    <div id="contenedor"></div>
    <script src="app.js"></script>
  </body>
</html>
```

**app.js**

```javascript
const contenedor = document.querySelector('#contenedor');
const btnUsuarios = document.querySelector('#btn-usuarios');
const btnPosts = document.querySelector('#btn-posts');

async function cargarUsuarios() {
  contenedor.innerHTML = '<p>Cargando...</p>';

  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/users');

    if (!response.ok) {
      throw new Error(`Error HTTP: ${response.status}`);
    }

    const usuarios = await response.json();

    contenedor.innerHTML = usuarios.map(usuario => `
      <article class="tarjeta">
        <h2>${usuario.name}</h2>
        <p>📧 ${usuario.email}</p>
        <p>🏙️ ${usuario.address.city}</p>
      </article>
    `).join('');

  } catch (error) {
    contenedor.innerHTML = `<p class="error">Error al cargar los usuarios: ${error.message}</p>`;
  }
}

async function cargarPosts() {
  contenedor.innerHTML = '<p>Cargando...</p>';

  try {
    const response = await fetch('https://jsonplaceholder.typicode.com/posts');

    if (!response.ok) {
      throw new Error(`Error HTTP: ${response.status}`);
    }

    const posts = await response.json();

    contenedor.innerHTML = posts.map(post => `
      <article class="tarjeta">
        <h2>${post.title}</h2>
        <p>${post.body}</p>
      </article>
    `).join('');

  } catch (error) {
    contenedor.innerHTML = `<p class="error">Error al cargar los posts: ${error.message}</p>`;
  }
}

btnUsuarios.addEventListener('click', cargarUsuarios);
btnPosts.addEventListener('click', cargarPosts);
```

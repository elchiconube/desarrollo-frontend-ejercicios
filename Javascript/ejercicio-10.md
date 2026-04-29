# Ejercicio 10 de JavaScript

## Enunciado

En este ejercicio practicaremos `localStorage` y la API `Date` con `Intl` para persistir preferencias del usuario en el navegador.

## Solución

**app.js**

```javascript
const campoNombre = document.querySelector('#nombre');
const campoCiudad = document.querySelector('#ciudad');
const selectorTema = document.querySelector('#tema');
const botonGuardar = document.querySelector('#btn-guardar');
const botonBorrar = document.querySelector('#btn-borrar');
const parrafoFecha = document.querySelector('#ultimo-guardado');

// Cargar preferencias guardadas al iniciar
function cargarPreferencias() {
  const datosGuardados = localStorage.getItem('preferencias');

  if (datosGuardados) {
    const { nombre, ciudad, tema, fecha } = JSON.parse(datosGuardados);

    campoNombre.value = nombre;
    campoCiudad.value = ciudad;
    selectorTema.value = tema;

    // Aplicar tema
    if (tema === 'oscuro') {
      document.body.classList.add('tema-oscuro');
    }

    // Mostrar fecha del último guardado
    const fechaFormateada = new Intl.DateTimeFormat('es-ES', {
      dateStyle: 'full',
      timeStyle: 'short'
    }).format(new Date(fecha));

    parrafoFecha.textContent = `Último guardado: ${fechaFormateada}`;
  }
}

// Guardar preferencias
function guardarPreferencias() {
  const preferencias = {
    nombre: campoNombre.value,
    ciudad: campoCiudad.value,
    tema: selectorTema.value,
    fecha: new Date().toISOString()
  };

  localStorage.setItem('preferencias', JSON.stringify(preferencias));

  // Aplicar tema
  if (preferencias.tema === 'oscuro') {
    document.body.classList.add('tema-oscuro');
  } else {
    document.body.classList.remove('tema-oscuro');
  }

  // Mostrar fecha actualizada
  const fechaFormateada = new Intl.DateTimeFormat('es-ES', {
    dateStyle: 'full',
    timeStyle: 'short'
  }).format(new Date());

  parrafoFecha.textContent = `Último guardado: ${fechaFormateada}`;
}

// Borrar preferencias
function borrarPreferencias() {
  localStorage.removeItem('preferencias');

  campoNombre.value = '';
  campoCiudad.value = '';
  selectorTema.value = 'claro';
  document.body.classList.remove('tema-oscuro');
  parrafoFecha.textContent = '';
}

// Eventos
botonGuardar.addEventListener('click', guardarPreferencias);
botonBorrar.addEventListener('click', borrarPreferencias);

// Cargar al iniciar la página
document.addEventListener('DOMContentLoaded', cargarPreferencias);
```

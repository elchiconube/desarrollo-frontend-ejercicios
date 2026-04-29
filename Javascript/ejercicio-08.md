# Ejercicio 8 de JavaScript

## Enunciado

En este ejercicio practicaremos los eventos añadiendo interactividad a la lista de tareas del ejercicio anterior.

## Solución

**index.html** — Añadir antes de `</main>`:

```html
<div class="nueva-tarea">
  <input type="text" id="campo-tarea" placeholder="Nueva tarea..." />
  <button id="boton-agregar">Añadir tarea</button>
  <p class="error" id="mensaje-error"></p>
</div>
```

**app.js**

```javascript
const lista = document.querySelector('.lista');
const campo = document.querySelector('#campo-tarea');
const botonAgregar = document.querySelector('#boton-agregar');
const mensajeError = document.querySelector('#mensaje-error');
const contador = document.querySelector('.contador');

// Función para actualizar el contador
function actualizarContador() {
  const total = document.querySelectorAll('.tarea').length;
  contador.textContent = `Total de tareas: ${total}`;
}

// Inicializar contador
actualizarContador();

// Delegación de eventos — marcar/desmarcar tareas con un único listener
lista.addEventListener('click', (e) => {
  if (e.target.classList.contains('tarea')) {
    e.target.classList.toggle('completada');
  }
});

// Función para añadir tarea
function añadirTarea() {
  const texto = campo.value.trim();

  if (!texto) {
    mensajeError.textContent = 'El campo no puede estar vacío';
    return;
  }

  mensajeError.textContent = '';

  const nuevaTarea = document.createElement('li');
  nuevaTarea.classList.add('tarea');
  nuevaTarea.textContent = texto;
  lista.appendChild(nuevaTarea);

  campo.value = '';
  actualizarContador();
}

// Añadir tarea al hacer clic en el botón
botonAgregar.addEventListener('click', añadirTarea);

// Limpiar campo al pulsar Escape
campo.addEventListener('keydown', (e) => {
  if (e.key === 'Escape') {
    campo.value = '';
    mensajeError.textContent = '';
  }
});
```

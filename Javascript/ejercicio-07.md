# Ejercicio 7 de JavaScript

## Enunciado

En este ejercicio practicaremos la manipulación del DOM — seleccionar, leer y modificar elementos HTML desde JavaScript.

## Solución

```javascript
// Seleccionar el h1 y cambiar su texto
const titulo = document.querySelector('#titulo');
titulo.textContent = 'Mis tareas pendientes';

// Seleccionar todas las tareas y mostrar cuántas hay
const tareas = document.querySelectorAll('.tarea');
console.log(`Hay ${tareas.length} tareas`); // Hay 4 tareas

// Añadir clase 'completada' a la primera tarea
tareas[0].classList.add('completada');

// Quitar 'completada' de la primera y añadirla a la última
tareas[0].classList.remove('completada');
tareas[tareas.length - 1].classList.add('completada');
// O usando at():
tareas.item(tareas.length - 1).classList.add('completada');

// Crear nueva tarea y añadirla al final
const lista = document.querySelector('.lista');
const nuevaTarea = document.createElement('li');
nuevaTarea.classList.add('tarea');
nuevaTarea.textContent = 'Publicar mi portfolio';
lista.appendChild(nuevaTarea);

// Eliminar la segunda tarea
const segundaTarea = document.querySelectorAll('.tarea')[1];
segundaTarea.remove();

// Actualizar el contador
const contador = document.querySelector('.contador');
const totalTareas = document.querySelectorAll('.tarea').length;
contador.textContent = `Total de tareas: ${totalTareas}`;
```

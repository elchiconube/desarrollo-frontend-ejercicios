# Ejercicio 1 de JavaScript

## Enunciado

En este primer ejercicio practicaremos la declaración de variables y los tipos de datos. El objetivo es familiarizarse con `const`, `let` y `typeof`.

## Solución

```javascript
// Variables con const — valores que no cambiarán
const nombre = 'Óscar';
const edad = 30;

// Variable con let — valor que puede cambiar
let ciudad = 'León';

// Booleano
const estudiaFrontend = true;

// Array
const tecnologias = ['HTML', 'CSS', 'JavaScript'];

// Objeto
const perfil = {
  nombre: 'Óscar',
  edad: 30,
  ciudad: 'León',
  hobby: 'música'
};

// Mostrar variables y tipos por consola
console.log(nombre, typeof nombre);         // 'Óscar' 'string'
console.log(edad, typeof edad);             // 30 'number'
console.log(ciudad, typeof ciudad);         // 'León' 'string'
console.log(estudiaFrontend, typeof estudiaFrontend); // true 'boolean'
console.log(tecnologias, typeof tecnologias); // ['HTML', 'CSS', 'JavaScript'] 'object'
console.log(perfil, typeof perfil);         // {...} 'object'

// Cambiar ciudad con let — funciona
ciudad = 'Madrid';
console.log(ciudad); // 'Madrid'

// Intentar cambiar edad con const — lanza error
// edad = 31; // Uncaught TypeError: Assignment to constant variable.
```

# Ejercicio 3 de JavaScript

## Enunciado

En este ejercicio practicaremos los operadores de comparación, los valores falsy y las sentencias condicionales.

## Solución

```javascript
// Calificación con if/else if
const nota = 7;

if (nota >= 9) {
  console.log('Sobresaliente');
} else if (nota >= 7) {
  console.log('Notable');
} else if (nota >= 6) {
  console.log('Bien');
} else if (nota === 5) {
  console.log('Suficiente');
} else {
  console.log('Suspenso');
}
// 'Notable'

// Comprobación de nombre vacío usando falsy
const nombre = '';

if (nombre) {
  console.log(`Hola, ${nombre}`);
} else {
  console.log('No has introducido ningún nombre');
}
// 'No has introducido ningún nombre'

// Función con operador ternario
const esMayorDeEdad = (edad) => {
  return edad >= 18 ? 'Eres mayor de edad' : 'Eres menor de edad';
};

console.log(esMayorDeEdad(20));   // 'Eres mayor de edad'
console.log(esMayorDeEdad(15));   // 'Eres menor de edad'

// ¿Qué pasa con null y undefined?
console.log(esMayorDeEdad(null));      // 'Eres menor de edad' — null se convierte a 0
console.log(esMayorDeEdad(undefined)); // 'Eres menor de edad' — undefined se convierte a NaN

// Solución con ?? para controlar null y undefined
const esMayorDeEdadSeguro = (edad) => {
  const edadSegura = edad ?? 0;
  return edadSegura >= 18 ? 'Eres mayor de edad' : 'Eres menor de edad';
};

console.log(esMayorDeEdadSeguro(null));      // 'Eres menor de edad'
console.log(esMayorDeEdadSeguro(undefined)); // 'Eres menor de edad'
console.log(esMayorDeEdadSeguro(20));        // 'Eres mayor de edad'
```

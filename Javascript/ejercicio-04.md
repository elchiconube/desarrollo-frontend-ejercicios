# Ejercicio 4 de JavaScript

## Enunciado

En este ejercicio practicaremos las funciones — declaradas, arrow functions y parámetros por defecto.

## Solución

```javascript
// 1. Función declarada con parámetros por defecto
function calcularArea(ancho = 1, alto = 1) {
  return ancho * alto;
}

console.log(calcularArea(5, 3)); // 15
console.log(calcularArea(4));    // 4 — alto usa el valor por defecto
console.log(calcularArea());     // 1 — ambos usan el valor por defecto

// 2. La misma función como arrow function
const calcularAreaArrow = (ancho = 1, alto = 1) => ancho * alto;

console.log(calcularAreaArrow(5, 3)); // 15
console.log(calcularAreaArrow());     // 1

// 3. Función saludar con saludo por defecto
function saludar(nombre, saludo = 'Hola') {
  return `${saludo}, ${nombre}!`;
}

console.log(saludar('Óscar'));          // 'Hola, Óscar!'
console.log(saludar('Óscar', 'Buenas')); // 'Buenas, Óscar!'

// 4. Función esPar como arrow function concisa
const esPar = n => n % 2 === 0;

console.log(esPar(4));  // true
console.log(esPar(7));  // false
console.log(esPar(0));  // true

// 5. Función calcularMedia
function calcularMedia(notas) {
  if (notas.length === 0) return 0;
  return notas.reduce((total, nota) => total + nota, 0) / notas.length;
}

console.log(calcularMedia([5, 7, 8, 9, 6])); // 7
console.log(calcularMedia([]));               // 0
console.log(calcularMedia([10]));             // 10
```

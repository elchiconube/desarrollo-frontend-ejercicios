# Ejercicio 2 de JavaScript

## Enunciado

En este ejercicio practicaremos los métodos de strings y los template literals.

## Solución

```javascript
const pelicula = '   el señor de los anillos: la comunidad del anillo   ';

// Eliminar espacios del principio y del final
const sinEspacios = pelicula.trim();
console.log(sinEspacios); // 'el señor de los anillos: la comunidad del anillo'

// Convertir a mayúsculas
console.log(sinEspacios.toUpperCase()); // 'EL SEÑOR DE LOS ANILLOS: LA COMUNIDAD DEL ANILLO'

// Comprobar si contiene 'anillos'
console.log(sinEspacios.includes('anillos')); // true

// Comprobar si empieza por 'el'
console.log(sinEspacios.startsWith('el')); // true

// Extraer 'comunidad' — empieza en el índice 36 y tiene 9 caracteres
console.log(sinEspacios.slice(36, 45)); // 'comunidad'

// Sustituir 'anillos' por 'hobbits'
console.log(sinEspacios.replace('anillos', 'hobbits'));
// 'el señor de los hobbits: la comunidad del anillo'

// Dividir por los dos puntos
const partes = sinEspacios.split(':');
console.log(partes[0].trim()); // 'el señor de los anillos'
console.log(partes[1].trim()); // 'la comunidad del anillo'

// Ficha de película con template literal
const film = {
  titulo: 'El señor de los anillos: La comunidad del anillo',
  director: 'Peter Jackson',
  año: 2001,
  valoracion: 8.8
};

const ficha = `
  🎬 ${film.titulo}
  🎥 Director: ${film.director}
  📅 Año: ${film.año}
  ⭐ Valoración: ${film.valoracion}/10
`;

console.log(ficha);
```

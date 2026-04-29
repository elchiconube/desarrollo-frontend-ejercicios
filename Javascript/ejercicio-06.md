# Ejercicio 6 de JavaScript

## Enunciado

En este ejercicio practicaremos los objetos, el destructuring y el spread operator.

## Solución

```javascript
const usuario = {
  nombre: 'Óscar',
  apellido: 'Bustos',
  edad: 30,
  ciudad: 'León',
  profesion: 'Desarrollador Frontend',
  redes: {
    twitter: '@elchiconube',
    github: 'elchiconube'
  }
};

// Destructuring de nombre, edad y ciudad
const { nombre, edad, ciudad } = usuario;
console.log(nombre); // 'Óscar'
console.log(edad);   // 30
console.log(ciudad); // 'León'

// Destructuring de twitter en una sola línea
const { redes: { twitter } } = usuario;
console.log(twitter); // '@elchiconube'

// Combinar con spread sin modificar el original
const perfil = { ...usuario, pais: 'España', activo: true };
console.log(perfil);
// { nombre: 'Óscar', ..., pais: 'España', activo: true }
console.log(usuario); // El original no ha cambiado

// Copia con ciudad cambiada
const usuarioMadrid = { ...usuario, ciudad: 'Madrid' };
console.log(usuarioMadrid.ciudad); // 'Madrid'
console.log(usuario.ciudad);       // 'León' — el original no cambia

// Object.keys()
console.log(Object.keys(usuario));
// ['nombre', 'apellido', 'edad', 'ciudad', 'profesion', 'redes']

// Object.values()
console.log(Object.values(usuario));
// ['Óscar', 'Bustos', 30, 'León', 'Desarrollador Frontend', {...}]

// Object.entries() con forEach
Object.entries(usuario).forEach(([clave, valor]) => {
  console.log(`${clave}: ${valor}`);
});
// nombre: Óscar
// apellido: Bustos
// edad: 30
// ciudad: León
// profesion: Desarrollador Frontend
// redes: [object Object]
```

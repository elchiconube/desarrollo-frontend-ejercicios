# Ejercicio 11 de JavaScript

## Enunciado

En este ejercicio practicaremos los diferentes tipos de bucles para recorrer arrays y objetos de forma eficiente.

## Solución

```javascript
const alumnos = [
  { nombre: 'María', notas: [7, 8, 9, 6] },
  { nombre: 'Carlos', notas: [5, 4, 6, 7] },
  { nombre: 'Laura', notas: [9, 10, 8, 9] },
  { nombre: 'Javier', notas: [3, 5, 4, 6] },
  { nombre: 'Ana', notas: [8, 7, 9, 8] }
];

// 1. for/of — mostrar el nombre de cada alumno
for (const alumno of alumnos) {
  console.log(alumno.nombre);
}
// María, Carlos, Laura, Javier, Ana

// 2. forEach — nombre y número de notas
alumnos.forEach(alumno => {
  console.log(`${alumno.nombre} tiene ${alumno.notas.length} notas`);
});

// 3. for/of con reduce — media de cada alumno
for (const alumno of alumnos) {
  const media = alumno.notas.reduce((total, nota) => total + nota, 0) / alumno.notas.length;
  console.log(`${alumno.nombre}: ${media.toFixed(2)}`);
}
// María: 7.50, Carlos: 5.50, Laura: 9.00, Javier: 4.50, Ana: 8.00

// 4. for/in — propiedades del primer alumno
for (const clave in alumnos[0]) {
  console.log(`${clave}: ${alumnos[0][clave]}`);
}
// nombre: María
// notas: 7,8,9,6

// 5. for clásico al revés
for (let i = alumnos.length - 1; i >= 0; i--) {
  console.log(alumnos[i].nombre);
}
// Ana, Javier, Laura, Carlos, María

// 6. for/of — alumno con la media más alta
let mejorAlumno = null;
let mejorMedia = 0;

for (const alumno of alumnos) {
  const media = alumno.notas.reduce((total, nota) => total + nota, 0) / alumno.notas.length;
  if (media > mejorMedia) {
    mejorMedia = media;
    mejorAlumno = alumno.nombre;
  }
}

console.log(`El alumno con la media más alta es ${mejorAlumno} con un ${mejorMedia.toFixed(2)}`);
// El alumno con la media más alta es Laura con un 9.00
```

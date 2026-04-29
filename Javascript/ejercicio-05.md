# Ejercicio 5 de JavaScript

## Enunciado

En este ejercicio practicaremos los arrays y sus métodos modernos.

## Solución

```javascript
const productos = [
  { nombre: 'Camiseta', precio: 15, categoria: 'ropa', disponible: true },
  { nombre: 'Zapatillas', precio: 89, categoria: 'calzado', disponible: false },
  { nombre: 'Pantalón', precio: 45, categoria: 'ropa', disponible: true },
  { nombre: 'Mochila', precio: 35, categoria: 'accesorios', disponible: true },
  { nombre: 'Calcetines', precio: 5, categoria: 'ropa', disponible: true },
  { nombre: 'Cinturón', precio: 20, categoria: 'accesorios', disponible: false },
];

// Filtrar productos disponibles
const disponibles = productos.filter(p => p.disponible);
console.log(disponibles);
// [Camiseta, Pantalón, Mochila, Calcetines]

// Filtrar productos de la categoría 'ropa'
const ropa = productos.filter(p => p.categoria === 'ropa');
console.log(ropa);
// [Camiseta, Pantalón, Calcetines]

// Array solo con nombres
const nombres = productos.map(p => p.nombre);
console.log(nombres);
// ['Camiseta', 'Zapatillas', 'Pantalón', 'Mochila', 'Calcetines', 'Cinturón']

// Precios de productos disponibles
const preciosDisponibles = productos
  .filter(p => p.disponible)
  .map(p => p.precio);
console.log(preciosDisponibles);
// [15, 45, 35, 5]

// Precio total de productos disponibles
const totalDisponibles = productos
  .filter(p => p.disponible)
  .reduce((total, p) => total + p.precio, 0);
console.log(totalDisponibles); // 100

// ¿Algún producto cuesta menos de 10€?
const hayBaratos = productos.some(p => p.precio < 10);
console.log(hayBaratos); // true — los calcetines cuestan 5€

// ¿Todos los productos disponibles cuestan menos de 100€?
const todosAsequibles = productos
  .filter(p => p.disponible)
  .every(p => p.precio < 100);
console.log(todosAsequibles); // true

// Primer producto de la categoría 'accesorios'
const primerAccesorio = productos.find(p => p.categoria === 'accesorios');
console.log(primerAccesorio); // { nombre: 'Mochila', ... }

// Último producto con at()
console.log(productos.at(-1));
// { nombre: 'Cinturón', precio: 20, categoria: 'accesorios', disponible: false }
```

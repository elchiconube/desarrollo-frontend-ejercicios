# Ejercicio 7 de CSS

## Enunciado

En este ejercicio practicaremos las propiedades del box-model: ancho, alto, bordes, espaciado y overflow.

## Solución

**css/style.css**

```css
:root {
  --color-border: #3b599b;
  --spacing: 1rem;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  padding: 2rem;
}

.contenedor {
  width: 300px;
  height: 300px;
  margin: 0 auto;
  border: 2px solid var(--color-border);
  padding: var(--spacing);
  overflow-y: scroll;
  overflow-x: hidden;
}

.contenedor h2 {
  margin-bottom: var(--spacing);
  color: var(--color-border);
}

.contenedor p {
  margin-bottom: var(--spacing);
  line-height: 1.6;
}
```

> **Prueba:** Cambia `box-sizing` de `border-box` a `content-box` y observa cómo el padding se suma al ancho y alto definidos, haciendo el contenedor más grande de lo esperado.

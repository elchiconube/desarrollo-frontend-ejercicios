# Ejercicio 6 de CSS

## Enunciado

En este ejercicio practicaremos las propiedades de fondo de CSS experimentando con colores sólidos, gradientes, patrones e imágenes.

## Solución

**css/style.css**

```css
:root {
  --color-primary: #3b599b;
  --color-secondary: #e63946;
  --color-light: #f5f5f5;
  --spacing: 2rem;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
}

header {
  background: linear-gradient(135deg, var(--color-primary), #6a8fd8);
  padding: var(--spacing);
  color: white;
}

header h1 {
  margin: 0;
}

.seccion-color {
  background-color: var(--color-light);
  padding: var(--spacing);
}

.seccion-gradiente {
  background: linear-gradient(to right, var(--color-secondary), #ff9a3c);
  padding: var(--spacing);
  color: white;
}

.seccion-patron {
  background-color: #e5e5f7;
  background-image: radial-gradient(#444cf7 0.5px, #e5e5f7 0.5px);
  background-size: 10px 10px;
  padding: var(--spacing);
}

.seccion-imagen {
  background-image: url('https://images.unsplash.com/photo-1461988320302-91bde64fc8e4');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: calc(var(--spacing) * 4);
  color: white;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.8);
}
```

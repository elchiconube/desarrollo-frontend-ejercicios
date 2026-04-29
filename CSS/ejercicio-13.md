# Ejercicio 13 de CSS

## Enunciado

En este ejercicio recibes un CSS con valores repetidos y dispersos. Tu tarea es refactorizarlo usando variables CSS en `:root`.

## Solución

```css
:root {
  --color-primary: #3b599b;
  --color-text: #333;
  --color-white: white;
  --color-bg: #f5f5f5;
  --font-family: Arial, sans-serif;
  --font-size-base: 16px;
  --font-size-large: 32px;
  --font-size-medium: 24px;
  --spacing: 24px;
  --spacing-sm: 16px;
  --spacing-btn: 8px;
  --border-radius: 8px;
  --border-width: 2px;
}

.header {
  background-color: var(--color-primary);
  padding: var(--spacing);
  font-family: var(--font-family);
}

.header__titulo {
  color: var(--color-white);
  font-size: var(--font-size-large);
}

.header__nav a {
  color: var(--color-white);
  font-size: var(--font-size-base);
  margin-right: var(--spacing);
}

.contenido {
  display: flex;
  gap: var(--spacing);
  padding: var(--spacing);
  font-family: var(--font-family);
  background-color: var(--color-bg);
}

.tarjeta {
  background-color: var(--color-white);
  border: var(--border-width) solid var(--color-primary);
  border-radius: var(--border-radius);
  padding: var(--spacing);
}

.tarjeta__titulo {
  color: var(--color-primary);
  font-size: var(--font-size-medium);
  font-family: var(--font-family);
  margin-bottom: var(--spacing-sm);
}

.tarjeta__texto {
  color: var(--color-text);
  font-size: var(--font-size-base);
  font-family: var(--font-family);
  margin-bottom: var(--spacing-sm);
}

.tarjeta__boton {
  background-color: var(--color-primary);
  color: var(--color-white);
  font-size: var(--font-size-base);
  padding: var(--spacing-btn) var(--spacing);
  border-radius: var(--border-radius);
}

.footer {
  background-color: var(--color-primary);
  color: var(--color-white);
  font-size: var(--font-size-base);
  padding: var(--spacing);
  font-family: var(--font-family);
}
```

> **Prueba:** Cambia el valor de `--color-primary` en `:root` y observa cómo el cambio se propaga automáticamente a todos los elementos que lo usan.

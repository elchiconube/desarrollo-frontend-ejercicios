# Ejercicio 5 de CSS

## Enunciado

Este ejercicio es una continuación del anterior. El objetivo es sustituir las fuentes del sistema por fuentes personalizadas de Google Fonts.

## Solución

**index.html** — Añadir en el `<head>` antes del CSS:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Roboto:wght@400;700&family=Slabo+27px&family=Ubuntu+Mono&display=swap" rel="stylesheet">
```

**css/style.css**

```css
:root {
  --color-text: #333;
  --font-display: 'Pacifico', cursive;
  --font-serif: 'Slabo 27px', serif;
  --font-sans: 'Roboto', sans-serif;
  --font-mono: 'Ubuntu Mono', monospace;
}

body {
  padding: 2rem;
  color: var(--color-text);
}

h1 {
  font-family: var(--font-display);
  text-align: center;
  text-decoration: underline;
  font-size: 28px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  margin-bottom: 2rem;
}

h2 {
  text-transform: uppercase;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  margin-bottom: 0.5rem;
}

article {
  margin-bottom: 2rem;
}

article:nth-child(1) h2,
article:nth-child(1) p {
  font-family: var(--font-serif);
  color: var(--color-text);
}

article:nth-child(2) h2,
article:nth-child(2) p {
  font-family: var(--font-sans);
  color: var(--color-text);
}

article:nth-child(3) h2,
article:nth-child(3) p {
  font-family: var(--font-mono);
  color: var(--color-text);
}
```

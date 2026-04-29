# Ejercicio 4 de CSS

## Enunciado

En este ejercicio practicaremos las reglas CSS de tipografía aplicando diferentes estilos de texto a cada elemento.

## Solución

**css/style.css**

```css
:root {
  --color-text: #333;
  --font-serif: Georgia, 'Times New Roman', serif;
  --font-sans: Arial, Helvetica, sans-serif;
  --font-mono: 'Courier New', Courier, monospace;
}

body {
  padding: 2rem;
  color: var(--color-text);
}

h1 {
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

article:nth-child(1) p {
  font-family: var(--font-serif);
  color: var(--color-text);
}

article:nth-child(2) p {
  font-family: var(--font-sans);
  color: var(--color-text);
}

article:nth-child(3) p {
  font-family: var(--font-mono);
  color: var(--color-text);
}
```

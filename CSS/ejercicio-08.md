# Ejercicio 8 de CSS

## Enunciado

En este ejercicio practicaremos las propiedades de Flexbox para distribuir elementos y controlar su orden.

## Solución

**css/style.css**

```css
:root {
  --color-primary: #3b599b;
  --color-bg: #f0f4ff;
  --gap: 1rem;
  --padding: 1rem;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  padding: var(--padding);
  margin: 0;
}

.flex {
  display: flex;
  gap: var(--gap);
  align-items: flex-start;
}

.flex__item {
  flex: 1;
  background-color: var(--color-bg);
  border: 2px solid var(--color-primary);
  border-radius: 8px;
  padding: var(--padding);
}

.flex__item:nth-child(3) {
  order: -1;
}

.flex__item h2 {
  color: var(--color-primary);
  margin-bottom: 0.5rem;
  font-size: 1rem;
}

@media (max-width: 600px) {
  .flex {
    flex-direction: column;
  }
}
```

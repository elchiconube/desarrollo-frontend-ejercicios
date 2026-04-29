# Ejercicio 2 de CSS

## Enunciado

En este ejercicio practicaremos las unidades CSS y el uso de clases. El objetivo es entender cómo funcionan los tamaños relativos usando `rem`.

## Solución

**css/style.css**

```css
:root {
  --font-size-base: 16px;
  --font-size-big: 2rem;
  --font-size-bigger: 3rem;
}

body {
  font-size: var(--font-size-base);
  padding: 1.5rem;
  line-height: 1.6;
}

p {
  margin-bottom: 1rem;
}

.big {
  font-size: var(--font-size-big);
}

.bigger {
  font-size: var(--font-size-bigger);
}
```

# Ejercicio 3 de CSS

## Enunciado

En este ejercicio practicaremos los selectores CSS de clase y las propiedades de color. El objetivo es aplicar a cada red social el color corporativo que le corresponde usando variables CSS.

## Solución

**css/style.css**

```css
:root {
  --color-facebook: #1877F2;
  --color-twitter: #000000;
  --color-instagram: #E1306C;
  --color-youtube: #FF0000;
  --color-linkedin: #0A66C2;
  --color-tiktok: #010101;
  --color-pinterest: #E60023;
  --color-spotify: #1DB954;
}

body {
  padding: 2rem;
  font-family: Arial, sans-serif;
}

ul {
  list-style: none;
}

li {
  padding: 0.5rem 1rem;
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  font-weight: bold;
  border-radius: 4px;
  color: white;
}

.facebook  { background-color: var(--color-facebook); }
.twitter   { background-color: var(--color-twitter); }
.instagram { background-color: var(--color-instagram); }
.youtube   { background-color: var(--color-youtube); }
.linkedin  { background-color: var(--color-linkedin); }
.tiktok    { background-color: var(--color-tiktok); }
.pinterest { background-color: var(--color-pinterest); }
.spotify   { background-color: var(--color-spotify); }
```

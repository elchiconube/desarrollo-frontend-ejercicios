# Ejercicio 1 de CSS

## Enunciado

En este primer ejercicio vamos a sentar las bases de cualquier proyecto CSS. El objetivo es crear la estructura de archivos correcta, aplicar el reset y definir variables CSS.

## Solución

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 1 CSS</title>
    <link rel="stylesheet" type="text/css" href="css/style.css" />
  </head>
  <body>
    <h1>Mi primer proyecto CSS</h1>
    <p>Este es el primer párrafo de mi proyecto. Las variables CSS nos permiten centralizar los valores que más usamos.</p>
    <p>Gracias al reset CSS partimos de una base uniforme en todos los navegadores.</p>
  </body>
</html>
```

**css/style.css**

```css
/* Reset CSS */
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

body {
  line-height: 1;
  -webkit-font-smoothing: antialiased;
}

*, *::before, *::after {
  box-sizing: border-box;
}

/* Variables CSS */
:root {
  --color-primary: #3b599b;
  --color-secondary: #ffcc00;
  --font-size-base: 1rem;
  --spacing-base: 1.5rem;
}

/* Estilos */
body {
  font-size: var(--font-size-base);
  padding: var(--spacing-base);
  color: #333;
}

h1 {
  color: var(--color-primary);
  margin-bottom: var(--spacing-base);
}

p {
  margin-bottom: var(--spacing-base);
  line-height: 1.6;
}
```

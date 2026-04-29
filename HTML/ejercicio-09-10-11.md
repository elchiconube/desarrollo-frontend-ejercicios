# Ejercicio 9 de CSS

## Enunciado

En este ejercicio practicaremos Grid creando un layout de rejilla básico usando `grid-template-columns` y `grid-template-rows`.

## Solución

```css
:root {
  --gap: 0.5rem;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  padding: 1rem;
  font-family: Arial, sans-serif;
}

.grid {
  display: grid;
  gap: var(--gap);
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto;
}

.grid__item {
  background-color: #3b599b;
  color: white;
  padding: 1rem;
  text-align: center;
  border-radius: 4px;
  font-weight: bold;
}

.grid__item--a {
  grid-column: span 2;
}

.grid__item--e {
  grid-column: span 3;
}
```

> Puedes consultar la solución en [CodePen](https://codepen.io/elchiconube/pen/yGvOqG).

---

# Ejercicio 10 de CSS

## Enunciado

En este ejercicio practicaremos Grid con un layout más complejo usando `grid-template-areas`.

## Solución

```css
:root {
  --gap: 0.5rem;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  padding: 1rem;
  font-family: Arial, sans-serif;
}

.grid {
  display: grid;
  gap: var(--gap);
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    "a a b"
    "c d b"
    "c e f";
}

.grid__item {
  background-color: #3b599b;
  color: white;
  padding: 2rem;
  text-align: center;
  border-radius: 4px;
  font-weight: bold;
}

.grid__item--a { grid-area: a; }
.grid__item--b { grid-area: b; }
.grid__item--c { grid-area: c; }
.grid__item--d { grid-area: d; }
.grid__item--e { grid-area: e; }
.grid__item--f { grid-area: f; }
```

> Puedes consultar la solución en [CodePen](https://codepen.io/elchiconube/pen/wRyWvx).

---

# Ejercicio 11 de CSS

## Enunciado

En este ejercicio practicaremos el Holy Grail Layout usando Grid y `grid-template-areas`.

## Solución

```css
:root {
  --gap: 0.5rem;
  --color-header: #3b599b;
  --color-nav: #e63946;
  --color-main: #2a9d8f;
  --color-aside: #e9c46a;
  --color-footer: #264653;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  min-height: 100vh;
}

.grid {
  display: grid;
  min-height: 100vh;
  gap: var(--gap);
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header header"
    "nav    main   aside"
    "footer footer footer";
}

.grid__header { grid-area: header; background-color: var(--color-header); }
.grid__nav    { grid-area: nav;    background-color: var(--color-nav); }
.grid__main   { grid-area: main;   background-color: var(--color-main); }
.grid__aside  { grid-area: aside;  background-color: var(--color-aside); }
.grid__footer { grid-area: footer; background-color: var(--color-footer); }

.grid > * {
  padding: 1rem;
  color: white;
  font-weight: bold;
}
```

> Puedes consultar la solución en [CodePen](https://codepen.io/elchiconube/pen/WLMxGm).

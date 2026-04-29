# Ejercicio 12 de CSS

## Enunciado

En este ejercicio practicaremos Grid recreando el logo de Windows usando colores corporativos y variables CSS.

## Solución

```css
:root {
  --color-rojo: #F25022;
  --color-verde: #7FBA00;
  --color-azul: #00A4EF;
  --color-amarillo: #FFB900;
  --tamano: 120px;
  --gap: 8px;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
  background-color: #f5f5f5;
}

.logo {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--gap);
  width: calc(var(--tamano) * 2 + var(--gap));
}

.logo__cuadrado {
  width: var(--tamano);
  height: var(--tamano);
  border-radius: 4px;
}

.logo__cuadrado--rojo    { background-color: var(--color-rojo); }
.logo__cuadrado--verde   { background-color: var(--color-verde); }
.logo__cuadrado--azul    { background-color: var(--color-azul); }
.logo__cuadrado--amarillo { background-color: var(--color-amarillo); }
```

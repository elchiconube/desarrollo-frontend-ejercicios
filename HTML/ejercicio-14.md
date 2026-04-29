# Ejercicio 14 de CSS

## Enunciado

En este ejercicio practicaremos las animaciones CSS creando tres elementos animados usando `transition`, `transform` y `@keyframes`.

## Solución

**css/style.css**

```css
:root {
  --color-primary: #3b599b;
  --color-secondary: #e63946;
  --color-pulse: #2a9d8f;
  --transition-speed: 0.3s;
  --border-radius: 8px;
}

*, *::before, *::after {
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  padding: 2rem;
  display: flex;
  gap: 2rem;
  align-items: center;
  flex-wrap: wrap;
}

/* Tarjeta con hover */
.tarjeta-hover {
  background-color: var(--color-primary);
  color: white;
  padding: 2rem;
  border-radius: var(--border-radius);
  cursor: pointer;
  transition: background-color var(--transition-speed) ease,
              transform var(--transition-speed) ease;
}

.tarjeta-hover:hover {
  background-color: var(--color-secondary);
  transform: scale(1.05);
}

/* Tarjeta con giro */
.tarjeta-giro {
  width: 200px;
  height: 150px;
  position: relative;
  perspective: 800px;
  cursor: pointer;
}

.tarjeta-giro__frente,
.tarjeta-giro__dorso {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: var(--border-radius);
  font-weight: bold;
  color: white;
  backface-visibility: hidden;
  transition: transform 0.6s ease;
}

.tarjeta-giro__frente {
  background-color: var(--color-primary);
}

.tarjeta-giro__dorso {
  background-color: var(--color-secondary);
  transform: rotateY(180deg);
}

.tarjeta-giro:hover .tarjeta-giro__frente {
  transform: rotateY(-180deg);
}

.tarjeta-giro:hover .tarjeta-giro__dorso {
  transform: rotateY(0deg);
}

/* Círculo con pulso */
@keyframes pulso {
  0% {
    transform: scale(1);
    background-color: var(--color-pulse);
  }
  50% {
    transform: scale(1.2);
    background-color: #38b2a0;
  }
  100% {
    transform: scale(1);
    background-color: var(--color-pulse);
  }
}

.circulo-pulso {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background-color: var(--color-pulse);
  animation: pulso 1.5s ease-in-out infinite;
}

/* Accesibilidad */
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition: none !important;
  }
}
```

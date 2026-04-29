# Ejercicio 6 de HTML

## Enunciado

Vamos a crear dos documentos HTML enlazados entre sí. El objetivo es practicar la etiqueta `<a>` con diferentes tipos de enlaces: externos, mailto e internos entre documentos.

## Solución

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 6 HTML</title>
  </head>
  <body>
    <h1>Menú de opciones</h1>

    <ul>
      <li>
        <a href="https://maps.google.com/?q=Google+Madrid" title="Cómo llegar a Google Madrid" target="_blank">
          Cómo llegar
        </a>
      </li>
      <li>
        <a href="mailto:oscar@ejemplo.com" title="Enviar correo de contacto">
          Contacto
        </a>
      </li>
      <li>
        <a href="biografia.html" title="Ver biografía">
          Biografía
        </a>
      </li>
    </ul>
  </body>
</html>
```

**biografia.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Biografía</title>
  </head>
  <body>
    <h1>Óscar Bustos</h1>

    <a href="index.html" title="Volver al inicio">Volver</a>

    <p>
      Desarrollador frontend natural de Altea (Alicante). Estudié Publicidad y RR.PP. en Valencia
      y desde entonces he trabajado con equipos de diferentes sectores, tanto nacionales como internacionales.
    </p>
    <p>
      Me considero un eterno aprendiz, apasionado de la tecnología, el diseño y la enseñanza.
    </p>
  </body>
</html>
```

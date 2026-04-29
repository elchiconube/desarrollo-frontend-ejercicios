# Ejercicio 8 de HTML

## Enunciado

Vamos a crear un documento HTML donde practicaremos la incrustación de contenido multimedia mediante la etiqueta `<iframe>`. Para ello insertaremos un vídeo de YouTube de tu elección.

Accede a YouTube y elige un vídeo que te guste. Haz clic en **Compartir → Insertar** para obtener el código `<iframe>` que YouTube genera automáticamente y pégalo en tu documento HTML.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 8 HTML</title>
  </head>
  <body>
    <h1>Documental: Abstract — El arte del diseño</h1>

    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/DYaq2sWTWAA"
      title="Abstract — El arte del diseño"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
    </iframe>

    <p>
      Abstract es una serie documental de Netflix que explora el mundo del diseño a través
      de algunos de sus profesionales más influyentes.
    </p>

    <time datetime="2017-02-10">Publicado el 10 de febrero de 2017</time>
  </body>
</html>
```

> **Nota:** El `src` del `<iframe>` variará según el vídeo que elijas. YouTube genera este código automáticamente al hacer clic en Compartir → Insertar.

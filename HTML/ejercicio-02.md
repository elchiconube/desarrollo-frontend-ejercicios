# Ejercicio 2 de HTML

## Enunciado

Vamos a crear un documento HTML con una nueva noticia periodística. En este ejercicio practicaremos las etiquetas del ejercicio anterior y añadiremos otras nuevas: `<blockquote>` y `<cite>` para la cita textual, `<address>` para el autor y `<time>` para la fecha de publicación.

**Titular**: Kim Jong-un se ofrece a destruir a Donald Trump

**Subtítulo**: Es un gesto de apertura y solidaridad sin precedentes por parte del régimen norcoreano

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 2 HTML</title>
  </head>
  <body>
    <h1>Kim Jong-un se ofrece a destruir a Donald Trump</h1>
    <h2>Es un gesto de apertura y solidaridad sin precedentes por parte del régimen norcoreano</h2>

    <address>Por Xavi Puig</address>
    <time datetime="2017-09-04">04 de Septiembre de 2017</time>

    <p>
      El ofrecimiento se produce horas <strong>después del discurso de Trump</strong> en el 72°
      período de sesiones de la Asamblea General de la ONU, en el que el mandatario norteamericano
      ha hecho gala del talante belicista que tanto preocupa dentro y fuera de Estados Unidos.
    </p>

    <blockquote>
      Es un gesto de buena voluntad que sin duda será tenido en consideración, parece que al fin
      avanzamos por el buen camino. Puede que estos misiles finalmente sirvan para algo.
    </blockquote>
    <cite>Antonio Cabano, Secretario General de la ONU</cite>

    <p>
      "Nadie regala nada a cambio de nada y quién sabe si acaba exigiendo más cosas que no le
      podamos conceder", argumenta.
    </p>
  </body>
</html>
```

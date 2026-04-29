# Ejercicio 7 de HTML

## Enunciado

Vamos a crear un documento HTML con un listado de películas. El objetivo es practicar las etiquetas `<figure>`, `<img>`, `<figcaption>` y `<a>` combinando imágenes con enlaces.

Busca en Internet las portadas de 5 películas del estudio Ghibli, guárdalas en una carpeta `img` junto a tu documento HTML y enlaza cada imagen a su entrada de Wikipedia.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 7 HTML</title>
  </head>
  <body>
    <h1>Las mejores películas del estudio Ghibli</h1>

    <figure>
      <a href="https://es.wikipedia.org/wiki/El_viaje_de_Chihiro" title="Ver en Wikipedia" target="_blank">
        <img src="img/chihiro.jpg" alt="Portada de El viaje de Chihiro" />
      </a>
      <figcaption>El viaje de Chihiro (2001)</figcaption>
    </figure>

    <figure>
      <a href="https://es.wikipedia.org/wiki/Mi_vecino_Totoro" title="Ver en Wikipedia" target="_blank">
        <img src="img/totoro.jpg" alt="Portada de Mi vecino Totoro" />
      </a>
      <figcaption>Mi vecino Totoro (1988)</figcaption>
    </figure>

    <figure>
      <a href="https://es.wikipedia.org/wiki/La_princesa_Mononoke" title="Ver en Wikipedia" target="_blank">
        <img src="img/mononoke.jpg" alt="Portada de La princesa Mononoke" />
      </a>
      <figcaption>La princesa Mononoke (1997)</figcaption>
    </figure>

    <figure>
      <a href="https://es.wikipedia.org/wiki/El_castillo_ambulante" title="Ver en Wikipedia" target="_blank">
        <img src="img/castillo.jpg" alt="Portada de El castillo ambulante" />
      </a>
      <figcaption>El castillo ambulante (2004)</figcaption>
    </figure>

    <figure>
      <a href="https://es.wikipedia.org/wiki/Naussica%C3%A4_del_Valle_del_Viento" title="Ver en Wikipedia" target="_blank">
        <img src="img/nausicaa.jpg" alt="Portada de Nausicaä del Valle del Viento" />
      </a>
      <figcaption>Nausicaä del Valle del Viento (1984)</figcaption>
    </figure>
  </body>
</html>
```

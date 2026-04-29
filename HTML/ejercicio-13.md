# Ejercicio 13 de HTML

## Enunciado

A lo largo del capítulo hemos visto la importancia de la accesibilidad web. En este ejercicio recibes un documento HTML con varios problemas de accesibilidad. Tu tarea es identificarlos y corregirlos.

Los errores a corregir son:
1. Los textos de los enlaces no son descriptivos
2. La jerarquía de encabezados no es correcta
3. Una imagen no tiene atributo `alt`
4. Una imagen decorativa tiene el `alt` vacío siendo una imagen con contenido relevante
5. Las cabeceras de la tabla no usan `<th>` ni el atributo `scope`
6. Los campos del formulario no tienen `<label>` asociado
7. El campo de email usa `type="text"` en lugar del tipo correcto

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Tienda online</title>
  </head>
  <body>
    <header>
      <h1>Tienda online</h1>
      <nav>
        <ul>
          <!-- Error 1 corregido: textos descriptivos en los enlaces -->
          <li><a href="index.html">Inicio</a></li>
          <li><a href="productos.html">Ver todos los productos</a></li>
          <li><a href="contacto.html">Contactar con nosotros</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <!-- Error 2 corregido: jerarquía correcta h1 → h2 -->
      <h2>Productos destacados</h2>

      <figure>
        <!-- Error 3 corregido: añadido atributo alt descriptivo -->
        <img src="zapatillas.jpg" alt="Zapatillas deportivas blancas modelo Runner X" />
        <figcaption>Zapatillas</figcaption>
      </figure>

      <figure>
        <!-- Error 4 corregido: alt descriptivo en imagen con contenido relevante -->
        <img src="mochila.jpg" alt="Mochila de viaje gris con capacidad de 40 litros" />
        <figcaption>Mochila de viaje</figcaption>
      </figure>

      <table>
        <tr>
          <!-- Error 5 corregido: uso de th con scope -->
          <th scope="col">Producto</th>
          <th scope="col">Precio</th>
          <th scope="col">Disponibilidad</th>
        </tr>
        <tr>
          <td>Zapatillas</td>
          <td>59,99€</td>
          <td>En stock</td>
        </tr>
      </table>

      <form action="#" method="post">
        <!-- Error 6 corregido: labels asociados a cada input -->
        <label>
          Nombre
          <input type="text" name="nombre" />
        </label>
        <!-- Error 7 corregido: type="email" en lugar de type="text" -->
        <label>
          Email
          <input type="email" name="email" />
        </label>
        <input type="submit" value="Enviar" />
      </form>
    </main>

    <footer>
      <p>© 2024 Tienda online</p>
    </footer>
  </body>
</html>
```

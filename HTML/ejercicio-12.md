# Ejercicio 12 de HTML

## Enunciado

Este es el ejercicio final de HTML. El objetivo es maquetar en HTML una página completa de un blog personal aplicando todo lo que hemos aprendido: estructura semántica, texto, imágenes, enlaces, listas, tablas y formularios.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Mi Blog de Frontend</title>
  </head>
  <body>

    <header>
      <h1>Mi Blog de Frontend</h1>
      <nav>
        <ul>
          <li><a href="index.html">Inicio</a></li>
          <li><a href="portfolio.html">Portfolio</a></li>
          <li><a href="sobre-mi.html">Sobre mí</a></li>
          <li><a href="contacto.html">Contacto</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <article>
        <header>
          <h2>Cómo aprender HTML desde cero en 2024</h2>
          <time datetime="2024-04-29">29 de abril de 2024</time>
          <address>Por Óscar Bustos</address>
        </header>

        <figure>
          <img src="img/html.jpg" alt="Código HTML en un editor de texto" />
          <figcaption>El editor de código, tu mejor aliado para aprender HTML</figcaption>
        </figure>

        <p>
          Aprender HTML es el primer paso para cualquier persona que quiera adentrarse en
          el mundo del desarrollo web. Es un lenguaje <strong>accesible y directo</strong>
          que no requiere conocimientos previos de programación.
        </p>
        <p>
          Lo más importante al empezar es entender que HTML es un lenguaje de
          <em>marcado semántico</em> — cada etiqueta tiene un significado y una función concreta.
          No se trata de memorizar etiquetas sino de entender cuándo y por qué usarlas.
        </p>
        <p>
          Con constancia y práctica diaria, en pocas semanas serás capaz de estructurar
          cualquier página web con criterio y profesionalidad.
        </p>

        <blockquote>
          El aprendizaje más eficiente es el que se hace con las manos en la masa.
          Lee, practica y rompe cosas.
        </blockquote>
        <cite>Óscar Bustos</cite>

        <h3>Últimas entradas</h3>
        <ul>
          <li>
            <a href="#">Introducción a CSS</a>
            <time datetime="2024-04-22">22 de abril de 2024</time>
          </li>
          <li>
            <a href="#">Flexbox para principiantes</a>
            <time datetime="2024-04-15">15 de abril de 2024</time>
          </li>
          <li>
            <a href="#">JavaScript moderno: lo que necesitas saber</a>
            <time datetime="2024-04-08">8 de abril de 2024</time>
          </li>
          <li>
            <a href="#">Accesibilidad web: por qué importa</a>
            <time datetime="2024-04-01">1 de abril de 2024</time>
          </li>
        </ul>
      </article>

      <aside>
        <h2>Mis tecnologías favoritas</h2>
        <table>
          <tr>
            <th scope="col">Tecnología</th>
            <th scope="col">Descripción</th>
          </tr>
          <tr>
            <td>HTML5</td>
            <td>El lenguaje que estructura la web</td>
          </tr>
          <tr>
            <td>CSS3</td>
            <td>El lenguaje que da forma y vida a la web</td>
          </tr>
          <tr>
            <td>JavaScript</td>
            <td>El lenguaje que añade interactividad a la web</td>
          </tr>
        </table>

        <h2>Recursos recomendados</h2>
        <ul>
          <li><a href="https://developer.mozilla.org" target="_blank">MDN Web Docs</a></li>
          <li><a href="https://css-tricks.com" target="_blank">CSS Tricks</a></li>
          <li><a href="https://web.dev" target="_blank">Web.dev</a></li>
          <li><a href="https://a11yproject.com" target="_blank">The A11Y Project</a></li>
        </ul>
      </aside>
    </main>

    <footer>
      <small>© 2024 Mi Blog de Frontend. Todos los derechos reservados.</small>

      <section>
        <h2>Suscríbete al newsletter</h2>
        <form action="#" method="post">
          <label>
            Nombre
            <input type="text" name="nombre" required />
          </label>
          <label>
            Email
            <input type="email" name="email" required />
          </label>
          <label>
            Frecuencia de envío
            <select name="frecuencia">
              <option value="diaria">Diaria</option>
              <option value="semanal" selected>Semanal</option>
              <option value="mensual">Mensual</option>
            </select>
          </label>
          <input type="submit" value="Suscribirse" />
        </form>
      </section>
    </footer>

  </body>
</html>
```

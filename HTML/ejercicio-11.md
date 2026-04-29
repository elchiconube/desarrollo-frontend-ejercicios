# Ejercicio 11 de HTML

## Enunciado

En este ejercicio recibes un documento HTML mal etiquetado — todo el contenido está estructurado con `<div>` y etiquetas genéricas. Tu tarea es sustituirlas por las etiquetas semánticas de HTML5 más adecuadas para cada parte del contenido.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Blog de tecnología</title>
  </head>
  <body>
    <header>
      <h1>Blog de tecnología</h1>
      <nav>
        <ul>
          <li><a href="index.html">Inicio</a></li>
          <li><a href="about.html">Sobre mí</a></li>
          <li><a href="contacto.html">Contacto</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <article>
        <header>
          <h2>Cómo aprender HTML en 2024</h2>
          <time datetime="2024-03-15">15 de marzo de 2024</time>
          <address>Por Óscar Bustos</address>
        </header>
        <p>HTML es el lenguaje de marcado que estructura el contenido de la web...</p>
        <footer>
          <p>Etiquetas: HTML, Frontend, Web</p>
        </footer>
      </article>

      <aside>
        <h2>Artículos relacionados</h2>
        <ul>
          <li><a href="#">Introducción a CSS</a></li>
          <li><a href="#">JavaScript para principiantes</a></li>
          <li><a href="#">Accesibilidad web</a></li>
        </ul>
      </aside>
    </main>

    <footer>
      <small>© 2024 Blog de tecnología. Todos los derechos reservados.</small>
      <address>Contacto: <a href="mailto:hola@blogdetecnologia.com">hola@blogdetecnologia.com</a></address>
    </footer>
  </body>
</html>
```

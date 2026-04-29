# Ejercicio 4 de HTML

## Enunciado

Vamos a crear un documento HTML con un listado de tecnologías agrupadas por perfiles profesionales del mundo del desarrollo web. El objetivo es practicar las listas desordenadas `<ul>` y `<li>` con listas anidadas.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 4 HTML</title>
  </head>
  <body>
    <h1>Las tecnologías más utilizadas en el desarrollo web</h1>

    <ul>
      <li>
        Desarrollo <em>frontend</em>
        <ul>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>Javascript</li>
          <li>React</li>
          <li>Vue</li>
        </ul>
      </li>
      <li>
        Desarrollo <em>backend</em>
        <ul>
          <li>PHP</li>
          <li>Python</li>
          <li>Java</li>
          <li>Node.js</li>
          <li>Ruby</li>
        </ul>
      </li>
      <li>
        Perfil <em>fullstack</em>
        <ul>
          <li>Combinación de tecnologías frontend y backend</li>
          <li>Docker</li>
          <li>Git</li>
        </ul>
      </li>
      <li>
        Responsable de sistemas
        <ul>
          <li>Linux</li>
          <li>AWS</li>
          <li>Nginx</li>
        </ul>
      </li>
    </ul>
  </body>
</html>
```

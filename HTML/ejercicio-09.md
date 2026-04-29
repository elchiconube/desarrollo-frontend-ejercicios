# Ejercicio 9 de HTML

## Enunciado

Vamos a crear un documento HTML con una tabla comparativa. El objetivo es practicar las etiquetas `<table>`, `<caption>`, `<tr>`, `<th>` y `<td>`, así como los atributos `scope`, `colspan` y `rowspan`.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 9 HTML</title>
  </head>
  <body>
    <h1>Los lenguajes de programación más populares</h1>

    <table>
      <caption>Comparativa de lenguajes de programación</caption>
      <tr>
        <th scope="col">Lenguaje</th>
        <th scope="col">Tipo</th>
        <th scope="col">Usos principales</th>
        <th scope="col">Año de creación</th>
      </tr>
      <tr>
        <td>JavaScript</td>
        <td>Interpretado</td>
        <td>Frontend, Backend, Mobile</td>
        <td>1995</td>
      </tr>
      <tr>
        <td>Python</td>
        <td>Interpretado</td>
        <td>Data Science, IA, Backend</td>
        <td>1991</td>
      </tr>
      <tr>
        <td>Java</td>
        <td>Compilado</td>
        <td>Backend, Android, Empresarial</td>
        <td>1995</td>
      </tr>
      <tr>
        <td>PHP</td>
        <td>Interpretado</td>
        <td>Backend, Web</td>
        <td>1994</td>
      </tr>
      <tr>
        <td>Swift</td>
        <td>Compilado</td>
        <td>iOS, macOS</td>
        <td>2014</td>
      </tr>
      <tr>
        <td>Rust</td>
        <td>Compilado</td>
        <td>Sistemas, WebAssembly</td>
        <td>2010</td>
      </tr>
      <tr>
        <td colspan="4">Fuente: Stack Overflow Developer Survey 2024</td>
      </tr>
    </table>
  </body>
</html>
```

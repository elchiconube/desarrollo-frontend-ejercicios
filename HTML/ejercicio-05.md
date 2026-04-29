# Ejercicio 5 de HTML

## Enunciado

Vamos a crear un documento HTML con un listado de términos y sus definiciones. El objetivo es practicar las listas de definiciones usando las etiquetas `<dl>`, `<dt>` y `<dd>`. Para ello busca el significado de cada una de las siguientes palabras raras del castellano y añádelas como definición.

**Titular**: Las palabras más raras del castellano

**Listado de términos**: Acmé, Burdégano, Uebos, Bluyín

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 5 HTML</title>
  </head>
  <body>
    <h1>Las palabras más raras del castellano</h1>

    <dl>
      <dt>Acmé</dt>
      <dd>Período de mayor intensidad de una enfermedad o de cualquier otro proceso. También se usa para referirse al punto más alto o culminante de algo.</dd>

      <dt>Burdégano</dt>
      <dd>Híbrido estéril nacido de caballo y burra, a diferencia del mulo, que nace de asno y yegua.</dd>

      <dt>Uebos</dt>
      <dd>Voz antigua que significa necesidad o cosa necesaria. Procede del latín "opus" (obra, necesidad).</dd>

      <dt>Bluyín</dt>
      <dd>Adaptación al español de la palabra inglesa "blue jeans". Pantalón vaquero de tela resistente, generalmente de color azul.</dd>
    </dl>
  </body>
</html>
```

# Ejercicio 10 de HTML

## Enunciado

Vamos a crear un documento HTML con un formulario de registro. El objetivo es practicar las etiquetas de formulario que hemos visto: `<form>`, `<input>`, `<label>`, `<select>`, `<textarea>`, `<fieldset>`, `<legend>`, `<meter>` y `<progress>`.

## Solución

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ejercicio 10 HTML</title>
  </head>
  <body>
    <h1>Formulario de registro</h1>

    <form action="#" method="post">

      <fieldset>
        <legend>Datos personales</legend>

        <label>
          Nombre completo
          <input type="text" name="nombre" required />
        </label>

        <label>
          Fecha de nacimiento
          <input type="date" name="fecha_nacimiento" />
        </label>

        <label>
          DNI
          <input type="text" name="dni" maxlength="9" />
        </label>

        <label>
          Correo electrónico
          <input type="email" name="email" required />
        </label>

        <label>
          Género
          <select name="genero">
            <option value="">Selecciona una opción</option>
            <option value="hombre">Hombre</option>
            <option value="mujer">Mujer</option>
            <option value="no-decir">Prefiero no decirlo</option>
          </select>
        </label>
      </fieldset>

      <fieldset>
        <legend>Días de reparto</legend>

        <label>
          <input type="checkbox" name="dias" value="lunes" />
          Lunes
        </label>
        <label>
          <input type="checkbox" name="dias" value="martes" />
          Martes
        </label>
        <label>
          <input type="checkbox" name="dias" value="miercoles" />
          Miércoles
        </label>
        <label>
          <input type="checkbox" name="dias" value="jueves" />
          Jueves
        </label>
        <label>
          <input type="checkbox" name="dias" value="viernes" />
          Viernes
        </label>
      </fieldset>

      <fieldset>
        <legend>Comentarios y valoración</legend>

        <label>
          Comentarios adicionales
          <textarea name="comentarios" rows="4"></textarea>
        </label>

        <label for="satisfaccion">Nivel de satisfacción:</label>
        <meter id="satisfaccion" min="0" max="10" low="3" high="7" optimum="9" value="7">7 de 10</meter>

        <label for="progreso">Progreso del registro:</label>
        <progress id="progreso" max="100" value="80">80%</progress>
      </fieldset>

      <label>
        <input type="checkbox" name="privacidad" required />
        He leído y acepto la política de privacidad
      </label>

      <input type="reset" value="Limpiar formulario" />
      <input type="submit" value="Enviar" />

    </form>
  </body>
</html>
```

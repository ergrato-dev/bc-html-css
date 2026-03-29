# Glosario — Semana 03: Formularios y Multimedia

Términos clave de la semana ordenados alfabéticamente.

---

## A

**`action`**
Atributo de `<form>`. Define la URL a la que se envían los datos del formulario al hacer submit.

**`allowfullscreen`**
Atributo booleano de `<iframe>`. Permite que el contenido embebido se expanda a pantalla completa.

**`<audio>`**
Elemento HTML5 para reproducir audio nativo en el navegador. Requiere `controls` para que el usuario pueda interactuar.

**`autocomplete`**
Atributo de `<input>` y `<form>`. Indica al navegador si puede autocompletar el campo con datos guardados (`email`, `name`, `tel`, etc.).

---

## B

**`<button>`**
Elemento de botón interactivo. `type="submit"` envía el formulario; `type="reset"` lo limpia; `type="button"` no hace nada por defecto.

---

## C

**`<caption>`**
Elemento opcional de `<table>` que provee un título descriptivo. Visible y anunciado por lectores de pantalla antes de la tabla.

**`checkbox`**
Tipo de input para selección múltiple. Múltiples checkboxes con el mismo `name` permiten seleccionar varias opciones.

**`colspan`**
Atributo de `<td>` o `<th>`. Define cuántas columnas abarca la celda horizontalmente.

**`controls`**
Atributo booleano de `<video>` y `<audio>`. Muestra los controles del reproductor (play, volumen, barra de progreso).

---

## D

**`<datalist>`**
Provee sugerencias para un `<input type="text">`. Vinculado al input con el atributo `list` = `id` del datalist.

---

## F

**`<fieldset>`**
Agrupa campos de formulario relacionados. Mejora la accesibilidad y organización visual. Siempre usar con `<legend>`.

**`<form>`**
Contenedor de elementos de formulario. Sus atributos principales son `action` (destino) y `method` (GET/POST).

**`frameborder`**
Atributo de `<iframe>` con valor `"0"` para eliminar el borde del iframe (aunque es preferible usar CSS).

---

## I

**`<iframe>`**
Elemento para incrustar contenido externo (videos de YouTube, mapas, etc.). Siempre requiere `title` descriptivo.

**`<input>`**
Elemento de entrada de datos en formularios. El atributo `type` define su comportamiento visual e interactivo.

---

## L

**`<label>`**
Etiqueta accesible para un control de formulario. El atributo `for` debe coincidir con el `id` del input al que describe.

**`<legend>`**
Subtítulo accesible de un `<fieldset>`. Describe el grupo de campos que contiene.

**`loading="lazy"`**
Atributo de `<img>` e `<iframe>`. Carga el elemento solo cuando está a punto de aparecer en el viewport.

---

## M

**`maxlength` / `minlength`**
Atributos de texto en `<input>` y `<textarea>`. Limitan la cantidad de caracteres permitidos.

**`method`**
Atributo de `<form>`. `GET` envía datos en la URL (visible); `POST` los envía en el cuerpo de la petición (más seguro para datos sensibles).

**`min` / `max`**
Atributos de `<input type="number">` y `<input type="date">`. Definen el rango de valores válidos.

---

## O

**`<option>`**
Cada item seleccionable dentro de `<select>`. El atributo `value` define el dato enviado al servidor.

---

## P

**`pattern`**
Atributo de `<input>`. Define una expresión regular que el valor debe cumplir para ser válido.

**`placeholder`**
Texto de sugerencia visible cuando el campo está vacío. **No reemplaza al `<label>`**.

**`poster`**
Atributo de `<video>`. URL de una imagen que se muestra como miniatura antes de reproducir el video.

**`preload`**
Atributo de `<video>` y `<audio>`. Valores: `none` (no precarga), `metadata` (solo metadatos), `auto` (carga completa).

---

## R

**`radio`**
Tipo de input para selección única dentro de un grupo. Todos los radios del mismo `name` forman el grupo.

**`required`**
Atributo booleano de inputs. El formulario no puede enviarse si este campo está vacío.

**`rowspan`**
Atributo de `<td>` o `<th>`. Define cuántas filas abarca la celda verticalmente.

---

## S

**`<select>`**
Lista desplegable de opciones. Contiene elementos `<option>` y opcionalmente `<optgroup>` para agrupar opciones.

**`<source>`**
Elemento hijo de `<video>` o `<audio>`. Define un formato alternativo de media. El navegador elige el primero que soporta.

**`scope`**
Atributo de `<th>`. Indica si el encabezado aplica a `col` (columna), `row` (fila), `colgroup` o `rowgroup`.

---

## T

**`<table>`**
Elemento para datos tabulares con relación de filas y columnas.

**`<tbody>`**
Cuerpo de la tabla. Contiene las filas de datos principales.

**`<td>`**
Celda de datos en una tabla. Se ubica dentro de `<tr>`.

**`<textarea>`**
Campo de texto de múltiples líneas. Los atributos `rows` y `cols` sugieren su tamaño inicial.

**`<tfoot>`**
Pie de la tabla. Contiene filas de resumen, totales o notas.

**`<th>`**
Celda de encabezado. A diferencia de `<td>`, su contenido se formatea en negrita y se centra por defecto. Usar `scope` siempre.

**`<thead>`**
Encabezado de la tabla. Contiene la fila (o filas) de títulos de columna.

**`<track>`**
Subtítulos o captions para `<video>`. El atributo `kind` define si son `subtitles`, `captions`, `descriptions`, etc.

**`<tr>`**
Fila de una tabla. Contiene células `<td>` o `<th>`.

---

## V

**`<video>`**
Elemento HTML5 para video nativo. Atributos clave: `controls`, `src`, `poster`, `preload`, `width`, `height`.

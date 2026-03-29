# Glosario — Semana 02: HTML Fundamentos

Términos clave de la semana ordenados alfabéticamente.

---

## A

**`alt` (atributo)**
Texto alternativo de una imagen. Es obligatorio en todo `<img>` — describe la imagen para lectores de pantalla y se muestra si la imagen no carga. Debe ser vacío (`alt=""`) solo en imágenes decorativas.

**`<article>`**
Elemento semántico para contenido autocontenido que puede distribuirse independientemente: un post de blog, una noticia, una tarjeta de producto.

**`<aside>`**
Contenido relacionado pero no principal de la página. Ejemplo: barras laterales, publicidad, citas relacionadas.

**`<a>`** (anchor)
Elemento para crear hipervínculos. El atributo `href` define el destino del enlace.

---

## B

**`<body>`**
Elemento que contiene todo el contenido visible de la página HTML.

---

## C

**`charset`**
Atributo de `<meta charset="UTF-8">`. UTF-8 permite mostrar caracteres de cualquier idioma, incluyendo acentos y ñ.

---

## D

**DOCTYPE**
Declaración `<!DOCTYPE html>` que indica al navegador que el documento usa HTML5. Siempre va en la primera línea.

**`<dl>` / `<dt>` / `<dd>`**
Lista de definición. `<dt>` es el término, `<dd>` es su descripción. Útil para glosarios y metadatos.

---

## E

**Elemento semántico**
Etiqueta HTML cuyo nombre describe el rol de su contenido (ej: `<nav>`, `<footer>`, `<article>`). Se opone a los "divs sin semántica" (divitis).

---

## F

**`<figure>` / `<figcaption>`**
Agrupan contenido multimedia con su descripción. `<figure>` es el contenedor; `<figcaption>` es el pie de foto.

**`<footer>`**
Pie de página de un documento o sección. Contiene información de contacto, copyright, links secundarios.

---

## H

**`<head>`**
Sección invisible del documento HTML. Contiene metadatos: charset, viewport, title, links a CSS, meta description.

**`<header>`**
Encabezado de la página o de una sección. Normalmente contiene el logo, título y navegación principal.

**Heading / `<h1>`–`<h6>`**
Etiquetas de encabezado que definen la jerarquía del contenido. Solo un `<h1>` por página; no saltar niveles.

**`href`**
Atributo de `<a>` que define el destino del enlace: URL, ruta relativa, ancla (`#id`), mailto o tel.

---

## I

**`<img>`**
Elemento de imagen en línea (inline). Requiere `src` (ruta) y `alt` (texto alternativo). Sin etiqueta de cierre.

---

## L

**`lang`**
Atributo de `<html lang="es">`. Indica el idioma principal del documento. Esencial para lectores de pantalla y SEO.

---

## M

**`<main>`**
Contenido principal único de la página. Solo debe haber uno por documento. Es el área central de contenido, excluyendo header, nav y footer.

**`<meta>`**
Elemento de metadatos en el `<head>`. Ejemplos: `charset`, `viewport`, `description`.

---

## N

**`<nav>`**
Elemento semántico para conjuntos de enlaces de navegación: menú principal, breadcrumbs, paginación.

---

## P

**`<p>`**
Párrafo de texto. Elemento de bloque con margen automático arriba y abajo.

**Ruta relativa**
Ruta de archivo que parte desde la ubicación actual: `./imagen.png`, `../assets/img.jpg`.

**Ruta absoluta**
URL completa que incluye protocolo y dominio: `https://ejemplo.com/imagen.png`.

---

## R

**`rel="noopener noreferrer"`**
Atributo de seguridad obligatorio en enlaces con `target="_blank"`. Evita que la pestaña nueva pueda acceder al contexto de la pestaña original.

---

## S

**`<section>`**
Agrupa contenido temáticamente relacionado dentro de `<main>`. Debe tener un heading que lo identifique.

**Semántica HTML**
Filosofía de usar las etiquetas HTML según su significado, no solo por su apariencia visual.

**`<strong>`**
Importancia semántica. El navegador lo muestra en negrita, pero su propósito es indicar importancia al procesamiento del lenguaje.

---

## T

**`target="_blank"`**
Atributo de `<a>` que abre el enlace en nueva pestaña. Siempre usar con `rel="noopener noreferrer"`.

**`<time>`**
Elemento semántico para representar fechas y horas. El atributo `datetime` proporciona el formato de máquina.

**`<title>`**
Título del documento que aparece en la pestaña del navegador y en resultados de búsqueda. Es obligatorio en `<head>`.

---

## V

**`viewport`**
`<meta name="viewport" content="width=device-width, initial-scale=1.0">`. Esencial para que el diseño se adapte correctamente en dispositivos móviles.

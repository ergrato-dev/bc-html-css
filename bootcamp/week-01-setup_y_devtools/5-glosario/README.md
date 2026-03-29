# Glosario — Semana 01: Setup y DevTools

Términos clave de la semana, ordenados alfabéticamente.

---

## A

### Activity Bar
Barra vertical en el extremo izquierdo de VS Code con iconos para acceder a los paneles principales: Explorer, Búsqueda, Control de versiones, Extensiones y más.

### Alt text (`alt`)
Atributo obligatorio en la etiqueta `<img>` que describe el contenido de la imagen para lectores de pantalla y en caso de que la imagen no cargue. Ejemplo: `<img src="foto.jpg" alt="Fotografía de un gato durmiendo" />`.

---

## B

### Breakpoint
Punto de interrupción en el código. En DevTools permite pausar la ejecución de JavaScript en una línea específica para inspeccionarlo paso a paso.

---

## C

### Cascada CSS
Mecanismo por el que el navegador determina qué regla CSS aplicar cuando varias reglas afectan al mismo elemento. Considera origen del estilo, especificidad y orden de aparición.

### Charset (`charset`)
Atributo de `<meta>` que declara la codificación de caracteres del documento. Siempre debe ser `UTF-8` para soportar cualquier idioma: `<meta charset="UTF-8" />`.

### Command Palette
Panel de comandos de VS Code. Se abre con `Ctrl+Shift+P` y permite acceder a cualquier función del editor escribiendo su nombre.

### Computed (panel)
Pestaña dentro del panel Elements de DevTools que muestra el valor **final** y calculado de cada propiedad CSS de un elemento, tras aplicar toda la cascada. Muestra los valores resueltos (en px, rgb, etc.), no los declarados.

### CSS (Cascading Style Sheets)
Lenguaje de estilos para definir la apariencia visual de documentos HTML: colores, tipografía, espaciado, layout y animaciones.

### Custom Properties (Variables CSS)
Valores reutilizables definidos en CSS con la sintaxis `--nombre-variable: valor`. Se declaran habitualmente en `:root` y se usan con `var(--nombre-variable)`.

---

## D

### DevTools
Conjunto de herramientas de desarrollo integradas en el navegador (Chrome, Firefox, Safari). Permiten inspeccionar el DOM, depurar estilos CSS, ver errores de red y mucho más. Se abren con `F12` o `Ctrl+Shift+I`.

### DOCTYPE
Declaración en la primera línea de un documento HTML que indica al navegador la versión de HTML usada. Para HTML5: `<!DOCTYPE html>`.

### DOM (Document Object Model)
Representación en forma de árbol de todos los elementos HTML de una página. El navegador lo crea al parsear el HTML y es lo que DevTools muestra en el panel Elements.

---

## E

### Emmet
Sistema de abreviaciones integrado en VS Code que permite escribir HTML y CSS rápidamente. Por ejemplo: `h1` + `Tab` → `<h1></h1>`, o `!` + `Tab` → plantilla HTML5 completa.

### Editor (VS Code)
Zona central de VS Code donde se edita el código. Soporta múltiples pestañas, resaltado de sintaxis, Emmet y formateo automático.

### Extensions (Extensiones)
Complementos que amplían las funcionalidades de VS Code. Se instalan depuis el panel de extensiones (`Ctrl+Shift+X`). Esenciales para esta semana: Live Server, Prettier, HTML CSS Support.

---

## F

### `formatOnSave`
Configuración de VS Code (`"editor.formatOnSave": true`) que formatea automáticamente el código al guardar el archivo. Requiere un formateador instalado como Prettier.

---

## G

### Git
Sistema de control de versiones distribuido. Permite rastrear cambios en el código y colaborar en equipo. Comandos básicos: `git init`, `git add .`, `git commit -m "mensaje"`.

---

## H

### HTML5 (HyperText Markup Language 5)
Versión actual del lenguaje de marcado para crear páginas web. Introduce nuevas etiquetas semánticas (`<header>`, `<main>`, `<footer>`, `<article>`, `<section>`, etc.) y APIs nativas del navegador.

### `href`
Atributo de la etiqueta `<a>` y `<link>` que define el destino de un enlace o la ruta de un recurso. Ejemplo: `<a href="https://ejemplo.com">`, `<link href="css/styles.css" />`.

---

## I

### IntelliSense
Sistema de autocompletado inteligente de VS Code. Sugiere etiquetas HTML, propiedades CSS y nombres de clases mientras escribes.

---

## K

### Kebab-case
Convención de nomenclatura para archivos, clases CSS e IDs HTML en la que las palabras se escriben en minúsculas y se separan con guiones. Ejemplos: `mi-proyecto`, `nav-item`, `hero-title`.

---

## L

### `lang`
Atributo de la etiqueta `<html>` que declara el idioma del documento. Importante para accesibilidad y SEO. Ejemplo: `<html lang="es">` para español.

### Live Server
Extensión de VS Code que lanza un servidor local y recarga el navegador automáticamente cada vez que se guarda un archivo. La URL es `http://localhost:5500`.

### `localhost`
Dirección que apunta a la misma máquina donde se ejecuta el servidor. `http://localhost:5500` es la URL que usa Live Server, a diferencia de `file://` que abre el archivo directamente.

---

## M

### `meta viewport`
Etiqueta HTML que controla cómo se escala la página en dispositivos móviles. Sin ella, los teléfonos muestran la página reducida como si fuera escritorio. Uso estándar: `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`.

### Mobile-first
Estrategia de diseño web que consiste en diseñar primero para pantallas pequeñas (móvil) y luego añadir estilos para pantallas más grandes mediante Media Queries con `min-width`.

---

## P

### Panel Elements
Pestaña principal de DevTools que muestra el árbol DOM de la página y permite editarlo en vivo: modificar atributos, texto, eliminar o mover nodos.

### Panel Styles
Subpanel dentro de Elements que muestra todas las reglas CSS que se aplican al elemento seleccionado, ordenadas de mayor a menor especificidad. Las propiedades sobreescritas aparecen tachadas.

### Prettier
Formateador de código para VS Code. Aplica reglas consistentes de formato (sangría, comillas, punto y coma) al guardar. Se configura con el archivo `.prettierrc`.

### `.prettierrc`
Archivo de configuración de Prettier ubicado en la raíz del proyecto. Define reglas como el ancho de línea (`printWidth`), el tamaño del tabulado (`tabWidth`) y el tipo de comillas (`singleQuote`).

---

## R

### Ruta relativa
Ruta de un archivo que parte desde la ubicación del archivo actual (no desde la raíz del sistema). Ejemplo: `css/styles.css` (en la misma carpeta) o `../images/foto.jpg` (en la carpeta padre).

---

## S

### `settings.json`
Archivo de configuración de VS Code en formato JSON. Se accede con `Ctrl+Shift+P` → "Open User Settings (JSON)". Permite configurar opciones como `formatOnSave`, `fontSize` y `tabSize`.

### Sidebar
Panel lateral izquierdo de VS Code que muestra el árbol de archivos del proyecto (Explorer), búsquedas, extensiones instaladas, etc.

### Especificidad CSS
Sistema de puntos que determina qué regla CSS "gana" cuando varias reglas aplican a un mismo elemento. Los IDs tienen más especificidad que las clases, y las clases más que las etiquetas.

---

## T

### Terminal integrada
Panel en VS Code que permite ejecutar comandos de la línea de comandos sin salir del editor. Se abre con `Ctrl+\`` o desde el menú **Terminal → New Terminal**.

---

## U

### UTF-8
Codificación de caracteres que soporta prácticamente todos los idiomas del mundo. Debe declararse siempre con `<meta charset="UTF-8" />` en el `<head>` de cualquier documento HTML.

---

## V

### Viewport
Área visible del navegador donde se muestra la página web. En dispositivos móviles, el viewport puede ser diferente al ancho físico de la pantalla; la etiqueta `<meta viewport>` lo controla.

### VS Code (Visual Studio Code)
Editor de código fuente gratuito y de código abierto creado por Microsoft. Es el estándar de la industria para desarrollo web. Disponible en [code.visualstudio.com](https://code.visualstudio.com).

---

## W

### W3C Validator
Herramienta oficial del World Wide Web Consortium para validar que el código HTML cumple con el estándar. Disponible en [validator.w3.org](https://validator.w3.org).

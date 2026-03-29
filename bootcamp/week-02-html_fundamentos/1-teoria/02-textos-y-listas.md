# 02 — Textos y listas

## 🎯 Objetivos

- Usar la jerarquía de headings correctamente
- Marcar énfasis semántico con `<strong>` y `<em>`
- Crear listas ordenadas, no ordenadas y de descripción

---

## 1. Jerarquía de headings

Los headings del `<h1>` al `<h6>` crean la estructura de contenido de la página. No son solo "títulos grandes o pequeños" — son la **tabla de contenidos** del documento.

```html
<h1>Título principal de la página</h1>      <!-- Solo uno por página -->
  <h2>Sección principal</h2>
    <h3>Subsección</h3>
      <h4>Sub-subsección</h4>
```

### Reglas fundamentales:

| Regla | Por qué |
|-------|---------|
| Un solo `<h1>` por página | Define el tema principal; duplicarlo confunde al SEO |
| No saltar niveles (h2 → h4) | Rompe la jerarquía para lectores de pantalla |
| El nivel refleja la estructura, no el tamaño visual | El tamaño se controla con CSS, no con el nivel del heading |

```html
<!-- ✅ CORRECTO -->
<h1>Mi Portfolio</h1>
<h2>Proyectos</h2>
<h3>Proyecto 1</h3>

<!-- ❌ INCORRECTO — saltó de h2 a h4 -->
<h1>Mi Portfolio</h1>
<h4>Proyectos</h4>
```

---

## 2. Párrafos y saltos de línea

```html
<!-- Párrafo — el elemento más común para texto -->
<p>Este es un párrafo. El navegador añade espacio automático entre párrafos.</p>
<p>Este es otro párrafo separado.</p>

<!-- Salto de línea dentro de un párrafo — usar con moderación -->
<p>
  Línea 1<br />
  Línea 2 (mismo párrafo, línea diferente)
</p>

<!-- Separación temática horizontal — elemento semántico, no decorativo -->
<hr />
```

> ⚠️ Nunca uses `<br />` para añadir espacio entre párrafos. Para espaciado, usa CSS (`margin`).

---

## 3. Énfasis semántico

```html
<!-- <strong> = importancia, urgencia o gravedad (bold por defecto) -->
<p>
  <strong>Atención:</strong> esta acción no se puede deshacer.
</p>

<!-- <em> = énfasis en la pronunciación (italic por defecto) -->
<p>
  La respuesta <em>correcta</em> es la tercera opción.
</p>

<!-- <small> = texto secundario, aclaraciones legales -->
<small>© 2026 ergrato-dev. Todos los derechos reservados.</small>
```

> 💡 **Buena práctica — año dinámico:** el año hardcodeado en el copyright necesita
> actualizarse a mano cada nuevo año. JavaScript lo resuelve con una línea:
>
> ```html
> <small>© <span id="copyright-year">2026</span> ergrato-dev</small>
>
> <script>
>   document.getElementById('copyright-year').textContent = new Date().getFullYear();
> </script>
> ```
>
> El `<span>` tiene el año estático como **fallback** y `new Date().getFullYear()`
> lo sobreescribe automáticamente al cargar la página.

```html
<!-- <mark> = texto resaltado (relevante en contexto) -->
<p>Busca la palabra <mark>semántica</mark> en el documento.</p>

<!-- <code> = código de programación en línea -->
<p>Usa la propiedad <code>display: flex</code> para activar Flexbox.</p>
```

> `<b>` y `<i>` existen pero no tienen significado semántico. Úsalos solo si no aplica `<strong>` ni `<em>`.

---

## 4. Listas

### Lista no ordenada `<ul>`

Para ítems sin orden específico (ingredientes, características, menús de navegación):

```html
<ul>
  <li>HTML5</li>
  <li>CSS3</li>
  <li>VS Code</li>
</ul>
```

### Lista ordenada `<ol>`

Para ítems que tienen un orden lógico (pasos, rankings, instrucciones):

```html
<ol>
  <li>Instalar VS Code</li>
  <li>Instalar Live Server</li>
  <li>Crear el archivo index.html</li>
</ol>
```

`<ol>` acepta atributos: `start="5"` (empezar desde 5), `reversed` (orden inverso), `type="A"` (letras).

### Lista de descripción `<dl>`

Para parejas término–definición (glosarios, metadatos, FAQs):

```html
<dl>
  <dt>HTML</dt>
  <dd>Lenguaje de marcado para estructurar contenido web.</dd>

  <dt>CSS</dt>
  <dd>Lenguaje de estilos para controlar la apariencia visual.</dd>
</dl>
```

### Listas anidadas

```html
<ul>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
  </li>
  <li>Backend</li>
</ul>
```

---

## 5. Texto preformateado

```html
<!-- <pre> preserva espacios y saltos de línea tal como están escritos -->
<pre>
  function saludar() {
    return "Hola";
  }
</pre>
```

---

## ✅ Checklist

- [ ] Solo un `<h1>` por página
- [ ] Headings en orden jerárquico continuo
- [ ] `<strong>` para importancia, `<em>` para énfasis (no para estilo)
- [ ] `<ul>` para listas sin orden, `<ol>` para listas con orden
- [ ] `<dl>` para glosarios y parejas término-definición
- [ ] Sin `<br />` para reemplazar márgenes CSS

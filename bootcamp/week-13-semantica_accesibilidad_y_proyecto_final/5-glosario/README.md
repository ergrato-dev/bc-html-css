# Glosario — Semana 13

Términos clave de Semántica HTML5, Accesibilidad Web, SEO y Rendimiento.

---

## A

### `<address>`
Elemento HTML semántico que marca información de contacto del autor o el propietario más cercano. Se renderiza en cursiva por defecto. No usar para direcciones postales genéricas, solo para el contexto del documento o sección.

```html
<footer>
  <address>
    Contacto: <a href="mailto:hola@ejemplo.com">hola@ejemplo.com</a>
  </address>
</footer>
```

---

### `alt` (atributo)
Texto alternativo en `<img>`. Leído por lectores de pantalla y mostrado cuando la imagen no carga. Si la imagen es decorativa, usar `alt=""`. Si es informativa, describir su contenido de forma concisa.

```html
<!-- Informativa: describir el contenido -->
<img src="foto.jpg" alt="Ana García sonriendo frente al mar" />

<!-- Decorativa: alt vacío -->
<img src="divider.svg" alt="" role="presentation" />
```

---

### `aria-current`
Atributo ARIA que indica que un elemento representa el ítem actual en un conjunto (página, step, location). Valores comunes: `"page"`, `"step"`, `"location"`, `"true"`.

```html
<nav>
  <a href="/inicio">Inicio</a>
  <a href="/contacto" aria-current="page">Contacto</a>
</nav>
```

---

### `aria-describedby`
Atributo ARIA que asocia un elemento con otro que lo describe. A diferencia de `aria-labelledby`, la descripción es información secundaria (como una pista o mensaje de error).

```html
<input id="email" aria-describedby="email-hint" />
<p id="email-hint">Ej: nombre@dominio.com</p>
```

---

### `aria-hidden`
Atributo ARIA que oculta un elemento y sus descendientes del árbol de accesibilidad. Usar en elementos decorativos para que los lectores de pantalla no los lean.

```html
<span aria-hidden="true">🎉</span>
<button>Celebrar<span aria-hidden="true"> 🎉</span></button>
```

---

### `aria-label`
Atributo ARIA que proporciona una etiqueta de texto accesible cuando no existe una etiqueta visual visible. Ideal para botones con solo iconos.

```html
<button aria-label="Cerrar ventana">×</button>
```

---

### `aria-labelledby`
Atributo ARIA que asocia un elemento con otro elemento visible que actúa como su etiqueta. El texto del elemento referenciado se convierte en el nombre accesible.

```html
<section aria-labelledby="sec-title">
  <h2 id="sec-title">Proyectos destacados</h2>
</section>
```

---

### `aria-live`
Atributo ARIA que convierte una región en una "live region". Cuando su contenido cambia, el lector de pantalla lo anuncia automáticamente. Valores: `"off"` (default), `"polite"` (espera turno), `"assertive"` (interrumpe).

```html
<p aria-live="polite" role="status">Guardando cambios...</p>
```

---

### Árbol de Accesibilidad
Representación del DOM creada por el navegador para los lectores de pantalla. Solo incluye elementos con rol semántico. Los elementos con `display:none`, `visibility:hidden` o `aria-hidden="true"` quedan excluidos.

---

### `<article>`
Elemento semántico para contenido autocontenido que podría redistribuirse de forma independiente: posts de blog, noticias, comentarios, tarjetas de producto. Puede contener su propio `<header>` y `<footer>`.

---

### `<aside>`
Elemento semántico para contenido relacionado indirectamente con el contenido principal: sidebars, pull quotes, publicidad, widgets. Su rol de landmark ARIA es `complementary`.

---

## C

### CLS (Cumulative Layout Shift)
Core Web Vital que mide la estabilidad visual de la página. Un valor ≤ 0.1 es considerado bueno. Se reduce estableciendo `width` y `height` en imágenes y reservando espacio para contenido que carga de forma asíncrona.

---

### Core Web Vitals
Conjunto de métricas de rendimiento definidas por Google que reflejan la experiencia real del usuario: **LCP** (carga), **CLS** (estabilidad visual) e **INP** (interactividad). Afectan el posicionamiento en buscadores.

---

## F

### `<figure>` y `<figcaption>`
`<figure>` agrupa contenido autocontenido con su descripción. `<figcaption>` es la leyenda opcional dentro de `<figure>`. Permite asociar semánticamente una imagen con su texto descriptivo.

```html
<figure>
  <img src="chart.png" alt="Gráfica de ventas 2025" />
  <figcaption>Ventas Q1–Q4 2025. Fuente: datos internos.</figcaption>
</figure>
```

---

### `:focus-visible`
Pseudo-clase CSS que representa el estado de foco solo cuando el navegador determina que el usuario está navegando con teclado o dispositivos de entrada equivalentes. Permite estilos de foco claros para teclado sin afectar la experiencia con ratón.

```css
:focus { outline: none; }
:focus-visible { outline: 3px solid #3b82f6; outline-offset: 3px; }
```

---

## I

### INP (Interaction to Next Paint)
Core Web Vital que mide la capacidad de respuesta a la interacción del usuario. Un valor ≤ 200ms es bueno. Reemplazó al FID en 2024.

---

## L

### Landmark
Región HTML con rol de navegación en el árbol de accesibilidad. Los lectores de pantalla usan las teclas de landmark para navegar rápidamente. Landmarks principales: `<header>` → `banner`, `<nav>` → `navigation`, `<main>` → `main`, `<aside>` → `complementary`, `<footer>` → `contentinfo`.

---

### LCP (Largest Contentful Paint)
Core Web Vital que mide el tiempo de carga del elemento más grande visible en la pantalla inicial. Un valor ≤ 2.5s es bueno. Se mejora con `fetchpriority="high"` en la imagen hero y evitando `loading="lazy"` en elementos above the fold.

---

## M

### `<main>`
Elemento semántico que marca el contenido principal de la página. Debe haber solo uno por página, no estar anidado dentro de `<article>`, `<aside>`, `<header>`, `<footer>` o `<nav>`. Su rol ARIA es `main`.

---

## O

### Open Graph
Protocolo de metadatos definido por Facebook para controlar cómo se muestra una URL al compartirse en redes sociales. Los tags `og:title`, `og:description`, `og:image` y `og:url` son los más importantes.

```html
<meta property="og:title" content="Mi Portfolio" />
<meta property="og:image" content="https://ejemplo.com/og.jpg" />
```

---

## P

### `prefers-reduced-motion`
Media query de preferencia del sistema operativo. Cuando el usuario activa "Reducir movimiento", las animaciones y transiciones deben eliminarse o reducirse significativamente para evitar malestar en personas con sensibilidad vestibular.

```css
@media (prefers-reduced-motion: no-preference) {
  .hero { animation: fade-in 0.5s ease; }
}
```

---

## R

### `role="alert"`
Propiedad ARIA que convierte un elemento en una "alert". El contenido es leído automáticamente por los lectores de pantalla cuando aparece o cambia, sin que el usuario tenga que moverle el foco. Equivalente a `aria-live="assertive"`.

---

## S

### `<section>`
Elemento semántico para agrupar contenido temáticamente relacionado. **Siempre debe tener un heading** (`h1`–`h6`) que la describa; si no, usar `<div>`. Su rol ARIA solo es `region` cuando tiene un nombre accesible (`aria-labelledby`).

---

### Skip link
Enlace al inicio de la página (normalmente `<a href="#main-content">`) que permite a los usuarios de teclado saltar la navegación repetitiva y llegar directamente al contenido principal. Se oculta fuera de pantalla y aparece solo cuando recibe el foco.

---

## T

### `tabindex`
Atributo HTML que controla si un elemento puede recibir el foco con el teclado. Valores: `0` = enfocable en el orden natural del DOM; `-1` = solo enfocable por JavaScript; positivos (≥1) = **evitar siempre**, alteran el orden natural.

---

### `<time>`
Elemento semántico para marcado de fechas y horas. El atributo `datetime` contiene la representación legible por máquina en formato ISO 8601.

```html
<time datetime="2025-03-15">15 de marzo de 2025</time>
```

---

## V

### `.visually-hidden`
Patrón CSS que oculta un elemento visualmente pero lo mantiene accesible para lectores de pantalla. Alternativa segura a `display:none` o `visibility:hidden` cuando el contenido es relevante para a11y.

```css
.visually-hidden {
  position: absolute;
  width: 1px; height: 1px;
  padding: 0; margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```

---

## W

### WCAG (Web Content Accessibility Guidelines)
Pautas internacionales de accesibilidad web publicadas por el W3C. La versión WCAG 2.1 define tres niveles de conformidad: A (básico), AA (estándar recomendado) y AAA (avanzado). El nivel AA es el estándar mínimo exigido en muchas regulaciones.

**Criterios clave de accesibilidad:**
- Contraste de color: 4.5:1 para texto normal, 3:1 para texto grande (≥ 18px negrita o ≥ 24px normal)
- Todo contenido no textual debe tener alternativa textual (`alt`)
- Los formularios deben tener labels visibles
- El sitio debe ser navegable completamente con teclado
- Los indicadores de foco deben ser visibles

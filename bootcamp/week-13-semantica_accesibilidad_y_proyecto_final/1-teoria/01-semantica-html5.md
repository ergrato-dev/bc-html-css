# HTML5 Semántico en Profundidad

> Semana 13 · Teoría 01

## 🎯 Objetivos

- Comprender la diferencia entre elementos estructurales, semánticos y genéricos
- Usar correctamente los landmarks HTML5: `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
- Aplicar elementos de contenido semántico: `<figure>`, `<figcaption>`, `<time>`, `<address>`, `<mark>`, `<details>`
- Mantener una jerarquía de headings correcta

---

## 1. ¿Qué es HTML Semántico?

HTML semántico es escribir marcado donde **el nombre de la etiqueta describe el significado** del contenido, no su apariencia visual.

```html
<!-- ❌ Sin semántica — solo estructura visual -->
<div class="header">
  <div class="nav">...</div>
</div>
<div class="contenido-principal">
  <div class="articulo">...</div>
</div>
<div class="pie">...</div>

<!-- ✅ Con semántica — el nombre describe el contenido -->
<header>
  <nav>...</nav>
</header>
<main>
  <article>...</article>
</main>
<footer>...</footer>
```

**Beneficios reales:**
- Lectores de pantalla navegan por landmarks (`<nav>`, `<main>`, `<aside>`)
- Los motores de búsqueda entienden la jerarquía del contenido
- El código es más fácil de mantener y entender

---

## 2. Elementos Landmark

Los landmarks son los "bloques principales" de una página. Cada uno aparece en el árbol de accesibilidad del navegador.

![Diagrama de roles ARIA landmark](../0-assets/01-aria-roles.svg)

### `<header>`
Encabezado de la página o de una sección. Normalmente contiene el logo, título y navegación principal.

```html
<!-- header de página (landmark banner) -->
<header>
  <a href="/" class="logo">Mi Portfolio</a>
  <nav aria-label="Navegación principal">...</nav>
</header>

<!-- header dentro de un article (no es landmark) -->
<article>
  <header>
    <h2>Título del artículo</h2>
    <time datetime="2025-03-15">15 de marzo, 2025</time>
  </header>
</article>
```

### `<nav>`
Bloque de **enlaces de navegación**. Puede haber varios en la página; usa `aria-label` para diferenciarlos.

```html
<nav aria-label="Navegación principal">
  <ul>
    <li><a href="#sobre-mi">Sobre mí</a></li>
    <li><a href="#proyectos">Proyectos</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>

<nav aria-label="Ruta de navegación" aria-label="breadcrumb">
  <ol>
    <li><a href="/">Inicio</a></li>
    <li><a href="/blog/">Blog</a></li>
    <li aria-current="page">Artículo actual</li>
  </ol>
</nav>
```

### `<main>`
Contenido **principal y único** de la página. Solo debe haber uno. No usarlo dentro de `<article>`, `<aside>`, `<footer>`, `<header>` o `<nav>`.

```html
<main id="main-content">
  <!-- Todo el contenido principal aquí -->
</main>
```

### `<article>`
Contenido **autocontenido y redistribuible**: un post de blog, una tarjeta de producto, un comentario, una noticia. Si puedes sacarlo de la página y tiene sentido por sí solo → usa `<article>`.

```html
<article>
  <header>
    <h2>Mi primer proyecto web</h2>
    <p>Por <address><a rel="author" href="/about">Ana García</a></address></p>
    <time datetime="2025-01-10">10 de enero, 2025</time>
  </header>
  <p>Este proyecto fue mi introducción al CSS Grid...</p>
  <footer>
    <a href="/proyectos/primer-proyecto">Ver proyecto completo →</a>
  </footer>
</article>
```

### `<section>`
Sección temática del documento que **merece su propio heading**. Diferencia clave con `<div>`: una `<section>` siempre debe tener un `<h2>`–`<h6>`.

```html
<!-- ✅ section con su heading -->
<section aria-labelledby="skills-heading">
  <h2 id="skills-heading">Habilidades</h2>
  <ul>...</ul>
</section>

<!-- ❌ section sin heading — usar <div> en su lugar -->
<section>
  <p>Texto sin encabezado temático...</p>
</section>
```

### `<aside>`
Contenido **complementario** pero no esencial: sidebar, notas relacionadas, anuncios, bio del autor. No es lo mismo que contenido "secundario" — debe ser relacionado.

```html
<article>
  <p>Hablando sobre CSS Grid...</p>
  <aside>
    <h3>¿Sabías que?</h3>
    <p>CSS Grid fue estandarizado en 2017.</p>
  </aside>
</article>
```

### `<footer>`
Pie de página o de sección. Típicamente contiene: copyright, enlaces legales, información de contacto, redes sociales.

```html
<footer>
  <p>© 2025 Ana García · <a href="/privacidad">Privacidad</a></p>
  <address>
    <a href="mailto:ana@ejemplo.com">ana@ejemplo.com</a>
  </address>
</footer>
```

---

## 3. Elementos de Contenido Semántico

### `<figure>` y `<figcaption>`

Agrupa **contenido autocontenido** (imagen, código, diagrama, vídeo) con su descripción.

```html
<figure>
  <img
    src="assets/images/captura-proyecto.jpg"
    alt="Captura de pantalla del portfolio con diseño responsive en tres dispositivos"
    width="800"
    height="500"
    loading="lazy"
  />
  <figcaption>
    Vista responsive del portfolio en móvil, tablet y escritorio.
  </figcaption>
</figure>
```

> **Alt vs figcaption:**
> - `alt` describe la imagen para quien no puede verla (screen readers, imágenes rotas)
> - `<figcaption>` es visible para todos y complementa el contexto

### `<time>`

Representa una fecha, hora o duración **legible por máquinas** con el atributo `datetime`.

```html
<!-- Fecha completa -->
<time datetime="2025-06-15">15 de junio de 2025</time>

<!-- Solo año -->
<time datetime="2025">este año</time>

<!-- Fecha y hora -->
<time datetime="2025-06-15T14:30">15 de junio a las 14:30</time>

<!-- Duración (ISO 8601) -->
<time datetime="PT2H30M">2 horas y 30 minutos</time>
```

### `<address>`

Información de **contacto del autor** del contenido más cercano (`<article>`, `<body>`). No se usa para direcciones postales genéricas.

```html
<footer>
  <address>
    Escrito por <a rel="author" href="/about">Ana García</a>
    · <a href="mailto:hola@anagarcia.dev">hola@anagarcia.dev</a>
    · <a href="https://github.com/ana">GitHub</a>
  </address>
</footer>
```

### `<mark>`

Resalta texto **relevante para el contexto actual** (resultado de búsqueda, término relevante).

```html
<p>La propiedad <mark>display: grid</mark> activa el modo Grid en el contenedor.</p>
```

### `<details>` y `<summary>`

Contenido **expandible/colapsable** nativo, sin JavaScript.

```html
<details>
  <summary>¿Qué es el Box Model?</summary>
  <p>El Box Model define cómo se calcula el espacio que ocupa un elemento...</p>
</details>
```

---

## 4. Jerarquía de Headings

Regla fundamental: **nunca saltar niveles** de heading, y solo un `<h1>` por página.

```html
<!-- ✅ Jerarquía correcta -->
<h1>Ana García — Frontend Developer</h1>         <!-- 1 solo -->
  <h2>Sobre mí</h2>
  <h2>Proyectos</h2>
    <h3>Portfolio Personal</h3>
    <h3>E-commerce React</h3>
  <h2>Habilidades</h2>
  <h2>Contacto</h2>

<!-- ❌ Jerarquía incorrecta — salto de h1 a h3 -->
<h1>Ana García</h1>
  <h3>Sobre mí</h3>   <!-- ❌ salta h2 -->
```

> Los lectores de pantalla permiten navegar por headings con la tecla `H`. Una jerarquía correcta es como un índice de libro.

---

## 5. Estructura Completa de una Página

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ana García — Frontend Developer</title>
  <meta name="description" content="Portfolio de Ana García, desarrolladora frontend especializada en HTML, CSS y JavaScript." />
  <link rel="stylesheet" href="css/styles.css" />
</head>
<body>

  <!-- Landmark: banner -->
  <header>
    <a href="#main-content" class="skip-link">Saltar al contenido</a>
    <a href="/" class="site-logo" aria-label="Ana García — Inicio">AG</a>
    <nav aria-label="Navegación principal">
      <ul>
        <li><a href="#sobre-mi">Sobre mí</a></li>
        <li><a href="#proyectos">Proyectos</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Landmark: main -->
  <main id="main-content">

    <!-- Solo un h1 por página -->
    <section aria-labelledby="hero-heading">
      <h1 id="hero-heading">Ana García</h1>
      <p>Frontend Developer · HTML · CSS · JavaScript</p>
    </section>

    <section aria-labelledby="about-heading">
      <h2 id="about-heading">Sobre mí</h2>
      <p>...</p>
    </section>

    <section aria-labelledby="projects-heading">
      <h2 id="projects-heading">Proyectos</h2>
      <ul>
        <li>
          <article>
            <h3>Portfolio Personal</h3>
            <p>...</p>
          </article>
        </li>
      </ul>
    </section>

  </main>

  <!-- Landmark: contentinfo -->
  <footer>
    <address>
      <a href="mailto:hola@anagarcia.dev">hola@anagarcia.dev</a>
    </address>
    <p><small>© 2025 Ana García</small></p>
  </footer>

</body>
</html>
```

---

## 📚 Recursos Adicionales

- [MDN — HTML elements reference](https://developer.mozilla.org/es/docs/Web/HTML/Element)
- [HTML5 Outliner (extensión)](https://chrome.google.com/webstore/detail/html5-outliner)
- [W3C HTML Validator](https://validator.w3.org/)

---

## ✅ Checklist de Verificación

- [ ] Un solo `<h1>` por página
- [ ] No se saltan niveles de heading
- [ ] `<main>` presente con `id="main-content"`
- [ ] `<nav>` con `aria-label` descriptivo
- [ ] `<img>` con `alt` en todas las imágenes
- [ ] `<figure>` + `<figcaption>` para imágenes con descripción
- [ ] `<time datetime="">` para fechas
- [ ] Documento válido en W3C Validator

# SEO Básico y Rendimiento Web

> Semana 13 · Teoría 03

## 🎯 Objetivos

- Escribir `<head>` completo con meta tags esenciales
- Implementar Open Graph para previsualización en redes sociales
- Entender qué son las Core Web Vitals y cómo el HTML las afecta
- Aplicar una checklist de rendimiento básica desde el HTML

---

## 1. El `<head>` Completo

El `<head>` es invisible para el usuario pero crítico para buscadores, redes sociales y rendimiento.

```html
<head>
  <!-- 1. Codificación de caracteres — siempre primero -->
  <meta charset="UTF-8" />

  <!-- 2. Viewport para dispositivos móviles -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- 3. Título de la página — aparece en el tab y en Google -->
  <!-- Formato recomendado: "Título de la página | Nombre del sitio" -->
  <!-- Longitud ideal: 50-60 caracteres -->
  <title>Ana García — Frontend Developer Portfolio</title>

  <!-- 4. Descripción para buscadores -->
  <!-- Longitud ideal: 120-160 caracteres -->
  <meta
    name="description"
    content="Portfolio de Ana García, desarrolladora frontend especializada en HTML5, CSS3 y JavaScript. Proyectos responsive, accesibles y optimizados."
  />

  <!-- 5. URL canónica (evita contenido duplicado) -->
  <link rel="canonical" href="https://anagarcia.dev/" />

  <!-- 6. Open Graph (Facebook, LinkedIn, WhatsApp...) -->
  <meta property="og:title"       content="Ana García — Frontend Developer" />
  <meta property="og:description" content="Portfolio de proyectos web accesibles y responsive." />
  <meta property="og:image"       content="https://anagarcia.dev/assets/og-image.jpg" />
  <meta property="og:url"         content="https://anagarcia.dev/" />
  <meta property="og:type"        content="website" />
  <meta property="og:locale"      content="es_ES" />

  <!-- 7. Twitter Card -->
  <meta name="twitter:card"        content="summary_large_image" />
  <meta name="twitter:title"       content="Ana García — Frontend Developer" />
  <meta name="twitter:description" content="Portfolio de proyectos web accesibles y responsive." />
  <meta name="twitter:image"       content="https://anagarcia.dev/assets/og-image.jpg" />

  <!-- 8. Favicon -->
  <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
  <link rel="icon" type="image/png"     href="/favicon.png" />
  <link rel="apple-touch-icon"          href="/apple-touch-icon.png" />

  <!-- 9. Fuentes web — preconnect antes del link -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap"
    rel="stylesheet"
  />

  <!-- 10. CSS principal -->
  <link rel="stylesheet" href="css/styles.css" />
</head>
```

---

## 2. SEO On-Page con HTML

### Jerarquía de headings

Los buscadores usan los headings para entender la estructura del contenido.

```html
<!-- ✅ Un solo h1, descriptivo y con la palabra clave principal -->
<h1>Portfolio de Ana García — Frontend Developer</h1>
  <h2>Proyectos Destacados</h2>
    <h3>E-commerce accesible con React</h3>
    <h3>Dashboard CSS Grid</h3>
  <h2>Sobre mí</h2>
  <h2>Contacto</h2>
```

### Texto alternativo en imágenes

Las imágenes sin `alt` son invisibles para Google Image Search.

```html
<!-- Imagen de contenido — describir qué muestra -->
<img
  src="proyecto-dashboard.jpg"
  alt="Dashboard de analítica con gráficos de barras y líneas, diseño oscuro"
/>

<!-- Logo — describir el nombre de la marca -->
<img src="logo.svg" alt="Ana García — Portfolio" width="120" height="40" />

<!-- Imagen decorativa — alt vacío -->
<img src="wave-divider.svg" alt="" role="presentation" />
```

### Links descriptivos

```html
<!-- ❌ Link sin contexto (mala práctica SEO y accesibilidad) -->
<a href="/proyectos/dashboard">Haz clic aquí</a>
<a href="/proyectos/dashboard">Ver más</a>

<!-- ✅ Link descriptivo -->
<a href="/proyectos/dashboard">Ver proyecto: Dashboard de analítica</a>

<!-- ✅ Con visually-hidden para contexto extra -->
<a href="/proyectos/dashboard">
  Ver proyecto
  <span class="visually-hidden">Dashboard de analítica CSS Grid</span>
</a>
```

### Datos estructurados (JSON-LD)

Markup semántico que Google usa para rich snippets. No requiere modificar el HTML visible.

```html
<!-- Al final del <body> o en el <head> -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Ana García",
  "jobTitle": "Frontend Developer",
  "url": "https://anagarcia.dev",
  "email": "hola@anagarcia.dev",
  "sameAs": [
    "https://github.com/ana",
    "https://linkedin.com/in/ana-garcia"
  ]
}
</script>
```

---

## 3. Core Web Vitals

Google usa tres métricas principales para medir la experiencia del usuario:

| Métrica | Qué mide | Meta (bueno) |
|---------|----------|--------------|
| **LCP** — Largest Contentful Paint | Cuándo se pinta el elemento más grande visible | ≤ 2.5 s |
| **CLS** — Cumulative Layout Shift | Cuánto se desplazan los elementos mientras carga | ≤ 0.1 |
| **INP** — Interaction to Next Paint | Respuesta a la primera interacción del usuario | ≤ 200 ms |

### Cómo el HTML afecta LCP

```html
<!-- ❌ LCP lento: imagen hero sin preload, lazy loading accidental -->
<img src="hero.jpg" alt="..." loading="lazy" />

<!-- ✅ LCP óptimo: imagen hero con fetchpriority alta y preload -->
<link rel="preload" as="image" href="hero.jpg" />
<img
  src="hero.jpg"
  alt="Ana García en una conferencia de frontend"
  fetchpriority="high"
  width="1200"
  height="600"
/>
```

### Cómo el HTML afecta CLS

El CLS sube cuando los elementos se mueven porque el navegador no sabe su tamaño antes de cargarlos.

```html
<!-- ❌ Sin dimensiones — causa CLS cuando carga -->
<img src="foto.jpg" alt="..." />

<!-- ✅ Con width+height — el navegador reserva el espacio -->
<img src="foto.jpg" alt="..." width="400" height="300" />
```

```css
/* ✅ aspect-ratio como alternativa moderna */
.hero-img {
  width: 100%;
  aspect-ratio: 16 / 9;
  object-fit: cover;
}
```

---

## 4. Rendimiento: Checklist HTML

### Imágenes

```html
<!-- loading="lazy" para imágenes fuera del viewport inicial -->
<img src="proyecto.jpg" alt="..." loading="lazy" width="800" height="500" />

<!-- decoding="async" para no bloquear el hilo principal -->
<img src="avatar.jpg" alt="..." decoding="async" width="64" height="64" />

<!-- Formato moderno con fallback (cuando sea posible) -->
<picture>
  <source srcset="imagen.avif" type="image/avif" />
  <source srcset="imagen.webp" type="image/webp" />
  <img src="imagen.jpg" alt="..." width="800" height="500" />
</picture>
```

### Fuentes web

```css
/* font-display: swap — muestra texto con fuente del sistema mientras carga la web font */
@font-face {
  font-family: 'Inter';
  src: url('inter.woff2') format('woff2');
  font-display: swap;
}
```

### CSS crítico

```html
<!-- CSS crítico (above the fold) inline — renderiza sin bloquear -->
<style>
  /* Solo los estilos necesarios para el contenido visible inicial */
  body { font-family: system-ui, sans-serif; margin: 0; }
  .hero { min-height: 100vh; background: #0d1117; }
</style>

<!-- Resto del CSS cargado de forma normal -->
<link rel="stylesheet" href="css/styles.css" />
```

### Recursos externos

```html
<!-- preconnect para dominios externos (fuentes, CDNs) -->
<link rel="preconnect" href="https://fonts.googleapis.com" />

<!-- prefetch para recursos que se usarán en navegación futura -->
<link rel="prefetch" href="/proyectos/" />

<!-- preload para recursos críticos de la página actual -->
<link rel="preload" href="css/styles.css" as="style" />
<link rel="preload" href="assets/hero.jpg" as="image" />
```

---

## 5. Herramientas de Diagnóstico

| Herramienta | Para qué | URL |
|-------------|----------|-----|
| W3C Validator | Validar HTML | https://validator.w3.org/ |
| Lighthouse | Auditoría completa (perf, SEO, a11y) | DevTools > Lighthouse |
| PageSpeed Insights | Core Web Vitals reales | https://pagespeed.web.dev/ |
| axe DevTools | Auditoría de accesibilidad WCAG | Extensión Chrome/Firefox |
| Google Rich Results Test | Validar datos estructurados | https://search.google.com/test/rich-results |
| Squoosh | Optimizar imágenes online | https://squoosh.app/ |

---

## 📚 Recursos Adicionales

- [web.dev — Learn Performance](https://web.dev/learn/performance)
- [Google Search Central — SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
- [Core Web Vitals — web.dev](https://web.dev/vitals/)
- [Open Graph Protocol](https://ogp.me/)

---

## ✅ Checklist de Verificación

**SEO:**
- [ ] `<title>` único y descriptivo (50-60 caracteres)
- [ ] `<meta name="description">` específica (120-160 caracteres)
- [ ] `<link rel="canonical">` presente
- [ ] Open Graph tags completos (title, description, image, url, type)
- [ ] Solo un `<h1>` con la palabra clave principal
- [ ] Links con texto descriptivo

**Rendimiento:**
- [ ] Imágenes con `width` y `height` explícitos
- [ ] Imagen hero con `fetchpriority="high"` (sin `loading="lazy"`)
- [ ] Imágenes secundarias con `loading="lazy"`
- [ ] `font-display: swap` en fuentes custom
- [ ] `<link rel="preconnect">` para dominios externos

**Auditoría:**
- [ ] Sin errores en W3C Validator
- [ ] Lighthouse score ≥ 90 en Performance y SEO
- [ ] Sin errores críticos en axe DevTools

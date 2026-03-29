# Accesibilidad y ARIA

> Semana 13 · Teoría 02

## 🎯 Objetivos

- Entender qué es el árbol de accesibilidad y cómo lo usan los lectores de pantalla
- Aplicar atributos ARIA correctamente: `aria-label`, `aria-labelledby`, `aria-describedby`, `aria-hidden`
- Implementar navegación por teclado: skip links, `tabindex`, `:focus-visible`
- Conocer los criterios WCAG 2.1 AA más importantes

---

## 1. El Árbol de Accesibilidad

Cuando el navegador carga una página HTML, construye dos árboles:
1. **DOM Tree** — todos los elementos HTML
2. **Accessibility Tree** — solo los elementos con _rol semántico_ (el que leen NVDA, VoiceOver, JAWS)

```
DOM:                          Accessibility Tree:
<header>                  →   [landmark: banner]
  <nav>                   →     [landmark: navigation "Nav principal"]
    <a href="#main">      →       [link: "Saltar al contenido"]
    <ul><li><a>...        →       [link: "Sobre mí"] ...
<main>                    →   [landmark: main]
  <h1>Ana García</h1>     →     [heading level 1: "Ana García"]
  <button>Contactar</button>→   [button: "Contactar"]
<span class="icon">✕</span>→  (oculto — sin rol semántico)
```

> Los lectores de pantalla navegan por el árbol de accesibilidad, **no por el DOM visual**.

---

## 2. Roles ARIA

ARIA (Accessible Rich Internet Applications) permite **añadir semántica** a elementos que no la tienen, o **corregir/ampliar** la semántica existente.

![Diagrama de roles ARIA landmark](../0-assets/01-aria-roles.svg)

**Regla de oro: no usar ARIA si el HTML semántico ya resuelve el problema.**

```html
<!-- ❌ ARIA innecesario — <nav> ya tiene el rol implícito -->
<nav role="navigation">...</nav>

<!-- ✅ ARIA necesario — <div> no tiene rol semántico -->
<div role="navigation" aria-label="Navegación lateral">...</div>
```

### Roles landmark más usados

| Rol ARIA | Equivalente HTML | Descripción |
|----------|------------------|-------------|
| `banner` | `<header>` (nivel página) | Encabezado global del sitio |
| `navigation` | `<nav>` | Región de navegación |
| `main` | `<main>` | Contenido principal |
| `complementary` | `<aside>` | Contenido complementario |
| `contentinfo` | `<footer>` (nivel página) | Pie de página global |
| `search` | — | Formulario de búsqueda |
| `form` | `<form>` con nombre | Formulario identificado |
| `region` | `<section>` con nombre | Sección nombrada |

---

## 3. Atributos ARIA Esenciales

### `aria-label`
Etiqueta accesible **directamente en el elemento**, cuando no hay texto visible que lo identifique.

```html
<!-- Botón solo con icono — sin texto visible -->
<button type="button" aria-label="Cerrar menú">
  <span aria-hidden="true">✕</span>
</button>

<!-- Nav con aria-label si hay múltiples navs -->
<nav aria-label="Navegación del pie de página">...</nav>
```

### `aria-labelledby`
Usa el texto de **otro elemento** como etiqueta. Más potente que `aria-label` porque el texto está visible en pantalla.

```html
<section aria-labelledby="skills-title">
  <h2 id="skills-title">Habilidades técnicas</h2>
  <!-- El lector dirá: "región: Habilidades técnicas" -->
</section>

<!-- Formulario con título como label -->
<form aria-labelledby="contact-form-title">
  <h2 id="contact-form-title">Formulario de contacto</h2>
  ...
</form>
```

### `aria-describedby`
Asocia una **descripción adicional** (sugerencia, error, nota) a un elemento.

```html
<label for="email">Correo electrónico</label>
<input
  type="email"
  id="email"
  aria-describedby="email-hint email-error"
  aria-invalid="true"
/>
<p id="email-hint">Usaremos este correo solo para confirmar tu cuenta.</p>
<p id="email-error" role="alert">Por favor ingresa un correo válido.</p>
```

### `aria-hidden="true"`
Elimina un elemento del árbol de accesibilidad. Úsalo para **iconos decorativos**, texto duplicado o elementos puramente visuales.

```html
<!-- Icono decorativo junto a texto — el icono no aporta info extra -->
<button type="button">
  <span aria-hidden="true" class="icon">💾</span>
  Guardar cambios
</button>

<!-- Sin aria-hidden: el lector diría "Emoji diskette Guardar cambios botón" -->
<!-- Con aria-hidden en el icono: "Guardar cambios botón" -->
```

### `aria-current`
Indica el elemento **activo** en una lista de navegación (página actual, paso actual, etc.).

```html
<nav aria-label="Navegación principal">
  <ul>
    <li><a href="/">Inicio</a></li>
    <li><a href="/proyectos/" aria-current="page">Proyectos</a></li>
    <li><a href="/contacto/">Contacto</a></li>
  </ul>
</nav>
```

### `role="alert"`
Anuncia un mensaje **urgente** al lector de pantalla en cuanto aparece en el DOM, sin necesidad de foco.

```html
<!-- Se anuncia automáticamente al hacerse visible -->
<p role="alert" id="form-success" hidden>
  ¡Mensaje enviado correctamente!
</p>
```

---

## 4. Navegación por Teclado

### Skip link

Enlace que permite a usuarios de teclado **saltar directamente al contenido principal**, evitando repetir toda la navegación en cada página.

```html
<!-- Primero en el <body> — visible solo al recibir foco -->
<a href="#main-content" class="skip-link">Saltar al contenido principal</a>

<header>...</header>
<main id="main-content">...</main>
```

```css
/* Oculto visualmente, presente en el árbol de accesibilidad */
.skip-link {
  position: absolute;
  top: -100%;
  left: 1rem;
  z-index: 100;
  padding: 0.5rem 1rem;
  background: var(--color-primary);
  color: white;
  border-radius: 0 0 4px 4px;
  text-decoration: none;
  font-weight: bold;
  transition: top 0.2s;
}

/* Se hace visible al recibir foco con Tab */
.skip-link:focus {
  top: 0;
}
```

### `.visually-hidden` (clase helper)

Oculta contenido **visualmente** pero lo mantiene en el árbol de accesibilidad. No uses `display:none` ni `visibility:hidden` para contenido que deben leer los screen readers.

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```

```html
<!-- El contexto "GitHub" y "-" son visualmente redundantes pero útiles para screen readers -->
<a href="https://github.com/ana">
  <span aria-hidden="true">GH</span>
  <span class="visually-hidden">Ana García en GitHub</span>
</a>
```

### `tabindex`

Controla si un elemento recibe foco con la tecla Tab.

| Valor | Comportamiento |
|-------|----------------|
| `tabindex="0"` | Añade al orden natural de tabulación |
| `tabindex="-1"` | Solo accesible con foco programático (JS) |
| `tabindex="1+"` | ❌ NUNCA — rompe el orden natural de tabulación |

```html
<!-- div interactivo que no es botón/link — necesita tabindex="0" -->
<div role="button" tabindex="0" class="custom-toggle">Activar modo oscuro</div>

<!-- Elemento que recibirá focus() por JS, no por Tab -->
<div id="modal-content" tabindex="-1" role="dialog">...</div>
```

### `:focus-visible`

Muestra el outline de foco **solo cuando se navega con teclado**, no con clic de ratón (WCAG 2.1 criterio 2.4.11).

```css
/* Quitar outline para todos (clic de ratón no muestra outline) */
:focus {
  outline: none;
}

/* Mostrar outline SOLO cuando se navega con teclado */
:focus-visible {
  outline: 3px solid var(--color-primary);
  outline-offset: 3px;
  border-radius: 3px;
}
```

---

## 5. WCAG 2.1 — Criterios AA Fundamentales

WCAG (Web Content Accessibility Guidelines) 2.1 define tres niveles: A, AA, AAA. El nivel **AA** es el estándar legal en muchos países.

### Contraste de color

| Tipo de texto | Contraste mínimo AA |
|---------------|---------------------|
| Texto normal (< 18px o < 14px bold) | **4.5:1** |
| Texto grande (≥ 18px o ≥ 14px bold) | **3:1** |
| Componentes UI (botones, inputs, iconos funcionales) | **3:1** |

```css
/* ✅ Contraste suficiente: texto blanco sobre fondo verde oscuro */
.btn-primary {
  background: #1a7f37; /* verde oscuro */
  color: #ffffff;      /* relación: ~7.5:1 ✅ */
}

/* ❌ Contraste insuficiente: gris claro sobre blanco */
.helper-text {
  color: #aaaaaa; /* sobre #ffffff: relación ~2.3:1 ❌ */
}
```

**Herramienta:** [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

### Alt text en imágenes

```html
<!-- Imagen informativa — describir qué muestra -->
<img src="grafico.png" alt="Gráfico de barras: visitas por mes en 2025, pico en marzo con 12.000 visitas" />

<!-- Imagen decorativa — alt vacío (el lector la ignora) -->
<img src="separador.svg" alt="" />

<!-- ❌ Alt incorrecto — no describe el contenido -->
<img src="foto.jpg" alt="imagen" />
<img src="foto.jpg" alt="foto.jpg" />
```

### Formularios accesibles

```html
<!-- ✅ Label vinculado — nunca usar solo placeholder -->
<div class="form-field">
  <label for="nombre">Nombre completo</label>
  <input type="text" id="nombre" name="nombre" autocomplete="name" required />
</div>

<!-- ✅ Mensaje de error vinculado con aria-describedby -->
<div class="form-field">
  <label for="email">Correo electrónico</label>
  <input
    type="email"
    id="email"
    name="email"
    aria-describedby="email-error"
    aria-invalid="true"
    required
  />
  <p id="email-error" class="error-msg" role="alert">
    Ingresa un correo con formato válido (ejemplo@dominio.com)
  </p>
</div>
```

---

## 6. `prefers-reduced-motion`

Para usuarios con epilepsia fotosensible o vértigo, desactiva o reduce animaciones cuando el sistema operativo lo indica.

```css
/* Estilo base: animaciones activas */
.hero-section {
  animation: slide-up 0.6s ease both;
}

.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Cuando el usuario prefiere movimiento reducido */
@media (prefers-reduced-motion: reduce) {
  .hero-section {
    animation: none;
  }

  .card {
    transition: none;
  }
}
```

---

## 📚 Recursos Adicionales

- [MDN — ARIA](https://developer.mozilla.org/es/docs/Web/Accessibility/ARIA)
- [WebAIM — Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [axe DevTools](https://www.deque.com/axe/devtools/) — extensión de Chrome para auditar accesibilidad
- [WCAG 2.1 (español)](https://www.w3.org/TR/WCAG21/)
- [The A11Y Project Checklist](https://www.a11yproject.com/checklist/)

---

## ✅ Checklist de Verificación

- [ ] Skip link al inicio del `<body>` y visible con foco
- [ ] `.visually-hidden` implementado correctamente
- [ ] `:focus-visible` con outline en todos los interactivos
- [ ] Sin `tabindex` positivo en el HTML
- [ ] `aria-label` en botones sin texto visible
- [ ] Todo `<img>` con `alt` (descriptivo o vacío si decorativa)
- [ ] Todo `<input>` con `<label>` vinculado
- [ ] Contraste AA verificado con herramienta
- [ ] `prefers-reduced-motion` respetado
- [ ] Sin errores en axe DevTools

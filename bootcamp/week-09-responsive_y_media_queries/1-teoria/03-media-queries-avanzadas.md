# Media Queries Avanzadas

> Semana 09 · Teoría 03

---

## 🎯 Objetivos

- Combinar múltiples condiciones en una media query
- Usar media features más allá del ancho (orientación, prefer-color-scheme, hover)
- Aplicar `max-width` en contenedores responsivos con margen automático

---

## 1. Tipos de media queries

```css
/* Por tipo de medio (raramente necesario hoy en día) */
@media screen { }  /* pantallas */
@media print  { }  /* impresión */
@media all    { }  /* todos (por defecto) */

/* Por condición (lo más común) */
@media (min-width: 768px) { }
@media (max-width: 767px) { }
@media (orientation: landscape) { }
@media (prefers-color-scheme: dark) { }
@media (prefers-reduced-motion: reduce) { }
@media (hover: hover) { }
```

---

## 2. Combinaciones con `and`, `not`, `,`

```css
/* AND — ambas condiciones deben cumplirse */
@media (min-width: 768px) and (max-width: 1023px) {
  /* solo tablet */
}

/* AND — pantalla + ancho mínimo */
@media screen and (min-width: 1024px) {
  /* desktop en pantalla (no impresión) */
}

/* , (OR) — cualquiera de las dos */
@media (max-width: 480px), (orientation: portrait) {
  /* mobile O portrait */
}

/* NOT — niega la condición */
@media not (min-width: 1024px) {
  /* todo lo que NO sea desktop */
}
```

---

## 3. Medias features útiles

### `prefers-color-scheme`

Detecta si el sistema operativo usa tema claro u oscuro:

```css
:root {
  --color-bg: #ffffff;
  --color-text: #0d1117;
}

@media (prefers-color-scheme: dark) {
  :root {
    --color-bg: #0d1117;
    --color-text: #f0f6fc;
  }
}

/* El body usa las variables → cambia automáticamente */
body {
  background: var(--color-bg);
  color: var(--color-text);
}
```

### `prefers-reduced-motion`

Respeta la preferencia de usuarios que tienen configurado "reducir movimiento" (accesibilidad):

```css
.card {
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-4px);
}

/* Elimina la animación para usuarios sensibles al movimiento */
@media (prefers-reduced-motion: reduce) {
  .card {
    transition: none;
  }
  .card:hover {
    transform: none;
  }
}
```

### `hover`

Detecta si el dispositivo tiene cursor (mouse) o es touch:

```css
/* El efecto hover solo se aplica en dispositivos con cursor */
@media (hover: hover) {
  .btn:hover {
    background: var(--color-blue);
    color: #fff;
  }
}
```

### `orientation`

```css
/* Ajuste especial para landscape en móvil */
@media (orientation: landscape) and (max-height: 500px) {
  .hero {
    min-height: auto;
    padding: 2rem;
  }
}
```

---

## 4. Contenedores responsivos

El patrón estándar para limitar el ancho del contenido:

```css
.container {
  width: 100%;         /* ocupa todo el ancho disponible */
  max-width: 1200px;   /* pero nunca más de 1200px */
  margin: 0 auto;      /* centrado horizontal */
  padding: 0 1rem;     /* aire lateral en mobile */
}

/* Variaciones de ancho */
.container--narrow  { max-width: 720px; }   /* artículos, formularios */
.container--wide    { max-width: 1440px; }  /* hero, full-width sections */
```

---

## 5. Estrategia de breakpoints en proyectos reales

```css
/* ─────────────────────────────────────
   Sistema de breakpoints recomendado
   ───────────────────────────────────── */

/* MOBILE BASE (0–479px) — sin @media */
.layout { display: grid; grid-template-columns: 1fr; }

/* MOBILE LARGE (480px+) */
@media (min-width: 480px) {
  .layout { grid-template-columns: repeat(2, 1fr); }
}

/* TABLET (768px+) */
@media (min-width: 768px) {
  .layout { grid-template-columns: repeat(2, 1fr); gap: 1.5rem; }
  .nav    { flex-direction: row; }
}

/* DESKTOP (1024px+) */
@media (min-width: 1024px) {
  .layout { grid-template-columns: repeat(3, 1fr); }
}

/* LARGE DESKTOP (1280px+) */
@media (min-width: 1280px) {
  .container { max-width: 1280px; }
  .layout    { grid-template-columns: repeat(4, 1fr); }
}
```

---

## 6. `@media` en `print`

Estilos para cuando el usuario imprime la página:

```css
@media print {
  /* Ocultar elementos no imprimibles */
  .site-header,
  .site-footer,
  .sidebar,
  .btn { display: none; }

  /* Optimizar para papel */
  body {
    font-size: 12pt;
    color: #000;
    background: #fff;
  }

  a::after {
    content: " (" attr(href) ")";
    font-size: 0.8em;
    color: #666;
  }
}
```

---

## 📚 Recursos adicionales

- [MDN — @media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)
- [MDN — prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
- [MDN — prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)
- [web.dev — Responsive design](https://web.dev/learn/design/)

---

## ✅ Checklist

- [ ] `prefers-color-scheme: dark` implementado con CSS Custom Properties
- [ ] `prefers-reduced-motion` aplicado a transiciones y animaciones
- [ ] Contenedor con `max-width` + `margin: 0 auto`
- [ ] Media queries en orden creciente de `min-width`

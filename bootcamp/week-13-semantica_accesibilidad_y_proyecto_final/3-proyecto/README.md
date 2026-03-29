# Proyecto Final — Portfolio Personal

## 🎯 Descripción

Construye tu **portfolio profesional** aplicando todas las técnicas aprendidas durante el bootcamp: HTML5 semántico, CSS moderno con Custom Properties, Flexbox, Grid, diseño responsive mobile-first, accesibilidad y SEO básico.

Este es el proyecto capstone: el resultado final debe poder incluirse en tu curriculum como muestra real de tus habilidades.

---

## 📋 Objetivos del proyecto

- Aplicar HTML5 semántico en una página completa de producción
- Cumplir accesibilidad WCAG 2.1 AA: skip link, `:focus-visible`, alt en imágenes, labels en formularios, contraste 4.5:1
- Implementar CSS responsive mobile-first con breakpoints a `768px` y `1024px`
- Usar CSS Custom Properties para todos los tokens de diseño
- Añadir los meta tags SEO mínimos (title, description, Open Graph)
- Entregar código limpio, sin errores en el W3C Validator

---

## 🗂️ Estructura de archivos

```
starter/
├── index.html
└── css/
    ├── reset.css          ← ya incluido, no modificar
    ├── variables.css      ← ya incluido, puedes personalizar los valores
    └── styles.css         ← aquí completas los TODOs
```

---

## 📝 Secciones del portfolio

### 1. `<header>` — Navegación

- Skip link al contenido principal
- Logo / nombre del autor
- Nav con enlaces a cada sección
- Mobile: menú hamburguesa CSS-only (`:checked` trick)
- El enlace activo tiene `aria-current="page"` o resaltado visual

### 2. `<section id="hero">` — Presentación

- `<h1>` con tu nombre
- `<p>` con tu título profesional
- Dos botones CTA: "Ver proyectos" y "Contactar"
- Animación de entrada CSS (`@keyframes` + `prefers-reduced-motion`)

### 3. `<section id="about">` — Sobre mí

- Layout de 2 columnas: foto de perfil + descripción
- `<figure>` con `<img>` y `<figcaption>` para la foto
- Lista de habilidades en grid con `::before` bullets

### 4. `<section id="projects">` — Proyectos

- Grid CSS `auto-fit, minmax(280px, 1fr)`
- Mínimo 3 tarjetas de proyecto
- Cada tarjeta con: `<figure>`, `<figcaption>`, título, descripción, enlace
- Al menos una tarjeta con la clase `.card.is-featured` (ribbon decorativo con `::before`)

### 5. `<section id="contact">` — Contacto

- Formulario accesible completo
- Todos los campos con `<label>` vinculado (`for`/`id`)
- `aria-describedby` en los campos con instrucciones adicionales
- `role="alert"` en el mensaje de confirmación
- Estilos de `:valid` / `:invalid` en los inputs

### 6. `<footer>` — Pie de página

- `<address>` con datos de contacto
- enlaces a redes sociales con `aria-label` descriptivo
- Texto de copyright con `<time>`

---

## 📐 Requisitos de diseño

| Requisito | Detalle |
| --- | --- |
| Mobile-first | Estilos base para `< 768px`, luego `@media (min-width: 768px)` y `(min-width: 1024px)` |
| Tokens CSS | Todos los colores, tipografías y espaciados en `variables.css` |
| Skip link | Oculto fuera de pantalla, visible al recibir `:focus` |
| `:focus-visible` | Outline 3px visible en todos los elementos interactivos |
| Alt text | Toda imagen con `alt` descriptivo (o `alt=""` si es decorativa) |
| Contraste | Mínimo 4.5:1 para texto normal, 3:1 para texto grande |
| Validación HTML | Sin errores en [validator.w3.org](https://validator.w3.org/) |
| Animación segura | `@keyframes` siempre con `@media (prefers-reduced-motion: no-preference)` |

---

## 🎯 Criterios de evaluación

| Criterio | Puntos |
| --- | --- |
| HTML semántico (landmarks + section/article/figure/time correcto) | 5 |
| CSS responsive y mobile-first funcional | 5 |
| Accesibilidad (skip link, focus visible, alt, labels, aria-*) | 5 |
| CSS avanzado (pseudo-elementos, variables, animación) | 5 |
| SEO meta tags completos (title, description, og:*) | 4 |
| Calidad de código (sin errores W3C, nombrado consistente) | 3 |
| Entrega puntual | 3 |
| **Total** | **30** |

---

## ✅ Checklist de entrega

- [ ] `<html lang="es">` presente
- [ ] `<meta charset>` y `<meta viewport>` en `<head>`
- [ ] `<title>` descriptivo (50-60 caracteres)
- [ ] `<meta name="description">` (120-160 caracteres)
- [ ] Open Graph: `og:title`, `og:description`, `og:image`, `og:url`
- [ ] Skip link funcional (oculto → visible con Tab)
- [ ] Todas las imágenes con `alt`
- [ ] Todos los inputs con `<label>` vinculado
- [ ] `:focus-visible` con outline visible en todos los interactivos
- [ ] Formulario con `aria-describedby` y `role="alert"`
- [ ] Contraste WCAG AA verificado
- [ ] Sin errores en W3C HTML Validator
- [ ] Diseño funcional en móvil (320px) y escritorio (1440px)
- [ ] Animación con `prefers-reduced-motion`

---

## 🔗 Herramientas de validación

- **HTML:** [validator.w3.org](https://validator.w3.org/)
- **CSS:** [jigsaw.w3.org/css-validator](https://jigsaw.w3.org/css-validator/)
- **Contraste:** [webaim.org/resources/contrastchecker](https://webaim.org/resources/contrastchecker/)
- **Accesibilidad:** Extensión axe DevTools en Chrome/Firefox
- **Rendimiento:** [PageSpeed Insights](https://pagespeed.web.dev/)

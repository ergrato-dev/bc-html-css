# Proyecto — Responsive Landing Page

## 🎯 Objetivo

Construir una **landing page multi-sección** completamente responsive usando **Mobile-first**, unidades relativas (`rem`, `clamp()`, `vw`/`vh`), y `@media` queries para los breakpoints 768px y 1024px.

Además, implementar soporte de `prefers-color-scheme: dark` y `prefers-reduced-motion` para accesibilidad.

---

## 📋 Descripción

La landing page presentará los servicios de una agencia ficticia de diseño web llamada **"Craft Studio"**. Debe incluir las secciones:

| Sección | Componentes principales |
|---|---|
| Header | Logo + navegación responsive |
| Hero | Título `clamp()`, subtítulo, botón CTA, `min-height: 100vh` |
| Features | Grid de 3–6 tarjetas con `auto-fit` + `minmax()` |
| Testimonials | 2 columnas en tablet+, 1 en mobile |
| CTA | Sección centrada con formulario de suscripción |
| Footer | Columnas responsive |

---

## ⏱️ Tiempo estimado

**1.5–2 horas**

---

## 📁 Estructura

```
3-proyecto/
├── README.md           ← este archivo
├── starter/
│   ├── index.html      ← ¡NO modificar!
│   └── css/
│       └── styles.css  ← implementa los TODOs aquí
└── solution/           ← OCULTA: solo para instructores
```

---

## ✅ Requisitos

### Responsive

- [ ] Diseño Mobile-first funcional en pantallas de 320px
- [ ] Breakpoint tablet: `@media (min-width: 768px)`
- [ ] Breakpoint desktop: `@media (min-width: 1024px)`
- [ ] Sin scroll horizontal en ningún viewport

### Unidades

- [ ] Usar `rem` para tipografía y espaciados
- [ ] Usar `clamp()` para el título Hero
- [ ] Usar `min-height: 100vh` para el hero
- [ ] Usar `%` o `vw` para anchos fluidos de contenedores

### Layout

- [ ] Navegación: vertical en mobile → horizontal en tablet+
- [ ] Features: 1 columna en mobile → `auto-fit / minmax(280px, 1fr)` en tablet+
- [ ] Testimonials: 1 columna en mobile → 2 columnas en tablet+
- [ ] Container: `max-width: 1200px; margin: 0 auto`

### Accesibilidad y polish

- [ ] `prefers-color-scheme: dark` — aplica variables alternativas
- [ ] `prefers-reduced-motion: reduce` — deshabilita transiciones
- [ ] `max-width: 100%` en imágenes

---

## 📝 Instrucciones

1. Abre `starter/css/styles.css`
2. Lee cada bloque `TODO` con atención — cada uno indica qué propiedad implementar
3. No modifiques `starter/index.html`
4. Valida el resultado en el navegador a varios anchos de pantalla (320px, 768px, 1024px)
5. Usa DevTools Device Mode para verificar

---

## 🎓 Criterios de Evaluación

| Criterio | Puntos |
|---|---|
| Mobile-first funcional (320px) | 20 |
| Breakpoint 768px correcto | 15 |
| Breakpoint 1024px correcto | 15 |
| `clamp()` en hero + `100vh` | 15 |
| `rem` en tipografía y espaciados | 10 |
| `prefers-color-scheme: dark` | 10 |
| `prefers-reduced-motion` | 5 |
| Sin overflow/scroll horizontal | 10 |
| **Total** | **100** |

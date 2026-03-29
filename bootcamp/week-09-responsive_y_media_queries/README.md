# Semana 09 — Responsive & Media Queries

> Bootcamp HTML + CSS · Semana 9 de 13

Diseña interfaces que se adaptan a cualquier pantalla usando la estrategia **Mobile-first**, unidades relativas y `@media` queries. Aprende a pensar en breakpoints y a construir layouts que funcionen desde un teléfono de 320px hasta un monitor de 1440px.

---

## 🎯 Objetivos de aprendizaje

Al finalizar esta semana serás capaz de:

- ✅ Aplicar la estrategia **Mobile-first** en todos tus proyectos CSS
- ✅ Usar unidades relativas: `rem`, `em`, `vw`, `vh`, `%`, `vmin`, `vmax`
- ✅ Escribir `@media` queries con `min-width` (y cuándo usar `max-width`)
- ✅ Definir breakpoints semánticos basados en el contenido, no en dispositivos
- ✅ Combinar Flexbox y Grid con Media Queries para layouts totalmente responsivos
- ✅ Usar `clamp()` para tipografía fluida sin media queries adicionales

---

## 📚 Requisitos previos

- Semana 05 — Box Model y display
- Semana 07 — Flexbox
- Semana 08 — CSS Grid

---

## 🗂️ Estructura de la semana

```
week-09-responsive_y_media_queries/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-mobile-first.svg
│   └── 02-unidades-relativas.svg
├── 1-teoria/
│   ├── 01-mobile-first-y-breakpoints.md
│   ├── 02-unidades-relativas.md
│   └── 03-media-queries-avanzadas.md
├── 2-practicas/
│   ├── 01-ejercicio-mobile-first/
│   ├── 02-ejercicio-unidades/
│   └── 03-ejercicio-breakpoints/
├── 3-proyecto/
│   ├── README.md
│   ├── starter/
│   └── solution/
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md
```

---

## 📝 Contenidos

| # | Teoría | Tema |
|---|--------|------|
| 1 | [Mobile-first y breakpoints](1-teoria/01-mobile-first-y-breakpoints.md) | Estrategia mobile-first, breakpoints semánticos |
| 2 | [Unidades relativas](1-teoria/02-unidades-relativas.md) | rem, em, vw, vh, %, clamp() |
| 3 | [Media Queries avanzadas](1-teoria/03-media-queries-avanzadas.md) | @media, combinaciones, prefers-color-scheme |

| # | Práctica | Habilidad |
|---|----------|-----------|
| 1 | [Mobile-first](2-practicas/01-ejercicio-mobile-first/) | Construir desde mobile hacia desktop |
| 2 | [Unidades](2-practicas/02-ejercicio-unidades/) | Aplicar rem/em/vw/vh/% |
| 3 | [Breakpoints](2-practicas/03-ejercicio-breakpoints/) | Grid + Flex responsive con @media |

---

## ⏱️ Distribución del tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría: Mobile-first + breakpoints | 1h |
| Teoría: Unidades relativas | 45min |
| Teoría: Media Queries avanzadas | 45min |
| Práctica 01: Mobile-first | 1h |
| Práctica 02: Unidades | 45min |
| Práctica 03: Breakpoints | 1h |
| Proyecto: Responsive Landing Page | 2h |
| Revisión y DevTools | 45min |

---

## 🎓 Conceptos clave

| Concepto | Descripción |
|----------|-------------|
| Mobile-first | Escribir estilos base para móvil; escalar hacia arriba con `min-width` |
| `@media (min-width)` | Media query que aplica estilos a partir de cierto ancho |
| Breakpoint | Punto de quiebre donde cambia el layout |
| `rem` | Relativo al `font-size` del elemento `<html>` (generalmente 16px) |
| `em` | Relativo al `font-size` del elemento padre |
| `vw` / `vh` | 1% del ancho / alto del viewport |
| `%` | Relativo al contenedor padre |
| `clamp(min, ideal, max)` | Valor fluido entre mínimo y máximo |
| `min-width` 480px | Breakpoint móvil → tablet pequeña |
| `min-width` 768px | Breakpoint tablet → tablet landscape |
| `min-width` 1024px | Breakpoint tablet grande → desktop |
| `min-width` 1280px | Breakpoint desktop → desktop grande |

---

## ✅ Checklist de verificación

- [ ] Los estilos base funcionan correctamente en 320px de ancho
- [ ] Los `@media` queries usan `min-width` (no `max-width`)
- [ ] La tipografía usa `rem` o `clamp()`, no `px` fijos
- [ ] Los espaciados usan `rem` o `em`
- [ ] Los ancho máximos usan `max-width` + `margin: auto`
- [ ] El layout de columnas se activa en breakpoints correctos
- [ ] Las imágenes tienen `max-width: 100%` para no desbordar
- [ ] El proyecto funciona en Chrome, Firefox y Safari móvil
- [ ] No hay scroll horizontal en ningún viewport

---

## 📌 Entregables

1. Los 3 ejercicios completados (código descomentado)
2. Proyecto "Responsive Landing Page" con diseño funcional en móvil, tablet y desktop

---

## 🔗 Navegación

← [Semana 08 — CSS Grid](../week-08-css_grid/README.md) | [Semana 10 — Tipografía, Colores y Variables](../week-10-tipografia_colores_y_variables/README.md) →

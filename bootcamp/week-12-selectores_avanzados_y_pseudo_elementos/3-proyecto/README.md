# Proyecto — Component Showcase

> **Semana 12 · Proyecto Integrador** — Construir una página de componentes reutilizables usando exclusivamente CSS avanzado, sin ninguna línea de JavaScript.

---

## 🎯 Descripción

Crearás una página de demostración de componentes que exhiba el poder de los selectores avanzados y pseudo-elementos CSS.

La página incluye cuatro secciones:

1. **Tabla de datos** con zebra stripes, highlight por posición y badges de estado
2. **Checkboxes y radios custom** usando `:checked` y pseudo-elementos — sin JS
3. **Sistema de cards** con ribbons, badges y decoraciones via `::before`/`::after`
4. **Tooltips de información** con `[data-tooltip]` + `::after` puro CSS

---

## 📐 Estructura Visual

```
┌─────────────────────────────────────────────────┐
│  Component Showcase   Semana 12 - CSS Avanzado  │
├─────────────────────────────────────────────────┤
│                                                 │
│  [Tabla de Inventario]                          │
│  ┌──────────┬──────────┬───────┬──────────────┐ │
│  │ #  │ Producto │ Stock │ Estado │ Acciones  │ │
│  ├──────────┴──────────┴───────┴──────────────┤ │
│  │ fila clara   │  fila oscura  │  fila clara  │ │
│  └─────────────────────────────────────────────┘ │
│                                                 │
│  [Preferencias — Custom Form Controls]          │
│  ☑ Recibir notificaciones       ◉ Email        │
│  ☐ Modo oscuro automático       ○ SMS          │
│                                                 │
│  [Cards con decoraciones]                       │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐       │
│  │  NUEVO   │ │DESTACADO │ │ normal   │       │
│  │ Card A   │ │ Card B   │ │ Card C   │       │
│  └──────────┘ └──────────┘ └──────────┘       │
│                                                 │
│  [Iconos con Tooltips]                          │
│  [👁] [✏️] [⚙] [💾] [🗑]                     │
└─────────────────────────────────────────────────┘
```

---

## 📋 Requisitos

| Requisito | Descripción | Puntos |
|-----------|-------------|--------|
| Tabla con zebra stripes | `:nth-child(even)` y primera fila destacada | 5 |
| Custom checkboxes | `input:checked + label::before` — sin JS | 7 |
| Al menos un ribbon | `::before` con `position: absolute` + `rotate` | 5 |
| Sistema de tooltips | `[data-tooltip]::after` + `attr()` funcional | 6 |
| Uso de `:has()` | Aplicado en al menos un selector del proyecto | 4 |
| Zero JavaScript | Ningún `<script>` en el HTML ni inline | 3 |

**Total: 30 puntos** | Aprobación mínima: 21/30

---

## 🗂 Archivos

```
3-proyecto/
├── README.md               ← este archivo
├── starter/
│   ├── index.html          ← HTML completo — implementa los TODOs del CSS
│   └── css/
│       └── styles.css      ← 8 bloques TODO para implementar
└── solution/               ← ⚠️ Solo instructores
    ├── index.html
    └── css/
        └── styles.css
```

---

## ✅ Checklist de Entrega

- [ ] La tabla tiene zebra stripes con `:nth-child(even)` y borde lateral en la primera fila
- [ ] Los checkboxes y radios custom funcionan sin JavaScript
- [ ] Al menos una tarjeta tiene un ribbon diagonal con `::before` + `transform: rotate`
- [ ] Los tooltips aparecen al hacer hover y al navegar con Tab
- [ ] Se usa `:has()` en al menos una regla CSS
- [ ] El código CSS no usa `!important` salvo en el bloque `prefers-reduced-motion`
- [ ] HTML válido (W3C Validator sin errores)
- [ ] Zero `<script>` en el HTML

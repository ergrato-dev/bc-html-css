# Proyecto — AdminGrid

Dashboard de administración construido con CSS Grid. Consolida `grid-template-areas`, `auto-fit`, `minmax`, `span` y diseño responsive.

---

## 🎯 Objetivo

Implementar un panel de administración completo usando únicamente CSS Grid como sistema de layout, con una estructura semántica en HTML5.

---

## 🗺️ Layout

```
+----------------------------------+
|           site-header            |  ← grid-area: header (span 2 col)
+----------+-----------------------+
|          |                       |
|  sidebar |    main-content       |
|          |   +-stats-grid------+ |
|          |   | s1 | s2 | s3 |s4| |  ← auto-fit minmax(180px, 1fr)
|          |   +--project-grid---+ |
|          |   | p1 | p2 | p3   |  |  ← auto-fit minmax(220px, 1fr)
|          |   | featured (1/-1) |  |
+----------+-----------------------+
|           site-footer            |  ← grid-area: footer (span 2 col)
+----------------------------------+
```

---

## 📋 Requisitos

### Layout global (`grid-template-areas`)

- [ ] **TODO 1** — Contenedor `.page-grid` con `grid-template-areas`, `--sidebar-width` (240px), `min-height: 100vh`
- [ ] **TODO 2** — `.site-header { grid-area: header }` + flex interno (brand izquierda, actions derecha)
- [ ] **TODO 3** — `.sidebar { grid-area: sidebar }` + flex column interno para nav y user
- [ ] **TODO 4** — `.main-content { grid-area: main; overflow-y: auto }`
- [ ] **TODO 5** — `.site-footer { grid-area: footer }` + centrado del texto

### Grids internos

- [ ] **TODO 6** — `.stats-grid` con `repeat(auto-fit, minmax(180px, 1fr))` y `gap`
- [ ] **TODO 7** — `.stat-card` con flex interno: ícono izquierda, dato + label derecha
- [ ] **TODO 8** — `.projects-grid` con `repeat(auto-fit, minmax(220px, 1fr))` y `gap`
- [ ] **TODO 9** — `.project-card` con `display: flex; flex-direction: column`
- [ ] **TODO 10** — `.featured-card { grid-column: 1 / -1 }` — ocupa todo el ancho

### Responsive

- [ ] **TODO 11** — `@media (max-width: 767px)`: `.page-grid` pasa a 1 columna, sidebar se reordena debajo de main
- [ ] **TODO 12** — En mobile: `.sidebar` compacto (flex-direction: row, overflow-x: auto)

---

## 📁 Archivos

```
3-proyecto/
├── README.md            ← este archivo
├── starter/
│   ├── index.html       ← estructura HTML (no modificar)
│   └── css/
│       └── styles.css   ← implementa los TODOs aquí
└── solution/
    ├── index.html       ← igual que starter
    └── css/
        └── styles.css   ← implementación completa (solo instructores)
```

---

## ✅ Criterios de evaluación

| Criterio | Pts |
|---|---|
| Layout global con `grid-template-areas` correcto | 10 |
| Stats cards con `auto-fit` + `minmax` | 8 |
| `.featured-card` con `grid-column: 1 / -1` | 4 |
| CSS Custom Properties para colores y espaciados | 4 |
| HTML5 semántico (`header`, `aside`, `main`, `footer`) | 4 |
| Responsive mobile funcional (sidebar reordenado) | 6 |
| Diseño visual coherente en DevTools Grid Inspector | 4 |
| **Total** | **40** |

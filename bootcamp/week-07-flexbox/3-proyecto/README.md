# Proyecto Semana 07 — FlexDash

Construye un dashboard de analíticas usando **exclusivamente Flexbox** para todos los layouts: navegación, sidebar, área principal, tarjetas de estadísticas y grid de proyectos recientes.

---

## 🎯 Objetivo

Demostrar dominio de Flexbox construyendo un dashboard completo con:
- Navbar sticky con logo y acciones
- Layout principal de dos columnas (sidebar fijo + contenido)
- Fila de tarjetas de estadísticas adaptable
- Grid de proyectos con cards flexibles
- Sticky footer al fondo de la página

---

## 📋 Requisitos

### Estructura de Layout

1. **Body:** `display: flex; flex-direction: column; min-height: 100vh`
2. **Header sticky:** `display: flex; justify-content: space-between; align-items: center`
3. **Layout wrapper:** `display: flex; flex: 1` (sidebar + main)
4. **Sidebar:** `flex: 0 0 var(--sidebar-width)` — ancho fijo, no crece
5. **Main content:** `flex: 1` — ocupa todo el espacio restante

### Tarjetas de Estadísticas

- Contenedor: `display: flex; flex-wrap: wrap; gap: 1rem`
- Cada stat card: `flex: 1 1 180px` — se adapta al ancho disponible

### Grid de Proyectos

- `display: flex; flex-wrap: wrap; gap: 1rem`
- Cada card: `flex: 1 1 220px`

### Restricciones

- ❌ CSS Grid no está permitido en este proyecto (es el tema de la semana siguiente)
- ✅ Flexbox para todos los layouts
- ✅ CSS Custom Properties para colores y espaciados
- ✅ Mobile-first: en móvil el sidebar se oculta o apila

---

## 📁 Estructura

```
3-proyecto/
├── README.md
├── starter/
│   ├── index.html
│   └── css/
│       └── styles.css   ← Completa los TODOs
└── solution/
    ├── index.html
    └── css/
        └── styles.css   ← Implementación de referencia
```

---

## ⏱️ Distribución del Tiempo

| Actividad | Tiempo |
|-----------|--------|
| Leer e inspeccionar el starter | 15 min |
| TODO 1–4: Body, header, layout | 30 min |
| TODO 5–8: Sidebar, main, stats | 30 min |
| TODO 9–12: Cards, header-bar, footer | 30 min |
| TODO 13–14: Responsive (breakpoint 768px) | 15 min |

---

## 📊 Criterios de Evaluación

| Criterio | Puntos |
|----------|--------|
| Body sticky footer (flex column + min-height) | 10 |
| Header navbar (space-between + align-items) | 10 |
| Layout sidebar fijo + main flex:1 | 20 |
| Stat cards (flex-wrap + flex:1 1 180px) | 20 |
| Project cards (flex-wrap + flex:1 1 220px) | 20 |
| Responsive: sidebar oculto en móvil (<768px) | 10 |
| CSS Custom Properties usadas correctamente | 10 |
| **Total** | **100** |

---

## ✅ Checklist de Entrega

- [ ] Sticky footer funciona (footer siempre al fondo)
- [ ] Navbar: logo a la izquierda, acciones a la derecha
- [ ] Sidebar 240px fijo, main ocupa el resto
- [ ] Stat cards se reorganizan en pantallas pequeñas
- [ ] Project cards saltan de línea correctamente
- [ ] Sin CSS Grid ni `position: absolute` para layouts
- [ ] Código validado sin errores

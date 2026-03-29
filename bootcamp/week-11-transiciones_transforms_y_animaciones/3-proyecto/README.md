# Proyecto — Animated Portfolio Card

> **Semana 11: Transiciones, Transforms y Animaciones CSS**  
> **Entrega:** Al finalizar la semana

---

## 🎯 Descripción

Construye una tarjeta de portfolio animada que combine todo lo aprendido esta semana:
una animación de entrada con `@keyframes`, un efecto hover 3D con `transform`, un
badge de estado con `animation: pulse` infinita y un spinner de carga inicial.

La tarjeta representa a un desarrollador ficticio mostrando foto, nombre, rol,
habilidades (badges), y un botón de contacto.

---

## 📋 Requisitos

| Requisito | Descripción |
|-----------|-------------|
| Animación de entrada | `@keyframes slide-up` con `animation-fill-mode: forwards` |
| Hover 3D | `rotateY` con `perspective` en el contenedor |
| Hover lift | `translateY` + `box-shadow` via `transition` |
| Badge pulse | `@keyframes pulse` con `animation: infinite` en el punto de estado "disponible" |
| Spinner inicial | Muestra un spinner durante 1.5s antes de la tarjeta (simulado via `animation-delay`) |
| Tokens CSS | `--duration-*`, `--ease-*`, `--transition-*` en `:root` — sin magic numbers |
| `prefers-reduced-motion` | Desactiva todas las animaciones |
| HTML semántico | `<article>`, `<header>`, `<footer>`, `aria-label` |

---

## 🗂️ Estructura

```
3-proyecto/
├── README.md
├── starter/
│   ├── index.html     ← Implementa los TODOs
│   └── css/
│       └── styles.css ← Implementa los TODOs
└── solution/          ← Solo para instructores
```

---

## 📊 Rúbrica de Calificación

| Criterio | Pts |
|----------|-----|
| Animación de entrada con `@keyframes` + `fill-mode: forwards` | 20 |
| Hover con `transform` + `transition` suave (sin valores mágicos) | 20 |
| Badge pulse con `animation: infinite` | 15 |
| Tokens `--duration-*`, `--ease-*` en `:root` (sin magic numbers) | 20 |
| `prefers-reduced-motion: reduce` implementado | 15 |
| HTML semántico (`<article>`, `aria-label`, etc.) | 10 |
| **Total** | **100** |

---

## 💡 Guía Visual

La tarjeta en reposo:
```
┌──────────────────────────────┐
│  [foto de perfil circular]   │
│  ● Disponible                │  ← badge pulse
│  Ana García                  │
│  Frontend Developer          │
│  [HTML] [CSS] [Figma]        │
│  [Contactar →]               │
└──────────────────────────────┘
```

Al hacer hover: la tarjeta rota levemente en Y y sube 6px.

---

## ✅ Checklist

- [ ] La tarjeta aparece con animación de entrada al cargar
- [ ] El badge "Disponible" pulsa suavemente en loop
- [ ] Hover aplica `rotateY` y `translateY` suave
- [ ] `:root` tiene tokens de duración y easing
- [ ] `prefers-reduced-motion` elimina el movimiento
- [ ] El código NO tiene valores mágicos de tiempo (p. ej. `200ms` literal)

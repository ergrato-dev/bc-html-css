# Proyecto Semana 06 — NavLayout: Navbar, Cards y Modal

## 📋 Descripción

Construye **NavLayout**, una interfaz de producto con tres componentes de UI que requieren `position` en su implementación:

1. **Navbar sticky** — se fija al tope al hacer scroll
2. **Cards con badge** — badge posicionado absolutamente sobre la imagen
3. **Modal overlay** — ventana de detalle con overlay oscuro fijo

![Estructura NavLayout](../0-assets/01-position-contexts.svg)

---

## 🎯 Objetivos del proyecto

Aplicar `position: sticky`, `absolute` y `fixed` en contextos de UI reales.

---

## 📐 Requisitos técnicos

| # | Requisito |
|---|-----------|
| 1 | El header usa `position: sticky; top: 0` con `z-index` apropiado |
| 2 | Cada tarjeta tiene `position: relative` como containing block |
| 3 | Los badges usan `position: absolute` con `top` y `left` definidos |
| 4 | El overlay usa `position: fixed; inset: 0` con fondo semitransparente |
| 5 | El dialog del modal usa `position: fixed` centrado con `transform` |
| 6 | Sistema de `z-index` con variables CSS (³ niveles: header, overlay, modal) |
| 7 | Variables CSS en `:root` para colores, espaciados y z-index |
| 8 | Al menos 4 tarjetas con imagen, nombre, categoría, precio y badge |
| 9 | El código HTML es semántico (`<header>`, `<main>`, `<article>`, `<dialog>`) |
| 10 | Diseño responsive básico: las tarjetas no desbordan en pantallas pequeñas |

---

## 🗂️ Estructura del proyecto

```
3-proyecto/
├── README.md              ← Este archivo
├── starter/
│   ├── index.html         ← Tu punto de partida (con TODOs)
│   └── css/
│       └── styles.css     ← Estilos base + TODOs
└── solution/              ← ⚠️ Solo para instructores (.gitignore)
```

---

## ⏱️ Tiempo estimado

1.5 – 2 horas

---

## ✅ Checklist de entrega

- [ ] Navbar pegajosa al hacer scroll
- [ ] Mínimo 4 tarjetas con badge absoluto
- [ ] Modal overlay visible al hacer clic en "Ver detalle"
- [ ] Sistema de z-index con variables CSS
- [ ] Código HTML válido (W3C Validator)
- [ ] Sin errores en DevTools Console

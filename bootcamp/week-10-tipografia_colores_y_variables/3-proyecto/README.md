# Proyecto — Design Tokens Page

## 🎯 Objetivo

Crear una **página de documentación visual** que presente el sistema de design tokens del proyecto. La página debe demostrar sus propios tokens — colores, tipografía, espaciados, radios y sombras — usando únicos CSS Custom Properties, sin valores mágicos.

---

## 📋 Descripción

La página "**Craft Tokens**" es una guía de estilo (style guide) minimalista que muestra:

| Sección | Contenido |
|---|---|
| Header | Nombre del sistema + descripción |
| Colores | Paleta primaria, éxito, advertencia, peligro y neutros |
| Tipografía | Escala modular 1.25 + fuentes + pesos |
| Espaciados | Escala de 8 niveles visualizados |
| Formas | Border-radius + sombras |
| Botones | Variantes del sistema de botones |

---

## ⏱️ Tiempo estimado

**2 horas**

---

## 📁 Estructura

```
3-proyecto/
├── README.md
├── starter/
│   ├── index.html   ← NO modificar
│   └── css/
│       └── styles.css  ← Implementa los TODOs
└── solution/        ← OCULTA
```

---

## ✅ Requisitos

- [ ] Sistema completo de tokens en `:root` (colores HSL, tipo, espaciados, radios)
- [ ] Paleta de colores en HSL con primitivos y semánticos separados
- [ ] Escala tipográfica modular (razón 1.25) con `rem`
- [ ] Espaciados usando la escala de tokens (`var(--space-*)`)
- [ ] Sombras y border-radius declarados como variables
- [ ] `calc()` usado en al menos 2 declararaciones
- [ ] Tema oscuro con `prefers-color-scheme: dark`
- [ ] Sin valores mágicos — todo usa `var()`
- [ ] Responsive: funcional en 320px, 768px y 1024px

---

## 🎓 Criterios de Evaluación

| Criterio | Puntos |
|---|---|
| Sistema de tokens completo en `:root` | 25 |
| Paleta HSL con primitivos + semánticos | 15 |
| Escala tipográfica modular aplicada | 15 |
| `calc()` en mínimo 2 declaraciones | 10 |
| Tema oscuro con CSS Variables | 15 |
| Sin valores mágicos | 10 |
| Responsive funcional | 10 |
| **Total** | **100** |

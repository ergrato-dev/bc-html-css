# Proyecto Semana 04 — Página Estilizada con Selectores CSS

## 🎯 Descripción

Toma una página HTML ya construida y dale estilo completo usando selectores CSS variados: tipo, clase, ID, atributo, combinadores y pseudo-clases. El objetivo es demostrar que puedes apuntar con precisión a cualquier elemento sin modificar el HTML.

## 📋 Requisitos

Trabajarás **solo en los archivos CSS**. El HTML no debe modificarse.

### Funcionalidades mínimas

1. **Header fijo:** background oscuro, logo en `color: #e34f26`, navbar con links estilizados
2. **Tarjetas de perfil:** al menos 3 cards con hover effect
3. **Formulario de contacto:** labels, inputs con `:focus`, botón con `:hover`
4. **Tabla de habilidades:** encabezado diferenciado, filas alternadas con `:nth-child`
5. **Footer:** links con `:visited` y `:hover` diferenciados

### Selectores que debes usar (mínimo)

| Selector | Dónde usarlo |
|----------|-------------|
| Selector de tipo | Base para `p`, `h1–h3`, `ul`, `a` |
| Selector de clase | `.card`, `.btn`, `.nav-link` |
| Selector de ID | `#contact-form`, `#hero` |
| Selector de atributo | Links externos `a[href^="https"]` |
| Combinador descendiente | `nav a`, `.card p` |
| Combinador hijo | `ul > li` |
| Hermano adyacente | `h2 + p` |
| Pseudo-clase `:hover` | Botones, cards, enlaces |
| Pseudo-clase `:focus-visible` | Inputs y botones para accesibilidad |
| Pseudo-clase `:nth-child` | Filas alternadas de tabla |

## 🗂️ Estructura

```
3-proyecto/
├── README.md           ← Este archivo
├── starter/
│   ├── index.html      ← HTML completo (NO modificar)
│   └── css/
│       └── styles.css  ← Tu trabajo: añadir estilos
└── solution/           ← Solo para instructores
```

## ⏱️ Tiempo estimado

1.5–2 horas

## ✅ Criterios de evaluación

- [ ] Al menos 7 tipos de selectores distintos usados
- [ ] Sin `!important` en el CSS
- [ ] Hover effect funcional en cards y botón
- [ ] Inputs con `:focus-visible` visibles y accesibles
- [ ] Contraste de texto mínimo 4.5:1 (WCAG AA)
- [ ] CSS sin errors en [W3C Validator](https://jigsaw.w3.org/css-validator/)
- [ ] Código revisado en DevTools → Elements → Computed

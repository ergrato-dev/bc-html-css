# Ejercicio 03 — Navegación por Teclado

## 🎯 Objetivo

Implementar los patrones CSS y HTML que garantizan una experiencia accesible para usuarios que navegan exclusivamente con el teclado: skip links, contenido visualmente oculto, estilos de foco y roles de interactividad.

---

## 📋 Requisitos previos

- Haber completado el Ejercicio 01 (semántica HTML5)
- Haber completado el Ejercicio 02 (atributos ARIA)
- Leer `1-teoria/02-accesibilidad-aria.md`, secciones: skip link, `.visually-hidden`, `:focus-visible`, `tabindex`

---

## 🗂️ Estructura del ejercicio

```
03-ejercicio-keyboard/
├── README.md              ← este archivo
└── starter/
    ├── index.html         ← abre aquí en Live Server
    └── css/
        └── styles.css
```

---

## 📝 Instrucciones

### Paso 1: Skip link — enlace "Saltar al contenido"

El archivo `starter/styles.css` tiene el skip link posicionado de forma fija en pantalla (siempre visible). Los usuarios de teclado necesitan que esté **oculto hasta que reciba el foco**.

**Abre `starter/css/styles.css`** y descomenta el bloque **PASO 1**:

```css
/* Resultado: el `.skip-link` quedará fuera de pantalla por defecto
   y aparecerá en la posición `top: 0` al recibir foco con Tab  */
```

---

### Paso 2: `.visually-hidden` — texto solo para lectores de pantalla

En `starter/index.html` hay etiquetas `<span>` con información textual que se ocultan con `display: none` — esto las hace invisibles también para los lectores de pantalla.

**Abre `starter/index.html`** y descomenta el bloque **PASO 2** que reemplaza `display: none` por la clase `.visually-hidden`.

Luego **abre `starter/css/styles.css`** y descomenta el bloque **PASO 2** para añadir la definición del patrón `.visually-hidden`.

```css
/* .visually-hidden:
   - Visible para lectores de pantalla
   - Invisible y sin impacto en el layout visual  */
```

---

### Paso 3: `:focus-visible` — estilos de foco para teclado

El CSS inicial suprime todos los contornos de foco (`outline: none` global). Esto es un problema grave para la accesibilidad con teclado.

**Abre `starter/css/styles.css`** y descomenta el bloque **PASO 3**:

```css
/* Resultado: los elementos interactivos mostrarán un outline claro
   solo cuando se navegue con teclado (no al hacer clic con ratón) */
```

---

### Paso 4: `tabindex` — elementos interactivos personalizados

En `starter/index.html` hay una tarjeta `<div role="button">` que no recibe el foco con la tecla Tab porque no es un elemento nativo interactivo.

**Abre `starter/index.html`** y descomenta el bloque **PASO 4** que añade `tabindex="0"` al `div[role="button"]`.

```html
<!-- Resultado: el div con role="button" pasa a ser enfocable
     mediante Tab sin alterar el orden natural de la página  -->
```

---

## ✅ Resultado esperado

Al finalizar los 4 pasos:

- [ ] El skip link es invisible hasta presionar `Tab` y aparece en la esquina superior izquierda
- [ ] Los textos con `.visually-hidden` son leídos por VoiceOver / NVDA pero no se ven en pantalla
- [ ] Navegar con `Tab` muestra un contorno azul claro en cada elemento interactivo
- [ ] La tarjeta `div[role="button"]` recibe el foco con `Tab` como un botón nativo
- [ ] Los botones `<button>` y los `<a>` también muestran el outline correcto
- [ ] No hay ningún elemento con `tabindex` positivo (≥ 1) en el HTML

---

## 💡 Conceptos clave

| Patrón | ¿Para qué sirve? |
| --- | --- |
| Skip link | Permite a los usuarios de teclado saltar la navegación repetitiva |
| `.visually-hidden` | Provee contexto textual al lector sin afectar el diseño visual |
| `:focus-visible` | Muestra el indicador de foco solo cuando se navega con teclado |
| `tabindex="0"` | Hace enfocables elementos no interactivos nativos |
| `tabindex="-1"` | Permite enfoque programático (JS) sin entrar en el flujo Tab |

---

## 🔗 Recursos

- [MDN — `:focus-visible`](https://developer.mozilla.org/es/docs/Web/CSS/:focus-visible)
- [MDN — `tabindex`](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/tabindex)
- [Técnica — skip navigation links](https://www.w3.org/WAI/WCAG21/Techniques/general/G1)
- [web.dev — visually-hidden](https://web.dev/articles/keyboard-access)

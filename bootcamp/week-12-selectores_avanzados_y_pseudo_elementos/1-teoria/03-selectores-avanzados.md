# Selectores Avanzados CSS

> **Semana 12 — Teoría 03**: `:has()`, `:is()`, `:where()`, `:not()`, selectores de atributo y estados de formulario.

---

## 🎯 Objetivos

- Agrupar selectores repetidos con `:is()` y `:where()` para reducir código
- Usar `:not()` para excluir elementos de una regla
- Aplicar el selector parental `:has()` para estilar contenedores según su contenido
- Seleccionar elementos por sus atributos con `[attr]`, `[attr=value]`, `[attr^=]`, `[attr*=]`
- Controlar estados de formulario: `:checked`, `:valid`, `:invalid`, `:focus-within`

---

## 1. `:not()` — Excluir Elementos

`:not(selector)` aplica estilos a todos los elementos que **no** coincidan con el argumento.

```css
/* Todos los <li> excepto el último — elimina el borde inferior */
.menu li:not(:last-child) {
  border-bottom: 1px solid var(--color-border);
}

/* Todos los botones que no sean de tipo submit */
button:not([type="submit"]) {
  background: transparent;
  border: 1px solid var(--color-primary);
}

/* Imágenes que no tienen atributo alt — alerta visual */
img:not([alt]) {
  outline: 3px solid red;
}
```

---

## 2. `:is()` — Agrupar Selectores

`:is()` agrupa múltiples selectores en una misma regla. La especificidad es la del **selector más específico** del grupo.

```css
/* ❌ Sin :is() — código repetitivo */
article h1,
article h2,
article h3,
aside h1,
aside h2,
aside h3 {
  color: var(--color-text);
  line-height: 1.3;
}

/* ✅ Con :is() — mismo resultado, menos código */
:is(article, aside) :is(h1, h2, h3) {
  color: var(--color-text);
  line-height: 1.3;
}
```

> 📌 **Especificidad de `:is()`:** La especificidad del selector completo usa el selector más específico de dentro. `:is(#id, .class)` tiene especificidad de `#id` (1,0,0).

---

## 3. `:where()` — Agrupar sin Especificidad

`:where()` funciona exactamente igual que `:is()` pero con **especificidad cero**. Ideal para estilos base fácilmente sobrescribibles.

```css
/* Estilos base con especificidad 0 — cualquier regla posterior los sobreescribe */
:where(h1, h2, h3, h4, h5, h6) {
  font-family: var(--font-display);
  line-height: 1.2;
}

/* Esta regla de componente (especificidad 0-1-0) gana sin necesidad de !important */
.card h2 {
  line-height: 1.5;
}
```

| Selector | Especificidad |
|----------|---------------|
| `:is(h1, .text, #main)` | (1,0,0) — toma el más específico: `#main` |
| `:where(h1, .text, #main)` | (0,0,0) — siempre cero |

---

## 4. `:has()` — El Selector Parental

`:has()` selecciona un elemento **padre** si contiene un hijo que coincida con el selector. Es el "selector parental" que CSS nunca tuvo hasta 2023.

```css
/* Tarjeta que contiene una imagen: mayor padding */
.card:has(img) {
  padding: 0;
}

/* Formulario con algún input inválido: borde de error */
form:has(input:invalid) {
  border: 2px solid hsl(0 72% 51%);
}

/* Sección de lista vacía — ocultar si no tiene hijos */
.results-section:not(:has(li)) {
  display: none;
}

/* Figura con pie de foto: diferente espaciado */
figure:has(figcaption) {
  margin-bottom: var(--space-8);
}

/* Párrafo que viene inmediatamente después de un h2 */
h2 + p:has(strong) {
  font-size: 1.05rem;
}
```

> 🆕 `:has()` está disponible en todos los navegadores modernos desde 2023 (Chrome 105, Firefox 121, Safari 15.4).

---

## 5. Selectores de Atributo

```css
/* ── Selección por atributo ── */
[href]         /* cualquier elemento con atributo href */
[type="text"]  /* input con type exactamente "text" */
[class~="btn"] /* elemento cuya clase contiene la palabra "btn" */
[lang|="en"]   /* lang igual a "en" o empieza con "en-" */

/* ── Coincidencia de cadena ── */
[href^="https"]  /* href empieza con "https" — enlaces externos */
[href$=".pdf"]   /* href termina con ".pdf" */
[href*="github"] /* href contiene "github" */
```

```css
/* Aplicaciones prácticas */

/* Icono de enlace externo */
a[href^="https://"]::after {
  content: " ↗";
  font-size: 0.8em;
  opacity: 0.7;
}

/* Advertencia en links a PDF */
a[href$=".pdf"]::before {
  content: "📄 ";
}

/* Inputs de búsqueda con estilo especial */
input[type="search"] {
  border-radius: 9999px;
  padding-inline-start: 2rem;
}
```

---

## 6. Estados de Formulario

### `:checked`

```css
/* checkbox o radio marcado */
input[type="checkbox"]:checked + label {
  color: var(--color-primary);
  font-weight: 600;
}

/* ── Custom checkbox puro en CSS ── */
/* Ocultar el input nativo pero mantenerlo accesible */
.custom-checkbox input[type="checkbox"] {
  position: absolute;
  opacity: 0;
  width: 0;
  height: 0;
}

/* La caja visual */
.custom-checkbox label::before {
  content: "";
  display: inline-block;
  width: 1.2em;
  height: 1.2em;
  border: 2px solid var(--color-border);
  border-radius: 4px;
  margin-right: 0.5rem;
  vertical-align: middle;
  transition: background 150ms ease-out, border-color 150ms ease-out;
}

/* Estado marcado: relación sibling con + */
.custom-checkbox input:checked + label::before {
  background: var(--color-primary);
  border-color: var(--color-primary);
}
```

### `:valid`, `:invalid` y `:focus-within`

```css
/* Input con valor válido para el tipo */
input:valid  { border-color: hsl(142 61% 38%); }
input:invalid { border-color: hsl(0 72% 51%); }

/* Solo mostrar error si el usuario ya interactuó — usar :not(:placeholder-shown) */
input:not(:placeholder-shown):invalid {
  border-color: hsl(0 72% 51%);
}

/* ── :focus-within ── */
/* El padre recibe estilos cuando cualquier hijo tiene foco */
.form-group:focus-within label {
  color: var(--color-primary);
  transform: translateY(-2px);
}
```

---

## ✅ Checklist

- [ ] Uso `:not()` en lugar de añadir una clase "last" o "first" al HTML
- [ ] Conozco la diferencia de especificidad entre `:is()` y `:where()`
- [ ] Aplico `:has()` para al menos un caso donde antes necesitaría JS
- [ ] Uso selectores de atributo para estilar por datos (`[href^=]`, `[data-*]`)
- [ ] Mis formularios usan `:valid`/`:invalid` con condiciones apropiadas

---

## 📚 Recursos

- [MDN — :has()](https://developer.mozilla.org/es/docs/Web/CSS/:has)
- [MDN — :is()](https://developer.mozilla.org/es/docs/Web/CSS/:is)
- [MDN — :not()](https://developer.mozilla.org/es/docs/Web/CSS/:not)
- [MDN — Attribute selectors](https://developer.mozilla.org/es/docs/Web/CSS/Attribute_selectors)
- [Can I Use — :has()](https://caniuse.com/css-has)

# Sintaxis CSS y Selectores

## 🎯 Objetivos

- Escribir reglas CSS con la estructura correcta
- Dominar los selectores principales: tipo, clase, ID, atributo
- Usar combinadores para seleccionar elementos en contexto

---

## 1. Anatomía de una regla CSS

```css
/* Selector — define a qué elementos se aplica el estilo */
.btn-primary {
  /* Propiedad: valor; */
  background-color: #3b82f6;
  color: #ffffff;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-size: 1rem;
}
```

Una **declaración** = propiedad + valor (terminada en `;`)
Un **bloque** = conjunto de declaraciones entre `{}`
Una **regla** = selector + bloque

Para vincular CSS externo al HTML:

```html
<!-- En el <head> del HTML -->
<link rel="stylesheet" href="css/styles.css" />
```

> Orden correcto en `<head>`: primero `meta charset`, `meta viewport`, `title`, luego `<link>` CSS.

---

## 2. Selectores básicos

```css
/* Selector de tipo — selecciona todos los <p> */
p {
  line-height: 1.6;
}

/* Selector de clase — selecciona cualquier elemento con class="card" */
.card {
  background: #161b22;
  border-radius: 8px;
}

/* Selector de ID — selecciona el elemento único con id="hero" */
/* Usar solo para anchors y JS, evitar para estilos CSS */
#hero {
  min-height: 100vh;
}

/* Selector universal — selecciona todos los elementos */
* {
  box-sizing: border-box;
}
```

---

## 3. Selectores de atributo

```css
/* Tiene el atributo href */
a[href] { color: #58a6ff; }

/* El atributo href comienza con "https" */
a[href^="https"] { color: #3fb950; }

/* El atributo href termina con ".pdf" */
a[href$=".pdf"]::after { content: " (PDF)"; }

/* El atributo class contiene la palabra "btn" */
[class*="btn"] { cursor: pointer; }

/* El atributo type es exactamente "email" */
input[type="email"] { border-color: #264de4; }

/* El atributo lang es "es" o empieza con "es-" */
[lang|="es"] { font-family: "Noto Serif", serif; }
```

---

## 4. Combinadores

```css
/* Descendiente (espacio): cualquier <a> dentro de .nav */
.nav a {
  text-decoration: none;
}

/* Hijo directo (>): solo los <li> hijos directos de .nav-list */
.nav-list > li {
  display: inline-block;
}

/* Hermano adyacente (+): el <p> inmediatamente después de <h2> */
h2 + p {
  font-size: 1.1rem;
  font-weight: 500;
}

/* Hermanos siguientes (~): todos los <p> después de un <h2> */
h2 ~ p {
  color: #8b949e;
}
```

---

## 5. Pseudo-clases de interacción

```css
/* :hover — cuando el cursor pasa sobre el elemento */
.btn:hover {
  opacity: 0.85;
  transform: translateY(-2px);
}

/* :focus — cuando el elemento recibe el foco (teclado/clic) */
input:focus {
  outline: 2px solid #3b82f6;
  outline-offset: 2px;
}

/* :focus-visible — foco visible solo para navegación por teclado */
button:focus-visible {
  outline: 2px solid #3b82f6;
}

/* :active — mientras se hace clic */
.btn:active {
  transform: translateY(0);
}

/* :link y :visited — estados de enlace no visitado / visitado */
a:link { color: #58a6ff; }
a:visited { color: #bc8cff; }
```

---

## 6. Múltiples selectores y agrupación

```css
/* Aplicar el mismo estilo a múltiples selectores (separados por coma) */
h1,
h2,
h3 {
  font-weight: 700;
  line-height: 1.2;
}

/* Múltiples clases en un mismo elemento */
/* <div class="card card-featured"> */
.card.card-featured {
  border-color: #e34f26;
  box-shadow: 0 0 0 2px #e34f26;
}
```

---

## ✅ Checklist de verificación

- [ ] CSS en archivo externo (no `style=""` inline salvo excepción justificada)
- [ ] Clases en `kebab-case`: `.nav-item`, `.hero-title`, `.btn-primary`
- [ ] Sin IDs para estilos (solo para JS y anchors)
- [ ] Selectores tan simples como sea posible
- [ ] Selectores de atributo usados para formularios e inputs

## 📚 Recursos

- [MDN — Selectores CSS](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Selectors)
- [CSS-Tricks — Guide to CSS selectors](https://css-tricks.com/almanac/selectors/)

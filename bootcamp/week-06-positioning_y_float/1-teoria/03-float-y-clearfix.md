# Float y Clearfix

## 🎯 Objetivos

- Entender el comportamiento original de `float`
- Aplicar clearfix para evitar el colapso del contenedor
- Conocer la alternativa moderna: `display: flow-root`
- Saber cuándo usar (y no usar) `float` hoy en día

---

## 📋 Contenido

### 1. ¿Qué hace `float`?

`float` fue diseñado originalmente para **envolver texto alrededor de imágenes** (como en una revista). Saca parcialmente al elemento del flujo normal: los elementos de bloque lo ignoran, pero el texto inline (y los inline-blocks) lo rodean.

```css
/* Imagen flotando a la izquierda con texto alrededor */
.article-image {
  float: left;
  margin-right: 1.5rem;
  margin-bottom: 1rem;
  width: 200px;
}
```

```html
<article>
  <img src="photo.jpg" alt="Fotografía" class="article-image" />
  <p>Este texto fluye alrededor de la imagen flotante. Lorem ipsum dolor
  sit amet, consectetur adipiscing elit. Suspendisse varius enim in
  eros elementum tristique.</p>
</article>
```

---

### 2. El problema del contenedor colapsado

Cuando todos los hijos de un contenedor flotan, el contenedor colapsa a altura cero porque **los floats no contribuyen a la altura del padre**.

```html
<!-- ❌ El .container colapsa — no abraza los floats -->
<div class="container">
  <div class="float-left">Columna 1</div>
  <div class="float-right">Columna 2</div>
</div>
```

```css
.float-left { float: left; width: 48%; }
.float-right { float: right; width: 48%; }
/* .container ahora tiene height: 0 */
```

---

### 3. La solución clásica: clearfix

El *clearfix* fuerza al contenedor a expandirse para abarcar sus floats hijos:

```css
/* ✅ Clearfix clásico con pseudo-elemento (compatible con todos los navegadores) */
.clearfix::after {
  content: "";
  display: block;   /* o table */
  clear: both;
}
```

```html
<div class="container clearfix">
  <div class="float-left">Columna 1</div>
  <div class="float-right">Columna 2</div>
</div>
<!-- Ahora .container abraza ambas columnas correctamente -->
```

---

### 4. La solución moderna: `display: flow-root`

Desde CSS3, la forma más limpia es usar `display: flow-root` en el contenedor. Crea un **Block Formatting Context (BFC)** que contiene los floats automáticamente:

```css
/* ✅ Solución moderna (Chrome 58+, Firefox 53+, Safari 12+) */
.container {
  display: flow-root;
  /* Eso es todo. Sin pseudoelementos, sin hacks. */
}
```

También activa un BFC y contiene floats:
```css
.container {
  overflow: hidden;  /* ← solución heredada, también funciona */
}
```

---

### 5. `clear` — detener el flujo del float

`clear` indica que el elemento no puede estar al lado de un float:

```css
.footer {
  clear: both;   /* no al lado de float left NI float right */
  /* otros valores: left, right, none */
}
```

---

### 6. Float hoy en día: ¿cuándo usarlo?

| Uso | ¿Correcto? |
|-----|-----------|
| Texto alrededor de imagen (estilo artículo) | ✅ Sí — para eso fue diseñado |
| Columnas de layout | ❌ No — usar Flexbox o Grid |
| Elementos en línea con espacio | ❌ No — usar Flexbox con `gap` |
| Navbars | ❌ No — usar Flexbox |

> **Regla práctica para 2026:** Float solo sirve para envolver texto alrededor de imágenes. Para todo lo demás: Flexbox (semana 07) o Grid (semana 08).

---

## 📚 Recursos adicionales

- [MDN — float](https://developer.mozilla.org/es/docs/Web/CSS/float)
- [MDN — clear](https://developer.mozilla.org/es/docs/Web/CSS/clear)
- [MDN — Block formatting context](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context)
- [MDN — display: flow-root](https://developer.mozilla.org/en-US/docs/Web/CSS/display#flow-root)

---

## ✅ Checklist de verificación

- [ ] Puedo hacer que el texto fluya alrededor de una imagen con `float`
- [ ] Sé por qué el contenedor colapsa cuando sus hijos flotan
- [ ] Puedo aplicar clearfix con `::after` o `display: flow-root`
- [ ] Entiendo que `float` no se usa para layouts en CSS moderno

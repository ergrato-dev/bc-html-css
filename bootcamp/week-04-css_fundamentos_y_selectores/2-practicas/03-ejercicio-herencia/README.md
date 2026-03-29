# Ejercicio 03 — Herencia y Reset CSS

## 🎯 Objetivo

Comprender qué propiedades CSS se heredan automáticamente y cuáles no. Aplicar un reset mínimo con `box-sizing` y practicar las palabras clave `inherit`, `initial` y `unset`.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque y observa cómo cambia el layout.

---

## Paso 1: Ver herencia automática

`color` y `font-family` se heredan de padres a hijos. `margin`, `padding` y `border` no se heredan.

```css
/* Esto se hereda en todos los descendientes */
body {
  font-family: system-ui, sans-serif;
  color: #c9d1d9;
}
```

**Antes de descomentar el PASO 1:** observa que el texto aparece con estilos por defecto del navegador.

**Descomenta el bloque `/* PASO 1 */`** y mira cómo cambia la tipografía en todo el documento de una sola declaración.

---

## Paso 2: Reset con box-sizing y márgenes

Sin reset, cada navegador aplica sus propios estilos por defecto (márgenes en `<body>`, `<h1>`, `<p>`, etc.). El reset homogeneiza la base.

```css
/* Reset mínimo: aplica box-sizing a todos los elementos */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

**Descomenta el bloque `/* PASO 2 */`** y observa que todo se "pega" al borde. Luego el resto de los estilos añadirán el espacio de vuelta de forma controlada.

---

## Paso 3: Usar la palabra clave `inherit`

A veces una propiedad no hereda por defecto (como `border-color`) pero queremos que tome el valor del padre.

```css
/* input no hereda font-family por defecto — lo forzamos */
input,
button,
textarea {
  font-family: inherit;
}
```

**Descomenta el bloque `/* PASO 3 */`** y compara la fuente del `<input>` antes y después.

---

## Paso 4: Usar `initial` y `unset`

```css
/* initial: devuelve la propiedad a su valor inicial definido por la spec CSS */
.reset-color {
  color: initial; /* negro en texto, pero depende del agente */
}

/* unset: si la propiedad hereda → usa inherit; si no → usa initial */
.unset-margin {
  margin: unset;
}
```

**Descomenta el bloque `/* PASO 4 */`** y observa el efecto en los elementos con esas clases.

---

## ✅ Verificación

- [ ] Sin reset: los elementos tienen márgenes y fuentes del navegador
- [ ] Con reset aplicado: todo está "a ras" del borde del viewport
- [ ] `font-family: inherit` iguala la fuente de inputs y botones al cuerpo
- [ ] `.reset-color` muestra el color inicial (negro por defecto)
- [ ] Puedes ver en DevTools → Computed qué propiedades están heredadas y cuáles no

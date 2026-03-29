# Ejercicio 02 — Especificidad CSS

## 🎯 Objetivo

Entender cómo el navegador resuelve conflictos cuando dos o más reglas CSS apuntan al mismo elemento. Practicar el cálculo de especificidad `(A, B, C)`.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. En este ejercicio verás estilos en conflicto y aprenderás cuál "gana" y por qué.

---

## Paso 1: Observar el conflicto base

El HTML tiene un botón con `id="save-btn"` y `class="btn btn-primary"`. Hay tres reglas que intentan colorearlo. Observa cuál gana **sin** descomentar nada.

```css
/* (0,0,1) — selector de tipo — especificidad baja */
button { background-color: gray; }

/* (0,1,0) — selector de clase — especificidad media */
.btn { background-color: #264de4; }

/* (1,0,0) — selector de ID — especificidad alta → GANA */
#save-btn { background-color: #e34f26; }
```

**Observa en el navegador:** el botón debe ser naranja (`#e34f26`), porque el ID tiene la mayor especificidad `(1,0,0)`.

No necesitas descomentar nada en este paso. Solo observa el resultado.

---

## Paso 2: Aumentar especificidad con combinación de selectores

Descomenta el bloque `/* PASO 2 */` en `styles.css`.

```css
/* (0,2,1) — .section-form .btn con p — "gana" al .btn (0,1,0) */
.section-form .btn {
  background-color: #3fb950;
  color: #0d1117;
}
```

Verás que el botón dentro de `.section-form` ahora es verde, porque `(0,2,0)` supera a `(0,1,0)`.

---

## Paso 3: El orden de aparición como desempate

Cuando dos selectores tienen la misma especificidad, **el que aparece último en el CSS gana**.

Descomenta el bloque `/* PASO 3 */`.

```css
/* Ambas tienen especificidad (0,1,0) — la segunda gana */
.btn-primary { color: white; }
.btn-winner  { color: #f0e68c; }  /* ← esta gana por orden */
```

---

## Paso 4: El problema de !important

Descomenta el bloque `/* PASO 4 */` y observa que `!important` sobreescribe todo, incluyendo el ID. Es un anti-patrón que rompe la cascada normal.

```css
/* ⚠️ !important sobreescribe incluso el ID #save-btn */
.btn-danger {
  background-color: #da3633 !important;
}
```

---

## ✅ Verificación

- [ ] El botón base es naranja (ID gana sobre clase y tipo)
- [ ] El botón en `.section-form` es verde (especificidad más alta)
- [ ] El texto del botón `.btn-winner` es amarillo claro (orden en CSS)
- [ ] El botón `.btn-danger` con `!important` es rojo aunque tenga un ID
- [ ] Puedes calcular `(A,B,C)` de cualquier selector en DevTools → Styles

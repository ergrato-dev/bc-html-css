# Ejercicio 02 — Z-index y Stacking Context

## 🎯 Objetivo

Comprender cómo funciona el orden de apilamiento con `z-index` y por qué a veces "no funciona".

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque siguiendo los pasos.

---

## Paso 1: Entender que z-index requiere position

`z-index` no tiene efecto en elementos con `position: static`.

```css
/* ❌ Esto no funciona */
.element {
  position: static; /* por defecto */
  z-index: 999; /* ignorado */
}

/* ✅ Esto sí funciona */
.element {
  position: relative; /* o absolute/fixed/sticky */
  z-index: 999;
}
```

**Descomenta el bloque `/* PASO 1 */`** para ver cómo activar z-index en las capas.

---

## Paso 2: Apilar capas en el orden correcto

Con `z-index` podemos controlar qué capa queda encima:

```css
.layer-back   { z-index: 1; }
.layer-middle { z-index: 2; }
.layer-front  { z-index: 3; }
```

**Descomenta el bloque `/* PASO 2 */`** y observa cómo cambia el orden visual.

---

## Paso 3: El problema del stacking context

Cuando un padre crea su propio stacking context, sus hijos no pueden competir con elementos externos.

```css
/* Padre con z-index:1 crea stacking context */
.parent-a { position: relative; z-index: 1; }

/* Este hijo tiene z-index:999, pero pertenece al contexto de parent-a (z:1) */
.child-tooltip { position: absolute; z-index: 999; }

/* parent-b tiene z-index:2 — GANARÁ sobre el hijo aunque éste sea 999 */
.parent-b { position: relative; z-index: 2; }
```

**Descomenta el bloque `/* PASO 3 */`** y observa el comportamiento.

---

## Paso 4: `isolation: isolate` — solución moderna

Para crear un stacking context sin valores numéricos:

```css
.isolated-component {
  isolation: isolate;
}
```

**Descomenta el bloque `/* PASO 4 */`** y compara el comportamiento.

---

## ✅ Verificación

- [ ] Las capas se apilan en el orden correcto con z-index numérico
- [ ] Entiendo por qué un hijo con z-index:999 puede quedar detrás de otro elemento
- [ ] Puedo usar `isolation: isolate` para aislar el contexto de un componente

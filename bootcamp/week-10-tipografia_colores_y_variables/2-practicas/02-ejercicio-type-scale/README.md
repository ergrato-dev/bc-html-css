# Ejercicio 02 — Escala Tipográfica Modular

## 🎯 Objetivo

Implementar un sistema de escala tipográfica basado en la razón modular **1.25** (Major Third), declarando cada nivel como CSS Custom Property y aplicándolo a una jerarquía de headings y texto.

---

## 📋 Pasos

### Paso 1: Declarar la escala de tamaños en `:root`

Abre `starter/css/styles.css` y descomenta la sección **PASO 1**.

Verás 8 niveles definidos con valores `rem`:

```css
:root {
  --text-xs:   0.75rem;    /*  12px  */
  --text-sm:   0.875rem;   /*  14px  */
  --text-base: 1rem;       /*  16px  ← base */
  --text-md:   1.25rem;    /*  20px  */
  --text-lg:   1.563rem;   /*  25px  */
  --text-xl:   1.953rem;   /*  31px  */
  --text-2xl:  2.441rem;   /*  39px  */
  --text-3xl:  3.052rem;   /*  49px  */
}
```

### Paso 2: Aplicar la escala a los headings

Descomenta la sección **PASO 2** — asigna los tamaños a `h1`–`h4` usando `var()`.

### Paso 3: Cuerpo y texto auxiliar

Descomenta la sección **PASO 3** — aplica `--text-base` a `body` y `--text-sm` a `.lead-text` y `.caption`.

### Paso 4: Probar con `calc()` — escala dinámica

Descomenta la sección **PASO 4** — muestra cómo calcular un nivel de la escala con `calc()` en lugar de declarar el valor hardcoded.

---

## ✅ Resultado Esperado

Al terminar, la jerarquía visual debe ser clara y progresiva. Cada heading debe ser visualmente más grande que el siguiente, con línea de base limpia.

Verifica los tamaños en DevTools → tab **Computed** → `font-size`.

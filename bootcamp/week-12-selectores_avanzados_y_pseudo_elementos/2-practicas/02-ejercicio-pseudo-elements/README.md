# Ejercicio 02 — Pseudo-elementos Decorativos

> **Semana 12 · Práctica 02** — Crear bullets, badges y ribbons con `::before` y `::after` sin modificar el HTML.

---

## 🎯 Objetivos

- Crear bullets personalizados con `::before` y `content`
- Implementar un badge "NUEVO" usando `::before` con posición absoluta
- Construir un ribbon diagonal en la esquina de una tarjeta con `::before`
- Añadir una línea decorativa a headings con `::before`

---

## 📋 Descripción

La página muestra cuatro secciones de demostración. En cada una aplicas una técnica diferente de pseudo-elementos.

Abre `starter/css/styles.css` y descomenta los bloques paso a paso.

---

## Paso 1 — Bullets decorativos en lista

Reemplazar los bullets estándar por un carácter personalizado usando `::before`.

```css
/* Lista sin estilo predeterminado */
.features-list {
  list-style: none;
  padding: 0;
}

/* Bullet decorativo: flecha azul antes de cada item */
.features-list li::before {
  content: "▸";
  color: var(--color-primary);
  font-weight: 700;
  margin-right: 0.6rem;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección `PASO 1`.

---

## Paso 2 — Badge "NUEVO" con `::before`

Insertar un badge de texto antes del contenido de una tarjeta marcada como nueva.

```css
.card.is-new {
  position: relative;
  padding-top: 2.5rem;
}

.card.is-new::before {
  content: "NUEVO";
  position: absolute;
  top: 0.75rem;
  left: 1rem;
  background: hsl(142 61% 38%);
  color: #fff;
  font-size: 0.65rem;
  font-weight: 700;
  padding: 0.2em 0.6em;
  border-radius: 9999px;
}
```

**Descomenta la sección `PASO 2`** en el CSS.

---

## Paso 3 — Ribbon diagonal con `::before`

Crear una etiqueta en diagonal en la esquina superior derecha de una tarjeta destacada.

```css
.card.is-featured {
  position: relative;
  overflow: hidden;
}

.card.is-featured::before {
  content: "DESTACADO";
  position: absolute;
  top: 20px;
  right: -30px;
  width: 130px;
  background: hsl(45 96% 55%);
  color: hsl(45 96% 15%);
  font-size: 0.6rem;
  font-weight: 700;
  text-align: center;
  padding: 4px 0;
  transform: rotate(45deg);
}
```

**Descomenta la sección `PASO 3`** en el CSS.

---

## Paso 4 — Línea decorativa en headings con `::before`

Añadir una línea de color a la izquierda de los headings de sección usando `position: absolute`.

```css
.decorated-title {
  position: relative;
  padding-left: 1rem;
}

.decorated-title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 3px;
  background: var(--color-primary);
  border-radius: 2px;
}
```

**Descomenta la sección `PASO 4`** en el CSS.

---

## ✅ Resultado esperado

- Lista con flechas azules `▸` antes de cada item
- Tarjeta con clase `.is-new` muestra badge "NUEVO" verde en la esquina superior izquierda
- Tarjeta con clase `.is-featured` muestra ribbon amarillo diagonal en la esquina superior derecha
- Todos los `.decorated-title` tienen una línea vertical azul a su izquierda

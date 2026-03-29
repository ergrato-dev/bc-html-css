# Ejercicio 01 — Patrones con `:nth-child`

> **Semana 12 · Práctica 01** — Seleccionar elementos por posición sin añadir clases al HTML.

---

## 🎯 Objetivos

- Aplicar zebra stripes a una tabla con `:nth-child(even/odd)`
- Destacar el primer y último elemento con `:first-child` / `:last-child`
- Usar la fórmula `3n+1` para crear un patrón de cuadrícula
- No modificar el HTML durante el ejercicio

---

## 📋 Descripción

Tienes una página con tres secciones:
1. **Tabla de pedidos** → aplicarás zebra stripes y destacarás la cabecera
2. **Lista de equipo** → marcarás el primero, el último y cada tercero
3. **Cuadrícula de fotos** → aplicarás un patrón de tamaño con `3n+1`

Abre `starter/index.html` y descomenta los bloques CSS paso a paso.

---

## Paso 1 — Zebra stripes en la tabla

Aplicar colores alternos a las filas del cuerpo de la tabla para mejorar la legibilidad.

```css
/* Filas pares del cuerpo de la tabla */
tbody tr:nth-child(even) {
  background: hsl(220 14% 10%);
}

/* Primera fila del cuerpo — dato más reciente */
tbody tr:first-child {
  border-left: 3px solid var(--color-primary);
}
```

**Abre `starter/css/styles.css`** y descomenta la sección `PASO 1`.

---

## Paso 2 — Primer y último elemento

Aplicar estilos diferenciados al primer y último `<li>` de la lista de equipo.

```css
/* Primera persona del equipo — líder */
.team-list li:first-child {
  font-weight: 700;
  color: var(--color-primary);
}

/* Último elemento — sin borde inferior */
.team-list li:last-child {
  border-bottom: none;
}
```

**Descomenta la sección `PASO 2`** en el CSS.

---

## Paso 3 — Patrón `3n+1` en la cuadrícula

Hacer que cada tercer elemento (1, 4, 7, 10…) ocupe más espacio en el grid.

```css
/* Elementos en posición 1, 4, 7, 10… */
.photo-grid .photo:nth-child(3n+1) {
  grid-column: span 2;
  grid-row: span 2;
}
```

**Descomenta la sección `PASO 3`** en el CSS.

---

## Paso 4 — Fórmula inversa: los 3 últimos

Reducir la opacidad de los 3 últimos elementos de la lista para indicar que son los más antiguos.

```css
/* Los últimos 3 items del equipo */
.team-list li:nth-last-child(-n+3) {
  opacity: 0.55;
}
```

**Descomenta la sección `PASO 4`** en el CSS.

---

## ✅ Resultado esperado

- Tabla con filas alternas de diferente color de fondo
- Primera fila de la tabla con borde izquierdo azul
- Primer miembro del equipo en negrita y con color primario
- Último miembro sin borde inferior
- Fotos en posición 1, 4, 7 más grandes en el grid
- Últimos 3 miembros del equipo con opacidad reducida

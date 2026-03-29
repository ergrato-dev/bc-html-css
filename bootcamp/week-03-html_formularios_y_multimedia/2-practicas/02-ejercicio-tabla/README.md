# Ejercicio 02 — Tabla Semántica de Horarios

## 🎯 Objetivo

Construir una tabla HTML completamente semántica con `<thead>`, `<tbody>`, `<tfoot>`, encabezados con `scope`, y uso de `colspan` / `rowspan`.

## 📋 Instrucciones

Abre `starter/index.html` con Live Server y descomenta cada paso.

---

### Paso 1: Estructura básica de la tabla

```html
<table>
  <caption>Horario de clases del Bootcamp HTML + CSS</caption>
  <thead>
    <tr>
      <th scope="col">Hora</th>
      <th scope="col">Lunes</th>
      <th scope="col">Martes</th>
      <th scope="col">Miércoles</th>
      <th scope="col">Jueves</th>
      <th scope="col">Viernes</th>
    </tr>
  </thead>
</table>
```

**Descomenta** el `PASO 1`.

---

### Paso 2: Cuerpo de la tabla con `<tbody>` y `<th scope="row">`

```html
<tbody>
  <tr>
    <th scope="row">09:00 – 11:00</th>
    <td>HTML Fundamentos</td>
    <td>Formularios</td>
    <td>—</td>
    <td>CSS Selectores</td>
    <td>Box Model</td>
  </tr>
</tbody>
```

**Descomenta** el `PASO 2`.

---

### Paso 3: `colspan` — Celdas que abarcan varias columnas

`colspan="3"` hace que una celda ocupe 3 columnas, útil para indicar que esa actividad dura todo el día o afecta varias columnas:

```html
<tr>
  <th scope="row">14:00 – 18:00</th>
  <td colspan="5">Proyecto integrador (trabajo autónomo)</td>
</tr>
```

**Descomenta** el `PASO 3`.

---

### Paso 4: `<tfoot>` — Pie de la tabla

```html
<tfoot>
  <tr>
    <th scope="row">Total horas</th>
    <td>4h</td>
    <td>4h</td>
    <td>2h</td>
    <td>4h</td>
    <td>6h</td>
  </tr>
</tfoot>
```

**Descomenta** el `PASO 4`.

---

## ✅ Verificación

- [ ] La tabla tiene `<caption>` descriptivo
- [ ] `<thead>`, `<tbody>` y `<tfoot>` presentes
- [ ] Los `<th>` de columna tienen `scope="col"`
- [ ] Los `<th>` de fila tienen `scope="row"`
- [ ] `colspan` se usa correctamente cuando una celda abarca varias columnas

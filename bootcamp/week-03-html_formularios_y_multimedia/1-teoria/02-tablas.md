# Tablas HTML

## 🎯 Objetivos

- Construir tablas HTML semánticas con la estructura correcta
- Usar `<thead>`, `<tbody>` y `<tfoot>` para organizar filas
- Aplicar `scope` en `<th>` para accesibilidad
- Combinar celdas con `colspan` y `rowspan`
- Entender cuándo usar y cuándo NO usar tablas

---

## 1. Anatomía de una tabla

Las tablas HTML se construyen fila por fila. La estructura semántica divide las filas en tres zonas:

```html
<table>
  <!-- caption: título accesible de la tabla (opcional pero recomendado) -->
  <caption>Horario de clases — Semestre 2026</caption>

  <!-- thead: encabezados de columna -->
  <thead>
    <tr>
      <!-- scope="col" indica que este th encabeza una columna -->
      <th scope="col">Hora</th>
      <th scope="col">Lunes</th>
      <th scope="col">Martes</th>
      <th scope="col">Miércoles</th>
    </tr>
  </thead>

  <!-- tbody: datos principales de la tabla -->
  <tbody>
    <tr>
      <!-- scope="row" indica que este th encabeza una fila -->
      <th scope="row">08:00</th>
      <td>Matemáticas</td>
      <td>Historia</td>
      <td>Ciencias</td>
    </tr>
    <tr>
      <th scope="row">10:00</th>
      <td>HTML/CSS</td>
      <td>HTML/CSS</td>
      <td>Inglés</td>
    </tr>
  </tbody>

  <!-- tfoot: totales, notas al pie, resumen -->
  <tfoot>
    <tr>
      <th scope="row">Total</th>
      <td>2 clases</td>
      <td>2 clases</td>
      <td>2 clases</td>
    </tr>
  </tfoot>
</table>
```

---

## 2. `scope` en `<th>` — por qué es importante

El atributo `scope` indica si un encabezado aplica a una columna o a una fila. Los lectores de pantalla lo usan para anunciar el encabezado de cada celda.

```html
<!-- scope="col": este <th> es el encabezado de su columna -->
<th scope="col">Producto</th>

<!-- scope="row": este <th> es el encabezado de su fila -->
<th scope="row">Subtotal</th>

<!-- scope="colgroup": encabeza varias columnas agrupadas -->
<th scope="colgroup" colspan="2">Primer semestre</th>
```

---

## 3. `colspan` y `rowspan` — combinar celdas

```html
<table>
  <caption>Resultados del torneo</caption>
  <thead>
    <tr>
      <th scope="col">Equipo</th>
      <!-- colspan="3": esta celda ocupa 3 columnas -->
      <th scope="colgroup" colspan="3">Partidos</th>
      <th scope="col">Puntos</th>
    </tr>
    <tr>
      <td></td>
      <th scope="col">G</th>
      <th scope="col">E</th>
      <th scope="col">P</th>
      <td></td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Equipo A</th>
      <td>5</td>
      <td>2</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <th scope="row" rowspan="2">Empate técnico</th>
      <!-- rowspan="2": esta celda ocupa 2 filas -->
      <td>4</td>
      <td>3</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>4</td>
      <td>3</td>
      <td>1</td>
      <td>15</td>
    </tr>
  </tbody>
</table>
```

---

## 4. ¿Cuándo usar tablas?

| ✅ Usar tabla | ❌ No usar tabla |
|--------------|-----------------|
| Datos tabulares (precios, horarios, comparativas) | Layouts de página |
| Comparación de características entre productos | Alinear imágenes |
| Resultados con múltiples filas y columnas | Centrar contenido |
| Calendarios | Crear columnas de texto |

> **Regla clave:** Si los datos tienen relación de fila + columna, usa tabla. Si solo quieres un diseño en columnas, usa Flexbox o Grid.

---

## 5. Tabla completa real: precios de planes

```html
<table>
  <caption>Comparativa de planes de suscripción</caption>
  <thead>
    <tr>
      <th scope="col">Característica</th>
      <th scope="col">Básico</th>
      <th scope="col">Pro</th>
      <th scope="col">Enterprise</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Proyectos</th>
      <td>3</td>
      <td>Ilimitados</td>
      <td>Ilimitados</td>
    </tr>
    <tr>
      <th scope="row">Colaboradores</th>
      <td>1</td>
      <td>10</td>
      <td>Ilimitados</td>
    </tr>
    <tr>
      <th scope="row">Soporte</th>
      <td>Email</td>
      <td>Email + Chat</td>
      <td>24/7 Dedicado</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Precio / mes</th>
      <td>Gratis</td>
      <td>$9 USD</td>
      <td>$49 USD</td>
    </tr>
  </tfoot>
</table>
```

---

## ✅ Checklist de verificación

- [ ] La tabla tiene `<caption>` descriptivo
- [ ] Estructura completa: `<thead>` + `<tbody>` (+ `<tfoot>` si aplica)
- [ ] `<th>` con `scope="col"` en encabezados de columna
- [ ] `<th>` con `scope="row"` en encabezados de fila
- [ ] `colspan` / `rowspan` solo cuando los datos lo requieren
- [ ] La tabla NO se usa para layout

## 📚 Recursos

- [MDN — `<table>`](https://developer.mozilla.org/es/docs/Web/HTML/Element/table)
- [WebAIM — Tablas accesibles](https://webaim.org/techniques/tables/data)

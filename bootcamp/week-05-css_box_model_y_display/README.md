# Semana 05 — CSS Box Model y Display

## 🎯 Objetivos de aprendizaje

Al finalizar esta semana, el estudiante será capaz de:

- ✅ Describir y visualizar los 4 componentes del Box Model: content, padding, border, margin
- ✅ Distinguir entre `box-sizing: content-box` y `box-sizing: border-box`
- ✅ Controlar el espaciado entre elementos con `margin` y `padding`
- ✅ Comprender el colapso de márgenes verticales
- ✅ Aplicar `display: block`, `inline`, `inline-block` y `none` correctamente
- ✅ Gestionar el desbordamiento con `overflow: hidden | scroll | auto`

## 📚 Requisitos previos

- Semana 04: Sintaxis CSS, selectores, especificidad, cascada y herencia
- Semana 03: HTML con formularios, tablas y multimedia
- Semana 02: HTML semántico

## 🗂️ Estructura de la semana

```
week-05-css_box_model_y_display/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-box-model.svg          # Diagrama del Box Model
│   └── 02-display-values.svg     # Comparativa de valores de display
├── 1-teoria/
│   ├── 01-box-model.md           # Content, padding, border, margin, box-sizing
│   ├── 02-margin-y-padding.md    # Shorthand, colapso, auto, negativos
│   └── 03-display-y-overflow.md  # block, inline, inline-block, none, overflow
├── 2-practicas/
│   ├── 01-ejercicio-box-model/
│   ├── 02-ejercicio-margin-padding/
│   └── 03-ejercicio-display/
├── 3-proyecto/
│   ├── README.md
│   ├── starter/
│   └── solution/
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md
```

## 📝 Contenidos

| # | Archivo | Tema |
|---|---------|------|
| 1 | [01-box-model.md](1-teoria/01-box-model.md) | Box Model, content-box vs border-box |
| 2 | [02-margin-y-padding.md](1-teoria/02-margin-y-padding.md) | Shorthand, colapso, margin auto |
| 3 | [03-display-y-overflow.md](1-teoria/03-display-y-overflow.md) | display: block/inline/none, overflow |

## ⏱️ Distribución del tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría: Box Model y box-sizing | 1h |
| Teoría: Margin, padding y colapso | 45 min |
| Teoría: Display y overflow | 45 min |
| Práctica 01: Ejercicio Box Model | 1h |
| Práctica 02: Ejercicio Margin/Padding | 1h |
| Práctica 03: Ejercicio Display | 1h |
| Proyecto: Tarjetas de Producto | 1.5h |
| Revisión y entrega | 1h |

## 📌 Entregables

1. **Ejercicios completados:** 3 ejercicios guiados en carpeta `2-practicas/`
2. **Proyecto:** "Tarjetas de Producto" — página con grid de cards usando Box Model

## 🎓 Conceptos clave

- **Box Model:** El modelo de caja es la base de todo layout en CSS. Cada elemento es una caja con content, padding, border y margin.
- **box-sizing:** Con `border-box` el padding y border se incluyen dentro del ancho/alto declarado.
- **Colapso de márgenes:** Los márgenes verticales adyacentes se fusionan en el mayor de los dos.
- **display:** Determina cómo se comporta un elemento en el flujo del documento.
- **overflow:** Controla qué pasa cuando el contenido es mayor que su contenedor.

## ✅ Checklist de verificación

- [ ] Puedo identificar los 4 componentes del Box Model en DevTools → Computed
- [ ] Entiendo la diferencia entre `content-box` y `border-box`
- [ ] Sé usar el shorthand de margin y padding (top/right/bottom/left)
- [ ] Comprendo por qué los márgenes verticales se colapsan
- [ ] Puedo centrar un bloque horizontalmente con `margin: 0 auto`
- [ ] Distingo cuándo usar `display: block`, `inline` e `inline-block`
- [ ] Sé cuándo usar `overflow: hidden` vs `overflow: auto`

## 🔗 Navegación

← [Semana 04 — CSS Fundamentos y Selectores](../week-04-css_fundamentos_y_selectores/README.md)

→ [Semana 06 — Positioning y Float](../week-06-positioning_y_float/README.md)

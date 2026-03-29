# Proyecto Semana 05 — Tarjetas de Producto

## 🎯 Descripción

Crea una página de catálogo con tarjetas de producto utilizando el Box Model correctamente. Cada tarjeta debe mostrar imagen, nombre, precio y botón. El layout principal usa un grid de 3 columnas.

## 📋 Requisitos

### HTML (ya incluido en starter)
El HTML en `starter/index.html` ya está completo. **Solo debes escribir el CSS**.

### CSS — Funcionalidades mínimas

1. **Reset con `box-sizing: border-box`** en todos los elementos
2. **Variables CSS** para colores, espaciados y tipografía en `:root`
3. **Cards con Box Model correcto:**
   - `padding` interno uniforme
   - `border` visible
   - `border-radius` redondeado
   - `overflow: hidden` para que las imágenes respeten el border-radius
4. **Grid de 3 columnas** con `display: flex` + `flex-wrap: wrap` (o los conocimientos de esta semana)
5. **Imagen con dimensiones controladas:** `width: 100%`, `height: 200px`, `object-fit: cover`
6. **Texto del producto truncado:** nombre largo con `text-overflow: ellipsis`
7. **Hover en la tarjeta:** cambio de borde o sombra con `transition`
8. **Botón centrado:** con `display: block` y `margin: 0 auto`

## 🗂️ Estructura

```
3-proyecto/
├── README.md
├── starter/
│   ├── index.html     ← No modificar
│   └── css/
│       └── styles.css ← Tu trabajo
└── solution/          ← Solo instructores
```

## ⏱️ Tiempo estimado

1.5–2 horas

## ✅ Criterios de evaluación

- [ ] `box-sizing: border-box` aplicado globalmente
- [ ] Variables CSS para todos los valores reutilizables
- [ ] Las 3 tarjetas tienen el mismo tamaño (sin layout roto)
- [ ] Las imágenes no se desbordan y tienen `object-fit: cover`
- [ ] El nombre largo del producto muestra `...` si no cabe
- [ ] Hover visible en cada tarjeta
- [ ] CSS validado en W3C CSS Validator

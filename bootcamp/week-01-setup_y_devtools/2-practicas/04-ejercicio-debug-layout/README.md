# Ejercicio 04 — Debug de layout con DevTools

## Objetivo

Usar las herramientas avanzadas de DevTools para diagnosticar y depurar problemas
de layout: panel Computed, modo responsive y consola de errores.

## Lo que practicarás

- Usar el panel **Computed** para ver los valores finales de las propiedades CSS
- Identificar y corregir errores en la **Console**
- Simular dispositivos móviles con el **modo responsive**
- Forzar estados `:hover` y `:focus` desde DevTools

---

## Paso 1: Panel Computed — valores resueltos

El panel **Computed** muestra el valor **final** de cada propiedad CSS tras aplicar toda
la cascada (especificidad, herencia, valores por defecto del navegador).

```
En DevTools → pestaña Elements → pestaña Computed (junto a Styles)
```

Diferencias clave con el panel Styles:

| Styles | Computed |
| ------ | -------- |
| Muestra las reglas escritas | Muestra los valores finales calculados |
| Puede mostrar `color: var(--color-text)` | Muestra `color: rgb(230, 237, 243)` |
| Puede haber valores tachados | Un solo valor por propiedad (el ganador) |
| Ordenado por archivo/regla | Ordenado alfabéticamente |

**Descomenta la sección PASO 1** en `starter/index.html` y estudia su Computed panel.

---

## Paso 2: Interpretar la Console

La pestaña **Console** de DevTools muestra errores en tiempo real.

Los tipos más comunes:

| Icono | Color | Qué significa |
| ----- | ----- | ------------- |
| `⊗` | Rojo | Error crítico: recurso no encontrado (404), sintaxis inválida |
| `⚠` | Amarillo | Advertencia: algo funciona pero podría fallar |
| `ℹ` | Azul | Información de nivel informativo |

**Errores frecuentes en HTML/CSS:**

```
GET http://localhost:5500/css/estilos.css [404]
→ El archivo no existe o la ruta está mal escrita (verifica href)

Document lacks a doctype
→ Falta <!DOCTYPE html> en la primera línea
```

**Descomenta la sección PASO 2** en `starter/index.html` para introducir un error intencional.

---

## Paso 3: Modo responsive (emulación de dispositivos)

DevTools incluye un emulador de dispositivos para probar diseños en distintos tamaños.

```
Ctrl+Shift+M    →  activa / desactiva el modo responsive
```

En la barra superior del emulador puedes:
- Seleccionar dispositivos predefinidos (iPhone, Pixel, iPad)
- Escribir dimensiones personalizadas (ej: `375 x 812`)
- Usar el selector de DPR (Device Pixel Ratio)

Prueba redimensionar la página de `starter/index.html` en el emulador.

**Descomenta la sección PASO 3** en `starter/index.html`.

---

## Paso 4: Forzar pseudo-clases (:hover, :focus)

Los estados `:hover` y `:focus` suelen ser difíciles de inspeccionar porque desaparecen
al mover el ratón. DevTools permite forzarlos sin tener el ratón encima.

```
1. Selecciona un elemento en el panel Elements
2. Haz clic en ":hov" (en la parte superior del panel Styles)
3. Marca la casilla ":hover" o ":focus"
4. Los estilos de ese estado se aplican permanentemente hasta desmarcarlo
```

También puedes forzarlo desde el menú contextual:
```
Clic derecho sobre el elemento (en el panel Elements) → Force state → :hover
```

**Descomenta la sección PASO 4** en `starter/index.html` para ver un botón con `:hover` estilizado.

---

## Verificación final

- [ ] Encuentras la diferencia entre el panel Styles y el panel Computed
- [ ] Identificas un error 404 en la Console y corriges la ruta
- [ ] Usas el modo responsive para ver la página en 375px de ancho
- [ ] Fuerzas el estado `:hover` en un botón desde DevTools

> ✅ ¡Has completado todos los ejercicios de la Semana 01!
> Pasa al [Proyecto Semanal](../../3-proyecto/README.md)

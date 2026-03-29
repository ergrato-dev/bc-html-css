# 📖 Glosario — Transiciones, Transforms y Animaciones CSS

> Términos clave de la semana ordenados alfabéticamente.

---

## @keyframes

Regla CSS que define los estados intermedios (fotogramas clave) de una animación. Usa `from/to` para dos estados o porcentajes para múltiples pasos.

```css
@keyframes slide-up {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}
```

---

## animation

Propiedad shorthand que combina las 8 sub-propiedades de animación: `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`, `animation-play-state`.

```css
.elemento { animation: slide-up 600ms ease-out 200ms both; }
```

---

## animation-delay

Tiempo de espera antes de que comience la animación. Un valor negativo hace que la animación empiece en un punto intermedio.

---

## animation-direction

Controla el sentido de reproducción: `normal` (forward), `reverse` (backward), `alternate` (forward→backward→forward…), `alternate-reverse`.

---

## animation-fill-mode

Define qué estilos aplica la animación **fuera** de su duración activa.

| Valor | Efecto |
|-------|--------|
| `none` | Ningún estilo fuera del rango activo (valor por defecto) |
| `forwards` | Mantiene los estilos del keyframe final al terminar |
| `backwards` | Aplica estilos del keyframe inicial durante el delay |
| `both` | Combinación de forwards y backwards |

---

## animation-iteration-count

Número de veces que se repite la animación. Valores: número entero, decimal (`0.5` = mitad) o `infinite`.

---

## animation-play-state

`running` (activa) o `paused` (en pausa). Permite detener/reanudar animaciones desde JavaScript cambiando esta propiedad.

---

## Compositor-only property

Propiedad CSS que el navegador puede animar en el hilo del compositor sin afectar el layout ni el paint. Las propiedades compositor-only son `transform` y `opacity` — animar estas propiedades es significativamente más eficiente que animar `left`, `top`, `width` o `background-color`.

---

## cubic-bezier()

Función para definir una curva de easing personalizada con 4 parámetros: `cubic-bezier(x1, y1, x2, y2)`. Los puntos de control determinan la aceleración y desaceleración de la animación.

```css
/* Easing con rebote suave */
--ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
```

---

## ease / ease-in / ease-out / ease-in-out

Nombres de curvas de easing predefinidas:
- `ease`: lento → rápido → lento (valor por defecto)
- `ease-in`: empieza lento, termina rápido
- `ease-out`: empieza rápido, termina suave — **el más natural para la mayoría de UI**
- `ease-in-out`: simétrico, lento en ambos extremos

---

## fill-mode

→ Ver **animation-fill-mode**

---

## linear

Timing function que mantiene velocidad constante de inicio a fin. Útil para spinners y rotaciones continuas.

---

## perspective

Propiedad CSS que define la distancia del observador al plano Z=0 en el espacio 3D. Se aplica en el **elemento padre** para crear el efecto de profundidad. Valor típico: `400px`–`1200px`.

```css
.scene { perspective: 800px; }
```

---

## prefers-reduced-motion

Media query de accesibilidad que detecta si el usuario ha activado la preferencia de sistema "reducir movimiento". Uso obligatorio en cualquier interfaz con animaciones.

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## rotate()

Función de transform que rota un elemento sobre su punto de origen. Acepta `deg`, `rad`, `turn`. Positivo = sentido horario.

```css
.icono:hover { transform: rotate(45deg); }
.girar-vuelta { transform: rotate(1turn); }
```

---

## scale()

Función de transform que escala un elemento. `scale(1)` = tamaño original. `scale(1.1)` = 10% más grande. Acepta dos parámetros para ejes independientes: `scale(1.5, 0.8)`.

---

## skewX() / skewY()

Funciones de transform que inclinan un elemento sobre el eje X o Y, produciendo un efecto de sesgo/itálica. Acepta grados (`deg`).

---

## steps()

Timing function que produce una animación escalonada (sin interpolación suave). Útil para animaciones de sprites o efectos de contador.

```css
animation-timing-function: steps(4, jump-start);
```

---

## transform

Propiedad CSS que aplica transformaciones geométricas al elemento sin afectar el flujo del documento. Acepta múltiples funciones en secuencia (aplicadas de derecha a izquierda).

```css
.card:hover {
  transform: translateY(-4px) rotateY(-5deg);
}
```

---

## transform-origin

Define el punto de pivote desde el que ocurren las transformaciones. Por defecto: `center` (50% 50%). Puede ser `top left`, `bottom right` o valores personalizados.

```css
.aguja { transform-origin: bottom center; }
```

---

## transform-style: preserve-3d

Permite que los elementos hijos participen en el espacio 3D del padre en lugar de aplanarse. Necesario para efectos de volteo de tarjetas (card flip).

---

## translate()

Función de transform que mueve un elemento sin afectar el layout circundante. Equivale a un `position: relative` visual, pero procesado en el compositor sin reflow.

```css
.box { transform: translate(20px, -10px); }
```

---

## transition

Propiedad shorthand que anima el cambio de valor de una o más propiedades CSS. Requiere un estado inicial y un estado final explícitos (por ejemplo, via `:hover`).

```css
.btn {
  background: blue;
  transition: background 200ms ease-out;
}
.btn:hover { background: darkblue; }
```

---

## transition-timing-function

Sub-propiedad de `transition` que define la curva de aceleración/desaceleración: `ease`, `ease-out`, `ease-in-out`, `linear`, `cubic-bezier()`, `steps()`.

---

## translate — CSS property (Level 4)

Desde CSS Transforms Level 4 existe una propiedad independiente `translate: x y` separada de `transform`. Permite combinar con otras propiedades de transform individuales (`rotate`, `scale`) sin sobreescribirse.

```css
/* CSS Transforms Level 4 */
.elemento { translate: 0 -20px; }
```

# Exploraciones conceptuales y descartes · 02 Dos Realidades

Archivo cronológico de las hipótesis, sistemas alternativos y variaciones cromáticas que probaste o diseñaste en tus apuntes antes de consolidar *Existir como estructura vs. acontecimiento*.

---

## 1. De "partículas genéricas" a "consecuencia en el agua"

En los primeros borradores, el sistema B era descrito simplemente como *partículas que nacen donde cambia el brillo* (*"las partículas no son una persona"* / *"constelación / tejido orgánico → somos polvo"*).  
A partir de esa observación surgieron dos giros decisivos:
- **Metáfora del estanque de agua:** las ondas superficiales transmiten energía sin desplazar el agua de un lugar a otro. En vez de dibujar huesos, los nudillos, muñecas o coronilla podían caer como *"gotas de lluvia cayendo sobre la superficie de un estanque digital"*.
- **Cambio de paradigma en el movimiento:** dejar de pensar *"si me muevo, aparece un efecto de colores"* para pensarlo como ***"mi movimiento no es representado: deja una consecuencia"*** (*"no se demuestra el cuerpo; sino el trauma luminoso dejado en el espacio"*).

---

## 2. Camino explorado A · Contorno lento / huella acumulada

- **Idea en apuntes:** trabajar cámara lenta o rastro continuo donde, a medida que el cuerpo se mueve, su contorno anterior queda grabado como *"huella arqueológica de tinta suspendida"* en arcos que no desaparecen y van llenando el espacio.
- **Estado final:** esta idea de persistencia sobrevivió transformada dentro de la **Realidad 1 (MediaPipe)**: en lugar de contorno infinito, cada desplazamiento deja una silueta mineral/fósil que flota **20 segundos** antes de disolverse.

---

## 3. Camino explorado B · Sistema "Anti-cuerpo" (inversión espacial y cromática)

Uno de los desarrollos conceptuales más detallados en tus apuntes fue imaginar qué ocurre si el movimiento del cuerpo **se interpreta al contrario**:

> *"La cámara observa un cuerpo → MediaPipe extrae su movimiento → el sistema invierte ese movimiento → esa información genera otro objeto. No estás viendo al cuerpo. Estás viendo la reacción del otro objeto ante el cuerpo."*

- **Lógica espacial planteada:** invertir `antiMovement = -realMovement` (brazo arriba genera curva abajo; acercar la mano hace que la masa de 300 partículas huya en diagonal opuesta, ignorando el rostro).
- **Mapeo anatómico anotado:** `mano derecha` (nube de partículas), `codo derecho` (curvatura), `hombros` (ancho), `cadera` (centro de gravedad), `pies` (base).
- **Lógica cromática inversa:** `rojo → cian`, `azul → naranja`, `verde → magenta`, `amarillo → azul/violeta`.
- **Estado final en `Realidades/`:** aunque redactaste una especificación completa para Antigravity ([ver prompt en registro-antigravity.md](registro-antigravity.md)), el proyecto final mantuvo el foco en la oposición **Estructura persistente vs. Acontecimiento efímero**, por lo que *Anti-cuerpo* quedó como exploración conceptual documentada y no como módulo principal de `index.html`.

---

## 4. Camino explorado C · Inversión de proximidad ("mientras más cerca, más te borras")

- **Hipótesis crítica:** *"la ironía de la tecnología: acercarse es poseer, y entre más cerca estás de una cámara, más grande, invasivo y detallado te vuelves."*
- **Propuesta inversa:** medir la escala real entre hombros (`d_real`) para aplicar una caída exponencial inversa: al acercarse a `50 cm`, el tamaño virtual (`scale → 0`) y la opacidad (`alpha → 0`) colapsan en ruido disperso; al alejarse, el rostro vuelve a enfocarse.
- **Estado final:** en el código implementado (`script.js` y `README.md`), la adaptación por proximidad sí quedó presente en MediaPipe Pose (enfocar topografía facial de cerca vs. figura completa de lejos), pero sin colapsar a opacidad cero al acercarse.

---

## 5. Camino explorado D · Tres fases de perturbación en línea estable

1. **Fase 1 — Línea estable (Silencio):** usuario inmóvil → retícula geométrica o línea horizontal silenciosa.
2. **Fase 2 — Ondulación (Presencia y ritmo):** movimiento suave → ondas senoidales concéntricas rítmicas.
3. **Fase 3 — Deformación intensa (Caos):** movimientos bruscos → colisión constructiva/destructiva (*patrones de Moiré*) y fractura geométrica.

- **Continuidad con lo implementado:** la idea de progresión desde calma hasta fractura/intensidad y retorno al silencio derivó directamente en los **5 estados de transición** del Sistema B implementados en `script.js` (`cambio · corriente · expansión · intensidad · disipación`).

---

## 6. Camino explorado E · De "Filtro de Calma (Tinta en Agua)" a "Espejismo Espectral (RGB Split)"

En una iteración anterior solicitaste a Antigravity restringir la paleta del Sistema B a una estética monocroma serena (*"Filtro de Calma: Gaussian Blur + Efecto Tinta en Agua"* sobre fondo negro y una sola gama azul medianoche/aguamarina, **prohibiendo partículas duras**).

Posteriormente cambiaste esa restricción por una lectura física y cromática reactiva a **velocidad + dirección**, consolidada finalmente en **`acontecimiento.py` y `script.js`**:
- **Por velocidad:** lento/suave en cian y azul profundo (`hsl(195..205)`); brusco/acelerado rompe la tensión superficial generando ondas de choque en naranja ardiente, rojo y magenta.
- **Por dirección:** arriba → verde lima; abajo → violeta eléctrico; derecha → amarillo solar; izquierda → cian puro.
- **El Espejismo (RGB Split):** separación en 3 capas translúcidas (cálida adelantada, color direccional al centro, fría rezagada) que al superponerse dan luz blanca/dorada y se disipan en `< 1 segundo` al quedar inmóvil.

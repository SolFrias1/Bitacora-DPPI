# 02 · Existir como estructura vs. acontecimiento (`Ejercicio 03`)

- **Repositorio independiente:** [`SolFrias1/Realidades`](https://github.com/SolFrias1/Realidades)
- **Carpeta local de referencia:** `Ejercicios/Ejercicio03/dos-realidades-main/`
- **Créditos base verificados en el código:** Arquitectura inicial *Existir como estructura vs. existir como acontecimiento* de Felipe Roa R. (`README.md`), extendida e iterada en interfaz, textos y motor visual por Victoria Sol Frías.
- **Documentos detallados de este expediente:**
  - [Exploraciones conceptuales y variantes descartadas o transformadas](exploraciones-y-descartes.md)
  - [Registro de prompts, iteraciones de UI y programación en Antigravity](registro-antigravity.md)

---

## 1. Punto de partida e investigación comparativa (`MediaPipe` vs. `OpenCV`)

El ejercicio parte observando una sola escena frente a la webcam con dos sistemas de visión artificial distintos (`12 pares` iniciales / `duplas de interfaz` exploradas también en `demo-12-realidades.html`) para comparar **qué reconoce cada herramienta, qué modifica y qué deja fuera**:

### MediaPipe (Visión corporal / Estructura)
- **Cómo lee:** framework de alta abstracción que reconoce anatomía y esqueleto mediante *landmarks* corporales (y manos).
- **Fortalezas anotadas:** corre online sin descarga previa; permite combinar componentes de percepción de forma rápida (*"despiezar el cuerpo en coordenadas es comprenderlo"*).
- **Límite experimental anotado:** la velocidad extrema, la oclusión total y la ambigüedad espacial.

### OpenCV / Diferencia de cuadros (Acontecimiento / Píxel)
- **Cómo lee:** lectura por fotograma y procesamiento directo de píxeles / umbrales, con alta flexibilidad de filtros pero sin buscar siluetas humanas (*"opencv: la opacidad; huella fantasmal del cambio corporal"*).
- **Límite experimental anotado:** el caos ambiental y la iluminación; la lógica lineal de los píxeles no tolera cambios drásticos de contexto sin una programación matemática pesada detrás.

### Cruce de lenguajes (`Python` vs. `JavaScript`)
- **Python (`acontecimiento.py`):** elegido originalmente por su legibilidad y simplicidad; basado en sangrías estrictas; corre desde la terminal del PC.
- **JavaScript (`script.js`):** elegido para despliegue directo en navegador sin instalación, controlando el canvas y la interfaz visual mediante llaves `{}` y `;`, cargando MediaPipe con `import` dinámico dentro de `initPose` para que un fallo de CDN no rompa el Sistema B ni la cámara.

---

## 2. Evolución reflexiva sobre *percepción y exilio*

En `apuntes.docx` quedaron guardadas tres versiones sucesivas de la misma reflexión central —no como simple repetición, sino como decantación gradual desde el borrador crudo hacia el texto curatorial final de la web (`index.html`):

1. **Borrador 1 (tono visceral e inmediato):** preguntas directas sobre si la percepción es apenas lo que tu cerebro logra ver o un espacio limitado a tu verdad (*"el tonto es más feliz, el cuerdo aburrido, el intelectual está deprimido y el justiciero es egoísta en percepción"*). Aparecen aquí frases clave que sostienen todo el proyecto: ***"la verdadera potencia artística y crítica radica en lo que queda en el exilio perceptual"***, ***"la máquina no ve la fatiga"*** y los límites del cuerpo.
2. **Borrador 2 (desarrollo conceptual):** introduce la idea de que *toda representación exilia información*: coordenadas, líneas y ondas hablan de una persona, pero *"ninguna representación es aquello que representa"*. Cuando se crea un comando en una máquina, se establecen sus límites y se decide qué dejar afuera.
3. **Versión publicada en la web (`index.html`):** sintetiza los dos sistemas frente a la misma cámara (*"Nunca dejas de ser tú frente a la cámara; simplemente aparece una versión de ti que quizás todavía no habías conocido aún"*), reemplazando títulos neutros con tono irónico y directo.

---

## 3. De la exploración múltiple al resultado implementado

Antes de llegar a la versión final del estanque dual, exploraste al menos **cinco lógicas alternativas** detalladas en [exploraciones-y-descartes.md](exploraciones-y-descartes.md) (*gotas en estanque*, *contorno lento persistente*, *Anti-cuerpo invertido*, *inversión de proximidad*, *tres fases de interferencia* y *Filtro de Calma / tinta en agua*).

### Qué quedó efectivamente implementado en `Realidades/`
Al inspeccionar `index.html`, `style.css` y `script.js` (926 líneas):
- **Interfaz sarcástica e interruptor táctil:** título *¿Hay alguien aquí?* / subtítulos interactivos bajo la cámara con tono escéptico (*"Todavía no veo nada. Por ahora, literalmente no estamos viendo nada"*, *"Interpretando la escena… Dándole sentido a cosas que probablemente no lo necesitan"*), accionados mediante un botón interruptor tipo switch (`#cameraToggle`) y un fondo de estanque con ondas reactivas al mouse (`#mouseRippleCanvas`).
- **Realidad 1 — Existir como estructura (`canvasStructure`):** MediaPipe Pose + Hand Tracking (constelación articulada de torso + 21 hitos por mano con suavizado `LERP_FACTOR = 0.42`) que estampa **huellas fósiles** persistentes en el estanque durante **20 segundos** (`FOOTPRINT_LIFETIME = 20000`).
- **Realidad 2 — Existir como acontecimiento (`canvasEvent`):** lectura por diferencia de luminancia (`160×120`, `acontecimiento.py` y `script.js`) regida por cinco estados (`cambio`, `corriente`, `expansión`, `intensidad`, `disipación`) y el motor **Espejismo Espectral (RGB Split)** según velocidad y dirección del gesto, evaporándose en menos de 1 segundo en quietud.

> **[Espacio reservado para evidencias]**  
> - Capturas de pantalla comparando ambas ventanas del estanque en vivo (`Pose+Hands` a la izquierda vs. `Espejismo RGB` a la derecha).  
> - Captura de `demo-12-realidades.html` si formó parte de las pruebas intermedias previas a `index.html`.

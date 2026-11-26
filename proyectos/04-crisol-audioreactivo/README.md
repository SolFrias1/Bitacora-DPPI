# 04 · Crisol Audioreactivo — Piedad (`Ejercicio 05`)

- **Repositorio independiente:** [`SolFrias1/vela-audioreactiva`](https://github.com/SolFrias1/vela-audioreactiva)
- **Carpeta local de referencia:** `Ejercicios/Ejercicio05/vela-audioreactiva/` (más carpetas locales `Proceso/` y `media/`)
- **Formato final:** Reel vertical `9:16` en navegador (60 FPS) sincronizado con *Piedad* de Camila Moreno (álbum *Mala madre*, `2:57 min`).

---

## 1. Punto de partida y lectura lírica de *Piedad*

Antes de definir la visual de la vela o la programación de shaders, los apuntes parten desde el sentido emocional de la letra de *Piedad* (Camila Moreno):

- **La añoranza con peso físico:** *"La añoranza no es solo un vacío, tiene 'espacio' y tiene 'sonido'. Extrañar aquí no es estático; es una acústica que resulta pesada, un eco persistente que golpea al sujeto pidiendo clemencia ('Piedad'). El dolor de la ausencia se vuelve físico, un espacio habitado por el eco de lo que ya no está."*
- **Mandato familiar y catarsis:** *"El sujeto lírico alcanza una revelación, pero esta no ocurre en la iluminación pura, sino en la caída."* Desobedecer el mandato de "lo que se debe ver" para encontrarse con los despojos de la memoria familiar: una *"catarsis de la repugnancia"* donde sumergirse en esa corriente turbia hace que el asco se desvanezca *"porque ella se fue"*.

---

## 2. Exploraciones visuales y sonoras en apuntes

### Exploración A · La tipografía como percusión
En una primera línea gráfica (anotada junto a patrones rítmicos tipo `Bp4bp2bp3bp`) se consideró que el texto mismo fuese el cuerpo visual principal:
- **Idea inicial:** *"Las letras de la canción se convierten en el elemento principal. Las palabras se comprimen, se expanden o se descomponen según los golpes y la intensidad vocal. Ideal si quieres una pieza gráfica, tipográfica y contundente."*
- **Cómo evolucionó hacia la versión final:** no toda la letra ocupó la pantalla como sistema tipográfico principal, pero el concepto de **tipografía ligada al clímax vocal** sobrevivió concentrado en una sola palabra: **«PIEDAD»** (en fuente *Cinzel*), emergiendo y disolviéndose en el humo exactamente en los segundos `25.8` y `172.3` cuando la voz canta el verso.

### Exploración B · Lluvia de referentes sonoros y referencias técnicas
En los apuntes aparecen también imágenes sonoras iniciales previas o paralelas:
- `corazón palpitando -> disparos -> o cruce de personas caminando o mascota relaja`
- `campanadas iglesia` / `pájaros cucururucucu` / `truenos y rayos` / `café filtrándose?`
- Notas técnicas cortas asociadas al proceso de audio/edición: `Davinci resolve`, `audio reactividad -> simil a adobe photoshop` (trabajar por capas visuales que reaccionan a señales), y `LFO` (*Low Frequency Oscillator*).

---

## 3. Qué quedó implementado finalmente en el código (`vela-audioreactiva`)

Al cruzar los apuntes con el repositorio (`index.html`, `song_b64.js`, `candle_b64.js`, `README.md`) se verifica que el salto conceptual se consolidó en la metáfora de **una vela que se consume hasta extinguirse**:

- **WebGL (GLSL Shaders):** deformación líquida y ondas de calor (*heat shimmer*) por ruido fractal (*Value Noise*) + aberración cromática (*RGB channel split*) en cada golpe de bombo.
- **Web Audio API:** análisis espectral FFT en graves, medios y agudos con detección dinámica de transitorios (*Flux*) usando la canción precargada (`cancion_piedad.mp3` / `song_b64.js`).
- **Canvas 2D + Extinción:** chispas doradas, partículas de ceniza y colapso final hacia escala de grises cuando termina la canción.
- **Grabación y registro local:** el proyecto incorpora una grabadora integrada a 60 FPS y en tu disco se conservan evidencias completas del proceso (`Proceso/animation.mp4`, `Proceso/process.mp4`, capturas `frame_5s.jpg` a `frame_59s.jpg`, `preview_frame.jpg`, `vela_final_extincion_*.webm` y `reel.mp4`).

> **[Espacio reservado / enlace a evidencias]**  
> - En los apuntes `.docx` no quedaron pegados los prompts exactos utilizados para programar los shaders GLSL de la vela ni la transición desde *tipografía percusiva* hacia *vela en extinción*. Si deseas agregar esa iteración de prompts más adelante, conviene ubicarla aquí.  
> - Las exportaciones pesadas (`reel.mp4`, `completesong*.mp4`) se mantienen en disco local / Releases sin duplicarse en `Bitacora`.

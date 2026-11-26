# 05 · Oír la luz · Domesticadas (`Ejercicio 06`)

- **Repositorio independiente:** [`SolFrias1/Oir-la-luz-_Domesticadas`](https://github.com/SolFrias1/Oir-la-luz-_Domesticadas)
- **Demo publicada:** [`https://solfrias1.github.io/Oir-la-luz-_Domesticadas/`](https://solfrias1.github.io/Oir-la-luz-_Domesticadas/)
- **Carpeta local de referencia:** `Ejercicios/Ejercicio06/oir-la-luz-main/`

---

## 1. Investigación sobre escucha, acústica y cuerpo

El bloque de apuntes correspondiente a este ejercicio (`Tarea 6: sentidos` / `Diseño acusmático`) parte preguntándose **qué significa escuchar** más allá de recibir ruido:

- *"compañía / relación de espacio y sociedad / regulación de ánimo / mood // proceso auditivo de reflexión de memoria"*
- *"transporte de espacios a través de un sentido / generación de estímulos del cuerpo"*
- *"genera respuesta en el cuerpo humano, que no se puede regular / controlar"*
- *"el sonido conecta detalles de funcionamiento, cuando los sonidos activan detalles de correcto manejo o adentrarse en la activación de sentidos"*

### Notas de clase recopiladas sobre acústica física y fisiología
1. **Impacto fisiológico (campanas y corazón):** estudio de cómo frecuencias armónicas y vibraciones graves de campanas de bronce activan el sistema parasimpático, disminuyen frecuencia cardíaca, estabilizan el pulso y reducen cortisol.
2. **Escucha acusmática:** oír un sonido sin ver la fuente o la causa que lo produce, articulado en tres modos de escucha:
   - **Causal:** *¿Qué lo produjo?*
   - **Semántica:** *¿Qué significa?*
   - **Reducida:** *¿Cómo es?*
3. **Física de la onda sonora:**
   - Cadena: `Fuente -> Vibración -> Medio -> Receptor` (cuerda / voz → aire / agua → oído / micrófono).
   - **Frecuencia (Hertz):** rango audible humano `20 – 20.000 Hz` (*"qué tan junta está la curva"*).
   - **Amplitud (dB SPL):** escala `0` umbral → `30` habitación tranquila → `60` conversación → `85` tráfico intenso → `110` concierto → `130` umbral del dolor (*"qué tanto se altera en altura de onda"*).
   - **Refracción atmosférica día vs. noche:** de día el suelo caliente eleva las ondas hacia el cielo; de noche el aire frío y denso queda abajo y desvía las ondas pegadas al suelo a mayor distancia.

---

## 2. Primeras ideas de traducción visual → sonido (descartadas)

En los apuntes tempranos, la idea inicial usaba **OpenCV** para leer cuadros de escenas cotidianas humanas o animales y cruzarlas con sonidos metafóricos:
- *"el frame moviéndose dentro de los espacios activa sonido"*
- *"personas caminando activando sonidos de trabajo, de diseño"*
- *"autos pasando activando sonidos de animales corriendo"*
- *"migrantes en frontera activan sonidos de aves migratorias"*

Ninguna de estas tres escenas específicas (peatones, tráfico ni frontera) pasó a la implementación final, aunque sí conservó su núcleo conceptual: **que un cuerpo en movimiento en video active un sonido que lo contrapone críticamente en lugar de ilustrarlo literalmente.**

---

## 3. Salto hacia el proyecto final (*Domesticadas · La Ilusión de la Libertad*)

*Nota de trazabilidad:* en `apuntes.docx` no quedaron guardados los prompts o notas intermedias del momento exacto en que la idea giró hacia **el corral de gallinas (`granja.mp4`) + voces humanas (`gossipesp.wav`)**, aunque los archivos locales de trabajo (`scratch/gossipesp_44k.wav`, `scratch/piano_44k.wav`, `scratch/write_script.py`, `Audios/`, `videos/`) sí muestran ese taller técnico.

Lo verificado en el repositorio final (`index.html`, `script.js`, `style.css`, `README.md`):
- **Relación imagen–sonido:** en vez de cacareos, las gallinas confinadas hablan mediante chismes, susurros y confesiones en español (`gossipesp_track.wav` + `chisme_1..6.wav`), contrapuestas a murmullos fantasmales (`fantasma_1/2.wav`), acordes de piano (`piano_1/2.wav`) en la zona superior y un paisaje libre de grillos/aves (`naturaleza_loop.wav`) que se asfixia al aumentar la actividad.
- **Disparador visual y rol del usuario:** *frame differencing* a `128×72 px` en grilla panóptica (`10×6` por defecto). El cursor actúa como **ojo panóptico invasor** (`StereoPannerNode` + curva exponencial de volumen según cercanía).
- **Autocrítica documentada en el repo:** al basarse únicamente en variación de píxeles, el sistema es sordo ante la gallina quieta en una esquina del galpón y tampoco distingue intención biológica (huida vs. picoteo), proponiendo a futuro detección semántica (YOLO/MediaPipe) o síntesis granular (`AudioWorklet`).

> **[Espacio reservado para evidencias]**  
> - Capturas de la grilla panóptica `10×6` sobre `granja_web.mp4` y del visualizador acústico (`Ventana 09`).  
> - Prompts de Antigravity usados en el rediseño visual hacia la estética carcelaria/forense (`#0B0A09`, `#E5B25D`, `#D63D3D`, `IBM Plex Mono`) si quedaron en tu historial externo.

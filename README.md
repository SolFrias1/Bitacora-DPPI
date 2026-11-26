# Bitácora de Proceso · DPPI 2026

Archivo de procesos creativos, investigación, experimentación técnica, descartes, iteraciones con Antigravity y reflexiones de desarrollo detrás de siete proyectos realizados durante el curso *Dispositivos Periféricos y Plataformas para la Interacción Digital* (DPPI — Escuela de Diseño UDP, Santiago de Chile).

- **Autora:** Victoria Sol Frías  
- **Repositorio de destino:** [`SolFrias1/Bitacora`](https://github.com/SolFrias1/Bitacora)  
- **Fuente documental original:** `Ejercicios/apuntes/apuntes.docx` (conservado intacto fuera del repositorio) + repositorios y archivos locales de desarrollo.

---

## Cómo leer esta bitácora

Esta bitácora no reemplaza los `README.md` finales ni las demos publicadas de cada proyecto: registra **cómo se llegó hasta ellos**, incluyendo hipótesis iniciales, apuntes de clase, ideas que no funcionaron o cambiaron de rumbo, prompts reales trabajados en **Antigravity** y fricciones técnicas concretas.

Cada expediente distingue explícitamente entre:
1. **Propuesta y apuntes originales** (qué se pensó o investigó).
2. **Interacción con Antigravity / herramientas** (qué se pidió y qué problemas aparecieron).
3. **Implementación verificada** (qué quedó realmente construido en los archivos del proyecto).

---

## Índice de proyectos documentados (7)

> *Nota sobre el Ejercicio 01:* El primer ejercicio del semestre no generó apuntes escritos ni registro técnico local, por lo que esta bitácora cubre los 6 ejercicios con registro (`02` al `07`) más el desarrollo del **Portafolio Web** como cierre.

| # | Carpeta en Bitácora | Proyecto real | Repositorio / estado verificado | Núcleo del proceso |
|---|---|---|---|---|
| 01 | [01 · Meowmeow Cat Cam Meme Detector](proyectos/01-cat-cam-memes/README.md) | Ejercicio 02 · `Gatos-main` | Local sin remoto Git vinculado aquí (`gesture_meme.py` + `app.js`) | Prompts en Antigravity para agregar gestos desde `Gestos.txt` y resolver errores de cámara y caché en `localhost:8000`. |
| 02 | [02 · Existir como estructura vs. acontecimiento](proyectos/02-dos-realidades/README.md) | Ejercicio 03 · `Realidades` | [`SolFrias1/Realidades`](https://github.com/SolFrias1/Realidades) | MediaPipe vs. OpenCV, *exilio perceptual*, múltiples variantes conceptuales (*Gotas*, *Anti-cuerpo*, *Proximidad inversa*, *3 Fases*, *Filtro de Calma*) hasta llegar al *Espejismo Espectral (RGB Split)*. |
| 03 | [03 · Tiempo e imagen: Slit Scan](proyectos/03-slit-scan/README.md) | Ejercicio 04 · `slit-scan-master` | Local sin remoto Git vinculado aquí (`Three.js` 3D) | Notas sobre la 4ta dimensión temporal, contexto social en Chile y pauta de ensayo reflexivo. |
| 04 | [04 · Crisol Audioreactivo — Piedad](proyectos/04-crisol-audioreactivo/README.md) | Ejercicio 05 · `vela-audioreactiva` | [`SolFrias1/vela-audioreactiva`](https://github.com/SolFrias1/vela-audioreactiva) | Lectura emocional de *Piedad* (Camila Moreno), idea de tipografía como percusión y salto técnico hacia shaders WebGL + Web Audio FFT. |
| 05 | [05 · Oír la luz · Domesticadas](proyectos/05-domesticadas/README.md) | Ejercicio 06 · `Oir-la-luz-_Domesticadas` | [`SolFrias1/Oir-la-luz-_Domesticadas`](https://github.com/SolFrias1/Oir-la-luz-_Domesticadas) | Investigación sobre escucha acusmática, acústica física e ideas iniciales con OpenCV en vía pública antes del giro hacia el corral panóptico. |
| 06 | [06 · UMWELT · El Jardín de Frankenstein](proyectos/06-umwelt/README.md) | Ejercicio 07 · `tacto-polinizador` | [`SolFrias1/tacto-polinizador`](https://github.com/SolFrias1/tacto-polinizador) | Tacto activo/pasivo (Gibson), protocolo MQTT/EMQX, prototipo sonoro previo descartado (`audio_rats/`) y traducción móvil hacia la metáfora de abeja / Mary Shelley. |
| 07 | [07 · Portafolio Web](proyectos/07-portafolio-web/README.md) | Cierre del semestre | Portafolio personal multipágina + Halo Ring 3D | Arquitectura editorial por bandas cromáticas, adaptación de componente 3D sin React, iteraciones UI y ordenamiento para GitHub Pages. |

---

## Exploraciones transversales

Conceptos que reaparecen a lo largo de varios ejercicios del semestre y dialogan entre sí:

- [Percepción, representación y exilio de información](exploraciones-transversales/percepcion-y-representacion.md) *(Ejercicios 02, 03, 06, 07)*
- [Cuerpo, tactilidad y desplazamiento](exploraciones-transversales/cuerpo-tacto-y-movimiento.md) *(Ejercicios 02, 03, 07)*
- [Sonido, tiempo y traducción audiovisual](exploraciones-transversales/sonido-espacio-y-tiempo.md) *(Ejercicios 04, 05, 06, 07)*

---

## Recursos técnicos, notas de clase y pendientes

- [Herramientas, notas transversales de clase y apuntes sin proyecto asignado](recursos-y-referencias/herramientas-y-apuntes-clase.md) — Notas sobre `Python vs. JavaScript`, `Three.js`, `Blendshapes`, `DaVinci Resolve`, `Figma / Viscom / Supabase / Stripe / Ko-fi`, `LFO`, `APIKEY`, `MCP`, más referencias UX y lista explícita de brechas pendientes por documentar.

---

## Nota metodológica y estado de publicación

- No se inventaron fechas, métricas, capturas ni asociaciones entre notas que no estuvieran respaldadas por `apuntes.docx` o los archivos locales.
- Donde el salto entre un apunte temprano y el resultado final ocurrió fuera del documento de texto (por ejemplo, entre las primeras ideas de *Domesticadas* y su versión final de corral panóptico), queda señalado honestamente en cada ficha.
- Este repositorio está pensado para publicarse de forma independiente en `SolFrias1/Bitacora` sin modificar ni eliminar los repositorios originales de cada entrega.

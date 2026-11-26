# 01 · Meowmeow Cat Cam Meme Detector (`Ejercicio 02`)

- **Carpeta local de referencia:** `Ejercicios/Ejercicio02/Gatos-main/dppi-tarea-02/`
- **Estado Git:** Carpeta local sin `.git` vinculado en este respaldo *(pendiente verificar URL de repositorio en GitHub si fue publicado de forma independiente)*.
- **Documentos relacionados:** [Registro de prompts e incidencias en Antigravity](registro-antigravity.md)

---

## 1. Punto de partida

Este proyecto corresponde al segundo ejercicio de visión artificial del semestre (`dppi-tarea-02`): capturar la cámara web en tiempo real, leer gestos de rostro y manos mediante **MediaPipe** y **OpenCV**, y asociar cada gesto detectado a una imagen/meme de gato (`memes/`).

En el documento de apuntes (`apuntes.docx`) no quedaron registradas notas conceptuales previas para este ejercicio; el material conservado corresponde directamente a **la secuencia de instrucciones enviadas a Antigravity**, la tabla de gestos (`Gestos.txt`) y los archivos implementados.

---

## 2. Desarrollo técnico verificado

Al revisar la carpeta local se verifica una implementación dual (escritorio + navegador):

- **Versión escritorio (`gesture_meme.py`):** usa `OpenCV` + `MediaPipe Tasks Python` (archivos en `models/`), mostrando lado a lado la cámara con landmarks / HUD de depuración (`Gesto`, `Pitch`, `Mouth Open`, `Yaw`) y la imagen del meme correspondiente. Incluye el archivo auxiliar `flow_debug_log.csv` y lanzador `Launch Gesture Meme.command`.
- **Versión web (`index.html` + `app.js`):** corre en el navegador mediante `@mediapipe/tasks-vision` WASM sin instalación previa, servida vía HTTP local (`Iniciar Servidor Web.command`, `python3 -m http.server 8000`).
- **Definición de gestos (`Gestos.txt`):**

| Orden / Idea en `Gestos.txt` | Archivo fuente en `Gestos.txt` | Identificador implementado en `README.md` |
|---|---|---|
| Orejas de gato con los dedos (dos manos arriba de la cabeza, índice y medio abajo) | `1.OrejaDeGato` | `orejaGato` (`1.Oreja de gato.jpeg`) |
| Cabeza hacia abajo | `2.MirarHaciaAbajo` | `mirarAbajo` (`2.MirarHaciaAbajo.jpeg`, `Pitch < -13°`) |
| Sacar la lengua | `3.Lengua` | `lengua` (`3.Lengua.jpeg`, `Mouth Open > 0.24`) |
| Inclinar cabeza hacia atrás | `4.CabezaHaciaAtras` | `cabezaAtras` (`4.CabezaHaciaAtras.jpeg`, `Pitch > +13°`) |
| Levantar brazos y echar hacia atrás | `5.BrazosHaciaAtras` | `brazosAtras` (`5.Brazos hacia atras.jpeg`) |
| Cruzar brazos a la altura del pecho | `6.Shocked` | `shocked` (`6.Shocked.jpeg`) |
| Cara duda, índice estirado tocando el lado de la cabeza | `7.Duda` | `duda` (`7.Duda.jpeg`) |
| Dedos pistola (índice y medio juntos arriba, pulgar al lado) | `8.-Pistola` | `pistola` (`8.Pistola.jpeg`) |

---

## 3. Fricciones técnicas y aprendizajes

Durante el traspaso desde una versión anterior de memes hacia los gestos de gatos surgieron dos problemas típicos de entorno local (ver detalle en [registro-antigravity.md](registro-antigravity.md)):

1. **Caché o carpeta anterior en `localhost:8000`:** el servidor web seguía leyendo la carpeta previa (`memes/`) en lugar de incorporar las imágenes nuevas provenientes de `Gatitoactualizado/`.
2. **Conflicto de acceso exclusivo a la cámara:** intentar correr la terminal (`gesture_meme.py`) al mismo tiempo que el navegador o sin permisos liberados bloqueaba la apertura de la webcam.

> **[Espacio reservado para evidencias]**  
> - Captura de pantalla de la vista doble en navegador (`localhost:8000`) mostrando el HUD de métricas y un gesto detectado.  
> - Captura o video breve probando `Launch Gesture Meme.command` en escritorio.  
> - Enlace al repositorio en GitHub de este ejercicio si se encuentra publicado.

---

## 4. Qué quedó documentado vs. pendiente

- **Verificado en código:** `Gestos.txt`, `Gatitoactualizado/`, `memes/`, `models/`, `gesture_meme.py`, `app.js`, `index.html`, `README.md` y carpeta `Video/` local.
- **No presente en apuntes:** reflexiones personales escritas sobre el resultado o evaluación crítica del funcionamiento de los umbrales (`Pitch` / `Mouth Open`) en uso real.

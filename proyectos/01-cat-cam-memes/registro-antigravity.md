# Registro de Antigravity · 01 Cat Cam Memes

Registro textual de los 3 pasos solicitados a **Antigravity** para adaptar el proyecto base a la nueva colección de gestos felinos (`Gestos.txt` + `Gatitoactualizado/`).

---

## Iteración 1 · Comprensión previa del proyecto

### Lo que solicité
```text
1.- Necesito que comprendas en detalle el funcionamiento del proyecto al interior de la carpeta y para validarlo necesito que expliques en detalle su funcionamiento y cada una de sus partes
```

### Propósito y decisión metodológica
Antes de alterar el código, le pedí que mapeara qué archivo hacía qué (Python escritorio vs. MediaPipe web) para no romper un proyecto ajeno o previo al entenderlo mal.

---

## Iteración 2 · Integración de nuevos gestos e imágenes (con validación previa)

### Lo que solicité
```text
2.-Necesito que implementes cambios en el repo:

Agregues nuevos gestos e imagenes, descritas en el archivo "gestos.txt" y las imagenes estan en la carpeta "Gatitoactualizado"

Haz todos los cambios pertinentes para que el repo pueda funcionar bajo la nueva estructura.

Antes de hacer cambios, asegurate de comprender los gestos para mediapipe, antes de ejecutar algo, dame la listado de cosas a hacer, para estar seguro de lo que vas a cambiar
```

### Propósito y resultado verificado
- **Estrategia de control:** exigir explícitamente *"dame la lista de cosas a hacer, para estar seguro de lo que vas a cambiar"* antes de ejecutar ediciones.
- **Resultado verificado en los archivos:** `gesture_meme.py` y `app.js` implementaron los 8 gestos en orden de prioridad (`orejaGato`, `brazosAtras`, `shocked`, `duda`, `pistola`, `lengua`, `cabezaAtras`, `mirarAbajo`) y las imágenes pasaron a `memes/` manteniéndose `Gatitoactualizado/` y `Gestos.txt` como referencia.

---

## Iteración 3 · Depuración de servidor local y bloqueo de cámara

### Problema que apareció y lo que solicité
```text
3.- hay un error, no me esta leyendo bien, localhost : 8000 sigue leyendo la carpeta anterior "memes" , y la terminal esta intendo abrir la camara y no puede, puedes solucionar?
```

### Lectura técnica del error
- Se superpusieron la prueba web (`localhost:8000`) con el script Python desde terminal (`gesture_meme.py`), compitiendo por el mismo dispositivo de cámara o manteniendo caché/rutas previas de `memes/`.
- **Estado final en disco:** existen dos lanzadores separados para macOS (`Iniciar Servidor Web.command` para la versión navegador y `Launch Gesture Meme.command` para la versión Python) más `flow_debug_log.csv` de pruebas de ejecución.

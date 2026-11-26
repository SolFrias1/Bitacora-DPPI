# Herramientas, notas de clase y pendientes por clasificar

Compilado de apuntes técnicos transversales presentes en `Ejercicios/apuntes/apuntes.docx` que no estaban asignados de forma explícita a un único ejercicio, junto con las dudas o vacíos detectados durante la inspección.

---

## 1. Comparativas de lenguajes y herramientas anotadas en clase

### Python vs. JavaScript (contexto *Dos Realidades* / DPPI)
- **Python:** anotado por su legibilidad y simplicidad; basado en sangrías / indentación estricta; ejecución directa en la terminal del PC (`gesture_meme.py`, `acontecimiento.py`).
- **JavaScript:** enfocado al desarrollo web y control de interfaz visual en tiempo real; lectura basada en llaves `{}` y `;`; permite publicar y ejecutar vía navegador (*deploy*) sin instalación local.

### Librerías, plataformas y términos técnicos mencionados
- **`Three.js`:** código abierto en JavaScript para animación 3D en navegador *(usado luego en Slit Scan `r128` y en el Halo Ring Hero `r170` del Portafolio)*.
- **OpenCV / MediaPipe en web:** anotación sobre delegar la recolección ligera de datos para no sobrecargar el navegador ni hacer caer la página.
- **`Blendshapes`:** nota breve sobre animación facial / deformación paramétrica *(sin proyecto implementado con blendshapes en este respaldo)*.
- **`DaVinci Resolve`:** referencia breve en el entorno de apuntes previos a video / edición.
- **`sketchdesign` (`sketchdesign.club?`):** anotación exploratoria de herramientas de boceto/UI.
- **Ecosistema backend/pagos (`Figma`, `Viscom`, `Supabase`, `Stripe`, `PayPal`, `Ko-fi`, `COCloud`):** apuntes explicativos de arquitectura comercial/apps (*"Stripe es el motor invisible"*, *"Ko-fi es la página bonita que ve el cliente"*, *"Supabase como backend para usuarios/fotos/contraseñas"*). *(No utilizados en los 7 proyectos de DPPI; corresponden probablemente a explicaciones de clases/consultas generales).*
- **Conceptos técnicos sueltos anotados:** `LFO`, `APIKEY`, `MCP`, `CLAUDE`, `deploy`.
- **Referentes UX de cierre / Portafolio:** `awwwards.com`, `uso de parallax scrolling`, *"qué se entiende en los primeros 5 segundos"*, *"grilla"*.

---

## 2. Registro transparente de notas pendientes o saltos no documentados

Al contrastar `apuntes.docx` contra el código final en `Ejercicios/`, quedaron identificados explícitamente estos puntos donde falta documentación intermedia o verificación externa:

1. **Ejercicio 01:** no tuvo apuntes escritos en `apuntes.docx` ni carpeta en `Ejercicios/`.
2. **Ejercicio 02 (`Cat Cam Memes`) y Ejercicio 04 (`Slit Scan`):** faltan verificar URLs de repositorios propios en GitHub (si fueron publicados bajo `SolFrias1/`) y falta el texto reflexivo de 400–600 palabras de *Slit Scan* si se redactó en otro documento.
3. **Ejercicio 05 (`Crisol`) y Ejercicio 06 (`Domesticadas`):** `apuntes.docx` conserva muy bien el punto de partida emocional/acústico, pero no conserva los prompts exactos de Antigravity que guiaron el paso hacia la vela GLSL ni hacia la estética del corral panóptico.
4. **Ejercicio 07 (`UMWELT`):** en `PRUEBA_1.md` quedó pendiente llenar la tabla con las mediciones reales obtenidas en iPhone/Android (presión, diámetro en px, latencia en ms).
5. **Perfil remoto en GitHub (`SolFrias1`):** al realizarse esta inspección en entorno sin acceso web, queda pendiente verificar en GitHub Desktop / navegador que los 7 repositorios cuenten con `About`, `Topics`, `GitHub Pages` activos y el README de perfil actualizado.

# 07 · Portafolio Web (`Cierre del semestre`)

- **Carpeta local:** `Ejercicios/portafolio/` (repositorio independiente para GitHub Pages)
- **Documentos relacionados:** [Iteraciones de diseño, Antigravity y gestión de carpetas](registro-antigravity.md)

---

## 1. Punto de partida en `apuntes.docx`: ¿qué se entiende en los primeros 5 segundos?

En el tramo final de tus apuntes aparece el planteamiento editorial del portafolio no solo como requisito técnico, sino como problema de comunicación visual:

- **Checklist base recopilado:** `about me` (quién soy, qué me interesa, dónde he trabajado), subpáginas por proyecto (nombre, descripción, repo, GitHub Pages, video), al menos dos proyectos de otros ramos/talleres, conceptos (`html`, `css`, `java`, `mqtt`) y reflexión de aprendizajes/desafíos/créditos sin redacción automática de IA.
- **Preguntas de diseño anotadas durante la planificación:**
  - *¿Qué se entiende en los primeros 5 segundos?*
  - *¿Por qué hay prioridades? / Grilla / ¿Qué se mueve, cuándo y cómo?*
  - *¿Cómo funciona la lista de proyectos?*
  - *¿Qué se muestra primero y cómo? / ¿El valor dónde está?*
  - *Buscar referentes y sacar provecho* (`awwwards.com`, `uso de parallax scrolling`, `2xA Studio`, `21st.dev`, `Aceternity UI`).
- **Frase rectora original:**  
  > *"Diseño desde la exploración; construyendo experiencias, objetos e interfaces que conectan visual, espacial y por fin... lo interactivo."*

---

## 2. Arquitectura y dirección visual implementada

A partir de ese diagnóstico se organizó una arquitectura estática multipágina sin frameworks (`index.html`, `about.html`, `work/index.html` y 7 fichas individuales) bajo una identidad visual unificada:

1. **Hero 3D (`Halo Ring Hero` adaptado sin React):** anillo cilíndrico en Three.js con 16 obras reales, odómetro `000% → 100%`, inmersión de cámara y arrastre manual, conectado por la palabra **`PORTAFOLIO`** surgiendo desde el borde inferior (`1/8` sumergido dentro del celeste de *About Me*).
2. **Narrativa cromática por disciplina:** Celeste (`#A4BCD4` · *About Me*), Café oscuro (`#1D120E` · *Interacción DPPI*), Verde oliva (`#7D7642` · *Indumentaria*), Burdeo (`#490B0C` · *Industrial*), Papel cálido (`#F4EFEB` · *Reflexión*) y Negro (`#1D120E` · *Contacto*).
3. **Tipografías propias y libres:** emparejamiento de **Galgo Condensed** (`@bojjoe`, Open Source) con **Cormorant Garamond Italic**, junto a **Unique** (*Commercial Use Allowed*) e **IBM Plex**. *(Se descartó explícitamente `Branch.otf` por tener licencia solo de uso personal).*
4. **Cruce físico + digital (7 proyectos finales):** los 4 ejercicios DPPI (`T07 UMWELT`, `T06 Domesticadas`, `T03 Dos Realidades`, `T05 Crisol Audioreactivo`) junto a `BIVALVIA`, `Vestido Yara` y `Taller Local · Mobiliario Postmob`.

---

## 3. Reflexión sobre el proceso de armado

Como sintetizaste en tu propia reflexión final del portafolio: más que juntar piezas terminadas, armar este archivo permitió reconocer intereses que se repiten entre el trabajo con telas, madera/acero, pintura y programación creativa —y decidir activamente qué proyectos dejar dentro (7), qué materiales visuales requerían un cuaderno técnico propio (fichas de indumentaria) y qué proyecto descartar por criterio estético.

> **[Espacio reservado para captura final]**  
> - Capturas del portafolio ya publicado en vivo en GitHub Pages (vista escritorio y vista teléfono).

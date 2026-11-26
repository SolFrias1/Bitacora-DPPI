# Iteraciones de diseño, Antigravity y repositorio · 07 Portafolio Web

Registro cronológico de decisiones, cambios solicitados a **Antigravity**, correcciones visuales e incidencias de repositorio que ocurrieron durante la construcción del portafolio (`Ejercicios/portafolio/`).

---

## 1. Evolución de la portada e identidad (`Hero` y bandas cromáticas)

| Iteración | Qué propusiste / observaste | Cambio técnico aplicado |
|---|---|---|
| **Órbita inicial → Halo Ring 3D** | Tras probar una órbita flotante con subtítulo "Portafolio", pediste integrar el código de [`Halo Ring Hero`](https://21st.dev/@kedhareswer/components/halo-ring-hero) manteniendo tu gráfica propia y palabras clave alrededor. | Se portó el componente de React/TypeScript a módulo ES vanilla con Three.js (`js/halo-hero.js`), reemplazando tarjetas de demo por imágenes reales de tus obras. |
| **Deslizamiento de `PORTAFOLIO`** | Al principio no se distinguía la palabra "Portafolio" o tapaba elementos. Pediste que emergiera desde abajo hacia arriba manteniendo `1/8` sumergido en el celeste de *About Me*, y con los links inferiores bien pegados a la orilla izquierda. | Posicionamiento de `.hrh-portafolio-rise` (`bottom: -0.11em`, revelado sincronizado en la fase de zoom del Hero) y ajuste de `.hrh-head` (`max-width: 240px`) sin choque. |
| **Color continuo y zoom lento** | Pediste más color por sección en vez de solo círculos flotantes, transición lenta de `1 segundo` al cambiar foto por su imagen de detalle al pasar el cursor, y números verticales ordenados semi-transparentes. | Bandas cromáticas completas (`band-about`, `band-ppi`, `band-indumentaria`, `band-industrial`, `band-reflection`), `.detail-swap-img` con transición `1000ms` (`delay 240ms`) y `.project-big-index` semi-transparente. |
| **Tipografía mixta Galgo + Serif itálica** | Compartiste una muestra tipográfica (`CONVERSAR Y colaborar`) y pediste aplicar esa combinación a los nombres de los proyectos y subpáginas. | Títulos renderizados mediante `titleHtml` (`Galgo` mayúscula + `<em>` en *Cormorant Garamond* itálica de acento). |

---

## 2. Depuración visual y criterios de curaduría

- **Franja blanca superior en el landing:** un `header.site-header` heredaba `position: sticky` de `base.css`, reservando `60px` arriba antes del Hero `100svh`. Se corrigió pasándolo a `position: fixed` oculto hasta superar el `72%` de scroll del Hero.
- **Animación de ingreso en *About Me*:** notaste que todas las imágenes subían al entrar menos el retrato de *About Me*; se aplicó `data-clip-reveal` a `.about-portrait-frame` y `.signature-corner-row` (en el contenedor interno para no chocar con el `transform` de `data-parallax`).
- **Eliminación de avisos de "video pendiente":** en `T07 UMWELT`, `T06 Domesticadas` y `T03 Dos Realidades` se retiraron las cajas provisionales de video faltante, dejando limpio el botón directo a la experiencia/repositorio.
- **Cuaderno abierto para indumentaria:** en `BIVALVIA` y `Vestido Yara` transformaste la lectura pesada de fichas en un **libro abierto de dos páginas lado a lado** (`data-tech-book`) donde deslizar el scroll vertical encima avanza/retrocede pliegos; en *Yara* se amplió verticalmente (`.book-tall`) al incorporar `yara-datayara1.png`, `yara-datayara2.png` y las láminas curatoriales/storytelling (`10` láminas en `5` pliegos).
- **Composición de *Taller Local*:** ordenaste la galería `taller-local-grid` dejando la foto vertical de curvatura a la izquierda (`span 2`) y apilando detalle de madera + geometría lateral a la derecha.
- **Descarte explícito de proyectos:**
  - *Ejercicio 04 (`Slit Scan`):* excluido del portafolio por decisión propia (conservado solo en repositorio/bitácora).
  - *Lab. Clínico Medicina Nuclear Bicentenario:* inicialmente incluido, luego eliminado por no convencerte visualmente frente al resto de las obras; se ajustaron tarjetas (16), métricas (`7 Proyectos / 3 Disciplinas`) y paginador circular.

---

## 3. Fricciones técnicas de Git, carpetas y despliegue

1. **Carpeta duplicada y peso para GitHub:** los respaldos (`Ejercicios/`, PDF original y videos pesados) compartían raíz con los archivos web. Se movieron las fuentes crudas a `_recursos_originales/` excluidas en `.gitignore`, dejando la raíz limpia en `Ejercicios/portafolio/` (~13.5 MB publicables).
2. **Error en GitHub Desktop ("no parece un repositorio Git"):** al no existir `.git/` ni al renombrar `Copia de Ejercicios` → `Ejercicios`, GitHub Desktop perdía rutas locales (caso `tacto-polinizador` → solucionado con *Locate...*; caso `portafolio` → solucionado ejecutando `git init -b main` y verificando `58` archivos limpios antes de `Commit` + `Publish`).
3. **Verificación automática:** en las iteraciones se detectaron y corrigieron llaves desbalanceadas tras ediciones rápidas (`js/subpages.js` y `css/landing.css`) comprobando el 100% de rutas locales (`203` referencias) antes de publicar.

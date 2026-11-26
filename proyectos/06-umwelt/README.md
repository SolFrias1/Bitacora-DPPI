# 06 · UMWELT · El Jardín de Frankenstein (`Ejercicio 07`)

- **Repositorio independiente:** [`SolFrias1/tacto-polinizador`](https://github.com/SolFrias1/tacto-polinizador)
- **Demo publicada:** [`https://solfrias1.github.io/tacto-polinizador/exp.html`](https://solfrias1.github.io/tacto-polinizador/exp.html)
- **Carpeta local de referencia:** `Ejercicios/Ejercicio07/tacto-main/` (incluyendo `PRUEBA_1.md`, `audio_rats/` y `audio_bee/`)
- **Documento técnico asociado:** [Arquitectura MQTT, matriz de traducción y registro de `PRUEBA_1.md`](registro-tecnico-y-pruebas.md)

---

## 1. Investigación en clase (`5/11/26`): Tacto, receptores y pérdida de control

El punto de partida nace desde las notas de clase sobre el sentido del tacto (**James J. Gibson**: *"tocar es moverse"*):

- **Tacto activo vs. pasivo:** en el tacto activo el cerebro sabe qué está pasando y dónde de antemano (*yo toco*); en el tacto pasivo el estímulo viene desde afuera (*algo me toca*).
- **Sistemas sensoriales ligados:** Tacto → Termocepción → Nocicepción (dolor/daño) → Propiocepción (dónde están las cosas), casi siempre apoyados por la vista (*"no ver lo que estamos haciendo → quita un factor de seguridad → control"*).
- **Mecanorreceptores de la piel:**
  - *Merkel:* textura (rugoso o liso).
  - *Meissner:* desplazamiento.
  - *Ruffini:* estiramiento de la piel.
  - *Pacini:* vibración (requiere un estímulo más fuerte).
- **Gestos de la mano:** deslizar (textura), sostener (peso), presionar (dureza), desplazamiento (forma), apoyar quieto (temperatura).
- **Qué puede medir realmente un teléfono:** posición (`x, y`), diámetro (`d`), presión (`f`, si el hardware la entrega), velocidad, cantidad de dedos y giro/inclinación (`gyro`). De ahí surge la tensión central: ***"no hay tacto a distancia"*** / ***"concepto: la proximidad destruye la percepción"***.

---

## 2. Exploraciones previas descartadas (evidencia verificada en apuntes y disco)

Antes de llegar al jardín y la abeja, en `apuntes.docx` quedaron documentadas dos rutas previas que se exploraron y luego se descartaron:

### Descarte A · "Acariciar recuerdos / desgastar la propia existencia"
- Idea de usar el teléfono como tacto para *"acariciar recuerdos"* y desgastar visualmente la propia imagen hasta eliminar el audio (*"que descubrir / qué sentidos necesitas"*).

### Descarte B · "Gato y ratas ciegas en alcantarillado" (`audio_rats/`)
- **Concepto anotado:** *"jugar con oscuridad y pérdida de visión — rats sin vista, buscando recuperarla — ruidos corriendo — teléfono como ratón — un gato en alcantarillado lleno de ratas mutantes — el celular es la pata, limpia un poco la vista con movimiento de limpiaparabrisas frente a los ojos, pero poco, buscar en la oscuridad los sonidos."*
- **Evidencia material verificada en disco:** esta iteración **llegó a producir audios propios**, conservados todavía en `Ejercicios/Ejercicio07/tacto-main/audio_rats/`:
  - `burla.wav`
  - `caida.wav`
  - `run.mp3`
  - `tantanTAAN.wav`
- **Decisión posterior:** se abandonó el escenario de oscuridad/alcantarillado para trasladar exactamente la misma problemática (*intentar habitar una percepción ajena sin poder ver como ella*) a un terreno opuesto en apariencia: la luz abierta de un prado floral vista desde la imposibilidad de ser abeja.

---

## 3. Giro definitivo: *El Jardín de Frankenstein* (`Umwelt` + Mary Shelley)

La pregunta que articula toda la etapa final cruza a **Jakob von Uexküll** (*Umwelt*, burbuja perceptual de cada especie) con **Mary Shelley** (*Frankenstein*):

> *"¿Podemos generar vida a partir de gestos si no comprendemos realmente cómo funciona aquello que intentamos imitar?"*  
> *"¿Qué pasa si intentamos florecer y polinizar un campo… pero no sabemos cómo es ser abeja?"*

### Tesis de diseño en tus apuntes
- *"La persona siente una intención, pero la máquina solo ve datos."*
- *"Entre la intención humana y la interpretación tecnológica siempre existe una pérdida."*
- **Distorsión deliberada:** tocar una zona hace aparecer la flor desplazada; acercarse dispersa el polen en vez de fecundar; inclinar el teléfono desorienta las partículas; usar varios dedos hace competir o agruparse las flores; **mantener demasiado tiempo o fuerza termina asfixiando lo que intentabas cuidar** (*"Lo divertido es que la persona podría terminar perjudicando aquello que intenta ayudar a crear"*).
- **Misión implícita y clímax autónomo:** al alcanzar el `80%` de floración colectiva en el código implementado (`exp.js`), el prado entra en fase autónoma en tonos ultravioleta y el enjambre ignora los dedos: la criatura técnica escapa del control humano.

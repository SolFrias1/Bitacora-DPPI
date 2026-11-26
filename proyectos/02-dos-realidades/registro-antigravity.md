# Registro de Antigravity · 02 Dos Realidades

Prompts reales, modificaciones de interfaz e iteraciones técnicas registradas en `apuntes.docx` junto con la verificación de lo implementado en `Realidades/`.

---

## 1. Prompts principales enviados a Antigravity

### Prompt A · Degradación por proximidad y ruido visual
```text
Degradación de la representación (Antigravity):
A medida que el cuerpo se acerca y la representación se aleja, puedes programar que pierda conexiones (líneas de la malla), reduzca su densidad de puntos y aumente el "ruido visual" (efecto partículas o desvanecimiento).
```
- **Estado:** explorado conceptualmente; la versión final optó por adaptar el encuadre de proximidad de la malla Pose manteniendo su legibilidad.

### Prompt B · Módulo interactivo "Anti-cuerpo" (`SISTEMA C`)
```text
Crea un módulo interactivo en JavaScript y HTML para mi proyecto web que implemente un "anti-cuerpo" visual basado en MediaPipe Pose (ignorando la cabeza). Requisitos específicos:
1. Inversión espacial total: Toma las coordenadas de las muñecas y codos e invierte tanto el eje X como el eje Y (canvasWidth - x, canvasHeight - y) para que la entidad huya del usuario en diagonal opuesta.
2. Sistema de partículas de repulsión: Genera una nube de 300 partículas que actúen como un campo de fuerza que se aparta dinámicamente cuando el usuario se acerca.
3. Ausencia de rostro y estética abstracta: No dibujes ningún esqueleto humano ni figura; solo muestra la nube de partículas abstractas cambiando de color a su opuesto cromático complementario en tiempo real.
```
Complementado en tus apuntes con las reglas detalladas de `SISTEMA C — ANTI-CUERPO` (`antiMovement = -realMovement`, interpolación con inercia, inversión cromática `rojo → cian`, `verde → magenta`, `azul → naranja` y *fade-out* sin persona).
- **Estado:** quedó como especificación documental/descarte frente a la línea elegida de dos realidades en el estanque (*Estructura* vs. *Acontecimiento*).

### Prompt C · Reprogramación del Sistema B hacia flujo líquido con calma
```text
Por favor, reprograma la Realidad 2 (OpenCV / Flujo Líquido) para que el movimiento de los píxeles no genere un caos de partículas, sino una corriente fluida y elegante regida por estas reglas:
1. Reducción de Ruido (Filtro de Calma): Gaussian Blur antes de calcular diferencias de fotogramas.
2. Inercia y Disipación (Efecto Tinta en Agua): fuerzas de empuje con viscosidad alta y disolución exponencial hacia la oscuridad.
3. Restricción Estética: fondo negro y una sola gama azul/aguamarina; prohíbe partículas duras o puntos sueltos.
4. Comportamiento en Reposo: calma total hasta que el estanque quede estático.
```
- **Resultado evolutivo:** esta instrucción fue la transición clave que eliminó el ruido de partículas dispersas heredado del prototipo inicial (`script.js`) y abrió paso al motor definitivo **Espejismo Espectral** (estelas continuas de flujo, ondas elípticas de choque y separación RGB por velocidad/dirección, con retorno a quietud en `< 1s`).

---

## 2. Rediseño de interfaz, tono y copys (`Edicion` en apuntes vs. `index.html`)

En `apuntes.docx` queda explícita la transformación del tono técnico frío inicial hacia una voz escéptica e irónica:

| Elemento | Versión inicial en apuntes | Cambio solicitado | Estado verificado en `index.html` |
|---|---|---|---|
| **Título / Subtítulo** | *"Dos realidades, todas las realidades"* / descripción neutra | *"¿Hay alguien aquí? Nuevas realidades, porque una sola no era suficiente..."* | En `index.html`: título *"Existir como estructura vs. existir como acontecimiento"* + subtítulo *"¿Qué ocurre cuando una máquina recuerda tu forma, mientras otra solo recuerda tus cambios?"* |
| **Estados bajo cámara** | *"La cámara aún no está activa / solicitando acceso / Listo"* | Reescritura sarcástica: *"Todavía no veo nada..."*, *"Interpretando la escena… Dándole sentido a cosas que probablemente no lo necesitan"*, *"No podemos conocerte aún… La tecnología también tiene límites. Qué decepción."* | Implementado en `index.html` (`statusMsg`: *"Todavía no veo nada. Por ahora, literalmente no estamos viendo nada."*) y textos dinámicos equivalentes. |
| **Control principal** | Botón estándar de encendido | *"Un botón táctil → un interruptor que enciende y apaga a comando, un toque lo prende, un toque lo vuelve a apagar"* | Implementado en `#cameraToggle` (`tactile-switch` con `switch-thumb` y `switch-led`). |
| **Disposición visual** | 2 paneles / intento de 4 círculos | *"las realidades: 2 paneles/recuadros cambiados a 4 círculos"* + *"Fondo estanque de agua"* | Fondo de estanque implementado (`.pond-background` + `#mouseRippleCanvas`), mientras el escenario principal mantuvo **2 paneles amplios contrapuestos** (`.dual-stage`). *(Además existe `demo-12-realidades.html` como prueba de múltiples módulos).* |

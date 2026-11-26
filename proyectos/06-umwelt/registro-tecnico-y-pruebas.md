# Registro técnico y pruebas · 06 UMWELT

Documentación de la arquitectura **MQTT**, decisiones de red entre servidor local vs. nube y matriz de traducción física implementada en `Ejercicios/Ejercicio07/tacto-main/`.

---

## 1. Arquitectura MQTT (Emisor → Broker → Experiencia)

A partir de los apuntes sobre telemetría (*"Vocero / Comunicación / Dealer"*):

```text
📱 Teléfono (Safari / Chrome) ──┐
                                 ├──→ 🖥️ BROKER MQTT (EMQX WSS :8084)
💻 Experiencia Web (exp.html) ───┘
```

### Decisiones técnicas registradas en apuntes y código
- **Seguridad y servidor (`apuntes.docx`):** nota explícita sobre `EMQX` (*"private → caro → se envía a USA"*, *"usar otra clave → security first"*, *"limitar permisos"*).
- **Solución implementada (`public/tacto.js` y `README.md`):** conexión mediante WebSocket seguro (`wss`) con salas dinámicas generadas por código aleatorio (`tacto/<sala>/<dispositivo>/touch` y `motion` a ~60 Hz).

---

## 2. Desafíos reales con teléfonos físicos (`PRUEBA_1.md`)

En el repositorio se conserva el protocolo `PRUEBA_1.md` diseñado para comprobar en **iPhone y Android** aspectos que no se pueden simular desde el computador:

1. **Presión vs. Diámetro:** muchos teléfonos iOS entregan presión *sin dato* o *constante*; por eso el sistema decidió utilizar **`touch.d` (diámetro del dedo en px)** como sustituto de la fuerza para activar necrosis y alerta.
2. **Certificados autofirmados en Safari (iPhone):** en servidor local (`node server.js` en `https://localhost:8443/exp`), Safari móvil suele bloquear WebSockets autofirmados; por esa limitación el despliegue móvil definitivo pasó a **GitHub Pages + broker público WSS**.
3. **Latencia de red:** el RTT real en Wi‑Fi/hotspot (~40–180 ms) dejó de tratarse como un fallo a ocultar y se asumió conceptualmente como *"desfase de polen"* entre el cuerpo humano y el sistema.

> **[Espacio reservado para resultados de prueba]**  
> En `PRUEBA_1.md`, la tabla inferior (`Resultados: una fila por teléfono`) quedó vacía sin los valores anotados por dispositivo (`Conexión`, `Presión`, `Diámetro`, `Dedos máx.`, `Giro`, `Latencia`, `Pantalla bloqueada`, `Mic/Cámara`). Si conservas esos registros de prueba en terreno, conviene traspasarlos aquí.

---

## 3. Mapeo implementado: de la idea en apuntes a `exp.js` / `audio_bee/`

| Gesto en teléfono | Idea anotada en `apuntes.docx` | Implementación verificada (`README.md` / `exp.js`) |
|---|---|---|
| **Tocar la pantalla** | Germina flor, pero activa zumbido desproporcionado | `touch.down` → dispara `audio.palpito` y semillas en coordenadas desplazadas |
| **Deslizar** | Transporta polen generando corriente sonora multiplicada | Velocidad (`dPos/dt`) → modula `audio.abeja`; fricción lenta/rígida (`< 0.08`) → `audio.mala_abeja` |
| **Inclinar teléfono** | Altera afinación y ritmo del ecosistema | Giroscopio (`ang.g` / `ang.b`) → vuelo FPV 3D (`-40°..+40°`, `-25°..+25°`) |
| **Varios dedos / Pinza** | Superposición de insectos, vibraciones y competencia | Pinza (`touch.dist`) → zoom inmersión macro al espectro UV; `>= 3 dedos` → `audio.robot` |
| **Mantener presión** | Satura el entorno y perjudica lo que se intenta cuidar | Tiempo `> 1.8s` → `audio.maquina`; diámetro `> 78px` → `flor.necrosis` + `alarma.wav` |
| **Soltar la pantalla** | *(añadido en diseño sonoro)* | `touch.down == 0` → `audio.pago` (corte metálico transaccional) |

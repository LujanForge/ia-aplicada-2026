# Plantilla: clasificación de incidente v1
# Variables: {ROL_LECTOR}, {CATEGORIAS}, {SEVERIDADES}, {EJEMPLO_ENTRADA}, {EJEMPLO_SALIDA}, {ENTRADA}

> ⚠️ BORRADOR: esta versión parte del prompt de la iteración 4 (rol + contexto + formato + ejemplo).
> Cuando tengas tus puntajes, ajústala a la iteración que decidas adoptar y llena los [corchetes] de "Instrucciones de uso".

```
Eres analista de seguridad de primer nivel en un centro de operaciones de seguridad (SOC). Tu lector es {ROL_LECTOR}.

Contexto: el texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: {CATEGORIAS}. Las severidades posibles son: {SEVERIDADES}.

Responde únicamente con esta tabla en Markdown, sin texto adicional:

| Campo | Valor |
|---|---|
| Tipo de incidente | |
| Severidad | |
| Activo afectado | |
| Primera acción recomendada | |
| Información faltante | |

Si un campo no puede determinarse a partir del texto, escribe "NO ESPECIFICADO" en Valor y explica qué falta en la fila "Información faltante".

Ejemplo de entrada:
{EJEMPLO_ENTRADA}

Ejemplo de salida:
{EJEMPLO_SALIDA}

Texto a clasificar:
{ENTRADA}
```

## Instrucciones de uso

| Variable | Qué poner | Valor probado en el laboratorio |
|---|---|---|
| {ROL_LECTOR} | Quién va a leer la clasificación | un técnico que atenderá el incidente y necesita información precisa |
| {CATEGORIAS} | Lista cerrada de tipos de incidente, separados por coma | acceso no autorizado, phishing, malware, pérdida de dispositivo, otro |
| {SEVERIDADES} | Lista cerrada de severidades | baja, media, alta |
| {EJEMPLO_ENTRADA} | Un reporte de ejemplo escrito por una persona del equipo (no generado por IA), distinto a los casos reales | caso de phishing por correo falso de RH (ver guía) |
| {EJEMPLO_SALIDA} | La tabla correcta para ese ejemplo, llenada a mano | tabla del ejemplo de RH |
| {ENTRADA} | El texto tal cual lo escribió el usuario, sin corregirlo | — |

- **Modelo probado:** [ej. ChatGPT, versión ___ , fecha ___]
- **Puntaje obtenido:** [__ / 18 con las 3 entradas · entrada de robustez: __ / 6]
- **Limitaciones conocidas:**
  - Si el ejemplo se parece mucho al caso real, el modelo puede copiarlo (revisar que el tipo de incidente tenga sentido).
  - La severidad la decide el modelo; un técnico debe validarla antes de actuar.
  - [agrega lo que observes en tus pruebas, ej. cómo manejó la entrada ambigua]

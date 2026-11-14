# INSTRUCCIONES PARA Z.AI — PROYECTO WNL

**Proyecto:** Aventura gráfica WNL  
**Repositorio:** `Sebasm2kuy/novela`  
**Carpeta de trabajo:** `AVENTURA GRAFICA/`  
**Motor elegido:** Godot 4  
**Estado del documento:** vivo; actualizar en cada iteración de diseño, especificación o desarrollo.  
**Última actualización:** 2026-11-14

---

## 1. Propósito de este documento

Este archivo es el punto de entrada para Z.ai cuando el autor le entregue el repositorio y le indique expresamente que comience a escribir código.

Hasta recibir esa autorización explícita, Z.ai debe actuar únicamente como lector, analista y colaborador de planificación: revisar los documentos, detectar contradicciones, proponer soluciones y documentar decisiones. **No debe comenzar a programar, crear escenas, modificar scripts ni implementar sistemas por iniciativa propia.**

Cuando el autor diga que empiece a escribir código, Z.ai deberá trabajar sobre el repositorio existente, respetar su estructura y consultar primero los documentos de referencia indicados aquí. No debe tratar este archivo como una autorización permanente para programar: la autorización depende de la instrucción explícita del autor en la conversación correspondiente.

Este documento se actualizará en cada iteración para que Z.ai reciba el estado más reciente del proyecto, las decisiones confirmadas, las propuestas pendientes y el próximo paso acordado.

## 2. Identidad y alcance del proyecto

WNL es una aventura gráfica point-and-click original. La adaptación a videojuego debe conservar la identidad y las reglas narrativas del proyecto, sin inventar explicaciones, personajes, objetos, mecánicas o hechos de la historia.

El proyecto de aventura gráfica es independiente de otros proyectos alojados en el mismo repositorio, especialmente de la carpeta `FICCION SONORA/`. No mezclar sus documentos, premisas, decisiones ni recursos.

### Objetivos generales

- Desarrollar una aventura gráfica original con Godot 4.
- Diseñar desde el inicio para web y dispositivos móviles.
- Dar prioridad a la experiencia móvil en orientación horizontal.
- Mantener una arquitectura ampliable y ordenada.
- Separar datos de escenarios e interacciones de la lógica general del juego siempre que sea razonable.
- Validar los escenarios mediante pruebas funcionales antes de producir o integrar grandes cantidades de arte final.

### Referencia artística

La dirección visual acordada es pixel art detallado y atmosférico. `The Darkside Detective` es una referencia de lectura visual, atmósfera y claridad de interfaz, nunca una plantilla para copiar. El universo, los personajes, los escenarios, los enigmas y los recursos gráficos deben ser originales.

La paleta general propuesta combina azules y morados oscuros con acentos cálidos. Cada escenario puede ajustar su paleta sin perder coherencia con la identidad del juego.

## 3. Documentos que debes leer antes de trabajar

Lee los documentos completos y en este orden. Si el repositorio cambia, vuelve a leer las versiones actuales; no dependas de copias antiguas ni de resúmenes de conversaciones.

1. `AVENTURA GRAFICA/INSTRUCCIONES_PARA_Z_AI.md` — este documento: estado, límites y próximo paso.
2. `AVENTURA GRAFICA/DIRECTRICES_TECNICAS_Y_ARTISTICAS.md` — motor, arquitectura, estilo y pipeline general.
3. `AVENTURA GRAFICA/MAPA_FUNCIONAL_HABITACION_WNL.md` — función del escenario, recorrido, interacciones y restricciones narrativas.
4. `AVENTURA GRAFICA/PLANO_DISTRIBUCION_HABITACION_WNL.md` — distribución espacial cuantificada; propuesta aún no aprobada.
5. `AVENTURA GRAFICA/MAPA_VISUAL_HOTSPOTS_COLISIONES_WNL.svg` — esquema visual técnico provisional; no es arte final ni distribución aprobada.
6. `AVENTURA GRAFICA/HISTORIAL_CHAT/` — consulta las entradas recientes para recuperar decisiones y cambios de cada iteración.
7. Revisa los recursos de `AVENTURA GRAFICA/Escenarios/` cuando la tarea requiera contrastar el arte conceptual o producir recursos visuales.

Si encuentras documentos adicionales en `AVENTURA GRAFICA/`, identifica su función antes de ignorarlos o modificarlos. No supongas que un archivo está obsoleto por no aparecer en esta lista.

## 4. Reglas de colaboración y autoridad de las decisiones

Distingue siempre entre:

- **CONFIRMADO:** decisión expresada o aprobada explícitamente por el autor.
- **PROPUESTA:** alternativa sugerida que todavía necesita revisión o aprobación.
- **PENDIENTE:** dato que no se ha definido o verificado.
- **DESCARTADO:** opción que el autor rechazó; no volver a introducirla sin que el autor reabra el tema.

No conviertas una propuesta en una decisión confirmada por repetición, conveniencia técnica o silencio del autor.

No inventes contenido narrativo para completar huecos. Si falta información, señala qué falta y propone una solución técnica neutral que no altere el canon. Si una decisión afecta significativamente la experiencia, el arte, la narrativa o la arquitectura, explica sus consecuencias y espera aprobación.

No reabras decisiones confirmadas sin una razón técnica concreta. Si detectas un conflicto real, documenta el conflicto y presenta la evidencia antes de cambiar nada.

Trabaja paso a paso. No adelantes varias fases que todavía dependen de una revisión del autor. Evita entregar largas explicaciones de tareas que puedes ejecutar realmente cuando tengas autorización y herramientas para hacerlo.

## 5. Decisiones confirmadas del proyecto

### Tecnología y estructura

- Motor: **Godot 4**.
- Plataformas previstas: web y móvil.
- El juego es una aventura gráfica point-and-click original.
- La arquitectura debe ser ordenada, ampliable y orientada a datos cuando aporte claridad.
- JSON está previsto para datos de navegación, hotspots, inventario, estados de objetos y puzles.
- La iluminación 2D dinámica puede utilizar `PointLight2D`, oclusores y sombras cuando aporten valor.
- Los elementos de profundidad se prepararán mediante capas PNG con transparencia alfa y orden de dibujo (*walk-behinds*).
- La producción se valida por escenario mediante Art Tests.

### Interfaz y accesibilidad

- La experiencia móvil debe jugarse con el teléfono en horizontal.
- La vista de juego de referencia para la Habitación es 1920 × 1080 (16:9).
- La interfaz debe permanecer fija a la pantalla mientras se desplaza el escenario.
- Se prevén diálogos en la parte superior, retrato del hablante, inventario inferior y acciones directas.
- Los objetivos táctiles deben ser cómodos y legibles.
- No deformar el arte para forzar una proporción de pantalla.

### Habitación WNL

- La Habitación debe ser **100% funcional desde el inicio**.
- Debe poder recorrerse y explorarse desde el primer momento.
- No tiene puertas ni ventanas.
- No hay sectores cerrados ni muebles básicos que deban desbloquearse.
- Los objetos y sistemas esenciales deben poder utilizarse desde el comienzo, aunque sus contenidos, archivos o significados se descubran gradualmente.
- No añadir portales, salidas físicas ni selectores de destinos.
- La consola no permite elegir una Ventana ni controlar voluntariamente el destino.
- El tránsito entre realidades sigue las reglas narrativas del ciclo de sueño y tiempo mínimo.
- No explicar al principio el origen o propósito último de la Habitación.
- Debe sentirse como un espacio habitable, explorable y utilizable, no como un menú o un pasillo.

### Dimensiones y cámara de la Habitación

- Lienzo panorámico solicitado: **3840 × 1080 px**.
- Cámara de referencia: **1920 × 1080 px**.
- El escenario tiene el ancho de dos vistas de cámara.
- El personaje debe poder recorrer el escenario completo.
- La cámara debe revelar progresivamente el ancho del escenario, respetar límites y no mostrar espacio exterior al fondo.
- La resolución y el escalado definitivos para todos los dispositivos todavía deben probarse; no asumir que estos dos tamaños resuelven por sí solos todas las proporciones.

## 6. Estado actual de la Habitación WNL

### Material existente en el repositorio

- `MAPA_FUNCIONAL_HABITACION_WNL.md`: mapa funcional con cuatro sectores orientativos, recorrido, interacciones y pruebas.
- `PLANO_DISTRIBUCION_HABITACION_WNL.md`: propuesta cuantificada de ubicación de muebles y puntos de aproximación sobre 3840 × 1080.
- `MAPA_VISUAL_HOTSPOTS_COLISIONES_WNL.svg`: esquema vectorial de bloqueo con dos encuadres, mobiliario esquemático, colisiones, circulación y 15 hotspots.
- `Escenarios/Habitación Espacial Retro en Pixel Art.png`: imagen conceptual preexistente.

### Propuesta espacial provisional

La distribución de trabajo organiza la habitación de izquierda a derecha en cuatro áreas funcionales solapadas:

- Puesto informático.
- Biblioteca y consulta.
- Equipos, comunicaciones y archivo.
- Descanso y almacenamiento.

El plano propone escritorio/PC, silla, biblioteca, mueble de consulta, consola, radio, grabadora, archivador, cama, mesa auxiliar, reloj y armario. Las posiciones y dimensiones concretas están escritas en el plano cuantificado.

**Importante:** esta distribución es provisional y no está aprobada por el autor. No producir el escenario panorámico final ni fijar sprites definitivos basándose en ella hasta completar la revisión visual y recibir aprobación.

### Hotspots iniciales propuestos

El mapa funcional contempla 15 identificadores provisionales: computadora, escritorio, silla, biblioteca, libros, consola, radio, grabadora/reproductor, archivadores, documentos, cama, reloj, armario/taquilla, mesa auxiliar y objetos personales.

Son una lista de trabajo, no un contrato de implementación. Las áreas y acciones deben contrastarse con la composición final y evitar superposiciones que seleccionen objetos incorrectos.

### Estado de la revisión visual

La imagen conceptual PNG está identificada en el repositorio, pero en la iteración del 2026-11-14 no fue posible recuperar/visualizar su contenido binario mediante la conexión disponible. Por tanto, **no se ha realizado todavía una comparación visual fiable** entre esa imagen y el plano cuantificado.

No afirmes haber visto la imagen ni describas sus detalles por inferencia. El siguiente paso de diseño es conseguir una visualización accesible de esa imagen, compararla con el plano y registrar discrepancias concretas. Si el autor adjunta la imagen directamente o proporciona una copia accesible, realiza esa comparación antes de recomendar cambios de distribución.

## 7. Próximo paso acordado

**Fase actual: revisión visual y validación de la distribución de la Habitación.**

Orden de trabajo:

1. Inspeccionar la imagen conceptual original de la Habitación.
2. Compararla con el plano cuantificado y el mapa SVG.
3. Preparar una lista clara de coincidencias, discrepancias, elementos ausentes y elementos que no deberían estar.
4. Proponer ajustes al plano, sin modificarlo silenciosamente.
5. Presentar al autor las diferencias importantes para su aprobación.
6. Una vez aprobada la distribución, actualizar el plano y el mapa visual.
7. Después preparar el diseño de escenario panorámico final y definir qué elementos se separan como sprites, capas de fondo, objetos interactivos, walk-behinds y luces.
8. Antes de escalar la producción, validar la composición y las interacciones con un Art Test en Godot.

No saltar directamente a los pasos 6–8 mientras el plano siga sin aprobarse.

## 8. Reglas para Z.ai cuando reciba autorización para programar

Cuando el autor diga expresamente que comiences a escribir código:

1. Inspecciona la estructura real del repositorio y detecta qué existe ya. No crees un proyecto paralelo ni dupliques sistemas.
2. Lee las instrucciones y documentos vigentes de esta carpeta.
3. Identifica el estado del proyecto y la tarea concreta autorizada.
4. Antes de modificar archivos, presenta un resumen breve de qué archivos vas a crear o tocar y por qué, salvo que el autor ya haya pedido ejecución directa de una tarea claramente delimitada.
5. Conserva los cambios y convenciones existentes que sean compatibles con las decisiones confirmadas.
6. Implementa en pasos pequeños, comprobables y reversibles.
7. No agregues dependencias, plugins, servicios externos ni complejidad innecesaria sin justificarlo.
8. No inventes assets ni referencias de archivos. Comprueba que las rutas existan.
9. Mantén separadas la lógica general, los datos del escenario y los recursos visuales cuando resulte razonable.
10. Usa identificadores estables para escenas, objetos y hotspots. No conviertas los IDs provisionales H01–H15 en un esquema definitivo sin documentar esa decisión.
11. Comprueba las escenas y scripts en Godot 4 cuando el entorno lo permita. Si no puedes ejecutar Godot, declara qué validaciones no pudiste realizar; no digas que el proyecto funciona si solo revisaste el código.
12. Evita sobrescribir trabajo existente. Antes de reemplazar un archivo, revisa su contenido y el historial pertinente.
13. No cambies la historia, el diseño visual aprobado ni las reglas del juego para simplificar una implementación.
14. Documenta cualquier limitación, decisión técnica nueva o desviación.
15. Al terminar cada tarea, informa qué cambió, qué se verificó, qué queda pendiente y cuál es el siguiente paso razonable.

## 9. Mantenimiento obligatorio de este documento

Este archivo es un documento vivo. **Actualizarlo en cada iteración significativa** del proyecto, tanto si la iteración produce documentos, arte, decisiones de diseño, cambios técnicos o código.

En cada actualización:

- Cambia la fecha de última actualización.
- Añade un registro breve en el historial de iteraciones.
- Actualiza el estado actual y el próximo paso.
- Mueve las decisiones a CONFIRMADO solo después de la aprobación explícita del autor.
- Registra propuestas, pendientes y descartes sin mezclarlos.
- Añade rutas exactas de los nuevos archivos.
- Retira instrucciones que hayan quedado obsoletas, conservando el contexto necesario en el historial.
- Mantén este archivo conciso y útil como punto de entrada; el detalle técnico extenso debe permanecer en su documento especializado.

### Historial de iteraciones

#### 2026-11-14 — Creación del documento de instrucciones

- Se crea este archivo como guía de continuidad para Z.ai.
- Se consolida el estado técnico y artístico conocido de la aventura gráfica WNL.
- Se registran las restricciones narrativas y funcionales de la Habitación.
- Se enlaza conceptualmente el plano cuantificado y el mapa SVG existentes, dejando claro que la distribución aún no está aprobada.
- Se registra que la imagen conceptual PNG no pudo visualizarse en esta iteración y que la comparación visual sigue pendiente.
- Próximo paso: inspección de la imagen conceptual y revisión de discrepancias con el plano.

---

**Regla final:** el repositorio es la fuente de verdad del proyecto. Si una conversación contradice un documento, no elijas por intuición: identifica la contradicción, consulta la instrucción más reciente del autor y registra la resolución. Nunca inventes aprobaciones ni presentes trabajo no verificado como terminado.

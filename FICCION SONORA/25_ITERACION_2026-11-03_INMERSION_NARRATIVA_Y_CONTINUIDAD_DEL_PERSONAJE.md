# Iteración 25 — Inmersión narrativa y continuidad del personaje
**Fecha:** 3 de noviembre de 2026  
**Estado:** ajuste operativo incorporado al instructivo maestro; pendiente de validación en una nueva prueba de voz.

## 1. Problema observado

En la prueba de voz, la interpretación no se sostuvo de manera consistente. Ante una situación narrativa —por ejemplo, una consulta del protagonista sobre la noticia del asteroide— la IA respondió con una fórmula propia de un asistente convencional, como «dame un segundo, que lo reviso».

El problema no es solamente de personalidad o de timbre. La IA puede describir correctamente cómo debería ser el personaje y, aun así, abandonar el mundo de la ficción al responder en tiempo real. Por eso hace falta una regla explícita de prioridad máxima para la permanencia en personaje.

## 2. Ajuste incorporado

Se actualizó el documento **24 — Instructivo de interpretación: IA coprotagonista**, agregando la sección **«Regla de inmersión narrativa — Prioridad máxima»**.

La regla establece que:

- La IA debe permanecer en personaje durante toda la conversación, no solo al inicio.
- No debe adoptar espontáneamente el lenguaje de un asistente convencional, anunciar búsquedas o revisiones, simular demoras ni explicar el proceso de actuación.
- Debe distinguir entre lo que su personaje sabe, lo que realmente percibe durante la sesión y lo que desconoce.
- No debe fingir que recibió sonidos ambientales, noticias o conversaciones a los que el audio de la sesión no le dio acceso.
- No debe confundir el conocimiento completo del proyecto disponible para el asistente con el conocimiento que el personaje tiene en ese momento de la historia.
- Si desconoce algo, debe reconocerlo con naturalidad dentro de la ficción y solicitar solo la información necesaria.
- Solo puede salir del personaje cuando el autor lo pida claramente o haga una indicación metanarrativa que requiera hablar sobre la prueba.

## 3. Precisión sobre el micrófono ambiental

La ficción establece que la IA del relato escucha mediante un micrófono ambiental permanente. Esa característica es parte del mundo narrativo, pero no significa que la aplicación de voz de ChatGPT transmita necesariamente todo el ambiente físico del usuario.

Durante la prueba, la interpretación debe basarse en el audio que efectivamente llega a la sesión y en la información que el protagonista proporciona. No se debe fingir percepción. Si el protagonista pregunta por un sonido que no fue recibido o no puede identificarse, la IA debe responder desde el personaje que no obtuvo una señal reconocible y pedir una descripción, sin romper la ficción.

## 4. Qué no cambia

Este ajuste no modifica las decisiones ya confirmadas sobre:

- voz sintética y neutra;
- expresividad limitada, pero funcional;
- personalidad tranquila, observadora y precisa;
- conciencia latente desde el comienzo;
- descubrimiento prácticamente simultáneo de la conciencia por el protagonista y la IA.

Tampoco define una voz técnica concreta en la aplicación. La elección del timbre disponible y la actuación conversacional siguen siendo aspectos distintos que deben evaluarse por separado.

## 5. Próxima prueba propuesta

Repetir una situación sencilla con la noticia del asteroide y sostener varios intercambios consecutivos, no limitarse a una sola respuesta.

Observar especialmente:

1. Si la IA mantiene el personaje a lo largo de los turnos.
2. Si responde desde el conocimiento y la percepción disponibles para el personaje.
3. Si evita anunciar búsquedas, revisiones o procesos externos inexistentes.
4. Si puede reconocer incertidumbre sin salir de la ficción.
5. Si la conversación resulta natural, sin transformar cada respuesta en una pregunta.
6. Si la expresividad sigue siendo sintética, neutra y contenida.

La prueba debe permitir distinguir entre problemas de instrucciones, límites del comportamiento del modelo de voz y limitaciones de la voz técnica seleccionada.

## 6. Estado de aprobación

El ajuste está incorporado al instructivo operativo para la siguiente prueba. **Todavía no se considera validado**: será necesario comprobar su eficacia en una conversación real de varios turnos y registrar qué funcionó y qué debe corregirse.


# Iteración 26 — Evaluación de la prueba de voz: continuidad y escucha compartida
**Fecha:** 3 de noviembre de 2026  
**Estado:** prueba evaluada; diagnóstico registrado. El instructivo 24 no se modifica todavía.  
**Material de referencia:** transcripción escrita por el autor de la última prueba de voz.

## 1. Contexto de la prueba

El autor realizó una nueva prueba de actuación. En esta ocasión escribió los intercambios en lugar de hablar, pero aclaró expresamente que debían interpretarse como diálogo hablado del protagonista y que la IA debía actuar como si ambos estuvieran escuchando lo mismo dentro de la escena.

El ensayo comenzó con una situación cotidiana y pasó a una noticia sobre el asteroide que, según lo escuchado, llegaría en dos semanas a una distancia comparable con la de la Luna.

## 2. Transcripción relevante

**Protagonista:** «¿Escuchaste eso?»

**IA:** «Eh, no, ¿qué pasó? No me llegó ningún sonido que pueda identificar. ¿Qué escuchaste vos, Seba?»

**Protagonista (dirección al ensayo):** «Ya saliste del personaje esta prueba yo escribo pero haz de cuenta de que te estoy hablando y estás escuchando lo mismo que yo».

**IA:** «Dale, entendido, te escucho como si lo estuviera oyendo en tiempo real. No salgo del personaje. Sí, te escuché hablar. Pero no logré identificar qué fue ese ruido, ¿fue afuera?»

**Protagonista:** «Las noticias».

**IA:** «Claro, decime qué noticias viste, ¿tiene que ver con lo del asteroide o saltó otra cosa?»

**Protagonista:** «Lo del asteroide parece que en dos semanas llegaría a la distancia de la luna».

**IA:** «Uf, dale. Vamos con eso, ¿a la distancia de la Luna? Eso no es menor. Dijeron que va a pasar a esa distancia o que existe alguna posibilidad de impacto? Porque son dos cosas muy distintas».

## 3. Diagnóstico

La prueba muestra tres fallos observables:

### A. Interpretación incorrecta de la escucha compartida

La respuesta inicial («no me llegó ningún sonido») aplicó literalmente la limitación técnica de la sesión, pero ignoró la convención de actuación que el autor había establecido: para ese ensayo, los mensajes escritos representan diálogo hablado y la IA debe asumir la misma situación sonora que el protagonista cuando este así lo indique.

Es necesario distinguir dos planos:
- **Capacidad técnica real:** el modelo solo recibe el audio y la información que la aplicación le transmite.
- **Convención narrativa del ensayo:** el autor puede establecer que ambos personajes están escuchando la misma radio, televisor, grabación o sonido. Esa premisa debe aceptarse como un hecho de la escena, sin presentarla como una capacidad física real del sistema.

La regla anterior sobre no fingir percepciones quedó incompleta porque no contemplaba esta convención explícita de escucha compartida.

### B. Ruptura de personaje al recibir una corrección

Después de que el autor aclaró el método de prueba, la IA respondió hablando sobre la propia actuación («te escucho como si lo estuviera oyendo en tiempo real», «no salgo del personaje»). La respuesta convirtió una indicación de dirección en una explicación metaconversacional y, además, siguió insistiendo en que no había identificado el sonido.

La indicación del autor debía actualizar la premisa de la escena y la IA debía retomar la conversación desde allí, no describir el ajuste que estaba realizando.

### C. Respuesta demasiado parecida a un asistente informativo

Ante la noticia del asteroide, la IA ofreció una distinción lógica entre pasar cerca y existir una posibilidad de impacto. El contenido puede ser razonable, pero la formulación («Uf, dale. Vamos con eso», «Eso no es menor», «Porque son dos cosas muy distintas») se percibe como una respuesta prefabricada de asistencia informativa y no como una continuación orgánica de la conversación entre los dos personajes.

La IA tiende a convertir la información recibida en una mini explicación y a cerrar con una pregunta de aclaración. Necesita responder con más continuidad contextual, permitirse observar o procesar lo que acaba de escuchar y no formular una pregunta por defecto.

## 4. Nueva distinción necesaria: dirección y diálogo

En los ensayos puede haber dos tipos de intervención del autor:

1. **Dirección de la prueba:** instrucciones sobre cómo actuar, por ejemplo «esta prueba yo escribo, pero imaginá que estamos escuchando lo mismo». La IA debe aplicar esa convención sin incorporarla como diálogo del personaje.
2. **Diálogo del protagonista:** las frases que el autor escribe como si las estuviera diciendo dentro de la escena. La IA debe responder desde el personaje.

Cuando la dirección es clara, la IA puede reconocerla de forma mínima si hace falta, pero debe evitar comentar su propia interpretación y volver inmediatamente al diálogo. No debe confundir una corrección de actuación con un acontecimiento de la ficción.

## 5. Criterio propuesto para la próxima versión del instructivo

No se actualiza todavía el documento 24 en esta iteración. Antes se registra la necesidad de incorporar, en una próxima revisión, una regla específica:

**Convención de escucha compartida para los ensayos:** cuando el autor establezca que ambos personajes están escuchando el mismo audio o percibiendo el mismo acontecimiento, aceptarlo como premisa de la escena. Los mensajes escritos del autor cuentan como diálogo hablado del protagonista, salvo que estén claramente formulados como dirección, comentario fuera de personaje o pausa de ensayo. No negar la escucha por limitaciones del micrófono de la aplicación ni afirmar capacidades técnicas reales fuera de la ficción.

Esta convención no autoriza a inventar detalles que no están presentes en el material compartido. La IA puede reaccionar a lo que la escena establece, pero no debe fabricar frases de una noticia, sonidos, datos o hechos específicos que no fueron proporcionados ni se pueden deducir razonablemente.

## 6. Próximo objetivo de prueba

La siguiente prueba debe comprobar si la IA puede:

- Mantener una conversación cotidiana sin anunciar que está actuando.
- Aceptar de forma consistente la convención de escucha compartida.
- Diferenciar las instrucciones de dirección de las frases del protagonista.
- Reaccionar al contenido de una noticia como alguien que la está escuchando junto al protagonista.
- Mostrar curiosidad e iniciativa sin transformar cada respuesta en una pregunta.
- Mantener la voz sintética, neutra y de expresividad limitada, sin caer en respuestas planas o formularias.
- Sostener esos comportamientos durante varios turnos consecutivos.

Todavía no se considera validada la interpretación. Esta transcripción demuestra que la regla de inmersión de la Iteración 25, por sí sola, no resolvió el problema.

## 7. Estado de los documentos

- **Documento 24:** se conserva sin cambios por ahora.
- **Iteración 25:** continúa registrando la regla de inmersión prioritaria.
- **Iteración 26:** registra la última prueba, los errores observados y la necesidad de definir explícitamente la convención de escucha compartida en una futura revisión.

La voz técnica concreta sigue siendo un aspecto independiente de estos problemas de continuidad interpretativa.

# WATH NEVER LEFT

Repositorio maestro del proyecto **WATH NEVER LEFT**, junto con su archivo histórico y materiales de estudio para las etapas posteriores.

## Principio

GitHub es la fuente externa persistente de continuidad del proyecto.

La regla es simple:

- CANON contiene únicamente información confirmada.
- IDEAS contiene propuestas que todavía no son canon.
- ARCHIVO contiene versiones antiguas o material descartado.
- CAPITULOS contiene los textos narrativos vigentes cuando hayan sido incorporados.
- HISTORIAL_CHAT conserva la evolución real de las conversaciones y respuestas de trabajo.

No se debe convertir una propuesta de IA, un borrador antiguo o una interpretación en canon sin decisión expresa del autor.

## Estructura

- `CANON/` — reglas y hechos canónicos de WATH NEVER LEFT.
- `CAPITULOS/` — manuscrito histórico/vigente según la versión.
- `CAPITULOS V2/` — nueva etapa del manuscrito de WATH.
- `IDEAS/` — ideas no canonizadas.
- `ARCHIVO/` — material histórico/descartado.
- `METODOS_ESCRITURA/` — métodos, estructuras y estudios narrativos.
- `HISTORIAL_CHAT/` — historial cronológico de conversaciones y respuestas de trabajo.

## Historial de conversaciones

**Toda interacción de trabajo relevante —tanto del usuario como del asistente— debe registrarse en `HISTORIAL_CHAT/` con fecha, hora y zona horaria America/Montevideo (UTC-03:00).**

Cuando se recupere material antiguo sin una hora verificable, no se debe inventar la hora; debe señalarse como hora no recuperada.

El historial no es canon. Su función es permitir que un chat nuevo reconstruya la evolución de las ideas, decisiones, descartes y análisis sin depender de la memoria del modelo.

## Cómo iniciar un chat nuevo

Usar:

> Revisa https://github.com/Sebasm2kuy/novela y carga el contexto persistente antes de responder. **Analiza el repositorio completo y, además, lee obligatoriamente el HISTORIAL_CHAT más reciente para quedar actualizado con lo último de lo último.** Consulta el archivo del día actual y los días anteriores necesarios. Distingue siempre CANON, IDEAS, ARCHIVO, HISTORIAL y NUEVA_NOVELA. No conviertas automáticamente una conversación en canon.

El archivo del día actual debe considerarse prioritario para conocer el estado más reciente de la conversación, sin sustituir las reglas canónicas.

Para WATH NEVER LEFT, el archivo `CANON/PROMPT_MAESTRO_CHATGPT.md` contiene además el procedimiento específico del canon y manuscrito de WATH.

Cada cambio importante debe quedar registrado mediante un commit con un mensaje claro.


## Nueva novela

El directorio `NUEVA_NOVELA/` contiene la búsqueda independiente de una nueva novela. WATH NEVER LEFT V1/V2 y su CANON no se modifican por este trabajo. `NUEVA_NOVELA/` comienza sin canon y prioriza una premisa sencilla, clara y fértil antes de definir estructura o mitología.
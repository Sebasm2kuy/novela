# WATH NEVER LEFT

Repositorio maestro del proyecto **WATH NEVER LEFT**, junto con su archivo histórico y materiales de estudio para las etapas posteriores.

## Principio

GitHub es la fuente externa persistente de continuidad del proyecto.

La regla es simple:

- CANON contiene únicamente información confirmada.
- IDEAS contiene propuestas que todavía no son canon.
- ARCHIVO contiene versiones antiguas o material descartado.
- `CAPITULOS/` conserva manuscritos consolidados/históricos; la ubicación vigente de cada texto se especifica en la sección de manuscrito actual.
- HISTORIAL_CHAT conserva la evolución real de las conversaciones y respuestas de trabajo.

No se debe convertir una propuesta de IA, un borrador antiguo o una interpretación en canon sin decisión expresa del autor.

## Estructura

- `CANON/` — reglas y hechos canónicos de WATH NEVER LEFT.
- `CAPITULOS/` — manuscrito consolidado/histórico de etapas anteriores.
- `CAPITULOS V2/` — capítulos de la etapa de reescritura actual (por ahora, capítulos 1–4).
- `CAPITULOS V3/` — prólogo vigente de la etapa actual.
- `IDEAS/` — ideas no canonizadas.
- `ARCHIVO/` — material histórico/descartado.
- `METODOS_ESCRITURA/` — métodos, estructuras y estudios narrativos.
- `HISTORIAL_CHAT/` — historial cronológico de conversaciones y respuestas de trabajo.

## Ubicación vigente del manuscrito WNL

La versión de trabajo actual está distribuida intencionalmente entre dos carpetas:

- **Prólogo:** `CAPITULOS V3/00_PROLOGO.md`
- **Capítulos 1–4:** `CAPITULOS V2/01_CAPITULO_1.md` a `CAPITULOS V2/04_CAPITULO_4.md`

No mover el prólogo a V2 ni los capítulos a V3. Los números de versión identifican la etapa de cada texto, no un canon nuevo ni una asignación automática a las ventanas. Los borradores actuales se revisan sin sobrescribir el manuscrito histórico de `CAPITULOS/`.

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
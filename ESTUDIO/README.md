# Estudio de Novela — memoria de la app

Esta carpeta ES la base de datos del Estudio de Novela: la app lee y escribe aquí.

- `perfil.md` — ficha de la novela y guía de estilo.
- `personajes/`, `mundo/`, `cronologia/`, `tramas/`, `capitulos/`, `ideas/` — una ficha por archivo .md.
- `chat/historial.json` — registro de conversaciones con la IA (el PROMPT_MAESTRO exige registrar cada interacción).

Puedes editar cualquier ficha a mano en GitHub: la app detecta los cambios del árbol del repo automáticamente.
No borres los campos `id` del frontmatter: son como la app relaciona las fichas.

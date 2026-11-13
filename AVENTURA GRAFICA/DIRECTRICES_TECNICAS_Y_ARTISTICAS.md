# Directrices técnicas y artísticas — Aventura gráfica

**Estado:** base de trabajo acordada  
**Proyecto:** aventura gráfica point-and-click original  
**Repositorio:** `Sebasm2kuy/novela`  
**Carpeta:** `AVENTURA GRAFICA/`

Este documento reúne las decisiones técnicas y artísticas compartidas para orientar el desarrollo. Separa las definiciones ya comunicadas de los parámetros que todavía deben especificarse.

---

## 1. Contexto y objetivo

Estamos diseñando una aventura gráfica point-and-click 100% original, tomando ideas narrativas del repositorio y adaptándolas a un formato de juego moderno, con especial atención a la **accesibilidad móvil**.

La referencia de diseño y presentación es *The Darkside Detective*, especialmente su lectura visual, su interfaz limpia y su estructura de aventura point-and-click. Es una referencia, no un modelo para copiar: el universo, los personajes, los enigmas y la identidad del proyecto deben ser propios.

Se busca una estructura técnica validada y una producción que permita probar los escenarios progresivamente, en lugar de desarrollar todo el contenido visual sin comprobar antes su funcionamiento.

## 2. Motor y arquitectura técnica

### Motor elegido

- **Godot 4**.
- Exportación prevista a web y dispositivos móviles.
- Se informó que ya se probó con éxito un prototipo inicial (*Art Test*) funcional en web mediante GitHub Pages.

### Lógica de juego

Se propone una arquitectura limpia y orientada a datos (*data-driven*), con JSON para gestionar:

- Navegación entre escenarios.
- Hotspots y zonas interactivas.
- Inventario.
- Estados de objetos.
- Cambios de estado necesarios para los puzles y la progresión.

La intención es separar, en la medida de lo posible, los datos de cada escenario y sus interacciones de la lógica general del juego.

### Iluminación y atmósfera

- Uso de iluminación 2D dinámica de Godot.
- Nodos `PointLight2D` con oclusores y sombras.
- Fondos estáticos sobre los que se aplican efectos de iluminación.
- Posibles usos: velas, linternas, parpadeos y otras fuentes de luz puntuales.

### Profundidad y capas

- Sistema de *walk-behinds* mediante capas PNG separadas con transparencia alfa.
- Ordenamiento por capas para que los personajes puedan pasar por detrás de muebles u otros elementos del escenario.
- Los elementos que requieran profundidad visual deberán prepararse de forma compatible con este sistema.

## 3. Dirección artística y estilo visual

### Estética

**Pixel art detallado y atmosférico de alta definición.**

Referencia visual directa: el estilo de *The Darkside Detective*, especialmente su paleta nocturna y su interfaz limpia.

### Paleta cromática

- Tonos nocturnos y contrastados.
- Morados y azules oscuros.
- Acentos cálidos para fuentes de luz puntuales y elementos que deban destacar.

La paleta concreta de cada escenario todavía puede variar según su ambientación, manteniendo una identidad visual común.

### Interfaz de usuario

Elementos previstos:

- Cajas de diálogo en la parte superior.
- Retrato del personaje que habla.
- Inventario inferior accesible.
- Verbos o acciones directas.
- Controles optimizados para pantallas táctiles y móviles.

La interfaz debe priorizar legibilidad, objetivos táctiles cómodos y claridad sobre qué elementos del escenario admiten interacción.

## 4. Pipeline de producción artística

El desarrollo visual se validará mediante *Art Tests* y por escenario, siguiendo este flujo:

1. **Thumbnail y composición:** definir la distribución general de la habitación o escenario.
2. **Mapa de interacción:** identificar hotspots, objetos examinables, salidas, personajes y elementos relevantes para los puzles.
3. **Capas gráficas:** preparar las capas necesarias, incluidas las capas con alfa para profundidad y *walk-behinds*.
4. **Especificación de exportación:** documentar cómo deben exportarse los recursos gráficos desde el archivo de trabajo, por ejemplo PSD, hacia los formatos que utilizará Godot.
5. **Montaje en Godot:** importar los recursos, configurar capas, iluminación, hotspots y navegación.
6. **Prueba:** comprobar legibilidad, interacción, profundidad, rendimiento y experiencia táctil.

La idea es validar sala por sala antes de escalar la producción artística.

## 5. Resolución, proporciones y escalado

- El lienzo base debe adaptarse para aprovechar pantallas panorámicas móviles.
- No se deben deformar los elementos gráficos para llenar la pantalla.
- La composición debe mantener la legibilidad de los elementos interactivos (*affordance* de hotspots).
- La interfaz y las zonas táctiles deben considerarse desde el diseño inicial, no como una adaptación posterior.

**Pendiente de definir:** resolución interna exacta, relación de aspecto de referencia, reglas de escalado, márgenes o áreas seguras y comportamiento en distintas proporciones de pantalla. No se fija aquí ningún valor numérico porque todavía no fue especificado.

## 6. Criterios de diseño

- Priorizar la accesibilidad móvil desde el comienzo.
- Mantener una arquitectura de datos clara y ampliable.
- Reutilizar sistemas comunes para navegación, hotspots, inventario y estados.
- Diseñar cada escenario con sus interacciones identificadas antes de producir todos sus recursos finales.
- Comprobar el resultado dentro de Godot mediante pruebas funcionales.
- Mantener una identidad visual coherente sin sacrificar la legibilidad.
- Diferenciar las referencias artísticas de los elementos originales del proyecto.

## 7. Decisiones confirmadas y aspectos pendientes

### Definiciones comunicadas como acordadas

- Motor: Godot 4.
- Destinos previstos: web y móvil.
- Arquitectura orientada a datos, con JSON.
- Gestión de navegación, hotspots, inventario y estados de objetos.
- Iluminación 2D dinámica con `PointLight2D`, oclusores y sombras.
- *Walk-behinds* mediante capas PNG con alfa y ordenamiento.
- Estética de pixel art detallado y atmosférico.
- Referencia visual: *The Darkside Detective*.
- Paleta nocturna de azules y morados oscuros con acentos cálidos.
- Diálogos superiores con retrato, inventario inferior y acciones directas.
- Diseño optimizado para pantallas táctiles.
- Producción validada sala por sala mediante Art Tests.

### Aspectos todavía no especificados en este documento

- Resolución interna y tamaño exacto del lienzo.
- Relación de aspecto de referencia y reglas detalladas de escalado.
- Formato definitivo de los archivos JSON y sus esquemas.
- Estructura concreta de carpetas para recursos y escenas.
- Especificación exacta de exportación desde PSD.
- Diseño final de controles táctiles y comportamiento de la interfaz.
- Requisitos de rendimiento y dispositivos móviles objetivo.

Estos puntos deben definirse mediante pruebas y decisiones explícitas; no deben darse por cerrados por inferencia.

## 8. Relación con el inventario narrativo

Este documento es la referencia técnica y artística. El inventario de premisas e historias se conserva por separado en:

`AVENTURA GRAFICA/INVENTARIO_IDEAS_ADAPTABLES.md`

La elección de una historia concreta no modifica automáticamente las directrices técnicas. Del mismo modo, las decisiones de motor y estilo visual no obligan a combinar premisas narrativas que originalmente eran independientes.

---

**Nota de mantenimiento:** actualizar este documento cuando una decisión técnica o artística se pruebe y se confirme. Mantener claramente diferenciados los acuerdos, las hipótesis y los asuntos pendientes.

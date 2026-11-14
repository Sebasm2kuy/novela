# WNL — Mapa funcional de la Habitación

**Fecha:** 2026-11-14  
**Proyecto:** Aventura gráfica WNL  
**Estado:** propuesta operativa para revisión. Las propuestas de distribución e interacción no se convierten automáticamente en canon narrativo.

## 1. Criterio rector

La Habitación es un escenario permanente, completamente explorable y funcional desde el primer momento en que aparece en el juego.

- No tiene puertas ni ventanas.
- No hay sectores cerrados ni mobiliario que deba desbloquearse para utilizarlo.
- El protagonista puede recorrer toda la superficie transitable desde el inicio.
- Los sistemas y objetos básicos están operativos desde el comienzo.
- Que un objeto funcione no significa que el protagonista conozca todos sus contenidos, archivos, secretos o significados.
- La Habitación conecta con las demás realidades según las reglas narrativas documentadas: el tránsito ocurre mediante el ciclo de sueño y tiempo mínimo. No se añade un selector de destinos ni un portal para elegir una Ventana.

La Habitación debe sentirse como un lugar habitable y utilizable —donde se puede trabajar, investigar, descansar y examinar objetos—, no como un menú o un pasillo de transición.

## 2. Base espacial y cámara

### Dimensiones de diseño

- Lienzo panorámico solicitado: **3840 × 1080 px**.
- Relación: 32:9.
- Ventana de cámara de referencia: **1920 × 1080 px**, 16:9.
- El escenario equivale a dos vistas de cámara de ancho.
- La imagen conceptual generada previamente no tiene estas dimensiones exactas; no debe usarse como archivo maestro ni deformarse para encajar.

### Comportamiento de cámara propuesto

- Cámara 2D horizontal que sigue al protagonista.
- Al inicio muestra el encuadre inicial que se defina para la entrada a la Habitación.
- Al acercarse el protagonista al margen de seguimiento, la cámara se desplaza suavemente y revela la otra mitad.
- Límites de cámara en los extremos: nunca mostrar espacio exterior al fondo.
- Usar una zona muerta o margen de seguimiento para evitar vibraciones.
- El personaje debe permanecer razonablemente visible durante el desplazamiento.
- La interfaz (diálogos, retrato, inventario y acciones) permanece anclada a la pantalla, no al escenario.

Pendiente de prueba: posición inicial exacta, velocidad de seguimiento, zona muerta y tratamiento de pantallas con proporciones distintas.

## 3. Distribución panorámica propuesta

La organización interpreta la ilustración conceptual como un único espacio continuo. Los rangos son orientativos, no medidas finales de cada mueble.

| Sector | Rango horizontal aproximado | Función principal |
|---|---:|---|
| A — Puesto informático | x = 0–1050 | Computadora y trabajo digital |
| B — Biblioteca y consulta | x = 900–2050 | Libros, manuales y consulta |
| C — Equipos y archivo | x = 1750–2850 | Comunicaciones, grabación y documentación |
| D — Descanso y almacenamiento | x = 2650–3840 | Cama, armario y objetos personales |

Los rangos se superponen deliberadamente: son áreas funcionales, no paredes ni divisiones físicas. La habitación debe leerse como un único ambiente.

### Sector A — Puesto informático

Elementos previstos:
- Escritorio principal.
- Computadora de escritorio con monitor CRT, teclado y dispositivo apuntador.
- Silla utilizable.
- Periféricos y documentos auxiliares.

Interacciones propuestas:
- Sentarse y levantarse.
- Encender, usar y apagar la computadora.
- Navegar por sus funciones y consultar los datos disponibles.
- Examinar periféricos y documentos sobre el escritorio.

La computadora debe poder utilizarse desde el inicio. Sus contenidos pueden revelar información progresivamente, sin bloquear el uso básico del equipo.

### Sector B — Biblioteca y consulta

Elementos previstos:
- Estanterías de libros.
- Manuales, enciclopedias, cuadernos y carpetas.
- Espacio accesible para consultar material.

Interacciones propuestas:
- Examinar estantes y títulos.
- Retirar y leer libros o cuadernos seleccionables.
- Consultar material de referencia.
- Devolver o dejar material en una superficie de apoyo, si se incorpora esa acción.

No todos los libros tienen por qué contener información relevante. La biblioteca es un elemento funcional del espacio, no una colección de pistas obligatorias.

### Sector C — Equipos, comunicaciones y archivo

Elementos previstos:
- Consola o mesa de equipos analógicos.
- Radio o equipo de comunicaciones.
- Grabadora/reproductor y otros dispositivos de registro.
- Archivadores y cajoneras.
- Superficie de trabajo para documentos y objetos.

Interacciones propuestas:
- Operar los equipos que se definan para el escenario.
- Escuchar o reproducir registros disponibles.
- Examinar controles, indicadores y conexiones.
- Abrir archivadores y consultar documentos.
- Organizar o examinar material sobre la mesa.

**Límite narrativo:** estos equipos no deben presentarse como un mecanismo para escoger o controlar a voluntad las Ventanas. La Habitación conecta realidades, pero el protagonista no elige conscientemente el destino.

### Sector D — Descanso y almacenamiento

Elementos previstos:
- Cama.
- Mesa auxiliar.
- Armario o taquilla.
- Reloj visible.
- Espacio para objetos personales.

Interacciones propuestas:
- Acercarse y utilizar la cama para descansar/dormir conforme a la mecánica narrativa.
- Examinar reloj y mobiliario.
- Abrir y consultar el almacenamiento.
- Examinar objetos personales y elementos de la mesa auxiliar.

La cama es importante porque el sueño participa en el ciclo de tránsito. Su uso debe respetar las reglas temporales de la Habitación documentadas en el mapa general de WNL.

## 4. Recorrido y superficie transitable

Debe existir una ruta continua y legible a lo largo de toda la habitación, desde el extremo izquierdo hasta el derecho.

- Dejar una franja principal de suelo libre frente a los muebles.
- Evitar que alfombras, mesas bajas, cajas o sillas bloqueen accidentalmente toda la ruta.
- Permitir pequeños desvíos hacia los puntos de interacción.
- Evitar pasillos estrechos que hagan incómodo el control táctil.
- El personaje debe poder acercarse a los muebles desde posiciones definidas para activar interacciones.
- No permitir que atraviese escritorios, estanterías, archivadores, cama u otros objetos sólidos.

### Zonas de colisión propuestas

1. **Suelo transitable:** superficie continua sobre la que se mueve el personaje.
2. **Bloqueos sólidos:** paredes, laterales de muebles, escritorios, estanterías, archivadores, cama y armario.
3. **Bloqueos bajos o parciales:** mesas auxiliares, cajas y objetos que realmente impidan el paso según su ubicación.
4. **Zonas de aproximación:** áreas invisibles frente a computadora, biblioteca, consola, archivadores, cama y armario. No son obstáculos; orientan al personaje y ejecutan interacciones.
5. **Walk-behinds:** elementos visuales delante de los cuales el personaje puede pasar para producir profundidad. Se preparan como capas con alfa y se ordenan correctamente.

Las colisiones no deben seguir cada píxel del dibujo. Se usarán formas simples y legibles que representen el volumen de los muebles.

## 5. Mapa inicial de hotspots

Todos estos puntos se consideran disponibles desde el comienzo. La lista es una propuesta de implementación y debe revisarse contra el diseño gráfico final.

| ID provisional | Objeto/zona | Acciones previstas |
|---|---|---|
| H01 | Computadora | Usar, examinar |
| H02 | Escritorio | Examinar |
| H03 | Silla | Usar, examinar |
| H04 | Biblioteca | Examinar |
| H05 | Libros seleccionados | Leer, examinar |
| H06 | Consola de equipos | Usar, examinar |
| H07 | Radio/comunicaciones | Usar, escuchar, examinar |
| H08 | Grabadora/reproductor | Usar, reproducir, examinar |
| H09 | Archivadores | Abrir, buscar, examinar |
| H10 | Documentos | Leer, examinar |
| H11 | Cama | Usar para descansar/dormir, examinar |
| H12 | Reloj | Consultar, examinar |
| H13 | Armario/taquilla | Abrir, guardar/retirar si se implementa almacenamiento |
| H14 | Mesa auxiliar | Examinar |
| H15 | Objetos personales | Examinar y, cuando corresponda, recoger |

Los IDs son identificadores técnicos provisionales; no son nombres definitivos de nodos ni claves JSON.

## 6. Estados e interacciones

La arquitectura acordada utiliza datos separados de la lógica general, con JSON para navegación, hotspots, inventario, estados de objetos y puzles.

Para la Habitación:
- Cada hotspot tendrá identificador estable, posición o área de interacción, acciones disponibles y referencia al objeto correspondiente.
- Los objetos que cambien visualmente tendrán estados explícitos.
- Las acciones deben producir una respuesta: animación, diálogo, descripción, sonido, apertura de interfaz, reproducción o cambio de estado.
- No crear hotspots invisibles sin respuesta perceptible.
- Computadora, biblioteca, consola, radio, grabadora, archivadores, cama y armario deben ser utilizables desde el estado inicial.
- La progresión podrá descubrir contenidos o información nuevos, pero no desbloquear el acceso básico a zonas o al funcionamiento esencial de esos objetos.

## 7. Capas gráficas previstas

Preparar recursos para modificar el escenario sin regenerar toda la imagen.

1. **Fondo base:** paredes, techo, suelo, paneles y arquitectura.
2. **Mobiliario de fondo:** estanterías, escritorios, archivadores, armario y cama, según profundidad.
3. **Objetos independientes:** monitor, teclado, libros seleccionados, radio, grabadora, documentos, reloj, lámparas y elementos que cambien de estado.
4. **Walk-behinds:** partes de muebles u objetos que deban dibujarse delante del personaje.
5. **Luces:** fuentes luminosas y máscaras/oclusores para iluminación 2D.
6. **Personaje:** sprite y animaciones de movimiento, espera e interacción.
7. **Hotspots y colisiones:** datos independientes del arte; no forman parte de la imagen final.

No es necesario que cada libro o tornillo sea un sprite independiente. Separar lo que requiera interacción, animación, cambio de estado, iluminación especial o profundidad.

## 8. Reglas de implementación en Godot 4

Propuesta técnica coherente con las directrices existentes:
- Una escena Godot para la Habitación.
- Fondo y capas visuales organizados por profundidad.
- Personaje controlable con movimiento 2D.
- Cámara 2D con límites y seguimiento suave.
- Áreas de interacción mediante Area2D o hotspots definidos por datos.
- Colisiones mediante formas simples.
- CanvasLayer para interfaz fija en pantalla.
- Luces con PointLight2D y oclusores donde aporten valor.
- Datos JSON para hotspots, acciones y estados, evitando codificar cada interacción directamente en el controlador general.

Los nombres de nodos y el esquema JSON definitivo quedan pendientes de una prueba funcional.

## 9. Pruebas de aceptación

La Habitación no se considera lista hasta comprobar:

- [ ] El personaje recorre el escenario de un extremo al otro sin bloqueos accidentales.
- [ ] La cámara revela ambos sectores y respeta los límites.
- [ ] La interfaz permanece fija mientras el escenario se desplaza.
- [ ] Las colisiones impiden atravesar muebles sólidos.
- [ ] Los walk-behinds producen profundidad correcta.
- [ ] Cada hotspot tiene una respuesta visible, sonora o narrativa.
- [ ] Computadora, biblioteca, equipos, radio, grabadora, archivadores, cama y almacenamiento son utilizables desde el inicio.
- [ ] El uso de la cama respeta el ciclo temporal y de sueño de la Habitación.
- [ ] Ningún dispositivo permite elegir voluntariamente una Ventana.
- [ ] Los controles y objetivos táctiles son cómodos en móvil horizontal.
- [ ] El escenario mantiene legibilidad en la vista 1920 × 1080.

## 10. Estado de las decisiones

### Confirmado por el autor
- La Habitación no tiene puertas ni ventanas.
- Debe tener estética retrofuturista de centro de mando, con computadora utilizable y biblioteca.
- Debe ser 100% funcional desde el inicio.
- El jugador puede recorrer una superficie más ancha que la pantalla y descubrir el resto mediante desplazamiento de cámara.
- Se solicitó una base panorámica de 3840 × 1080 y una vista de juego de 1920 × 1080.

### Propuestas de este mapa, pendientes de aprobación
- Distribución en cuatro sectores funcionales.
- Ubicación exacta y composición de cada mueble.
- Hotspots y acciones concretas de cada objeto.
- Ruta de circulación y geometría de colisiones.
- Cámara con seguimiento suave y zona muerta.
- Dimensiones finales de sprites y capas.
- Esquema JSON y nombres técnicos definitivos.
- Qué objetos se pueden recoger y cómo funciona el almacenamiento.

### Restricciones narrativas
- No introducir puertas, ventanas, portales ni salidas físicas.
- No presentar la Habitación como un centro de investigación cuya naturaleza el protagonista ya comprende.
- No convertir la consola en un selector de Ventanas.
- No explicar de entrada el origen o propósito último de la Habitación.
- El ciclo de tránsito continúa sujeto a las reglas de tiempo y sueño documentadas en el mapa general WNL.

---

Este documento es un mapa funcional de trabajo para la adaptación a videojuego. No modifica por sí mismo el canon de la novela ni sustituye las directrices técnicas y artísticas generales.

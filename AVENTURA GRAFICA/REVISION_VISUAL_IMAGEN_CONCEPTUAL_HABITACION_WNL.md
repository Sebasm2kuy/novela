# Revisión visual — Imagen conceptual de la Habitación WNL

**Fecha:** 2026-11-14  
**Proyecto:** Aventura gráfica WNL  
**Imagen revisada:** `AVENTURA GRAFICA/Escenarios/Habitación Espacial Retro en Pixel Art.png`  
**Dimensiones originales:** 2048 × 768 px  
**Estado:** revisión visual realizada; ajustes de distribución propuestos, pendientes de aprobación.

---

## 1. Resultado de la inspección

La imagen conceptual se recuperó desde la Biblioteca de archivos de ChatGPT, donde estaba disponible por su uso en la conversación anterior, y se contrastó visualmente con el PNG alojado en el repositorio.

Es una habitación panorámica retrofuturista, cerrada y continua, sin ventanas ni puertas visibles. La composición presenta tres grandes agrupaciones visuales de izquierda a derecha:

1. **Puesto de trabajo y equipos:** archivadores altos en el extremo izquierdo, escritorio con monitor CRT y silla, lámpara y periféricos; equipos analógicos y grabadora de cinta próximos al escritorio.
2. **Biblioteca central:** estantería grande repleta de libros, con objetos decorativos y plantas; alfombra amplia en el suelo.
3. **Descanso y almacenamiento:** archivadores/cajonera y reloj en la zona derecha-central; cama en el lado derecho, mesa baja delante de ella y armario/taquilla en el extremo derecho.

La imagen también contiene elementos de ambientación relevantes: paneles y tuberías en paredes/techo, luces lineales, pósteres técnicos, lámina espacial, lámparas, plantas, pequeños objetos, suelo metálico reflectante y alfombras.

La imagen es una referencia de composición y estilo, no el archivo maestro del escenario final.

## 2. Comparación con el plano cuantificado

El plano actual tiene una organización funcional válida como primer intento, pero varias posiciones no reproducen la composición de la referencia. Las diferencias más importantes son:

| Elemento | Imagen conceptual | Plano actual | Observación |
|---|---|---|---|
| Archivadores izquierdos | Mueble alto muy visible en el extremo izquierdo | No aparecen como mueble independiente | Falta incorporarlos o decidir expresamente si se omiten. |
| Escritorio y PC | Ocupan el sector izquierdo, con silla delante | Escritorio en X 180–790 | Coincidencia general de sector y función. |
| Equipos analógicos | Están junto al escritorio, entre el puesto informático y la biblioteca | Consola en X 1650–2200, al otro lado de la biblioteca | Discrepancia espacial importante. |
| Grabadora de cinta | Forma parte del conjunto de equipos junto al escritorio | Grabadora en X 2110–2340 | Debe revisarse su ubicación; la referencia la asocia al puesto de equipos de la izquierda. |
| Biblioteca | Gran estantería central, dominante y de gran altura | Biblioteca en X 900–1430 | Coincidencia aproximada de zona, pero debe comprobarse su anchura y relación con los equipos. |
| Cajonera/archivo derecho | A la derecha de la biblioteca, bajo el reloj | Archivador en X 2390–2700 | Coincidencia funcional, pero depende de reordenar la consola y la biblioteca. |
| Reloj | Pared sobre la cajonera derecha | X 3220–3380 | Posición horizontal demasiado a la derecha respecto de la referencia. |
| Cama | Zona derecha, detrás de la mesa baja | X 2850–3520 | Coincidencia general de sector. |
| Mesa baja | Delante de la cama, en primer plano | Mesa auxiliar en X 2700–2870 | Debe aclararse su relación visual y de circulación con la cama; la referencia la muestra delante de ella. |
| Armario/taquilla | Extremo derecho | X 3540–3800 | Coincidencia general de sector. |
| Alfombra principal | Gran alfombra en primer plano, delante de la biblioteca | No aparece en el plano de mobiliario | Falta incorporarla como elemento visual y revisar que no afecte a la navegación. |
| Elementos murales y techo | Pósteres, paneles, rejillas, tuberías y luces | No están detallados en el plano | Deben contemplarse como composición de fondo, sin convertirlos automáticamente en hotspots. |
| Plantas y objetos decorativos | Varias plantas, esfera/modelo planetario, lámparas y objetos | No están detallados | Añadirlos al inventario visual si se mantienen en el diseño. |

## 3. Discrepancias críticas

### 3.1 Equipos ubicados al lado equivocado de la biblioteca

La referencia sitúa los equipos analógicos y la grabadora cerca del escritorio, antes de llegar a la biblioteca central. El plano cuantificado actual sitúa la consola y la grabadora después de la biblioteca, hacia la mitad derecha.

Esta es la corrección espacial más importante. Si se mantiene la composición conceptual, el grupo de equipos debe quedar entre el escritorio y la biblioteca, o integrado visualmente con el puesto de trabajo.

### 3.2 Falta el archivador del extremo izquierdo

La referencia tiene un mueble alto de cajones en el extremo izquierdo. No está contemplado como pieza independiente en el plano actual. No debe confundirse con el archivador ubicado a la derecha de la biblioteca.

### 3.3 Biblioteca como centro visual

La biblioteca debe leerse como el núcleo central de la habitación. Su gran volumen vertical y la cantidad de libros son rasgos dominantes. La ubicación actual es aproximada, pero hay que reorganizar las piezas vecinas para conservar esa lectura.

### 3.4 Mesa baja, alfombras y circulación

La mesa baja aparece delante de la cama, y la alfombra principal ocupa el primer plano central. Son elementos de composición que no deben omitirse. En la implementación, la alfombra puede ser transitable si no bloquea el movimiento; la mesa sí requerirá una huella de colisión coherente con su volumen.

### 3.5 Reloj y cajonera

El reloj se encuentra sobre la cajonera situada a la derecha de la biblioteca, no encima de la cama ni cerca del armario. Su posición del plano debe desplazarse hacia la zona de esa cajonera cuando se rehaga la distribución.

## 4. Lectura espacial recomendada para una nueva versión del plano

Sin fijar todavía coordenadas definitivas, la secuencia visual más fiel a la referencia sería:

1. Archivadores altos del extremo izquierdo.
2. Escritorio, CRT, silla y lámpara.
3. Equipos analógicos, medidores y grabadora junto al puesto informático.
4. Biblioteca grande como foco central.
5. Cajonera/archivador y reloj a la derecha de la biblioteca.
6. Cama en el sector derecho, con mesa baja delante.
7. Armario/taquilla en el extremo derecho.

Esta secuencia es una **recomendación derivada de la imagen**, no una aprobación del autor ni un cambio automático del plano existente.

## 5. Adaptación a 3840 × 1080

La imagen original mide 2048 × 768 (relación 8:3), mientras que el lienzo de juego previsto mide 3840 × 1080 (relación 32:9). No se deben estirar, aplastar ni ampliar las coordenadas de la imagen de forma directa para obtener el escenario final.

El escenario final debe redibujarse/componerse para 3840 × 1080, preservando:
- El orden visual de los grupos de mobiliario.
- La jerarquía de tamaños y focos.
- La atmósfera y la identidad de pixel art.
- El espacio de circulación del personaje.
- La posibilidad de separar objetos, capas, walk-behinds, luces y elementos interactivos.

La cámara de 1920 × 1080 debe revisarse sobre la nueva composición. No asumir que la imagen conceptual representa exactamente uno o dos encuadres de cámara.

## 6. Elementos visuales a registrar para el arte final

- Arquitectura: paredes metálicas, paneles, rejillas, tuberías y techo.
- Iluminación: tiras de luz frías, lámpara de escritorio cálida, lámpara decorativa cálida y pequeñas luces de equipos.
- Puesto informático: CRT, teclado, silla, escritorio, cajoneras, papeles y periféricos.
- Equipos: grabadora de cinta de carrete, medidores, pantallas pequeñas y cajas electrónicas.
- Biblioteca: estantería completa, libros, cajas, planta colgante y objeto esférico decorativo.
- Archivo derecho: cajonera, reloj y lámpara.
- Descanso: cama, almohadas, ropa de cama, mesa baja, taza y papeles.
- Almacenamiento extremo derecho: taquilla/armario, prenda colgada y cajas superiores.
- Decoración: pósteres técnicos, lámina espacial, plantas, alfombra principal y alfombra pequeña.

No todos estos elementos deben convertirse en hotspots. La interacción se define por separado según su utilidad real en el juego.

## 7. Estado y próximos pasos

### Confirmado por referencia visual
- La secuencia general izquierda-derecha descrita en este documento.
- El puesto informático y los equipos están agrupados en el sector izquierdo.
- La biblioteca ocupa el centro visual.
- La cama y el armario se ubican en el sector derecho.
- La imagen no muestra puertas ni ventanas.

### Pendiente de aprobación del autor
- Reorganizar el plano cuantificado siguiendo la secuencia recomendada.
- Decidir si todos los elementos decorativos descritos se conservan.
- Confirmar qué objetos de ambientación serán interactivos y cuáles serán únicamente decorativos.
- Definir el espacio de circulación alrededor de la mesa baja, la silla y la cama.
- Aprobar las nuevas coordenadas antes de actualizar el mapa SVG de colisiones/hotspots.

### Próximo paso
Preparar una **versión revisada del plano de distribución** que respete la composición de la imagen conceptual, manteniendo el lienzo 3840 × 1080 y la vista 1920 × 1080. Presentar esa versión para revisión antes de convertirla en distribución aprobada o producir el arte final.

---

**Nota:** esta revisión se basa en la inspección directa del PNG y en la comparación con el plano y mapa técnico existentes. No modifica por sí misma el canon narrativo ni aprueba automáticamente una nueva distribución.

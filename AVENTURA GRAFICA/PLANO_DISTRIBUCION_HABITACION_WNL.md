# WNL — Plano de distribución de la Habitación

**Fecha:** 2026-11-14  
**Documento relacionado:** [MAPA_FUNCIONAL_HABITACION_WNL.md](MAPA_FUNCIONAL_HABITACION_WNL.md)  
**Estado:** propuesta espacial concreta para revisión; no aprobada todavía por el autor.

Este plano convierte la distribución funcional general en una primera implantación medible sobre el escenario panorámico. Las coordenadas son de diseño y sirven para organizar el arte, la navegación y las pruebas; no deben interpretarse como medidas arquitectónicas narrativas ni como píxeles definitivos de cada sprite.

---

## 1. Sistema de coordenadas

- Lienzo completo: **3840 × 1080 px**.
- Origen `(0,0)`: esquina superior izquierda.
- Eje X: aumenta hacia la derecha.
- Eje Y: aumenta hacia abajo.
- Vista de cámara de referencia: **1920 × 1080 px**.
- Mitad izquierda: X = 0–1919.
- Mitad derecha: X = 1920–3839.
- Suelo visible de referencia: Y = 760–1079.
- Franja principal de circulación: Y = 850–1015.
- La altura exacta del suelo y la línea de horizonte deberán ajustarse al arte final, manteniendo la franja transitable continua.

Las coordenadas de los muebles indican sus cajas de ocupación aproximadas `[X inicial, Y inicial, X final, Y final]`. No son rectángulos que deban dibujarse literalmente: cada objeto tendrá su silueta artística y una colisión simplificada adaptada a ella.

## 2. Implantación general

La habitación se organiza como un único ambiente. Los sectores son funcionales, no divisiones físicas.

| Elemento | Caja aproximada (X1, Y1 → X2, Y2) | Ubicación |
|---|---:|---|
| Escritorio y puesto PC | 180, 490 → 790, 825 | Sector A, pared/fondo |
| Silla de PC | 470, 690 → 650, 880 | Frente al escritorio |
| Biblioteca principal | 900, 300 → 1430, 790 | Sector B, pared/fondo |
| Mueble de consulta bajo | 1120, 680 → 1510, 830 | Delante o junto a biblioteca, sin cerrar el paso |
| Consola de equipos | 1650, 500 → 2200, 825 | Sector C, pared/fondo |
| Radio / equipo de comunicaciones | 1810, 420 → 2070, 590 | Sobre la consola |
| Grabadora / reproductor | 2110, 610 → 2340, 790 | Extremo derecho de consola |
| Archivador | 2390, 520 → 2700, 825 | Entre equipos y descanso |
| Cama | 2850, 500 → 3520, 850 | Sector D, pared/fondo |
| Mesa auxiliar | 2700, 690 → 2870, 835 | Junto a la cama |
| Armario / taquilla | 3540, 330 → 3800, 850 | Extremo derecho |
| Reloj | 3220, 170 → 3380, 330 | Pared sobre zona de cama |
| Objetos personales | 300, 650 → 760, 800; 2700, 650 → 2870, 820 | Sobre superficies, según composición |

**Lectura visual:** el puesto informático ocupa el primer tramo; la biblioteca forma una masa vertical que separa visualmente trabajo y consulta; la consola y el archivo constituyen el núcleo de equipos; la cama y el armario cierran visualmente el extremo derecho. No se agrega ninguna puerta, ventana ni salida física.

## 3. Recorrido del personaje

### Ruta principal

Se reserva una franja continua de suelo por delante de los muebles:

- Banda de circulación recomendada: **Y = 850–1015**.
- El personaje puede desplazarse en X a lo largo de todo el escenario.
- Se permite un pequeño ajuste de profundidad en Y para acercarse a los objetos, rodear muebles bajos y producir sensación de espacio.
- Ningún mueble debe ocupar toda la profundidad de la banda de circulación.
- No se debe forzar al personaje a pasar por huecos inferiores a unos 120 px de ancho útil.
- Mantener al menos 150 px de suelo libre frente a los frentes de interacción principales siempre que la composición lo permita.

La ruta no es un pasillo dibujado ni una línea obligatoria: es una zona libre que admite pequeñas variaciones de posición.

### Puntos de aproximación

Los puntos siguientes son posiciones sugeridas para que el personaje se detenga antes de activar cada hotspot. El motor podrá calcular el acercamiento desde la posición actual, pero debe evitar que el personaje termine dentro de una colisión.

| Interacción | Punto de aproximación sugerido (X, Y) | Orientación |
|---|---:|---|
| Silla / escritorio | (500, 850) | Hacia el escritorio |
| Computadora | (620, 845) | Hacia el monitor |
| Biblioteca | (1120, 850) | Hacia estantes |
| Libros / consulta | (1370, 850) | Hacia el mueble |
| Consola | (1840, 850) | Hacia controles |
| Radio | (2010, 850) | Hacia el equipo |
| Grabadora | (2260, 850) | Hacia reproductor |
| Archivador | (2530, 850) | Hacia cajones |
| Mesa auxiliar | (2780, 850) | Hacia la mesa |
| Cama | (3150, 870) | Hacia la cama |
| Armario | (3660, 865) | Hacia el armario |

Las coordenadas Y son puntos de suelo para el personaje, no el centro visual de los hotspots. La interacción se activa al llegar al punto de aproximación o al entrar en el área válida, según el sistema de control que se implemente.

## 4. Colisiones y profundidad

### Colisiones sólidas

Crear formas simples siguiendo el volumen de cada mueble, no el contorno de cada píxel:

- Escritorio: bloquear el cuerpo y laterales; dejar libre el espacio necesario para acercarse a la silla.
- Silla: colisión ajustada al asiento/base cuando esté ocupada en el escenario; si se anima al sentarse, cambiar a estado correspondiente.
- Biblioteca: bloquear la base y laterales; los estantes altos no requieren colisión adicional.
- Mueble de consulta: bloquear solo el volumen que llega al suelo.
- Consola: bloquear el cuerpo inferior; controles y equipos superiores son hotspots, no obstáculos.
- Archivador: bloquear el volumen inferior y permitir acercamiento frontal.
- Cama: bloquear el volumen de la estructura y colchón; no permitir atravesarla.
- Mesa auxiliar: bloquear su base, dejando espacio para aproximarse.
- Armario: bloquear el cuerpo y permitir acercamiento frontal.

### Walk-behinds

Elementos candidatos a capa delantera:
- Primer plano de la silla, si el personaje puede pasar delante de ella.
- Esquinas o laterales de muebles que deban tapar parcialmente al personaje.
- Elementos bajos del primer plano que no bloqueen el paso.
- Cualquier objeto que cruce visualmente la silueta del personaje durante el recorrido.

Los walk-behinds son máscaras visuales con alfa y orden de dibujo; no deben confundirse con colisiones.

### Regla de seguridad de navegación

La prioridad es que el personaje pueda llegar a cada punto de aproximación sin quedar atrapado. Si una colisión impide alcanzar un hotspot, se modifica la colisión o el punto de aproximación; no se obliga al jugador a encontrar un píxel exacto.

## 5. Hotspots ubicados en el plano

| ID | Área de interacción aproximada | Acción principal |
|---|---|---|
| H01 Computadora | X 530–760, Y 475–670 | Usar / examinar |
| H02 Escritorio | X 180–790, Y 650–825 | Examinar |
| H03 Silla | X 430–670, Y 680–890 | Sentarse / examinar |
| H04 Biblioteca | X 900–1430, Y 300–790 | Examinar |
| H05 Libros seleccionados | X 980–1400, Y 390–690 | Leer / examinar |
| H06 Consola | X 1650–2200, Y 500–825 | Usar / examinar |
| H07 Radio | X 1810–2070, Y 420–590 | Usar / escuchar |
| H08 Grabadora | X 2110–2340, Y 610–790 | Usar / reproducir |
| H09 Archivador | X 2390–2700, Y 520–825 | Abrir / buscar |
| H10 Documentos | X 1680–2700, Y 600–820 | Leer / examinar |
| H11 Cama | X 2850–3520, Y 500–850 | Descansar / dormir / examinar |
| H12 Reloj | X 3220–3380, Y 170–330 | Consultar |
| H13 Armario | X 3540–3800, Y 330–850 | Abrir / almacenamiento |
| H14 Mesa auxiliar | X 2700–2870, Y 690–835 | Examinar |
| H15 Objetos personales | Según objeto sobre escritorio, mesa o estantes | Examinar / recoger cuando corresponda |

Las áreas son cajas de referencia iniciales. En el montaje real deben recortarse para que un hotspot no tape a otro ni active interacciones a través de muebles. Los elementos colocados sobre una superficie pueden tener hotspots individuales.

## 6. Composición por encuadres de cámara

### Encuadre 1 — X = 0 a 1920

Debe mostrar:
- Puesto informático completo, con la computadora claramente reconocible.
- Silla y espacio de aproximación.
- Biblioteca como segundo foco visual.
- Inicio de la consola al borde derecho, suficiente para anticipar continuidad.

No cortar el monitor, la silla ni el acceso a la computadora. El borde derecho puede mostrar parte del siguiente sector, pero no debe dejar un objeto interactivo importante partido por la mitad.

### Encuadre 2 — X = 1920 a 3840

Debe mostrar:
- Continuación de la consola y grabadora.
- Archivador.
- Cama y reloj.
- Armario completo.
- Espacio de aproximación frente a cama y armario.

La cámara debe permitir que el jugador descubra el tramo derecho al caminar, sin que la cama o el armario aparezcan como una habitación separada.

### Zona de solape de composición

Entre X = 1700 y 2140 se recomienda una zona de transición visual: parte de la consola, estantería o paneles de pared pueden continuar entre encuadres. Evitar una división vertical que parezca una pantalla de carga o una pared invisible.

## 7. Reglas de cámara derivadas del plano

- Cámara de referencia: 1920 × 1080.
- Límites horizontales: X mínimo 0; X máximo 1920, expresados como posición de cámara para una ventana de 1920 px.
- La cámara no debe moverse antes de que el personaje se acerque a una zona de margen configurable.
- En la mitad inicial, permitir que el personaje se desplace sin seguimiento mientras siga dentro del encuadre.
- Al superar el margen, seguir suavemente al personaje.
- En el extremo derecho, detener el seguimiento cuando el borde de cámara alcance X = 1920.
- Mantener la interfaz en CanvasLayer.
- Probar el comportamiento en móvil horizontal y en pantallas con recortes/áreas seguras.

## 8. Riesgos detectados y correcciones preventivas

1. **Muebles demasiado profundos:** pueden cortar el recorrido. Solución: reducir su huella inferior o desplazar el punto de aproximación.
2. **Hotspots superpuestos:** pueden seleccionar el objeto equivocado. Solución: dividir objetos compuestos en áreas específicas y priorizar el objeto bajo el cursor/toque.
3. **Cama y armario juntos:** pueden dejar poco espacio para interactuar. Solución: reservar una zona frontal común, pero con puntos de aproximación separados.
4. **Biblioteca demasiado ancha:** puede parecer un muro infranqueable. Solución: mantener una base sólida y comprobar que el personaje pueda recorrer por delante.
5. **Corte entre cámaras:** puede partir objetos o revelar una unión artificial. Solución: revisar la composición en ambas vistas y en el desplazamiento continuo.
6. **Escala del personaje:** si el personaje resulta demasiado alto o bajo respecto de los muebles, las coordenadas Y y las colisiones pierden sentido. Solución: fijar primero una escala de prueba del personaje y ajustar la línea de suelo antes de exportar sprites finales.

## 9. Prueba de validación previa al arte definitivo

Antes de producir el escenario final:
1. Crear un bloque gris del lienzo 3840 × 1080.
2. Dibujar cajas de muebles con estas coordenadas.
3. Añadir un rectángulo de prueba que represente al personaje.
4. Marcar la banda transitable y los puntos de aproximación.
5. Simular la cámara 1920 × 1080 desplazándose de extremo a extremo.
6. Comprobar que se llega a los 11 puntos de aproximación sin atravesar muebles ni quedar bloqueado.
7. Revisar la lectura de cada mitad y la transición entre ambas.
8. Ajustar coordenadas y colisiones antes de crear sprites definitivos.

**Criterio de aprobación:** el plano se aprueba cuando el recorrido es cómodo, todos los objetos importantes son accesibles desde el inicio, ambos encuadres se leen como una sola habitación y no hay hotspots inaccesibles. Solo entonces se pasa al mapa visual definitivo de hotspots/colisiones y al escenario panorámico final.

---

## 10. Pendientes de revisión del autor

- Confirmar si la secuencia izquierda-derecha propuesta representa correctamente la distribución deseada.
- Confirmar si el escritorio, biblioteca, consola, archivo, cama y armario son los muebles correctos y están en el orden deseado.
- Ajustar cualquier mueble que no coincida con la imagen conceptual o con la intención espacial.
- Aprobar la franja de circulación y el nivel de libertad de movimiento en profundidad.
- Aprobar el plano antes de convertir estas coordenadas en un mapa técnico de colisiones y hotspots.

**Importante:** esta propuesta no modifica el canon narrativo. Tampoco declara aprobada la distribución: fija un primer plano cuantificado para poder revisarlo con precisión.

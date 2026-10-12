# WNL — Mapa general de funcionamiento de la novela
**Fecha:** 2026-10-12  
**Proyecto:** WATH NEVER LEFT  
**Estado:** mapa de trabajo; distingue canon documentado, preferencias exploratorias y dudas de continuidad. No modifica CANON ni el manuscrito.

> Principio rector: **Él vive las realidades. El lector descubre qué significan.**

## 1. Diagrama principal — mecánica, experiencia y misterio

```mermaid
flowchart TD
  classDef canon fill:#e5f2ff,stroke:#28649b,color:#132b43,stroke-width:1.5px
  classDef idea fill:#fff2d5,stroke:#ab7817,color:#48330b,stroke-dasharray:5 4
  classDef pending fill:#ffe8e8,stroke:#a33b3b,color:#501d1d,stroke-dasharray:3 3
  classDef story fill:#e8f5e9,stroke:#3f7c4b,color:#163e20

  subgraph MECHANIC["CICLO DE EXPERIENCIA — REGLAS DOCUMENTADAS"]
    W["Una de las 10 Ventanas<br/>vive una realidad por vez"]:::canon
    WS{"¿Se duerme?"}:::canon
    WWAIT["Permanece en esa Ventana.<br/>El tiempo mínimo todavía puede completarse."]:::canon
    WCHECK{"¿Transcurrieron al menos<br/>24 horas desde su llegada?"}:::canon
    ROOM["Habitación<br/>es real, no tiene puerta<br/>y posee tiempo propio"]:::canon
    RS{"¿Se duerme?"}:::canon
    RWAIT["Permanece en la Habitación.<br/>Puede seguir despierto indefinidamente."]:::canon
    RCHECK{"¿Transcurrieron al menos<br/>24 horas en la Habitación?"}:::canon
    NEXT["El sueño posterior al mínimo<br/>lo lleva automáticamente<br/>a otra Ventana no elegida"]:::canon

    W --> WS
    WS -- "No" --> WWAIT
    WWAIT --> WS
    WS -- "Sí" --> WCHECK
    WCHECK -- "No: aún no hay tránsito" --> W
    WCHECK -- "Sí: el sueño activa la salida" --> ROOM
    ROOM --> RS
    RS -- "No" --> RWAIT
    RWAIT --> RS
    RS -- "Sí" --> RCHECK
    RCHECK -- "No: aún no hay tránsito" --> ROOM
    RCHECK -- "Sí: el sueño activa la salida" --> NEXT
    NEXT --> W
  end

  subgraph RULES["OTRAS REGLAS DEL MUNDO"]
    TIMEADV["Las Ventanas ausentes avanzan durante<br/>las horas que él duerme fuera de ellas;<br/>las horas despierto en otra no se suman."]:::canon
    DEATH["Si muere en una Ventana,<br/>la muerte no activa el tránsito<br/>ni lo devuelve a la Habitación."]:::canon
    IDENTITY["La misma identidad/conciencia existe<br/>en las diez realidades; solo experimenta<br/>conscientemente una a la vez."]:::canon
    MEM["Recuerda todo lo vivido en las demás Ventanas;<br/>no hereda automáticamente recuerdos<br/>de la versión local."]:::canon
    TIMEADV -. "regla temporal al volver" .-> W
    IDENTITY --> MEM
  end

  subgraph STORY["CÓMO SE CUENTA"]
    POV["Primera persona estricta.<br/>El lector solo sabe lo que él percibe,<br/>recuerda, interpreta o descubre."]:::story
    MYSTERY["Las pistas son reales, pero incompletas.<br/>No todas las anomalías tienen que conectarse.<br/>No explicar pronto qué es él ni quién creó todo."]:::story
    LOCAL["Cada Ventana puede tener su propio conflicto<br/>y puede revisitase en otro capítulo.<br/>Los objetivos concretos siguen en desarrollo."]:::story
    GLOBAL["Dirección global explorada:<br/>descubrir el patrón y encontrar cómo romperlo.<br/>Su estatus debe unificarse en la documentación."]:::pending
    POV --> MYSTERY --> LOCAL
    LOCAL -. "posible dirección global" .-> GLOBAL
  end

  subgraph ILLNESS["ENFERMEDAD — PREFERENCIA EXPLORATORIA, NO CANON"]
    I1["Está presente en todas las realidades.<br/>No explica los desplazamientos."]:::idea
    I2["Deterioro físico y tiempo de vida perdido<br/>continúan; cambiar no lo salva ni reinicia la cuenta."]:::idea
    I3["Evolución irregular:<br/>aparentes mejoras y recaídas bruscas."]:::idea
    I4["Puede afectar cuerpo, mente<br/>o ambos, según lo que requiera cada Ventana."]:::idea
    I5["Efecto dramático: hace creer que todavía hay tiempo<br/>y puede impedirle actuar cuando más lo necesita."]:::idea
    I6["Problema sin resolver: cómo progresa la enfermedad<br/>entre cuerpos con relojes locales distintos."]:::pending
    I1 --> I2 --> I3 --> I4 --> I5
    I2 -. "requiere coherencia temporal" .-> I6
  end

  W -. "experiencia actual" .-> POV
  IDENTITY -. "una conciencia, experiencias múltiples" .-> POV
  W -. "puede manifestarse aquí" .-> I1
```

## 2. Qué significa el ciclo, explicado sin tecnicismos

- Hay exactamente diez Ventanas y la Habitación. Todas son reales para el protagonista mientras las experimenta; no sabe de antemano cuál sería una realidad «verdadera».
- El sueño es el disparador, pero no basta por sí solo: deben haber transcurrido al menos 24 horas en la estancia correspondiente. Las 24 horas no significan que deba mantenerse despierto. Dormirse antes del mínimo no desplaza.
- Después de cumplirse el mínimo, el siguiente sueño lo devuelve de una Ventana a la Habitación o lo lleva de la Habitación a una nueva Ventana. No elige conscientemente el destino.
- La Habitación posee continuidad temporal propia durante su estancia. Las Ventanas ausentes avanzan durante las horas que él duerme fuera de ellas; las horas despierto en otras no se suman a sus relojes.
- Morir en una Ventana no lo devuelve a la Habitación ni provoca otro tránsito. Para él, la muerte significa morir; no conoce una salida mediante ella.
- La misma identidad/conciencia existe en las diez realidades, pero solo experimenta una conscientemente a la vez. La hipótesis de que la conciencia pueda existir separada del cuerpo y el cerebro funcionar como interfaz es una posibilidad filosófica de ficción, no una explicación científica demostrada.

## 3. Las diez Ventanas — inventario interno

Estos son los conceptos registrados en CANON/VENTANAS.md. **No deben asignarse automáticamente a los capítulos V3:** el repositorio advierte que las correspondencias de la reescritura todavía deben revisarse.

| Ventana | Concepto registrado | Estado anotado en el archivo |
|---|---|---|
| 1 | 1999 — Y2K; el desastre temido ocurre y la historia diverge | Pendiente de uso |
| 2 | 2012 — CERN/LHC; experimentos vinculados a una posible catástrofe global | Usada en el manuscrito anterior, capítulo 2 |
| 3 | 2014 — Vida cotidiana; vida aparentemente normal | Asociada al prólogo V2; revisar para V3 |
| 4 | 2026 — Cortexia | Pendiente de uso/adaptación |
| 5 | 2056 — Las Siete Arquitecturas autónomas | Desarrollada en capítulos 7–8 del manuscrito anterior |
| 6 | Bajo la Ciudad — La Puerta Inexplicable | Usada en el capítulo 1 del manuscrito anterior |
| 7 | La Casa que Recuerda — familia, sótano, puerta y llave | Usada y revisitata en el manuscrito anterior |
| 8 | La Ciudad que Despierta — ciudad vacía pero funcional | Asociada al capítulo 4 del manuscrito anterior |
| 9 | El Mundo Perfecto — realidad en la que no desea marcharse | Pendiente de uso |
| 10 | Copia Exacta — realidad idéntica al mundo externo | Pendiente de uso |

El orden en que aparecen las Ventanas no indica su orden cronológico ni su importancia. Una misma Ventana puede reaparecer en varios capítulos.

## 4. Enfermedad — todo lo elegido hasta ahora, todavía no canon

- La misma enfermedad está presente en todas las realidades; cambiar no lo salva, no reinicia el deterioro ni devuelve el tiempo de vida perdido.
- Su manifestación será irregular: puede mejorar aparentemente y empeorar bruscamente.
- Puede afectar tanto al cuerpo como a la mente; qué manifestación usar dependerá de la Ventana y de su situación narrativa. Todavía no se han asignado síntomas concretos a Ventanas específicas.
- El efecto emocional buscado combina dos cosas: le hace creer que aún tiene tiempo cuando casi no le queda y puede quitarle la capacidad de actuar cuando más lo necesita.
- La enfermedad no explica los desplazamientos ni debe revelar prematuramente la arquitectura de la novela.
- Los síntomas pueden fluctuar, pero la preferencia es que el deterioro y el tiempo perdido no retrocedan.
- No se han elegido nombre, diagnóstico, síntomas fijos, desencadenantes ni mecanismo médico.

### Nudo crucial aún no resuelto

El reloj de una Ventana ausente avanza durante las horas que el protagonista duerme fuera de ella. Sigue pendiente diseñar con precisión cómo se refleja la progresión de la enfermedad en cuerpos y experiencias diferentes, manteniendo la preferencia de que el deterioro y el tiempo de vida perdido no se reinicien al cambiar de realidad.

## 5. Dirección narrativa y prólogo

- Narración estrictamente en primera persona: nada de información que el protagonista no pueda percibir, recordar, interpretar o descubrir.
- Principio guía: él vive las realidades; el lector descubre qué significan. Las pistas pueden ser ciertas sin que su significado se explique de inmediato.
- Proteger los misterios centrales: qué es realmente el protagonista, quién o qué creó la Habitación, qué significa la anomalía de la H y cuál es la arquitectura última del universo.
- Las conexiones entre Ventanas deben crecer solo cuando la historia lo necesite; no hacer que cada detalle extraño forme parte de un único rompecabezas.
- Preferencias de apertura: empezar dentro de una sola vida/realidad, sin abrir con la Habitación ni explicar otras realidades; evitar fechas y años al comienzo; no usar la desaparición pública de un avión ni «el mundo lo busca» como motor. Se busca un gancho cinematográfico y misterio, no una explicación temprana.
- La Habitación no tiene puerta y no debe aparecer al comienzo del prólogo según la dirección editorial expresada por el autor.

## 6. Estado real de la reescritura V3

- Hay borradores activos para prólogo y capítulos 1–4.
- El capítulo 4 V3 ocurre a bordo del velero Nereida: el protagonista está herido, no recuerda cómo llegó ni cómo se lesionó, el motor no arranca, la radio solo emite estática y los ruidos reciben explicaciones físicas dentro del propio capítulo.
- El capítulo 5 V3 no tiene una narración activa aprobada: la versión anterior fue descartada por el autor y debe replantearse desde cero.
- No hay conexiones confirmadas entre el velero, el prólogo y los capítulos 1–3.
- La asignación de las Ventanas a los capítulos V3 sigue pendiente de una revisión explícita.

## 7. Hipótesis relacionadas, pero aún no canonizadas

- La conciencia podría existir de algún modo independiente del cuerpo y el cerebro actuar como receptor/interfaz. Es una premisa de ficción que se explora, no un hecho científico demostrado.
- Está confirmado en CANON que el protagonista recuerda todo lo vivido por él en las demás Ventanas. Eso no implica heredar automáticamente los recuerdos personales de la versión local.
- La Habitación está confirmada como otra realidad donde el protagonista está encerrado al principio; no se explicará inicialmente qué es ni por qué está allí. Que más adelante registre o compare pistas puede desarrollarse orgánicamente, pero no hay que presentarla desde el comienzo como un centro de investigación que él comprende.
- Cada Ventana puede tener un conflicto local y coexistir con una dirección global de comprender el patrón y romperlo; la definición de objetivos concretos todavía está en desarrollo.
- El sueño real compartido por el autor —desastre accidental en unas escaleras, soledad ante una responsabilidad imposible, culpa, persecución y terror— está disponible como inspiración emocional, no como trama obligatoria ni canon.

## 8. Estado de decisiones y preguntas que siguen abiertas

Las aclaraciones siguientes fueron confirmadas por el autor el 2026-10-12 y deben reflejarse de forma consistente en los documentos operativos:
1. **Tiempo en Ventanas ausentes:** avanzan las horas que el protagonista duerme fuera de ellas, no las horas que permanece despierto en otra Ventana.
2. **Memoria:** recuerda todo lo vivido por él en las demás Ventanas, sin heredar automáticamente los recuerdos de la versión local.
3. **Habitación:** es otra realidad en la que está encerrado al principio; no se explicará de inmediato su naturaleza ni el motivo del encierro.
4. **Muerte:** no activa el tránsito. Si muere en una Ventana, muere en esa experiencia; para él, morir es el final y no conoce una salida mediante la muerte.

Pendientes que no se resuelven mediante estas aclaraciones:
- El mecanismo específico de la enfermedad y la forma de representar su progresión física y mental a través de realidades.
- Los síntomas concretos de la enfermedad y su asignación, si corresponde, a Ventanas específicas.
- La naturaleza última de la conciencia, el origen de la Habitación y las razones por las que existe el sistema de Ventanas.
- Los objetivos completos de las diez Ventanas y la forma de revelar gradualmente el objetivo o patrón global.
- La revisión explícita de las asignaciones de Ventanas a los capítulos V3, ya que parte del mapa procede de la versión anterior.

## 9. Leyenda de estado

- **Canon documentado:** regla escrita en los archivos operativos vigentes, salvo las inconsistencias señaladas.
- **Preferencia exploratoria:** dirección escogida por el autor para investigar, pero que no debe aplicarse como regla fija a la trama.
- **Pendiente:** pregunta, mecanismo o asignación que todavía no ha sido decidido.
- **Material histórico:** capítulos o mapas anteriores que ayudan a entender el proyecto, pero no deben imponerse automáticamente sobre la reescritura V3.

**Este archivo es un mapa de trabajo, no un reemplazo de la Biblia Maestra. No modifica CANON ni el manuscrito.**

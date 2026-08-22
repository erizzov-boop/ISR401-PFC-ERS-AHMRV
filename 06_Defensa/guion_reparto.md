# Guion de reparto — Defensa PE5

**SIMPA** · Equipo AHMRV · ISR-401 · UTEQ

17 diapositivas · **20 minutos de exposición + 10 de preguntas** · seis bloques de unos 3 min 20 s

---

## Regla que gobierna todo

> El tribunal no evalúa que cada uno domine su parte. Evalúa que **cualquiera pueda responder sobre
> cualquier parte**. El reparto es de la exposición, no del conocimiento.

El criterio C5 nivel N4 dice: *cada integrante domina el proyecto completo; las respuestas se anclan
en artefactos concretos; se reconocen limitaciones con criterio técnico*. Un bloque bien expuesto y
una respuesta vacía sobre otro bloque bajan la nota individual, no la del compañero.

---

## Reparto por bloques

| Bloque | Integrante | Diapositivas | Tiempo | Contenido |
|---|---|---|---|---|
| 1 | **Villafuerte, Allan** | 1–3 | 3:20 | Portada, problema, sistema y stakeholders |
| 2 | **Huilcapi, Denisses** | 4–6 | 3:20 | Proceso PE1–PE5, ERS en cifras, requisitos clave |
| 3 | **Macías, Josthyn** | 7–8 | 3:20 | Modelos UML, inspección formal y CCB |
| 4 | **Alcívar, Anderson** | 9–10 | 3:20 | Trazabilidad, sincronización, métricas |
| 5 | **Arboleda, Francisco** | 11–12 | 3:20 | Componentes de IA, límites del sistema |
| 6 | **Rizzo, Edson** | 13–16 | 3:20 | Lecciones, mejoras, conclusiones, artefactos |
| — | Los seis | 17 | — | Preguntas, de pie |

El reparto sigue el rol de cada uno: el analista líder abre con el problema y el cliente; la
documentadora expone la estructura del ERS; el modelador defiende los diagramas; el responsable del
repositorio y del tablero lleva trazabilidad y métricas; quien construyó los DFD y la §9 expone los
componentes de IA; el verificador cierra con lo que la auditoría enseñó.

---

## Qué decir en cada bloque

### Bloque 1 — Allan · diapositivas 1 a 3

**Diap. 1 (20 s).** Nombre del sistema, equipo, cliente. No leer la diapositiva.

**Diap. 2 (1:30).** Los cuatro problemas. Anclar cada uno en su evidencia: la asesoría visita cada
quince días (EV-02); la extractora penaliza desde el 3 % (EV-04); el 11,3 % del personal no tiene
teléfono (EV-12); el cálculo manual consume una jornada semanal (EV-13).

> **Frase clave:** «Ninguno de estos cuatro problemas es una suposición nuestra. Los cuatro salen de
> entrevistas con nombre y fecha.»

**Diap. 3 (1:30).** Seis clases de usuario. Mencionar que la planta extractora es actor externo y no
clase de usuario, y que confundir ambas cosas fue el defecto DR-05: falseaba el denominador de M1c.

### Bloque 2 — Denisses · diapositivas 4 a 6

**Diap. 4 (1:10).** La progresión PE1→PE5. No enumerar entregables: explicar que cada unidad añade
una propiedad comprobable, no volumen.

> **Frase clave:** «La Unidad V no produjo un ERS mejor. Produjo el instrumento capaz de decir si lo
> era.»

**Diap. 5 (1:10).** Las cifras y los siete bloques. Señalar que la prioridad MoSCoW está justificada
requisito a requisito, no asignada en bloque.

**Diap. 6 (1:00).** Los cinco requisitos clave. Uno solo en detalle —RF-37, la liquidación— y el
resto en una frase. Es la diapositiva donde más se tiende a alargarse.

### Bloque 3 — Josthyn · diapositivas 7 a 8

**Diap. 7 (1:30).** Los seis modelos. Insistir en dos puntos: el diagrama de clases es conceptual,
no son tablas de base de datos; y los DFD se produjeron porque M4 no podía calcularse sin el eslabón
de proceso.

> **Frase clave:** «Es el único caso de la auditoría en que medir obligó a construir.»

**Diap. 8 (1:50).** La inspección: 33 defectos, 0,52 por página, el 100 % de críticos y mayores
corregidos. Después las dos tarjetas, que son las que responden preguntas: ninguna RFC rechazada, y
RFC-03 aprobada pese a empeorar la cobertura del MVP.

### Bloque 4 — Anderson · diapositivas 9 a 10

**Diap. 9 (1:40).** Trazabilidad: 73 filas, 100 %, cero huérfanos, tres vacíos declarados. Después
la sincronización, que es lo delicado: el 67,1 % y el 58,5 % son **dos lecturas del mismo estado**,
no dos momentos.

> **Frase clave:** «El indicador que debía medir la desincronización estaba él mismo mal calibrado:
> ignorábamos no solo cuántos elementos faltaban, sino cuántos debían estar.»

**Diap. 10 (1:40).** El gráfico y el 3,70. Explicar M6 con calma: no es un fallo del trabajo, es la
señal de que la re-inspección se hizo de verdad.

### Bloque 5 — Francisco · diapositivas 11 a 12

**Diap. 11 (1:40).** Los dos componentes con sus umbrales cuantificados. Mencionar la exclusión de
la cuadrilla en IA-02 antes de que la pregunten: es una decisión declarada, no un olvido.

**Diap. 12 (1:40).** Los seis límites. Esta diapositiva anticipa la mitad de las preguntas del
tribunal y es la que sostiene el «se reconocen limitaciones con criterio técnico» de N4.

> **Frase clave:** «Declarar el límite es parte de la especificación, no una disculpa.»

### Bloque 6 — Edson · diapositivas 13 a 16

**Diap. 13 (1:00).** Las cuatro lecciones. Salen de la retrospectiva, no son genéricas.

**Diap. 14 (1:00).** Las cuatro mejoras, cada una con responsable nominal.

**Diap. 15 (1:00).** Las cinco conclusiones. Leerlas despacio: son el cierre argumental.

**Diap. 16 (20 s).** El mapa de artefactos. Dejarla proyectada durante las preguntas.

---

## Las preguntas

Los seis permanecen de pie. La diapositiva 16 queda proyectada como índice: cada respuesta señala
el artefacto que la respalda.

### Reparto de respuesta

El tribunal elige a quién pregunta. Si no lo hace, responde quien expuso el bloque, **salvo** que la
pregunta cruce bloques: entonces responde quien tenga el artefacto más cerca.

Nadie corrige a un compañero en voz alta. Si una respuesta quedó incompleta, se completa después con
«añado un dato», no con «lo que quiso decir es».

### Las cinco respuestas que hay que llevar preparadas

**1. ¿Qué RFC rechazó el CCB?**
Ninguna. Las tres reparaban defectos cuya corrección añadía alcance; rechazarlas habría dejado
abierto un defecto crítico o mayor. Sí se rechazó una alternativa dentro de RFC-03: diferir todo a
la Entrega 4. *Artefacto: acta del CCB en `03_CCB/`.*

**2. ¿Cómo saben que las correcciones no introdujeron defectos nuevos?**
No se sabe con certeza. Se hicieron tres comprobaciones y ninguna las cubre todas. Decirlo así.
*Artefacto: §5 del informe.*

**3. M6 no cumple. ¿Por qué no lo corrigieron?**
Porque el numerador es un hecho sobre la inspección anterior, no sobre el ERS actual. Los siete
defectos están reparados; repararlos no cambia cuántos escaparon. Un 0,00 habría sido la señal
sospechosa. *Artefacto: hoja `Reinspeccion_M6` del Anexo A.*

**4. M3 pasó de 39,3 % a 100 %. ¿Bajaron el listón?**
No se cambió ningún umbral ni se especificó ningún requisito nuevo. Los 37 criterios reescritos
conservan valor, unidad y método. Cambió la forma de enunciar la condición, no su contenido.
*Artefacto: Apéndice F del ERS.*

**5. ¿Por qué aprobaron RFC-03 si empeoró la cobertura del MVP?**
Porque cerraba un deber legal derivado de la LOPDP. La cobertura bajó del 38,1 % al 33,3 % porque
el denominador de Must creció. Un CCB que solo aprueba lo que mejora sus indicadores administra
apariencia, no gobierna alcance. *Artefacto: RFC-03 en `03_CCB/`.*

> El banco completo de 22 preguntas con respuestas está en el **Anexo B del informe**. Repartirlo
> antes del ensayo y hacer muestreo cruzado: cada uno responde preguntas de bloques ajenos.

### Si no se sabe la respuesta

Decirlo y señalar dónde se buscaría. «No tengo el dato exacto, está en la matriz, fila TR-xx» vale
más que una cifra inventada. Una cifra que el tribunal comprueba y no cuadra contamina todo lo
demás.

---

## Ensayo

| Paso | Qué hacer |
|---|---|
| 1 | Cada uno cronometra su bloque a solas. Si pasa de 3:30, recortar antes de ensayar en grupo |
| 2 | Pasada completa con reloj. Anotar dónde se pierde tiempo, sin interrumpir |
| 3 | Segunda pasada solo con los bloques que se pasaron |
| 4 | **Muestreo cruzado**: cada uno responde cinco preguntas del banco sobre bloques que no expone |
| 5 | Verificar cifra por cifra contra el informe. Una sola cifra mal en la exposición contradice el documento |

**Las transiciones se ensayan.** El paso de un expositor a otro es donde se pierden treinta
segundos. Cada uno cierra con una frase que enlace con lo siguiente, no con «bueno, ya».

---

## Cifras que hay que saber de memoria

| Concepto | Valor |
|---|---|
| Requisitos funcionales / no funcionales | 42 / 19 |
| Requisitos de IA | 18 (6 RF-IA + 12 RNF-IA) |
| Total auditado | 61 |
| Casos de uso | 18, todos especificados |
| Páginas ERS / informe | 106 / 55 |
| Defectos de la inspección | 33 (4 críticos, 24 mayores, 5 menores) |
| Densidad de defectos | 0,52 por página |
| Defectos residuales | 7 |
| M6 | 0,11 frente a 0,05 de referencia |
| Valoración ponderada | 3,70 sobre 4,00 |
| Filas de la matriz | 73, todas completas |
| Elementos en el tablero | 175 (10 epics, 79 stories, 86 sub-tasks) |
| Sincronización | 58,5 % inicial real → 100 % |
| Cobertura del MVP | 38,1 % sobre 21 Must · 33,3 % sobre 24 |

Si alguien duda de una cifra en plena defensa, **no la inventa**: remite al artefacto.

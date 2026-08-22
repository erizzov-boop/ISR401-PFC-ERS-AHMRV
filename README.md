# SIMPA — Sistema Inteligente de Mantenimiento de Palma Africana

Especificación de Requisitos de Software y auditoría de calidad para una unidad productiva de palma
africana de 100 hectáreas en el cantón El Empalme, provincia del Guayas.

**Práctica Experimental 5 · Unidad V** · Ingeniería de Requerimientos (ISR-401) · 4.º nivel
Carrera de Software · Facultad de Ciencias de la Computación · Universidad Técnica Estatal de Quevedo
Periodo 2026–2027 PPA · Docente: Ing. Gleiston Cicerón Guerrero Ulloa, PhD

---

## 1. Equipo AHMRV — Paralelo 4to "A"

| Integrante | Rol | GitHub |
|---|---|---|
| Villafuerte Rosero Allan Noe | Analista líder | [`AlanNVR`](https://github.com/AlanNVR) |
| Huilcapi León Denisses Fabiola | Documentadora | [`huilcapi`](https://github.com/huilcapi) |
| Rizzo Vélez Edson Nagib | Verificador | [`erizzov-boop`](https://github.com/erizzov-boop) |
| Macías Herrera Josthyn Esteban | Modelador | [`jmaciasherr4`](https://github.com/jmaciasherr4) |
| Arboleda Yanza Francisco Javier | Apoyo modelado | [`farboleday-wq`](https://github.com/farboleday-wq) |
| Alcívar Vélez Anderson Adonis | Apoyo repositorio | [`AdonisAlcivar`](https://github.com/AdonisAlcivar) |

El repositorio suma **81 _commits_** distribuidos entre los seis integrantes. La tabla de aporte
individual del Anexo C del informe declara el recuento al corte del 21/08/2026, previo al cierre
documental; los movimientos posteriores a ese corte no se contabilizan allí.

---

## 2. Cómo reproducir los PDF

Los dos documentos se generan desde sus fuentes LaTeX. No hay figuras externas que descargar: las
del ERS están versionadas en `01_ERS/img/` y las del informe se dibujan en TikZ y pgfplots durante
la compilación.

### 2.1 Requisitos

| Componente | Versión de referencia | Notas |
|---|---|---|
| Distribución TeX | TeX Live 2023 o posterior | También sirve MiKTeX 23+ u Overleaf |
| Motor | `pdflatex` | No usar XeLaTeX ni LuaLaTeX: el preámbulo emplea `inputenc` |
| Bibliografía | `bibtex` | No `biber` |

Paquetes empleados, todos incluidos en una instalación completa de TeX Live:

`inputenc` · `fontenc` · `babel` (spanish) · `geometry` · `graphicx` · `xcolor` · `array` ·
`longtable` · `booktabs` · `colortbl` · `multirow` · `float` · `caption` · `enumitem` · `hyperref` ·
`fancyhdr` · `tikz` · `pgfplots` · `amsmath` · `amssymb` · `url`

Con una instalación mínima: `sudo tlmgr install collection-latexextra collection-langspanish pgfplots`

### 2.2 Compilar el informe de la PE5

```bash
git clone https://github.com/erizzov-boop/ISR401-PFC-ERS-AHMRV.git
cd ISR401-PFC-ERS-AHMRV/05_Informe

pdflatex PE5_U5_PFC_ALCIVAR_ARBOLEDA_HUILCAPI_MACIAS_RIZZO_VILLAFUERTE
bibtex   PE5_U5_PFC_ALCIVAR_ARBOLEDA_HUILCAPI_MACIAS_RIZZO_VILLAFUERTE
pdflatex PE5_U5_PFC_ALCIVAR_ARBOLEDA_HUILCAPI_MACIAS_RIZZO_VILLAFUERTE
pdflatex PE5_U5_PFC_ALCIVAR_ARBOLEDA_HUILCAPI_MACIAS_RIZZO_VILLAFUERTE
```

**Archivo principal:** `PE5_U5_PFC_ALCIVAR_ARBOLEDA_HUILCAPI_MACIAS_RIZZO_VILLAFUERTE.tex`
**Resultado esperado:** 55 páginas, sin errores, sin citas ni referencias cruzadas sin resolver.

Las cuatro pasadas son necesarias: la primera genera los archivos auxiliares, `bibtex` resuelve las
citas, y las dos últimas fijan el índice, los índices de tablas y las referencias cruzadas.

El archivo principal carga trece secciones y cuatro tablas mediante `\input`: `sec1_introduccion`,
`sec2_metodologia`, `sec3_ers`, `tabla_rf`, `tabla_rnf`, `sec4_uml`, `sec5_validacion`,
`tabla_defectos`, `sec6_gestion`, `tabla_e2e`, `sec7_ia`, `sec8_metricas`, `sec9_retrospectiva`,
`sec10_conclusiones` y `anexos`. Todos deben estar en el mismo directorio.

### 2.3 Compilar el ERS

```bash
cd ../01_ERS

pdflatex ERS_SRS_2A
bibtex   ERS_SRS_2A
pdflatex ERS_SRS_2A
pdflatex ERS_SRS_2A
```

**Archivo principal:** `ERS_SRS_2A.tex`
**Resultado esperado:** 106 páginas, sin errores.

Carga seis archivos por `\input` —`seccion4_uml`, `seccion5_priorizacion`,
`seccion6_7_mvp_conclusiones`, `seccion8_dfd`, `seccion9_ia`, `cu_11_18`, `apendices` y
`apendice_bdd`— e incluye catorce figuras PDF vectoriales desde `img/`.

### 2.4 Verificación de reproducibilidad

Ambos documentos se han compilado desde una clonación limpia del repositorio, con el resultado
siguiente:

| Documento | Páginas | Errores | Citas sin resolver |
|---|---|---|---|
| ERS v1.1 | 106 | 0 | 0 |
| Informe PE5 | 55 | 0 | 0 |

Los PDF versionados en `01_ERS/ERS_v1_1.pdf` y `05_Informe/PE5_U5_PFC_ALCIVAR_..._VILLAFUERTE.pdf`
coinciden en número de páginas con los que producen estas instrucciones.

### 2.5 En Overleaf

Subir el contenido de la carpeta correspondiente como proyecto nuevo, fijar el **Main document** al
archivo principal indicado arriba y el compilador a **pdfLaTeX**. La compilación automática de
Overleaf ejecuta las pasadas necesarias.

---

## 3. Estructura del repositorio

```
ISR401-PFC-ERS-AHMRV/
├── 01_ERS/              Especificación de Requisitos de Software v1.1
│   ├── ERS_SRS_2A.tex       archivo principal
│   ├── ERS_v1_1.pdf         compilado, 106 páginas
│   ├── seccion*.tex         secciones 4 a 9
│   ├── cu_11_18.tex         casos de uso CU-11 a CU-18
│   ├── apendices.tex        apéndices A a E
│   ├── apendice_bdd.tex     apéndice F, criterios Dado–Cuando–Entonces
│   ├── referencias.bib
│   └── img/                 14 figuras PDF vectoriales
│
├── 02_Auditoria/        Instrumentos de medición de calidad
│   ├── AnexoA_auditoria_calidad.xlsx    seis métricas ISO/IEC 25010, fórmulas vivas
│   └── AnexoB_registro_defectos.xlsx    33 defectos de la inspección formal
│
├── 03_CCB/              Change Control Board
│   ├── Acta_CCB.pdf
│   └── RFC-01.pdf · RFC-02.pdf · RFC-03.pdf
│
├── 04_Trazabilidad/     Trazabilidad extremo a extremo y tablero CASE
│   ├── matriz_e2e.xlsx      73 filas, cadena completa
│   ├── backlog_export.csv   exportación de Jira, 175 elementos
│   └── Capturas/            evidencia del tablero
│
├── 05_Informe/          Informe final de la PE5
│   ├── PE5_U5_PFC_ALCIVAR_..._VILLAFUERTE.tex   archivo principal
│   ├── sec1..sec10 · tabla_* · anexos.tex
│   └── referencias.bib
│
├── 06_Defensa/          Material de la defensa técnica
│   ├── PE5_Defensa_AHMRV.pptx · .pdf
│   └── guion_reparto.md
│
├── CHANGELOG.md         Historial de cambios del ERS
└── .gitignore
```

---

## 4. Qué contiene el proyecto

### 4.1 El sistema

SIMPA registra la labor agrícola de campo, diagnostica plagas y deficiencias nutricionales por
análisis de imagen, estima la producción y liquida el avance semanal del personal. Se especifica
para una unidad productiva real con seis clases de usuario: administrador, jefe de polinización,
operario de campo, técnico fitosanitario, asesor técnico y la planta extractora como actor externo.

### 4.2 Cifras del ERS

| Concepto | Valor |
|---|---|
| Requisitos funcionales | 42 — 24 *Must*, 16 *Should*, 2 *Could* |
| Requisitos no funcionales | 19, mapeados sobre ISO/IEC 25010:2023 |
| Requisitos de inteligencia artificial | 18 — 6 `RF-IA` y 12 `RNF-IA` |
| Restricciones de diseño / legales | 10 / 8 |
| Casos de uso | 18, todos con especificación textual |
| Criterios de aceptación | 61 — 24 `CA-xx` y 37 `CB-xx` en formato Gherkin |
| Filas de trazabilidad | 73, con cadena completa |
| Páginas | 106 |

### 4.3 Auditoría de calidad

Seis métricas derivadas de ISO/IEC 25010:2023 e ISO/IEC/IEEE 29148:2018, calculadas sobre conteos
obtenidos por análisis programático de las fuentes LaTeX. Los patrones de conteo se declaran en la
hoja `Conteos_base` del Anexo A, de modo que cualquier evaluador pueda reproducir cada número.

| Métrica | Antes | Después | Referencia | |
|---|---|---|---|---|
| M1a Completitud de atributos | 98,4 % | 100 % | ≥ 95 % | ✅ |
| M1b Especificación de casos de uso | 55,6 % | 100 % | 100 % | ✅ |
| M1c Cobertura de actores | 75,0 % | 100 % | 100 % | ✅ |
| M2 Consistencia | 0,990 | 0,990 | ≥ 0,98 | ✅ |
| M3 Verificabilidad | 39,3 % | 100 % | ≥ 90 % | ✅ |
| M4 Trazabilidad | 100 % | 100 % | ≥ 90 % | ✅ |
| M5 Modificabilidad | 2,20 | 2,20 | ≤ 3,0 | ✅ |
| **M6 Corrección** | **0,11** | **0,11** | ≤ 0,05 | ❌ |

**Valoración ponderada: 3,70 sobre 4,00.**

**M6 se reporta sin corregir, y es deliberado.** Mide qué proporción de defectos escapó a la
inspección formal de la Unidad IV: siete defectos residuales sobre sesenta y un requisitos. Los
siete están reparados, pero repararlos no altera el numerador, porque el numerador es un hecho
sobre la eficacia de aquella inspección y no sobre el estado actual del documento. Bajar la cifra
exigiría declarar una re-inspección que no se hizo. La acción correctiva registrada es de proceso
—ampliar la lista de verificación a apéndices y conteos globales— y consta como elemento `S2` de la
retrospectiva.

### 4.4 Sincronización con el tablero CASE

El tablero de Jira contiene **175 elementos**: 10 epics, 79 *stories* y 86 *sub-tasks*. Todo
elemento especificado en el ERS tiene correspondencia en el tablero.

La cifra publicada al cierre de la Unidad IV fue 67,1 %, calculada sobre un denominador que no
contabilizaba los diecinueve requisitos no funcionales ni los doce `RNF-IA`. Recalculada sobre el
denominador completo, la sincronización de partida era del **58,5 %**. Ambas cifras y su
justificación constan en la hoja `Sincronizacion` de `matriz_e2e.xlsx` y en la §6 del informe.

---

## 5. Numeración de versiones

Conviven dos numeraciones y conviene no confundirlas:

| Numeración de la asignatura | Revisión interna del ERS | Contenido |
|---|---|---|
| — | 1.0 | Entrega 1A: planificación y elicitación |
| — | 1.1 | Correcciones docentes de la 1A |
| — | 2.0 | Entrega 1B: requisitos, UML, MoSCoW, trazabilidad parcial |
| **v1.0** | 3.0 | Entrega 2A: catálogo completo, i*, historias de usuario |
| **v1.1** | 3.1 | Línea base aprobada por el CCB, actualizada en la Unidad V |

La versión que este repositorio contiene es la **v1.1**, actualizada en sitio tras la re-inspección
de la PE5. No se abrió una v1.2 porque el alcance y el catálogo de requisitos no cambiaron. El
detalle de qué se añadió, cambió y no se corrigió está en [`CHANGELOG.md`](CHANGELOG.md).

---

## 6. Estándares y referencias

- **ISO/IEC/IEEE 29148:2018** — estructura del ERS y características de un buen conjunto de requisitos
- **ISO/IEC 25010:2023** — modelo de calidad de producto, taxonomía de requisitos no funcionales
- **ISO/IEC/IEEE 15288:2023** y **12207:2017** — procesos del ciclo de vida
- **Reglamento (UE) 2024/1689** — clasificación de riesgo de los componentes de inteligencia artificial
- **LOPDP** (Ecuador) — requisitos legales `RL-01` a `RL-08` y funcionales `RF-40` a `RF-42`
- Pohl · SWEBOK v4.0 · PMBOK 7.ª ed. · IREB CPRE FL · Vogelsang & Borg

---

## 7. Aviso de uso

Documento académico. La información sobre la unidad productiva se emplea con fines exclusivamente
educativos y se encuentra anonimizada en lo relativo a datos personales. Los requisitos `RF-40` a
`RF-42` especifican los derechos de exportación, rectificación y supresión conforme a la LOPDP,
pero el sistema no ha sido implementado: este repositorio contiene su especificación, no su código.

# Entrega 1 — Formulación del proyecto y revisión de antecedentes

**Universidad Icesi · Maestría en Inteligencia Artificial Aplicada · 2026-2**  
**Proyecto:** Estimación de la severidad del uso problemático de internet en niños y adolescentes.  
**Autora:** Viviana Fernández Payán · [GitHub: vivianaf926](https://github.com/vivianaf926)  
**Estado:** formulación revisada; los experimentos y resultados cuantitativos propios deben documentarse cuando se ejecuten.

> Esta entrega presenta el problema, las relaciones conceptuales, la pregunta de investigación, los objetivos, el estado del arte y el plan de trabajo. La bibliografía completa y su verificación están en [docs/referencias.md](../docs/referencias.md).

## 1. Presentación y contexto

Internet forma parte de las actividades de aprendizaje, comunicación y entretenimiento de niños y adolescentes. Su uso puede considerarse problemático cuando se acompaña de dificultades de autorregulación e interferencias significativas en el funcionamiento cotidiano. El fenómeno no equivale simplemente a pasar muchas horas conectado; requiere considerar los comportamientos observados, el contexto y las consecuencias funcionales [1], [11], [12].

Se han descrito asociaciones entre uso problemático de internet y síntomas de ansiedad, depresión, déficit de atención y otras manifestaciones del bienestar psicológico [1], [3], [14]. Estas relaciones no deben interpretarse automáticamente como causales: distintos factores pueden compartir antecedentes o influirse mutuamente. Otros estudios han investigado los patrones de uso de aplicaciones, los factores psicosociales y los instrumentos para su detección [2], [5], [12].

El **Child Mind Institute**, mediante la competición *Child Mind Institute — Problematic Internet Use* en Kaggle, propuso explorar si medidas físicas, información demográfica y datos de actividad ayudan a estimar cuatro niveles ordinales de severidad del uso problemático de internet en participantes del estudio **Healthy Brain Network (HBN)** [10], [17]. La propuesta de este proyecto es académica: examina la viabilidad y las limitaciones de la estimación mediante aprendizaje automático, no sustituye una evaluación clínica.

## 2. Delimitación y formulación del problema

La evaluación del uso problemático de internet presenta retos conceptuales y operativos: existen diferentes instrumentos y criterios de medición, manifestaciones heterogéneas y barreras para acceder a valoraciones especializadas [5], [11], [17]. Estas dificultades motivan el interés por estudiar indicadores complementarios, sin presuponer que sean equivalentes a una prueba diagnóstica.

Desde el punto de vista de ciencia de datos, el reto se concreta en **determinar cuánto pueden aportar indicadores no derivados directamente del cuestionario PCIAT para estimar la categoría ordinal de severidad `sii`**, teniendo en cuenta valores faltantes, cobertura desigual de instrumentos, posibles desequilibrios entre clases y riesgo de fuga de información [10].

### 2.1. Árbol de problemas y sustento

El árbol siguiente **organiza relaciones conceptuales plausibles** identificadas en los antecedentes. No representa un análisis causal probado experimentalmente:

```mermaid
flowchart BT
    C1["Diversidad de instrumentos y criterios de medición [5, 11]"] --> P["Dificultad para evaluar oportunamente y de forma consistente el uso problemático de internet"]
    C2["Barreras de acceso a evaluación especializada [17]"] --> P
    C3["Manifestaciones psicológicas y conductuales heterogéneas [1, 3]"] --> P
    C4["Diferencias en aplicaciones y contextos de uso [2, 12]"] --> P
    P --> E1["Riesgo de necesidades de apoyo no reconocidas oportunamente"]
    P --> E2["Menor comparabilidad de evaluaciones"]
    P --> E3["Posible demora en orientación y seguimiento"]
    P --> E4["Extrapolación inadecuada de indicadores inespecíficos"]
```

*Figura 1. Síntesis conceptual de factores asociados a dificultades de evaluación y consecuencias potenciales. Los cuatro factores se apoyan en las fuentes citadas; las cuatro consecuencias se presentan como riesgos razonados, no como efectos causales cuantificados.*

El árbol presentado en la primera entrega, que incluía cuatro causas y cuatro consecuencias relacionadas con el fenómeno, se conserva aquí como **material histórico**, sin asumir que sus flechas demuestran causalidad:

![Árbol de problemas original elaborado para la primera entrega](https://github.com/user-attachments/assets/44881d0e-d3c6-472a-8771-b5769ef8152e)

*Figura 2. Árbol original de Viviana. Requiere distinguir factores asociados, antecedentes, posibles efectos y respaldo documental.*

### 2.2. Pregunta de investigación

> **¿En qué medida los modelos de aprendizaje automático pueden estimar los cuatro niveles de severidad del uso problemático de internet (`sii`) a partir de características demográficas, físicas y de comportamiento disponibles en HBN, y cuáles son las principales limitaciones de esa estimación?**

La investigación plantea una **estimación concurrente y retrospectiva**. No se dispone aquí de evidencia de que los predictores se hayan medido necesariamente antes del desenlace; por tanto, no se afirmará detección anticipada de casos futuros.

## 3. Objetivos del proyecto (criterios SMART)

### Objetivo general

Desarrollar y evaluar **antes de finalizar el periodo académico 2026-2** al menos **dos modelos supervisados** para estimar los **cuatro niveles de `sii`** a partir de variables del HBN, mediante validación cruzada estratificada de cinco particiones, utilizando el **coeficiente kappa cuadrático ponderado (QWK)** como métrica principal y **F1-macro** como métrica complementaria. Como meta académica **exploratoria**, se plantea alcanzar un QWK medio de al menos **0,35** y superar una línea base definida previamente.

*La meta de QWK es un criterio de trabajo propuesto; no es un resultado obtenido ni un umbral de validez clínica. Deberá interpretarse frente a la distribución de clases y la línea base.*

### Objetivos específicos

1. **Caracterizar la viabilidad del conjunto de datos** antes del entrenamiento mediante un informe que cuantifique participantes, disponibilidad de `sii`, distribución por nivel, proporción de datos faltantes, valores implausibles y criterios de inclusión y exclusión de variables.
2. **Construir al menos dos configuraciones reproducibles de predictores** con selección razonada de características y transformaciones documentadas, excluyendo la etiqueta `sii`, `PCIAT-PCIAT_Total` y campos que permitan reconstruir directamente el desenlace; ajustar imputación, codificación y escalamiento solo en entrenamiento.
3. **Entrenar y comparar al menos dos algoritmos supervisados** bajo el mismo esquema de validación estratificada de cinco particiones, documentando QWK, F1-macro, matriz de confusión y sensibilidad por categoría, especialmente para las clases minoritarias.
4. **Seleccionar y discutir el modelo mejor sustentado** antes del cierre académico, contrastándolo con la línea base y presentando un informe de errores, limitaciones de representatividad, condiciones de reproducibilidad y necesidades de validación externa.

Estos objetivos expresan resultados verificables. El análisis exploratorio y el preprocesamiento son medios para obtener productos concretos, no fines en sí mismos.

## 4. Antecedentes y estado del arte

### 4.1. Evidencia sobre medición y asociaciones

Gómez Salgado y colaboradores diseñaron y evaluaron un instrumento breve para detectar uso problemático de internet en adolescentes; reportaron **sensibilidad de 0,80 y especificidad de 0,81** en su estudio [5]. Por su parte, Kuss y Lopez-Fernandez revisaron estudios clínicos que muestran diversidad en la conceptualización y valoración del fenómeno [11]. Estos antecedentes justifican aclarar qué variable mide el proyecto antes de atribuir al algoritmo utilidad clínica.

Los trabajos de Ko y colaboradores [1], Yen y colaboradores [3] y van Rooij y colaboradores [12] examinaron asociaciones con síntomas psiquiátricos y patrones de utilización de aplicaciones. Fisoun y colaboradores [7] describieron asociaciones con experiencia de consumo de sustancias en un estudio transversal; sus resultados no establecen causalidad. Ninguno de esos estudios evalúa directamente el mismo problema ordinal `sii` del conjunto HBN.

### 4.2. Comparación de soluciones existentes

| Fuente | Método, resultado o aporte documentado | Limitación y relevancia para el proyecto |
|---|---|---|
| Gómez Salgado y colaboradores (2014) [5] | Desarrollo de instrumento de cribado; sensibilidad **0,80** y especificidad **0,81**. | Evalúa una herramienta psicométrica, no un clasificador de `sii` en HBN. |
| Hassani, Pakzad y Asghari (2018) [6] | Propone un marco de modelación predictiva para detectar patrones de uso problemático de internet. | No utiliza el reto HBN; se requiere revisar muestra, predictores y validación antes de comparar rendimientos. |
| Ioannidis y colaboradores (2016) [8] | Emplea aprendizaje automático para estudiar asociaciones entre uso problemático e impulsividad/compulsividad. | Participantes adultos y desenlace diferente; no es una validación de clasificación ordinal pediátrica. |
| Haupts (primer lugar Kaggle, 2025) [15] | Ensamble con LightGBM, XGBoost, CatBoost y ExtraTrees; regresión sobre puntuación total PCIAT y conversión posterior a `sii`. | Solución de competencia; el puesto no demuestra generalización clínica y el resultado depende del protocolo usado. |
| Agarwal (segundo lugar Kaggle, 2024) [16] | Estrategias diferenciadas de imputación y ampliación de particiones de validación cruzada sobre una base CatBoost. | El autor describe discrepancia entre resultados públicos y privados; es un reporte técnico de competencia. |

La revisión de Kato y colaboradores [4] aporta un marco general sobre modelos computacionales de adicciones conductuales, mientras que Probierz y colaboradores [9] exploran algoritmos predictivos en datos de ciencias sociales. Feng y colaboradores [13] emplearon conectividad cerebral, una modalidad no equivalente a los indicadores tabulares de este proyecto. Esos aportes deben considerarse antecedentes conceptuales o metodológicos, no resultados comparables sobre HBN.

**Brecha abordada:** los antecedentes incluyen soluciones de diferentes muestras y enfoques, pero el proyecto necesita una comparación propia y reproducible del aporte de grupos de variables, preprocesamiento y algoritmos, manteniendo constantes el esquema de validación y las métricas. Se analizará especialmente el efecto de las categorías minoritarias y la posibilidad de fuga de información. No se anticipan mejoras antes de ejecutar los experimentos.

### 4.3. Relación con las variables candidatas

En HBN se incluyen instrumentos demográficos, medidas corporales y de aptitud física, cuestionarios de sueño y actividad, categorías de uso de internet y actigrafía [10]. La disponibilidad y la oportunidad temporal de cada predictor deben comprobarse antes de incorporarlo. La asociación estadística entre una variable y `sii` no constituye por sí misma prueba causal ni criterio suficiente de selección.

Los dos cuadros de síntesis elaborados originalmente se mantienen como antecedentes visuales; esta comparación narrativa es la que fundamenta explícitamente método, hallazgos y límites:

![Cuadro original sobre modelos de aprendizaje automático](https://github.com/user-attachments/assets/14ee8b59-786c-40f2-a32e-ddccce452dfa)

*Figura 3. Cuadro original de modelos; interpretar junto con la tabla de comparación y las referencias corregidas.*

![Cuadro original sobre variables predictoras](https://github.com/user-attachments/assets/2d827a9b-4a02-41b5-836a-68fefbac785b)

*Figura 4. Cuadro original de variables candidatas. Su pertinencia debe contrastarse con el diccionario y la calidad del HBN.*

## 5. Enfoque metodológico y evaluación

Se utilizará una adaptación de **CRISP-DM**: comprensión del problema, comprensión y preparación de los datos, modelado, evaluación y comunicación. La fuente prevista es el conjunto de la competencia Child Mind Institute — Problematic Internet Use [10].

| Etapa | Procedimiento propuesto | Evidencia esperada |
|---|---|---|
| Comprensión de datos | Diccionario, cobertura, faltantes, plausibilidad, distribución `sii`. | Informe EDA y matriz de variables. |
| Preparación | Exclusión de predictores con fuga; imputación y codificación dentro de entrenamiento. | Flujo reproducible de transformación. |
| Modelado | Línea base y al menos dos algoritmos supervisados bajo cinco particiones estratificadas. | Configuraciones y código documentado. |
| Evaluación | QWK principal, F1-macro y matrices de confusión; sensibilidad por clase. | Tabla comparativa y análisis de errores. |
| Discusión | Limitaciones de temporalidad, datos faltantes, desbalance, extrapolación y ética. | Informe final y recomendaciones metodológicas. |

La etiqueta `sii` procede del puntaje `PCIAT-PCIAT_Total` [10]. **No es válido utilizar este puntaje como una variable de entrada para predecir `sii`**; ello reconstruiría la respuesta. En cambio, entrenar una regresión cuyo *desenlace* sea el puntaje total y luego transformar sus predicciones a categorías es una estrategia distinta, documentada por Haupts [15], que requiere su propia validación.

El QWK considera que los niveles son ordenados; F1-macro y las matrices de confusión permitirán identificar diferencias entre clases. No se equipararán QWK, ROC-AUC, exactitud y errores de regresión sin explicar las tareas y escalas correspondientes.

## 6. Planificación y materiales de la entrega original

El proyecto contempla las actividades de revisión de antecedentes, comprensión de datos, preparación, entrenamiento, evaluación y documentación. Los diagramas originales de desglose de trabajo y cronograma se conservan como evidencia histórica de su planificación:

![Estructura de desglose de trabajo original](https://github.com/user-attachments/assets/9eaa1ecd-0e70-421c-ad03-78adc1cefad8)

*Figura 5. Estructura de desglose de trabajo (EDT) presentada originalmente.*

![Cronograma original del proyecto](https://github.com/user-attachments/assets/6a6011f0-8f81-46f3-92db-1961bae2c455)

*Figura 6. Cronograma original. Las fechas específicas deben contrastarse con los plazos de la asignatura.*

| Periodo | Actividad | Producto |
|---|---|---|
| Primera etapa | Formulación y revisión bibliográfica | Presente documento y referencias verificadas. |
| Segunda etapa | EDA, preparación y modelos de referencia | Informe, código y resultados **cuando se ejecuten**. |
| Etapa final | Comparación, discusión y sustentación | Informe final y presentación académica. |

## 7. Alcance, limitaciones y ética

El conjunto HBN tiene datos faltantes y diferencias de cobertura entre instrumentos [10]. Los resultados internos de una muestra no demuestran desempeño en otras poblaciones. Tampoco se debe inferir causalidad, capacidad diagnóstica, riesgo clínico individual ni predicción futura sin evidencia temporal y validación externa.

Este repositorio documenta el **proyecto académico de Viviana**; no incluye todavía resultados cuantitativos propios, notebooks ejecutables ni bases individuales. Cuando se publiquen resultados, deberán acompañarse de metodología, particiones, métricas y limitaciones verificables. Los datos originales se obtendrán desde Kaggle respetando sus condiciones de uso.

## 8. Cierre de la formulación

La propuesta delimita un problema de estimación ordinal sobre datos heterogéneos de niños y adolescentes. La revisión científica y los reportes técnicos de la competencia sustentan la pertinencia de explorar modelos, pero no autorizan a anticipar un rendimiento ni una utilidad clínica. El valor académico del proyecto dependerá de una comparación reproducible, control de fuga de información e interpretación crítica del error por categoría.

**Fuentes:** [Bibliografía completa, con autoría y enlaces verificados](../docs/referencias.md) · [Bitácora de correcciones](../docs/bitacora_bibliografica.md).

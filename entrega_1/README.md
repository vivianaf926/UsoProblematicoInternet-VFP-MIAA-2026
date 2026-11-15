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

Para evaluar el uso problemático de internet en niños y adolescentes se requiere considerar cómo se mide el fenómeno y quién puede acceder a la valoración. Los instrumentos y los puntos de corte varían entre estudios [5], [11]. Algunos métodos requieren valoración profesional y pueden resultar difíciles de aplicar en familias con barreras culturales o lingüísticas [10], [17]. Estas dificultades motivan explorar indicadores complementarios de severidad.

Desde el punto de vista de ciencia de datos, el reto se concreta en **determinar cuánto pueden aportar indicadores no derivados directamente del cuestionario PCIAT para estimar la categoría ordinal de severidad `sii`**, teniendo en cuenta valores faltantes, cobertura desigual de instrumentos, posibles desequilibrios entre clases y riesgo de fuga de información [10].

### 2.1. Árbol de problemas y sustento

El árbol se centra en la dificultad para evaluar el uso problemático de internet de forma oportuna y consistente en niños y adolescentes. Las raíces recogen dificultades de medición y acceso descritas en las fuentes. Las ramas muestran sus posibles consecuencias para la detección, la orientación y la interpretación de las evaluaciones.

```mermaid
flowchart BT
    C1["Instrumentos con dimensiones y definiciones distintas [5, 11]"] --> P["Dificultad para evaluar de forma oportuna y consistente el uso problemático de internet en niños y adolescentes"]
    C2["Puntos de corte que varían entre estudios [11]"] --> P
    C3["Acceso limitado a valoración profesional [10, 17]"] --> P
    C4["Barreras culturales y lingüísticas para las familias [10]"] --> P
    P --> E1["Posible subdetección de necesidades de apoyo"]
    P --> E2["Posibles demoras en la orientación a familias"]
    P --> E3["Menor comparabilidad entre evaluaciones"]
    P --> E4["Dificultad para estimar la magnitud del problema en distintas poblaciones"]
```

*Figura 1. Factores que pueden dificultar la evaluación y consecuencias potenciales. Las flechas representan relaciones conceptuales.*

Las diferencias en instrumentos y puntos de corte dificultan comparar resultados y estimar la magnitud del problema entre poblaciones [11]. Las barreras de acceso pueden reducir la probabilidad de que una necesidad de apoyo se reconozca o se atienda oportunamente [10], [17]. Los estudios sobre síntomas psicológicos y patrones de uso se discuten en los antecedentes [1], [2], [3], [12].

![Árbol de problemas original elaborado para la primera entrega](https://github.com/user-attachments/assets/44881d0e-d3c6-472a-8771-b5769ef8152e)

*Figura 2. Versión inicial del árbol de problemas presentada en la primera entrega.*

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

### 4.2. Comparación de métodos y modelos en estudios previos

La revisión reúne estudios de cribado, trabajos de clasificación binaria y dos soluciones de Kaggle que estimaron las cuatro categorías de `sii` en datos del HBN. Para cada trabajo se indica el método, el conjunto de evaluación, el resultado reportado y su pertinencia para el proyecto.

| Fuente | Población y tarea | Método y evaluación | Resultado reportado | Aporte y limitación para el proyecto |
|---|---|---|---|---|
| Gómez Salgado y colaboradores (2014) [5] | 2.339 estudiantes de secundaria de Galicia. Cribado de riesgo en una encuesta escolar. | Evaluación psicométrica y análisis ROC. El grupo de riesgo se definió con criterios de uso diario prolongado y conflictos familiares por el uso de internet. | **AUC ROC 0,90**. Con el punto de corte de 19, **sensibilidad 80 %** y **especificidad 81,2 %**. | Ilustra el efecto del umbral sobre los errores de cribado. Usa un criterio de riesgo definido en la encuesta y un desenlace distinto de `sii`. |
| Hassani, Pakzad y Asghari (2018) [6] | 245 estudiantes de una universidad iraní. Clasificación binaria de niveles derivados del *Internet Addiction Test* (IAT). | K vecinos más cercanos, selección de variables mediante algoritmos heurísticos, balanceo con SMOTE y validación cruzada de 10 particiones. | **Exactitud máxima de 99,75 %** tras el balanceo y **94,70 %** con los datos originales (tablas 3 y 4). | El modelo usa ítems del mismo cuestionario del que se deriva la etiqueta. El artículo describe el balanceo antes de la selección de variables y deja sin aclarar su aislamiento por partición. Esto limita la interpretación de la exactitud. |
| Ioannidis y colaboradores (2016) [8] | 2.006 adultos de Chicago y Stellenbosch, con 181 casos. Clasificación binaria de uso problemático de internet. | Regresión logística, bosque aleatorio y *naïve Bayes*. Evaluación con 50 repeticiones por esquema, particiones 75/25 dentro de muestra y pruebas entre sedes. | En el análisis combinado **AUC ROC 0,84** y **AUC precisión–recobrado 0,20** para el bosque aleatorio. La regresión logística obtuvo **0,83** y **0,26**, respectivamente. | Con pocos casos positivos, ambos indicadores ofrecen perspectivas distintas del desempeño. La población adulta y el desenlace binario limitan su traslado a `sii`. |
| Haupts (primer puesto de Kaggle) [15] | HBN. Estimación del puntaje total PCIAT como desenlace continuo y conversión a `sii`. | Ensamble por votación de LightGBM, dos modelos XGBoost, CatBoost y ExtraTrees. El notebook usa 10 particiones estratificadas por `sii` y calibra umbrales con los datos de entrenamiento de cada partición. | **QWK 0,469** del ensamble sobre las predicciones de validación de las 10 particiones, según la salida del [notebook](https://www.kaggle.com/code/lennarthaupts/1st-place-cmi-model-v4-1-1-reduced?scriptVersionId=213769368). | Ofrece un ejemplo de regresión seguida de clasificación ordinal. La imputación del notebook se ajusta antes de la validación cruzada. El puntaje corresponde a una evaluación interna del cuaderno. |
| Agarwal (segundo puesto de Kaggle) [16] | HBN. Regresión multisalida con CatBoost y conversión de la predicción del total PCIAT a `sii`. | Imputación según el tipo de variable y 20 particiones estratificadas por `sii`. Ajusta los umbrales con el conjunto de predicciones de validación. | **QWK 0,409** en la ejecución guardada del [notebook](https://www.kaggle.com/code/aradhyeagarwal/starter-notebook-with-polars-gpu), configurada con una iteración por modelo al usar el archivo de prueba de ejemplo. El autor reportó **0,435** en el tablero público para ese notebook. | La imputación usa conjuntamente las variables de entrenamiento y prueba antes de dividir las particiones. Además, el QWK interno se calculó sobre las mismas predicciones usadas para ajustar los umbrales. |

Las cifras de AUC, exactitud y QWK responden a tareas y métricas diferentes. Los QWK de 0,469 y 0,409 provienen de ejecuciones con protocolos distintos. Para los dos primeros puestos se verificó la posición final. Las cifras exactas de sus envíos en el tablero privado quedaron sin confirmar en los reportes y notebooks consultados.

La revisión de Kato y colaboradores [4] aporta un marco general sobre modelos computacionales de adicciones conductuales. Probierz y colaboradores [9] exploran algoritmos predictivos en datos de ciencias sociales. Feng y colaboradores [13] emplearon conectividad cerebral, una modalidad diferente de los indicadores tabulares de este proyecto. Los tres trabajos aportan contexto conceptual o metodológico.

**Brecha del proyecto.** Se evaluará cuánto añade cada grupo de variables frente a una línea base bajo las mismas particiones y métricas. La selección de variables, la imputación y cualquier ajuste de umbrales se harán con datos de entrenamiento de cada partición. La evaluación reportará QWK, F1-macro y errores por nivel de `sii`, con atención a las clases minoritarias.

### 4.3. Relación con las variables candidatas

En HBN se incluyen instrumentos demográficos, medidas corporales y de aptitud física, cuestionarios de sueño y actividad, categorías de uso de internet y actigrafía [10]. La disponibilidad y la oportunidad temporal de cada predictor deben comprobarse antes de incorporarlo. La asociación estadística entre una variable y `sii` no constituye por sí misma prueba causal ni criterio suficiente de selección.

Los dos cuadros de síntesis elaborados originalmente se mantienen como antecedentes visuales; esta comparación narrativa es la que fundamenta explícitamente método, hallazgos y límites:

![Cuadro original sobre modelos de aprendizaje automático](https://github.com/user-attachments/assets/14ee8b59-786c-40f2-a32e-ddccce452dfa)

*Figura 3. Cuadro original de modelos; interpretar junto con la tabla de comparación y las referencias corregidas.*

![Cuadro original sobre variables predictoras](https://github.com/user-attachments/assets/2d827a9b-4a02-41b5-836a-68fefbac785b)

*Figura 4. Cuadro original de variables candidatas. Su pertinencia debe contrastarse con el diccionario y la calidad del HBN.*

## 5. Enfoque metodológico y evaluación

Se seguirá una adaptación de **CRISP-DM** para comprender el problema, auditar y preparar los datos, entrenar los modelos, evaluar su desempeño y comunicar los resultados. El proyecto utilizará el conjunto de datos del HBN publicado en la competencia del Child Mind Institute [10].

### 5.1. Modelos propuestos

Para estimar los cuatro niveles de severidad de `sii`, se propone comparar una línea base y dos clasificadores supervisados. La regresión logística y el bosque aleatorio tienen un antecedente en la clasificación binaria de uso problemático de internet [8]. El proyecto evaluará sus versiones multiclase en el HBN.

| Método | Papel en la comparación |
|---|---|
| **Línea base de clase mayoritaria** | Asigna a cada registro la clase más frecuente del conjunto de entrenamiento de su partición. Permite observar el desempeño de una regla que solo usa la frecuencia de las clases. |
| **Regresión logística multinomial regularizada** | Estima la probabilidad de cada nivel de severidad mediante un modelo lineal. |
| **Bosque aleatorio** | Combina árboles de decisión para explorar relaciones no lineales e interacciones entre predictores. |

### 5.2. Protocolo de evaluación

Se utilizarán las mismas cinco particiones estratificadas para la línea base y los modelos. La imputación, la codificación y, cuando corresponda, el escalamiento y la selección de variables se ajustarán con los datos de entrenamiento de cada partición. Se excluirán de los predictores `sii`, `PCIAT-PCIAT_Total` y los ítems o campos que permitan reconstruir la etiqueta [10].

El **kappa cuadrático ponderado (QWK)** será la métrica principal porque penaliza más los errores entre niveles de severidad alejados. Se reportarán también F1-macro, la matriz de confusión y la sensibilidad por categoría, con atención a las clases minoritarias.

## 6. Plan de trabajo y cronograma

### 6.1. Tareas y entregables

El plan de trabajo vincula las tareas con los objetivos específicos y con los productos de cada entrega.

| Tarea | Actividades | Producto verificable |
|---|---|---|
| Formular el problema | Delimitar el alcance, construir el árbol de problemas, definir los objetivos y comparar los antecedentes. | Documento de formulación y bibliografía verificada. |
| Auditar y preparar los datos | Revisar la disponibilidad de la etiqueta, el desbalance, los valores faltantes y la plausibilidad de los registros. Definir al menos dos conjuntos de predictores y documentar sus transformaciones. | Informe exploratorio, matriz de variables y código de preparación. |
| Entrenar y evaluar los modelos | Ejecutar la línea base y los clasificadores con las mismas particiones. Comparar las métricas y revisar los errores por nivel de severidad. | Código de modelado, tabla de resultados y análisis de errores. |
| Integrar y comunicar los resultados | Documentar el método, discutir limitaciones, elaborar las conclusiones y preparar el video del proyecto. | Informe final y video de presentación. |

![Estructura de desglose de trabajo original](https://github.com/user-attachments/assets/9eaa1ecd-0e70-421c-ad03-78adc1cefad8)

*Figura 5. Estructura de desglose de trabajo (EDT) de la primera entrega.*

### 6.2. Cronograma

Las semanas se cuentan desde el inicio del plan de trabajo. Los hitos indican la semana prevista de cada entrega. La fecha y la hora de corte se registrarán según el calendario oficial de la asignatura.

| Semana prevista | Actividad principal | Hito previsto | Fecha y hora límite oficial |
|---|---|---|---|
| **1** | Formular el problema y los objetivos, revisar las fuentes y comparar soluciones previas. | **◆ Primera entrega.** Formulación y planificación. | Por confirmar |
| **2** | Explorar y preparar los datos. Revisar la calidad, los faltantes y la disponibilidad de predictores. | Informe exploratorio y selección inicial de variables. | — |
| **3** | Definir y ejecutar la línea base y los modelos. Comparar su desempeño. | **◆ Segunda entrega.** Análisis de datos y modelos de referencia. | Por confirmar |
| **4 y 5** | Redactar la metodología, discutir los resultados y preparar las conclusiones. | Borrador del informe final. | — |
| **6** | Consolidar el informe y grabar y editar el video. | **◆ Tercera entrega.** Informe final y video del proyecto. | Por confirmar |

En un diagrama de Gantt, las barras sombreadas indican la duración de las actividades. Cada entrega es un **hito** y se marca con un rombo en la celda del día de vencimiento una vez confirmada la fecha. En la tabla, **◆** identifica la semana prevista del hito.

<details>
<summary>Consultar el cronograma gráfico original</summary>

![Cronograma original del proyecto](https://github.com/user-attachments/assets/6a6011f0-8f81-46f3-92db-1961bae2c455)

*Figura 6. Cronograma de la primera entrega. El fondo rosado identifica las filas de entrega. El gráfico presenta semanas relativas y deja sin marcar el día de vencimiento.*

</details>

## 7. Alcance, limitaciones y ética

El conjunto HBN tiene datos faltantes y diferencias de cobertura entre instrumentos [10]. Los resultados internos de una muestra no demuestran desempeño en otras poblaciones. Tampoco se debe inferir causalidad, capacidad diagnóstica, riesgo clínico individual ni predicción futura sin evidencia temporal y validación externa.

Este repositorio documenta el **proyecto académico de Viviana**; no incluye todavía resultados cuantitativos propios, notebooks ejecutables ni bases individuales. Cuando se publiquen resultados, deberán acompañarse de metodología, particiones, métricas y limitaciones verificables. Los datos originales se obtendrán desde Kaggle respetando sus condiciones de uso.

## 8. Cierre de la formulación

La propuesta delimita un problema de estimación ordinal sobre datos heterogéneos de niños y adolescentes. La revisión científica y los reportes técnicos de la competencia sustentan la pertinencia de explorar modelos, pero no autorizan a anticipar un rendimiento ni una utilidad clínica. El valor académico del proyecto dependerá de una comparación reproducible, control de fuga de información e interpretación crítica del error por categoría.

## Referencias

- **[1]** Ko y colaboradores (2012). [DOI 10.1016/j.eurpsy.2010.04.011](https://doi.org/10.1016/j.eurpsy.2010.04.011).
- **[2]** Kuss y colaboradores (2013). [DOI 10.1016/j.chb.2013.04.002](https://doi.org/10.1016/j.chb.2013.04.002).
- **[3]** Yen y colaboradores (2008). [DOI 10.1111/j.1440-1819.2007.01770.x](https://doi.org/10.1111/j.1440-1819.2007.01770.x).
- **[4]** Kato y colaboradores (2023). [DOI 10.1016/j.addbeh.2022.107595](https://doi.org/10.1016/j.addbeh.2022.107595).

[Bibliografía completa](../docs/referencias.md) · [Bitácora de correcciones](../docs/bitacora_bibliografica.md).

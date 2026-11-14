# UsoProblematicoInternet-VFP-MIAA-2026

Proyecto para estimar la gravedad del uso problemático de internet en niños y adolescentes mediante el análisis de datos clínicos y de comportamiento

**Universidad Icesi — Especialización en Inteligencia Artificial Aplicada**  
**Asignatura:** Proyecto I de Innovación IA
**Autora:** Viviana Fernandez Payan.   [GitHub: vivianaf926](https://github.com/vivianaf926)

**Estado:** Entregas en construcción  

### Introducción

El uso problemático de Internet (PIU) en niños y adolescentes se ha convertido en una preocupación creciente para padres, educadores y profesionales de la salud. Esto se refiere al uso excesivo o descontrolado de tecnologías digitales que interfiere significativamente con la vida diaria, incluyendo el rendimiento académico, la actividad física,  las relaciones sociales y la salud.

En este sentido, el Child Mind Institute organizó en la plataforma Kaggle una competencia titulada "Child Mind Institute — Problematic Internet Use", que busca predecir el nivel de uso problemático de Internet en niños, utilizando un conjunto de datos de información demográfica, clínica y comportamental, facilitando la identificación de alertas tempranas y la intervención oportuna con hábitos más saludables.

La capacidad de identificar signos de niños en riesgo de desarrollar el uso problemático de Internet por medio de análisis de datos y modelos de aprendizaje automático puede proporcionar una herramienta valiosa para el diseño de políticas de salud mental preventiva en instituciones educativas, de salud y gubernamentales, promoviendo hábitos digitales más saludables.

Algunos estudios han descrito asociaciones entre el uso problemático de internet y síntomas de ansiedad, depresión o trastorno por déficit de atención con hiperactividad (TDAH) [1], [3], [14]; estas asociaciones no establecen causalidad. Otros trabajos han examinado patrones de uso de aplicaciones y variables psicosociales [2], [12], así como instrumentos de cribado y características de las muestras clínicas [5], [11].

Desde la modelación computacional se han revisado enfoques para estudiar adicciones conductuales [4] y se han aplicado métodos de aprendizaje automático al uso problemático de internet [6], [8], [9], [10]. Otras investigaciones han explorado modelos predictivos basados en conectividad cerebral [13]. Estas fuentes emplean muestras, mediciones y tareas diferentes.



En este contexto, el proyecto **UsoProblematicoInternet-VFP-MIAA-2026** Se propone una investigación académica mediante aprendizaje automático las posibilidades y limitaciones de un enfoque predictivo con datos disponibles. Su propósito es analítico y no pretende reemplazar diagnósticos ni valoraciones expertas.

 ### Planteamiento del problema

La acelerada adopción de tecnologías digitales en la infancia y la adolescencia ha transformado las dinámicas educativas, de entretenimiento y de socialización. Sin embargo, este entorno hiperconectado ha propiciado el surgimiento del Uso Problemático de Internet (PIU), entendido como un patrón de consumo tecnológico desadaptativo e incontrolado que genera severas interferencias en el desarrollo integral de los menores [2], [12].  Esta problemática no solo incide negativamente en el rendimiento académico y la actividad física, sino que se vincula estrechamente con afecciones de salud mental como la depresión, la ansiedad y el Trastorno por Déficit de Atención e Hiperactividad (TDAH), así como con factores sociales como el aislamiento y la falta de supervisión parental [1], [2]. También se ha estudiado la asociación entre uso problemático de internet y experiencia de consumo de sustancias en adolescentes [7]; el carácter transversal del estudio citado no permite establecer por sí solo causalidad ni predicción prospectiva.

## Arbol de problemas

De acuerdo a la problematica expuesta, se definen a continuación los objetivos y el árbol de problemas del proyecto:


<img width="399" height="231" alt="image" src="https://github.com/user-attachments/assets/44881d0e-d3c6-472a-8771-b5769ef8152e" />

Figura. 1. Árbol de problemas, Uso Problemático de Internet en niños.

## PROBLEMA CENTRAL

Uso problemático de Internet (PIU) en niños y adolescentes, caracterizado por un uso compulsivo y descontrolado de tecnologías digitales que interfiere en su bienestar psicológico, rendimiento académico, relaciones interpersonales y desarrollo cognitivo a largo plazo.

## CAUSAS PRINCIPALES
o	Comorbilidades psiquiátricas/ psicológicas preexistentes, déficit en el autocontrol y autoimagen deficiente, se refiere a trastornos de salud mental preexistentes (ansiedad, depresión, TDAH, trastornos del espectro impulsivo-compulsivo).
o	Distanciamiento social, déficit de monitoreo del entorno familiar y presión de grupo, se refiere a Supervisión parental insuficiente y ausencia de educación digital en el hogar, presión social, comparación en redes sociales y ciberacoso.
o	Acceso continuo a dispositivos, aplicaciones inmersivas y contenidos altamente estimulantes, se refiere a diseño de aplicaciones con técnicas de persuasión (recompensas intermitentes, notificaciones), exposición a contenido inapropiado o adictivo (juegos de azar, pornografía).
o	Políticas escolares, poca formación en uso de tecnologías, refiere a la desigualdad en el acceso a recursos de salud mental y educativa, normas culturales que promueven el uso intensivo de tecnología.

## CONSECUENCIAS PRINCIPALES

o	Deterioro de las relaciones familiares, escolares y aislamiento interpersonal
o	Riesgo de autolesión, retraso en el desarrollo cognitivo y deterioro de la salud física, problemas físicos (obesidad, trastornos del sueño, musculoesqueléticos.
o	Deficiente desempeño académico, postergación de deberes y probabilidad elevada de abandono escolar
o	Cuadros de ansiedad, trastornos del estado de ánimo y conductas adictivas digitales

## OBJETIVO PRINCIPAL

Desarrollar un modelo predictivo que permita identificar señales tempranas del uso problemático de Internet en niños y adolescentes, integrando datos demográficos, clínicos y comportamentales recolectados por el Child Mind Institute.

## OBJETIVOS ESPECÍFICOS

1.	Realizar un análisis exploratorio de datos (EDA) para identificar patrones y correlaciones de las variables disponibles en el conjunto de datos.
2.	Preprocesar los datos mediante limpieza, imputación de valores faltantes, normalización, codificación de variables categóricas y selección de características basada en importancia de variables, asegurando robustez e interpretabilidad del conjunto de datos.
3.	Implementar y comparar modelos de aprendizaje automático, evaluando el rendimiento, interpretabilidad y generalización, usando métricas como ROC-AUC, F1-score, precisión, recall, MAE y RMSE, “the quadratic weighted kappa”, entre otras.
4.	Seleccionar un modelo interpretable y escalable, con el mejor rendimiento en la métrica “the quadratic weighted kappa”, que permita identificar señales tempranas del uso problemático de Internet en niños.


## ESTADO DEL ARTE: Revisión bibliográfica y análisis de soluciones existentes

# MODELOS USADOS PARA LA RESOLUCIÓN DEL PROBLEMA

Se realiza una revisión de la literatura y el estado del arte de los modelos predictivos que permiten identificar señales tempranas del uso problemático de Internet. A continuación, se presenta un resumen de los modelos utilizados en los artículos consultados:

<img width="455" height="300" alt="image" src="https://github.com/user-attachments/assets/14ee8b59-786c-40f2-a32e-ddccce452dfa" />

Cuadro 1. Estado del arte Modelos de Aprendizaje automático. 

Posteriormente, se realiza una revisión de la literatura y el estado del arte para identificar las variables predictoras que podrían presentar mayor correlación en la detección temprana del uso problemático de Internet. A continuación, se presenta un resumen de las variables encontradas en los artículos consultados:

<img width="454" height="267" alt="image" src="https://github.com/user-attachments/assets/2d827a9b-4a02-41b5-836a-68fefbac785b" />

Cuadro 2. Estado del arte Variables Predictoras. 

## PLANTEAMIENTO DE TAREAS Y CRONOGRAMA DE ACTIVIDADES

A continuación se presentan las tareas y actividades diseñadas para cumplir con los objetivos del proyecto, que incluyen la realización de un análisis exploratorio, preprocesamiento de datos, implementación de modelos de aprendizaje automático, evaluación de rendimiento y un plan de documentación y comunicación de los resultados alcanzados, como se puede apreciar en la figura 2.

<img width="884" height="494" alt="image" src="https://github.com/user-attachments/assets/9eaa1ecd-0e70-421c-ad03-78adc1cefad8" />

Figura. 2. Estructura de desglose de trabajo.

Como se ilustra en la Figura 3, las actividades mencionadas se organizaron temporalmente en días, alineándose con los plazos de entrega previstos para el proyecto.

<img width="884" height="494" alt="image" src="https://github.com/user-attachments/assets/6a6011f0-8f81-46f3-92db-1961bae2c455" />

## REFERENCIAS

Se conservan las claves [1]–[14] para mantener la correspondencia con las citas del proyecto. Las entradas contienen autores completos, datos de publicación y enlaces directos a registros verificados.

[1] Chih-Hung Ko, Ju-Yu Yen, Cheng-Fang Yen, Cheng-Sheng Chen y Cheng-Chung Chen, “The association between Internet addiction and psychiatric disorder: A review of the literature”, *European Psychiatry*, 27(1), 1–8, 2012. https://doi.org/10.1016/j.eurpsy.2010.04.011

[2] Daria J. Kuss, Antonius J. van Rooij, Gillian W. Shorter, Mark D. Griffiths y Dike van de Mheen, “Internet addiction in adolescents: Prevalence and risk factors”, *Computers in Human Behavior*, 29(5), 1987–1996, 2013. https://doi.org/10.1016/j.chb.2013.04.002

[3] Ju-Yu Yen, Chih-Hung Ko, Cheng-Fang Yen, Sue-Huei Chen, Wei-Lun Chung y Cheng-Chung Chen, “Psychiatric symptoms in adolescents with Internet addiction: Comparison with substance use”, *Psychiatry and Clinical Neurosciences*, 62(1), 9–16, 2008. https://doi.org/10.1111/j.1440-1819.2007.01770.x

[4] Ayaka Kato, Kanji Shimomura, Dimitri Ognibene, Muhammad A. Parvaz, Laura A. Berner, Kenji Morita y Vincenzo G. Fiore, “Computational models of behavioral addictions: State of the art and future directions”, *Addictive Behaviors*, 140, artículo 107595, 2023. https://doi.org/10.1016/j.addbeh.2022.107595

[5] Patricia Gómez Salgado, Antonio Rial Boubeta, Teresa Braña Tobío, Jesús Varela Mallou y Carmen Barreiro Couto, “Evaluation and early detection of problematic Internet use in adolescents”, *Psicothema*, 26(1), 21–26, 2014. https://doi.org/10.7334/psicothema2013.109

[6] Zeinab Hassani, Aylin Pakzad y Arezou Asghari, “An Artificial Predictive Modeling Framework for Automatically Detecting Problematic Use of Internet”, *International Journal of Computer Applications*, 179(41), 31–38, 2018. https://doi.org/10.5120/ijca2018916983

[7] Virginia Fisoun, Georgios Floros, Konstantinos Siomos, Dimitrios Geroukalis y Klimis Navridis, “Internet addiction as an important predictor in early detection of adolescent drug use experience—implications for research and practice”, *Journal of Addiction Medicine*, 6(1), 77–84, 2012. https://doi.org/10.1097/ADM.0b013e318233d637

[8] Konstantinos Ioannidis, Samuel R. Chamberlain, Matthias S. Treder, Franz Kiraly, Eric W. Leppink, Sarah A. Redden, Dan J. Stein, Christine Lochner y Jon E. Grant, “Problematic internet use (PIU): Associations with the impulsive-compulsive spectrum. An application of machine learning in psychiatry”, *Journal of Psychiatric Research*, 83, 94–102, 2016. https://doi.org/10.1016/j.jpsychires.2016.08.010

[9] Eryka Probierz, Wojciech Sikora, Adam Gałuszka y Anita Gałuszka, “Predictive Algorithms in Social Sciences – Problematic Internet Use Example”, en *Man-Machine Interactions 6*, serie *Advances in Intelligent Systems and Computing*, vol. 1061, 89–98, Springer, 2020. https://doi.org/10.1007/978-3-030-31964-9_9

[10] Salma Abdel Wahed y Mutaz Abdel Wahed, “AI-Driven Digital Well-being: Developing Machine Learning Model to Predict and Mitigate Internet Addiction”, *LatIA*, vol. 3, 2025. Fuente editorial: https://latia.ageditor.uy/index.php/latia/article/view/134 ; DOI indicado por la editorial: https://doi.org/10.62486/latia2025134

[11] Daria J. Kuss y Olatz Lopez-Fernandez, “Internet addiction and problematic Internet use: A systematic review of clinical research”, *World Journal of Psychiatry*, 6(1), 143–176, 2016. https://doi.org/10.5498/wjp.v6.i1.143

[12] Antonius J. van Rooij, Christopher J. Ferguson, Dike van de Mheen y Tim M. Schoenmakers, “Time to abandon Internet addiction? Predicting problematic internet, game, and social media use from psychosocial well-being and application use”, *Clinical Neuropsychiatry*, 14(1), 113–121, 2017. https://research.tilburguniversity.edu/en/publications/time-to-abandon-internet-addiction-predicting-problematic-interne/

[13] Qiuyang Feng, Zhiting Ren, Dongtao Wei, Cheng Liu, Xueyang Wang, Xianrui Li, Bijie Tie, Shuang Tang y Jiang Qiu, “Connectome-based predictive modeling of Internet addiction symptomatology”, *Social Cognitive and Affective Neuroscience*, 19(1), nsae007, 2024. https://doi.org/10.1093/scan/nsae007

[14] Chih-Hung Ko, Ju-Yu Yen, Cheng-Sheng Chen, Yi-Chun Yeh y Cheng-Fang Yen, “Predictive values of psychiatric symptoms for Internet addiction in adolescents: A 2-year prospective study”, *Archives of Pediatrics & Adolescent Medicine*, 163(10), 937–943, 2009. https://doi.org/10.1001/archpediatrics.2009.159

### Registro de verificación bibliográfica — 14 de noviembre de 2026

- **Referencia [4] sustituida expresamente:** no se logró verificar el supuesto artículo de “P. Bélisle y M. Dixon”. Se reemplazó por una revisión verificable de Kato y colaboradores (2023), diferente de la fuente originalmente consignada; no se debe presentar como corrección de la misma obra.
- **Referencia [10] con inconsistencia editorial:** la página editorial consultada identifica a Salma Abdel Wahed y Mutaz Abdel Wahed, y publica el DOI terminado en **134**. Otro registro del artículo presenta el DOI terminado en **73**. Se consigna el DOI de la página editorial y queda pendiente consultar a la revista para resolver la discrepancia antes de la entrega definitiva.
- Las otras doce entradas se contrastaron con editoriales, PubMed o repositorios académicos. Se sustituyeron enlaces de búsquedas de Google por vínculos bibliográficos directos.
- **Límite del ajuste:** la corrección bibliográfica no constituye, por sí misma, una comparación crítica del estado del arte. Esa revisión metodológica queda para la siguiente prioridad.

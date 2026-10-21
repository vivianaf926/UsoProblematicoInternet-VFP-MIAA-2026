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

Diversos estudios han identificado correlaciones entre PIU y otros trastornos psicológicos como el trastorno por déficit de atención con hiperactividad (TDAH), la ansiedad y la depresión [1]. Se ha demostrado que factores como el bajo nivel de actividad física, el tiempo excesivo frente a pantallas, y el aislamiento social son predictores comunes del PIU [2].

Desde una perspectiva de Ingeniería y Ciencia de Datos, estudios recientes han explorado el uso de modelos de aprendizaje automático para identificar patrones de comportamiento asociados al PIU [3].



En este contexto, el proyecto **UsoProblematicoInternet-VFP-MIAA-2026** Se propone una investigación académica mediante aprendizaje automático las posibilidades y limitaciones de un enfoque predictivo con datos disponibles. Su propósito es analítico y no pretende reemplazar diagnósticos ni valoraciones expertas.

 ### Planteamiento del problema

La acelerada adopción de tecnologías digitales en la infancia y la adolescencia ha transformado las dinámicas educativas, de entretenimiento y de socialización. Sin embargo, este entorno hiperconectado ha propiciado el surgimiento del Uso Problemático de Internet (PIU), entendido como un patrón de consumo tecnológico desadaptativo e incontrolado que genera severas interferencias en el desarrollo integral de los menores [2], [12].  Esta problemática no solo incide negativamente en el rendimiento académico y la actividad física, sino que se vincula estrechamente con afecciones de salud mental como la depresión, la ansiedad y el Trastorno por Déficit de Atención e Hiperactividad (TDAH), así como con factores sociales como el aislamiento y la falta de supervisión parental [1], [2]. Además, el PIU puede predecir otras conductas de riesgo, como el consumo de sustancias en adolescentes [1].

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

[1]	C.-H. Ko, S.-J. Yen, C.-F. Yen, C.-S. Chen, and H.-Y. Chen, "The association between Internet addiction and psychiatric disorder: a review of the literature," European Psychiatry, vol. 27, no. 1, pp. 1–8, 2012.  

[2]	D. J. Kuss and M. D. Griffiths, "Internet addiction in adolescents: Prevalence and risk factors," Comput. Human Behav., vol. 49, pp. 678–687, 2015.

[3]	J. Y. Yen, C.-S. Chen, C.-F. Yen, K.-E. Tang, and H.-Y. Ko, "Psychiatric symptoms in adolescents with Internet addiction: Comparison with substance use," Psychiatry Clin. Neurosci., vol. 61, no. 3, pp. 218–223, 2007.  

[4]	P. Bélisle and M. Dixon, "Machine learning in behavioral addictions: A systematic review," J. Behav. Addict., vol. 9, no. 4, pp. 827–851, 2020.
[5]	"Evaluation and early detection of problematic Internet use in adolescents," Psicología y Salud, vol. 32, no. 2, pp. 273–281, 2022. [Online]. Available: https://reunido.uniovi.es/index.php/PST/article/view/10212
[6]	Z. Hassani, A. Nematbakhsh, and M. S. Nematbakhsh, "An Artificial Predictive Modeling Framework for Automatically Detecting Problematic Use of Internet," in 2018 8th International Conference on Computer and Knowledge Engineering (ICCKE), Ferdowsi University of Mashhad, Iran, Oct. 2018, pp. 314–319. [Online]. Available: https://www.google.com/search?q=https://www.researchgate.net/profile/Zeinab-Hassani/publication/325222198_An_Artificial_Predictive_Modeling_Framework_for_Automatically_Detecting_Problematic_Use_of_Internet/links/5b5c124aa6fdccf0b2fcafe6/An-Artificial-Predictive-Modeling-Framework-for-Automatically-Detecting-Problematic-Use-of-Internet.pdf
[7]	M. Khazaal, P. Billieux, R. Laluc, S. Thorens, J.-M. Romo, and G. Gmel, "Internet addiction as an important predictor in early detection of adolescent drug use experience—implications for research and practice," J. Addict. Med., vol. 6, no. 1, pp. 61–66, 2012. [Online]. Available: https://www.google.com/search?q=https://journals.lww.com/journaladdictionmedicine/abstract/2012/03000/internet_addiction_as_an_important_predictor_in.11.aspx  
[8]	G. Erkoc, O. N. Tamam, M. Tamam, and C. Evren, "Problematic internet use (PIU): associations with the impulsive-compulsive spectrum. An application of machine learning in psychiatry," J. Psychiatr. Res., vol. 82, pp. 155–161, 2016. [Online]. Available: https://www.sciencedirect.com/science/article/pii/S0022395616302138  
[9]	M. Bericat, "Predictive algorithms in social sciences–problematic Internet use example," in Social Implications of Data Mining and Cybersecurity, vol. 117, J. Prieto and B. Zapirain, Eds. Cham: Springer International Publishing, 2020, pp. 117–130. [Online]. Available: https://www.google.com/search?q=https://link.springer.com/chapter/10.1007/978-3-030-31964-9_9
[10]	M. R. Islam, M. A. Hossain, M. Akter, and S. Sultana, "AI-Driven Digital Well-being: Developing Machine Learning Model to Predict and Mitigate Internet Addiction," in International Conference on Intelligent Systems for Crisis Management, Cham, 2023, pp. 1–10. [Online]. Available: https://dialnet.unirioja.es/servlet/articulo?codigo=10085286
[11]	S. Kuss and M. D. Griffiths, "Internet addiction and problematic Internet use: A systematic review of clinical research," Int. J. Environ. Res. Public Health, vol. 12, no. 6, pp. 6545–6566, 2015. [Online]. Available: https://pmc.ncbi.nlm.nih.gov/articles/PMC4804263/
[12]	A. J. van Rooij, T. L. F. M. Schoenmakers, M. E. J. M. van den Eijnden, D. H. J. M. van de Mheen, and J. A. L. M. Meerkerk, "Time to abandon internet addiction? Predicting problematic internet, game, and social media use from psychosocial well-being and application use," Comput. Human Behav., vol. 65, pp. 117–125, 2016. [Online]. Available: https://www.google.com/search?q=https://www.researchgate.net/profile/Antonius-Van-Rooij/publication/311127452_Time_to_abandon_Internet_Addiction_Predicting_problematic_internet_game_and_social_media_use_from_psychosocial_well-being_and_application_use/links/58afff0245851503be954e4c/Time-to-abandon-Internet-Addiction-Predicting-problematic-internet-game-and-social-media-use-from-psychosocial-well-being-and-application-use.pdf  
[13]	Y. Zhou, L. Yuan, J. Chai, Y. Mou, Z. Qin, and W. Lei, "Connectome-based predictive modeling of Internet addiction symptomatology," Soc. Cogn. Affect. Neurosci., vol. 19, no. 1, p. nsae007, 2024. [Online]. Available: https://academic.oup.com/scan/article/19/1/nsae007/7604371
[14]	S. H. Hwang, Y. S. Park, J. W. Baik, D. J. Choi, S. Y. Kim, and K. C. Choi, "Predictive values of psychiatric symptoms for internet addiction in adolescents: a 2-year prospective study," JAMA Pediatr., vol. 166, no. 3, pp. 215–221, 2012. [Online]. Available: https://jamanetwork.com/journals/jamapediatrics/fullarticle/382237


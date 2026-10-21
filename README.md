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

MODELOS USADOS PARA LA RESOLUCIÓN DEL PROBLEMA
Se realiza una revisión de la literatura y el estado del arte de los modelos predictivos que permiten identificar señales tempranas del uso problemático de Internet. A continuación, se presenta un resumen de los modelos utilizados en los artículos consultados:

<img width="455" height="300" alt="image" src="https://github.com/user-attachments/assets/14ee8b59-786c-40f2-a32e-ddccce452dfa" />


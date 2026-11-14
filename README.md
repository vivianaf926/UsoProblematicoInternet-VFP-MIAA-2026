# Uso problemático de internet en niños y adolescentes — Proyecto MIAA 2026-2

**Universidad Icesi · Maestría en Inteligencia Artificial Aplicada**  
**Asignatura:** Proyecto I de Innovación IA  
**Autora:** [Viviana Fernández Payán](https://github.com/vivianaf926)  
**Estado:** primera entrega reorganizada y referencias depuradas; modelos y resultados propios pendientes de documentación.

## Resumen del proyecto

Este proyecto estudia la posibilidad de **estimar los cuatro niveles ordinales de severidad del uso problemático de internet (`sii`)** en niños y adolescentes mediante algoritmos de aprendizaje automático, utilizando variables demográficas, físicas y de comportamiento del estudio **Healthy Brain Network (HBN)**, difundidas a través de la competencia del Child Mind Institute en Kaggle.

La pregunta de investigación es: **¿en qué medida los modelos supervisados permiten estimar la severidad de `sii` a partir de indicadores disponibles y cuáles son las limitaciones metodológicas de esa estimación?**

El propósito es **académico y exploratorio**. Estimar una etiqueta de severidad a partir de mediciones disponibles no equivale a diagnosticar, demostrar causalidad ni predecir que un niño desarrollará el problema en el futuro.

## Documentación del proyecto

| Documento | Contenido y estado |
|---|---|
| [**Entrega 1: formulación del problema**](entrega_1/README.md) | Contexto, árbol de problemas, pregunta, objetivos SMART, comparación de antecedentes, metodología prevista y planificación. |
| [**Referencias bibliográficas**](docs/referencias.md) | Fuentes científicas y técnicas con autores, datos editoriales y vínculos directos verificables. |
| [**Bitácora de revisión bibliográfica**](docs/bitacora_bibliografica.md) | Registro de errores corregidos, sustituciones de referencias y criterios de verificación. |
| **Etapas posteriores** | Análisis exploratorio, modelos y resultados: por incorporar cuando existan experimentos documentados. |

## Datos y fuente

**Fuente oficial:** [Child Mind Institute — Problematic Internet Use (Kaggle)](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use).

El reto utiliza datos del HBN con instrumentos demográficos, físicos, de aptitud y actividad, cuestionarios y registros de actigrafía. La variable objetivo `sii` contiene cuatro categorías ordenadas: **0 (ninguno), 1 (leve), 2 (moderado) y 3 (severo)**.

Los datos presentan valores faltantes y diferencias de cobertura entre instrumentos. El repositorio **no publica datos individuales**. Su obtención corresponde a Kaggle y está sujeta a las condiciones de la competición.

## Objetivo y enfoque metodológico

Se propone desarrollar y comparar, **durante el periodo académico 2026-2**, al menos **dos modelos supervisados** de estimación ordinal, bajo un procedimiento reproducible de preparación y validación.

La evaluación utilizará el **coeficiente kappa cuadrático ponderado (QWK)** como métrica principal, acompañado de **F1-macro**, matrices de confusión y análisis por categoría. La meta QWK ≥ 0,35 incluida en la formulación es **exploratoria y todavía no constituye un resultado observado ni una referencia clínica**.

Las etapas previstas, siguiendo una adaptación de **CRISP-DM**, comprenden: comprensión del problema, auditoría y preparación de los datos, entrenamiento, validación y discusión. Se controlará la fuga de información, en especial el uso incorrecto de `PCIAT-PCIAT_Total` como predictor directo de `sii`.

La explicación detallada de la metodología y sus criterios está en la [primera entrega](entrega_1/README.md).

## Estado de avances y reproducibilidad

Actualmente se dispone de una formulación académica revisada, un estado del arte comparativo y una bibliografía trazable. **No se declara haber ejecutado modelos, alcanzado métricas ni validado resultados propios** en este repositorio.

Los notebooks, dependencias de ejecución y resultados experimentales deberán publicarse junto con sus procedimientos de reproducción cuando sean desarrollados. Esto permite diferenciar objetivos, antecedentes externos y evidencia efectivamente generada por la autora.

## Limitaciones y uso responsable

Los resultados futuros deberán interpretarse teniendo en cuenta el desbalance de categorías, los valores faltantes, la oportunidad temporal de las mediciones y los posibles sesgos de selección. La validación interna no garantiza generalización clínica. Este trabajo no reemplaza la valoración de profesionales de salud mental ni permite recomendaciones individuales automatizadas.

---

**Inicio de lectura:** [Entrega 1](entrega_1/README.md) · [Referencias](docs/referencias.md) · [Bitácora bibliográfica](docs/bitacora_bibliografica.md).

# Bitácora de depuración bibliográfica

**Fecha:** 14 de noviembre de 2026  
**Documento revisado:** `README.md` de la primera entrega, versión previa a la reorganización.  
**Responsabilidad:** control editorial y de consistencia; no implica validación independiente de los análisis de los artículos.

| Clave | Error en la versión inicial | Resolución |
|---|---|---|
| [1] | Autoría abreviada y sin URL verificable | Normalización y DOI de *European Psychiatry* (2012). |
| [2] | Se atribuía a dos autores (2015, vol. 49) | Corregidos cinco autores, 2013, vol. 29(5), pp. 1987–1996. |
| [3] | Año, volumen, páginas y parte de la autoría incorrectos; además se usaba como ejemplo de ML | Corregido artículo de síntomas psiquiátricos de Yen y colaboradores, 2008; retirada esa atribución metodológica. |
| [4] | Supuesta revisión de Bélisle y Dixon no corroborable con los metadatos ofrecidos | Retirada y **sustituida** por una revisión auténtica, Kato y colaboradores (2023); no es la misma publicación. |
| [5] | Faltaban autores; revista, año y paginación no coincidían | Corregido artículo de Gómez Salgado y colaboradores, *Psicothema*, 2014. |
| [6] | Autoría y congreso erróneos | Corregido artículo de Hassani, Pakzad y Asghari, *International Journal of Computer Applications*, 2018. |
| [7] | Autoría atribuida a otros investigadores y páginas equivocadas | Corregido estudio transversal de Fisoun y colaboradores, 2012; no debe interpretarse como prueba causal. |
| [8] | Atribuido a Erkoc y otros, volumen y páginas incorrectos | Corregido estudio de Ioannidis y ocho coautores, 2016. |
| [9] | Autor ficticio/inexacto para el capítulo y nombre del libro equivocado | Corregidos Probierz, Sikora y los dos Gałuszka; *Man-Machine Interactions 6*, pp. 89–98. |
| [10] | Se consignaba como congreso de 2023 y con autores ajenos; al verificar apareció un texto de 2025 con **dos DOI diferentes** publicados para el mismo título | Retirado de la bibliografía final para no perpetuar la ambigüedad; la clave [10] se asignó a la fuente primaria oficial de Kaggle, más pertinente para definir los datos y la tarea. |
| [11] | Citada como Kuss y Griffiths (2015, revista equivocada) | Corregido a Kuss y Lopez-Fernandez, *World Journal of Psychiatry*, 2016. |
| [12] | Autoría, revista y páginas erróneas | Corregido a van Rooij, Ferguson, van de Mheen y Schoenmakers, *Clinical Neuropsychiatry*, 2017. |
| [13] | Autoría atribuida a Zhou y colaboradores | Corregido a Feng y ocho coautores, 2024. |
| [14] | Autoría, revista, año y páginas erróneos | Corregido a Ko y colaboradores, *Archives of Pediatrics & Adolescent Medicine*, 2009. |
| [15]–[17] | No estaban en el listado inicial | Incorporados: primer y segundo puesto de Kaggle, y comunicado oficial del Child Mind Institute. |

## Criterios de control editorial

1. Eliminar búsquedas de Google como enlaces permanentes a fuentes; preferir DOI, registro editorial o repositorio institucional.
2. Mantener correspondencia entre la afirmación en el texto y el objetivo real de cada artículo: un estudio de asociación no acredita causalidad ni necesariamente evalúa aprendizaje automático.
3. Separar antecedentes clínicos, metodológicos y soluciones del **mismo reto**; no comparar métricas de tareas o poblaciones heterogéneas como si fueran equivalentes.
4. Diferenciar *predicción concurrente de `sii`* de predicción futura o diagnóstico clínico.
5. La procedencia exacta de cada referencia se consigna en [referencias.md](referencias.md). El historial de Git conserva la bibliografía original.

## Resoluciones sin intervención adicional de la autora

Se adoptaron decisiones editoriales verificables: [4] se sustituyó de forma explícita y [10] se reemplazó por la descripción oficial de la tarea en Kaggle. Ambas decisiones quedan transparentes en esta bitácora; ninguna fuente incierta se presenta como validada. Los cambios no presuponen resultados de modelos, revisión por pares de los write-ups de Kaggle, ni disponibilidad de código experimental de Viviana.

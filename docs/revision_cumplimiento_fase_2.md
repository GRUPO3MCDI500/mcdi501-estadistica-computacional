# Revision de cumplimiento - Evaluacion Sumativa Fase 2

## Resumen ejecutivo

Con el dataset Framingham Heart Study cargado en esta entrega, el proyecto cumple los criterios centrales de la Fase 2 despues de aplicar correcciones menores de reproducibilidad. El informe se mantiene en 6 paginas, dentro del maximo de 8 paginas, y el notebook queda ejecutable sin errores dentro de la estructura del repositorio.

## Hallazgos sobre el dataset

- Registros: 4.240.
- Variables: 16.
- Variable objetivo: `TenYearCHD`.
- Prevalencia de CHD a 10 anos: 15,19%.
- Filas con al menos un valor faltante: 582 (13,73%).
- Duplicados: 0.
- Variables con mayor porcentaje de faltantes: `glucose` (9,15%), `education` (2,48%), `BPMeds` (1,25%), `totChol` (1,18%).

## Revision del notebook

| Criterio de la instruccion | Estado corregido | Observacion |
|---|---:|---|
| Carga del dataset en Python | Cumple | Se corrigio la ruta de carga. El notebook original buscaba `framingham_heart_study.csv` en la carpeta local, pero el archivo entregado venia como `framingham heart study.csv`. En el repositorio se deja como `data/raw/framingham_heart_study.csv`. |
| Verificacion de estructura y tipos | Cumple | Incluye `df.info()`, clasificacion de variables nominales, ordinales, discretas y continuas. |
| Reporte de calidad | Cumple | Documenta faltantes, filas con NA, duplicados, prevalencia y desbalance de la variable objetivo. Se agrego chequeo de dominios y rangos simples. |
| Limpieza basica | Cumple con justificacion | No imputa ni elimina masivamente. Usa eliminacion por lista por calculo, lo cual esta justificado para esta fase exploratoria. |
| Descriptiva numerica | Cumple | Calcula medias, dispersion, CV, asimetria, curtosis, histogramas y boxplots. |
| Descriptiva categorica | Cumple | Calcula frecuencias absolutas y relativas y genera graficos de barras. |
| Analisis bivariado | Cumple | Incluye matriz de correlacion, prevalencia por edad y visualizaciones por factores. |
| Estimacion puntual e IC 95% | Cumple | Incluye medias con IC t para cuatro variables numericas y proporcion CHD con Wilson. |
| Pruebas de hipotesis | Cumple | Incluye t de Welch para medias y chi-cuadrado para independencia. Formula hipotesis, alpha=0,05 y verifica supuestos. |
| Interpretacion | Cumple | El notebook incluye conclusiones preliminares y proximos pasos de Fase 3. |
| Reproducibilidad | Cumple corregido | El notebook fue ejecutado completo sin errores dentro del repositorio. |

## Revision del informe PDF

| Criterio de la instruccion | Estado | Observacion |
|---|---:|---|
| Introduccion al problema | Cumple | Contextualiza CHD, Framingham y decision bajo incertidumbre. |
| Metodos estadisticos aplicados | Cumple | Describe descriptiva, IC, t de Welch, chi-cuadrado y supuestos. |
| Resultados e interpretacion | Cumple | Presenta tablas, graficos e interpretaciones en contexto clinico. |
| IC y pruebas de hipotesis | Cumple | Incluye estimaciones, IC 95%, alpha, decisiones e implicancias. |
| Proximos pasos | Cumple | Define Fase 3: imputacion, desbalance, clasificacion y analisis multivariado. |
| Maximo 8 paginas | Cumple | El PDF tiene 6 paginas. |
| Enlace GitHub | Corregido | Se reemplazo el placeholder por el repositorio oficial del grupo. |

## Correcciones aplicadas

1. Se corrigio la ruta de carga del dataset en el notebook para que funcione desde la raiz del repositorio, desde la carpeta del notebook o en una entrega local.
2. Se agrego una validacion basica de consistencia de dominios y rangos simples.
3. Se amplio la tabla de t de Welch en el notebook para incluir grados de libertad e IC 95% de la diferencia, alineandola mejor con el informe.
4. Se reemplazo en el PDF el enlace placeholder de GitHub por `https://github.com/GRUPO3MCDI500/mcdi501-estadistica-computacional`.
5. Se organizo el proyecto en carpetas para tres fases.

## Recomendacion para la entrega en Canvas

Entregar:

- PDF: `reports/fase_2/Informe_Sumativa1_Framingham.pdf`.
- Notebook: `notebooks/fase_2/Sumativa1_Framingham.ipynb`.
- Enlace GitHub: `https://github.com/GRUPO3MCDI500/mcdi501-estadistica-computacional`.

El CSV debe quedar en el repositorio para reproducibilidad, aunque Canvas solicite principalmente PDF, notebook y enlace.

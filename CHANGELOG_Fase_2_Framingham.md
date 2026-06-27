# CHANGELOG — Entrega Sumativa Fase 2

## Proyecto
**Análisis estadístico del riesgo coronario a 10 años — Framingham Heart Study**

## Repositorio
**mcdi501-estadistica-computacional**  
https://github.com/GRUPO3MCDI500/mcdi501-estadistica-computacional

## Versión documentada
Entrega corregida y organizada para la Evaluación Sumativa Fase 2.

---

## 1. Archivos base recibidos

Para la preparación de la entrega se recibieron los siguientes archivos originales:

- `framingham heart study.csv`
- `Sumativa1 Framingham.ipynb`
- `Informe Sumativa1 Framingham.pdf`

Estos archivos contenían el dataset utilizado, el notebook de análisis estadístico y el informe técnico correspondiente a la Fase 2 del proyecto.

---

## 2. Cambios realizados en el informe técnico

### 2.1 Corrección del enlace al repositorio GitHub

El informe original incluía un enlace de repositorio pendiente de completar:

```text
https://github.com/<usuario>/framingham-mds
```

En la versión corregida, dicho enlace fue reemplazado por el repositorio real del grupo:

```text
https://github.com/GRUPO3MCDI500/mcdi501-estadistica-computacional
```

### 2.2 Conservación del contenido técnico original

El contenido estadístico del informe fue mantenido. No se modificaron las conclusiones, resultados ni el enfoque metodológico del análisis. Se conservaron las siguientes secciones:

- Introducción al problema.
- Preparación y reporte de calidad de datos.
- Análisis exploratorio de variables numéricas y categóricas.
- Análisis bivariado.
- Estimación puntual.
- Intervalos de confianza al 95%.
- Pruebas de hipótesis.
- Interpretación preliminar.
- Próximos pasos del proyecto.

La intervención sobre el informe se limitó a la corrección necesaria del enlace de GitHub, con el objetivo de dejar el documento listo para su entrega formal.

---

## 3. Cambios realizados en el notebook Python

### 3.1 Ajuste en la carga del dataset

El notebook original presentaba riesgo de error al ejecutarse, debido a una diferencia entre el nombre del archivo recibido y el nombre esperado por el código.

Archivo recibido originalmente:

```text
framingham heart study.csv
```

Nombre esperado por el notebook original:

```text
framingham_heart_study.csv
```

Para evitar errores de ejecución, se ajustó la carga del dataset mediante una lógica más robusta, capaz de buscar el archivo en distintas ubicaciones esperadas dentro de la estructura del proyecto:

- `data/raw/framingham_heart_study.csv`
- `../../data/raw/framingham_heart_study.csv`
- `framingham_heart_study.csv`
- `framingham heart study.csv`

Este cambio mejora la reproducibilidad del análisis, permitiendo ejecutar el notebook tanto desde la raíz del repositorio como desde la carpeta donde se ubica el archivo `.ipynb`.

### 3.2 Validación adicional de consistencia de datos

Se incorporó una revisión complementaria de consistencia para fortalecer el apartado de calidad de datos solicitado en la evaluación.

La validación considera:

- Revisión de variables binarias.
- Revisión de la variable ordinal `education`.
- Revisión de rangos básicos en variables clínicas.
- Identificación de posibles valores fuera de dominio.

Esta mejora complementa el análisis inicial de valores faltantes, duplicados e inconsistencias.

### 3.3 Complemento de la prueba t de Welch

El notebook original ya ejecutaba pruebas de hipótesis mediante t de Welch. En la versión corregida se complementó la salida estadística para entregar una interpretación más completa.

La versión original incluía:

- Media del grupo sin CHD.
- Media del grupo con CHD.
- Diferencia de medias.
- Estadístico t.
- Valor p.
- Tamaño de efecto mediante d de Cohen.
- Decisión estadística.

La versión corregida agrega:

- Grados de libertad.
- Intervalo de confianza al 95% para la diferencia de medias.

Este ajuste permite una mejor alineación entre el notebook y el informe técnico.

### 3.4 Verificación de ejecución

Se verificó que el notebook corregido pueda ejecutarse correctamente dentro de la estructura final del repositorio, sin depender de rutas locales específicas del equipo de trabajo.

---

## 4. Cambios realizados en la estructura del repositorio

Los archivos originales fueron reorganizados en una estructura más ordenada y adecuada para un repositorio académico en GitHub.

### 4.1 Estructura final propuesta

```text
mcdi501-estadistica-computacional/
├── data/
│   ├── raw/
│   │   └── framingham_heart_study.csv
│   └── processed/
├── notebooks/
│   ├── fase_1/
│   ├── fase_2/
│   │   └── Sumativa1_Framingham.ipynb
│   └── fase_3/
├── reports/
│   ├── fase_1/
│   ├── fase_2/
│   │   └── Informe_Sumativa1_Framingham.pdf
│   └── fase_3/
├── docs/
│   └── revision_cumplimiento_fase_2.md
├── outputs/
├── src/
├── README.md
├── requirements.txt
└── .gitignore
```

Esta estructura permite separar claramente los datos, notebooks, informes, documentación y archivos auxiliares, facilitando la revisión del proyecto y su continuidad en fases posteriores.

---

## 5. Archivos agregados

### 5.1 `README.md`

Se agregó un archivo README para documentar el objetivo del repositorio, su estructura general y el uso esperado del proyecto.

### 5.2 `requirements.txt`

Se agregó un archivo de dependencias para facilitar la reproducción del análisis en Python.

### 5.3 `.gitignore`

Se agregó un archivo `.gitignore` para evitar subir al repositorio archivos temporales, cachés, checkpoints de Jupyter y otros elementos innecesarios.

### 5.4 `docs/revision_cumplimiento_fase_2.md`

Se agregó un documento de revisión de cumplimiento, donde se resume cómo la entrega responde a los criterios solicitados en la evaluación sumativa.

---

## 6. Resumen comparativo de cambios

| Elemento | Versión original | Versión corregida |
|---|---|---|
| Dataset | Archivo con espacios en el nombre | Dataset renombrado y ubicado en `data/raw/framingham_heart_study.csv` |
| Notebook | Riesgo de error por ruta o nombre del CSV | Carga robusta del dataset desde distintas ubicaciones |
| Informe | Enlace GitHub pendiente de completar | Enlace real del repositorio agregado |
| Pruebas estadísticas | Welch con métricas principales | Welch complementado con grados de libertad e IC95% de diferencia |
| Calidad de datos | Revisión de faltantes y duplicados | Revisión complementada con validación de consistencia |
| Repositorio | Archivos sueltos | Estructura ordenada por fases |
| Documentación | Limitada al informe y notebook | Se agrega README, requirements, .gitignore y revisión de cumplimiento |

---

## 7. Alcance de la actualización

Los cambios realizados corresponden a correcciones, ajustes de reproducibilidad, ordenamiento de archivos y mejoras de presentación del proyecto.

No se alteró el enfoque estadístico del trabajo, ni se modificaron las conclusiones principales del informe. El objetivo de la actualización fue dejar la entrega más clara, ejecutable y alineada con los requisitos solicitados en la Evaluación Sumativa Fase 2.

---

## 8. Commit sugerido

```text
feat(fase-2): agregar entrega sumativa Framingham
```

Descripción sugerida:

```text
Se organiza la entrega de la Fase 2 del proyecto Framingham, incorporando dataset, notebook ejecutable, informe técnico corregido, documentación del repositorio y revisión de cumplimiento.
```

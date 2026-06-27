# mcdi501-estadistica-computacional

Repositorio del GRUPO 3 para el proyecto de Estadistica Computacional.

Repositorio oficial: https://github.com/GRUPO3MCDI500/mcdi501-estadistica-computacional

## Estructura recomendada para 3 fases

```text
mcdi501-estadistica-computacional/
├── data/
│   ├── raw/                  # datasets originales sin modificar
│   └── processed/            # datos derivados o preparados, si aplica
├── notebooks/
│   ├── fase_1/               # exploracion o seleccion inicial del dataset
│   ├── fase_2/               # sumativa fase 2: descriptiva, IC y pruebas
│   └── fase_3/               # modelado, validacion y conclusiones finales
├── reports/
│   ├── fase_1/               # informes o entregables de la fase 1
│   ├── fase_2/               # PDF final de la fase 2
│   └── fase_3/               # PDF final de la fase 3
├── docs/                     # revision, bitacora, estructura y criterios
├── outputs/                  # figuras/tablas exportadas si se generan aparte
├── src/                      # funciones reutilizables, si el proyecto escala
├── requirements.txt          # dependencias Python
├── .gitignore
└── README.md
```

## Entrega Fase 2

Archivos principales:

- `reports/fase_2/Informe_Sumativa1_Framingham.pdf`
- `notebooks/fase_2/Sumativa1_Framingham.ipynb`
- `data/raw/framingham_heart_study.csv`

## Como ejecutar el notebook

Desde la raiz del repositorio:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Abrir `notebooks/fase_2/Sumativa1_Framingham.ipynb` y ejecutar todas las celdas.

Tambien puede ejecutarse por consola:

```bash
jupyter nbconvert --to notebook --execute notebooks/fase_2/Sumativa1_Framingham.ipynb --output Sumativa1_Framingham_ejecutado.ipynb --output-dir outputs
```

## Nota de reproducibilidad

El notebook busca el dataset en rutas comunes del repositorio, priorizando `data/raw/framingham_heart_study.csv`. El archivo CSV incluido conserva el contenido del dataset entregado; solo se usa un nombre sin espacios para facilitar la ejecucion.

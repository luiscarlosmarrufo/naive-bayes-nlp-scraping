# Ghostbusters: Clasificador Naïve Bayes con NLP (Count Vectorizer, Laplace, Poisson, Cross-Validation) para relatos paranormales

Proyecto que implementa un clasificador **Naïve Bayes** para categorizar relatos de fenómenos paranormales obtenidos mediante **web scraping** de la página [*Your Ghost Stories*](https://www.yourghoststories.com/).
El flujo incluye **scraping**, **preprocesamiento de texto** (NLP), construcción de **matrices dispersas** y experimentación con variantes del modelo (Laplace smoothing, distribución Poisson y validación cruzada).

El **reporte principal** con la metodología, resultados y conclusiones esta en la carpeta **`reports/`**.

## Integrantes

* **Luis Carlos Marrufo Padilla**
* **Gustavo Andrés Aguilar Torreblanca**
* **Joshua Alexander Chaidez Ochoa**
* **Ángel Esparza Enríquez**

## Estructura del repositorio

```
.
├─ data/
│  └─ stories.csv                    # Historias scrapeadas desde la página
├─ notebooks/
│  ├─ scraping.qmd                   # Web scraping de relatos paranormales
│  ├─ classification.qmd             # Clasificación Naïve Bayes con NLP
│  └─ classification.html            # Render del análisis de clasificación
├─ reports/
│  └─ Articulo_3_Naive.pdf           # Artículo con métodos, resultados y conclusiones
├─ README.md
├─ .gitignore
└─ naive-bayes-nlp-scraping.Rproj    # Proyecto de RStudio
```

## Datos

* Los **datos crudos** se obtienen de la página [*Your Ghost Stories*](https://www.yourghoststories.com/).
* El notebook **`notebooks/scraping.qmd`** realiza el scraping y genera el dataset **`data/stories.csv`**, que contiene título, lugar, tipo de evento y descripción de cada historia.
* Este archivo es la base para los experimentos en **`notebooks/classification.qmd`**, donde se entrenan y evalúan los clasificadores Naïve Bayes.

## Resumen

1. Ejecutar **`notebooks/scraping.qmd`** → produce **`data/stories.csv`**.
2. Ejecutar **`notebooks/classification.qmd`** → entrena y evalúa el clasificador Naïve Bayes.
3. El **reporte final** esta disponible en **`reports/`**.

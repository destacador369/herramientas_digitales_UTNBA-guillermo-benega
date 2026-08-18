# herramientas_digitales_UTNBA-guillermo-benega

**Trabajo final presentado para la obtención de la certificación del curso**

---

## Información del Proyecto

* **Alumno:** Guillermo Benega  
* **Institución:** Universidad Tecnológica Nacional – Facultad Regional Buenos Aires (UTN FRBA)  
* **Curso:** Herramientas Digitales  
* **Estado:** Trabajo Final  

---

## Objetivos / Preguntas de Investigación

El presente proyecto aborda el Análisis Exploratorio de Datos (EDA) para responder a los siguientes interrogantes clave sobre el desempeño y características de los futbolistas:

1. **Distribución Etaria:** ¿Qué rango de edad (`age`) tienen mayoritariamente los jugadores participantes en el mundial?
2. **Desempeño Defensivo según Posición:** Los jugadores cuya posición en cancha está más cerca del arco rival (`FW`, `MF`), ¿interceptaron una menor cantidad de pases (`interceptions`) que el resto (`DF`)? *(Análisis numérico vs. categórico: `interceptions` según `position`)*.
3. **Efectividad Ofensiva de Seleccionados Finalistas:** ¿Qué relación existe entre los goles marcados (`goals`) y los disparos intentados al arco rival (`shots`), según la posición de los jugadores (`position`), en los seleccionados finalistas de la competencia (`team_country`)?

---

## Fuente de Datos

* **Dataset:** FIFA World Cup 2026 Players
* **Plataforma:** Kaggle
* **Autor / Licencia:** Swapnil Tripathi (`swaptr`)
* **Enlace directo:** [FIFA WC 2026 Players Dataset](https://www.kaggle.com/datasets/swaptr/fifa-wc-2026-players)

---

## Pasos del Proyecto

### 1. Ingesta y Carga de Datos
* Descarga del archivo `.csv` desde Kaggle.
* Carga del conjunto de datos e inspección preliminar de variables y tipos de datos.

### 2. Limpieza y Preprocesamiento (ETL)
* Verificación y tratamiento de datos faltantes, duplicados y valores atípicos (outliers).
* Normalización de campos textuales y categóricos (posiciones `FW`, `MF`, `DF`, `GK`, países).
* Filtrado de los seleccionados finalistas para el análisis comparativo.

### 3. Análisis Exploratorio de Datos (EDA)
* **Objetivo 1:** Cálculo de métricas estadísticas (media, mediana, percentiles) e histograma/boxplot de edades (`age`).
* **Objetivo 2:** Comparación de medias/medianas de intercepciones (`interceptions`) agrupadas por posición (`position`).
* **Objetivo 3:** Evaluación de métricas de conversión (`goals` / `shots`) segmentadas por posición y selección finalista.

### 4. Visualización y Elaboración de Tableros
* Generación de gráficos descriptivos:
  * Histograma y curva de densidad para la distribución de edades.
  * Diagramas de caja (Boxplots) / gráficos de barras para intercepciones por posición.
  * Gráficos de dispersión (Scatter Plot) y mapas de calor para la relación disparos vs. goles.
* Ensamblado de un Dashboard interactivo con filtros por país y posición.

### 5. Documentación y Conclusiones
* Interpretación cuantitativa y cualitativa de las preguntas planteadas.
* Estructuración del repositorio final en GitHub para presentación.

---

## Tecnologías Utilizadas

| Categoría | Herramienta / Librería |
| :--- | :--- |
| **Lenguaje Base** | `Python 3.x` |
| **Control de Versiones** | `Git`, `GitHub` |
| **Entorno de Trabajo** | `Google Colab` |
| **Procesamiento de Datos** | `Pandas`, `NumPy` |
| **Visualización de Datos** | `Matplotlib`, `Seaborn`, `Plotly` |
| **Dashboarding / Presentación** | `Power BI` |

---

## Estructura del Repositorio

```text
herramientas_digitales_UTNBA-guillermo-benega/
│
├── data/
│   ├── raw/              # Dataset original descargado de Kaggle
│
├── notebooks/
│   ├── 01_Datos_Jugadores_Mundial_Futbol_2026.ipynb   # Análisis exploratorio y respuesta a los objetivos
│       # Limpieza de datos y tratamiento de variables
│
├── dashboard/            # Archivos del tablero interactivo
├── README.md             # Documentación principal del proyecto

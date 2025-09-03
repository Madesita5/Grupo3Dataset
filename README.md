# 📊 Análisis de Ofertas Laborales en Ecuador

Este proyecto tiene como objetivo analizar un conjunto de datos reales sobre ofertas de empleo en Ecuador para identificar patrones relevantes en cuanto a demanda de cargos, ubicación geográfica, y niveles salariales. El análisis se basa en técnicas de limpieza de datos, transformación de variables y visualización exploratoria, todo desarrollado en Python con apoyo de bibliotecas como Pandas, Matplotlib y Seaborn.

---

## 🗂️ Descripción del Dataset

El dataset original (oferta_laboral_ecuador.csv) contiene registros de vacantes laborales publicadas en Ecuador, con variables como:

- **Cargo ofertado**: el puesto o función laboral solicitada.  
- **Ciudad**: ubicación geográfica de la vacante.  
- **Rango de remuneración**: salario mínimo y máximo ofrecido.  
- **Fecha de publicación**: día en que se publicó la oferta.

## 🧹 Limpieza y Transformación
Durante el preprocesamiento del dataset se realizaron las siguientes tareas:

   1. Eliminación de duplicados y valores nulos

   2. Estandarización de nombres de columnas

   3. Conversión de fechas al formato datetime

    4. Extracción del mes de publicación

    5. Transformación de rangos salariales:

        * Se extrajeron los valores numéricos desde strings tipo "USD 600 a USD 900"

        * Se creó una nueva variable: remuneracion_mid, que representa el promedio entre salario mínimo y máximo

## 🔍 Análisis Exploratorio

Con los datos limpios, se realizaron diversos análisis y visualizaciones:

# 📌 Cargos Más Demandados

Se identificaron los puestos más ofertados en el país, revelando los sectores con mayor necesidad de talento.

# 🌆 Ciudades con Más Ofertas

Se analizó la concentración de vacantes por ciudad, destacando Quito y Guayaquil como los principales centros laborales.

# 💰 Distribución de Salarios

Se exploró la variable remuneracion_mid para comprender la variabilidad de los sueldos, detectando también valores atípicos (outliers).

# 📅 Evolución Temporal

Se evaluó la cantidad de publicaciones por mes, identificando picos y caídas en la actividad de contratación.

## 📊 Visualizaciones

Se generaron gráficos con Matplotlib, Seaborn y Plotly para comunicar los resultados:

   * Gráficos de barras para cargos y ciudades más frecuentes

   * Boxplots de salarios por ciudad y por cargo

   * Histogramas de distribución de sueldos promedio

    * Gráfico de líneas para analizar la evolución mensual de publicaciones

Todas las figuras están guardadas en la carpeta Figuras.

## 💡 Principales Hallazgos

  1. Alta concentración de ofertas en pocas ciudades y cargos, lo cual sugiere una estructura laboral centralizada.

  2. Dispersión significativa en los salarios, con diferencias notables entre regiones.

  3. Estacionalidad en la publicación de ofertas, útil para quienes planifican estrategias de reclutamiento o búsqueda de empleo.

## 🧰 Tecnologías Utilizadas
  - Python 3

  - Pandas para manejo de datos

  - Matplotlib y Seaborn para visualización estática

  - Plotly para gráficos interactivos

  - Google Colab como entorno de trabajo

## 📂 Estructura del Proyecto

├── Datos/
│   └── oferta_laboral_ecuador.csv
├── Notebooks/
│   └── analisis_ofertas_ec_colab_completo.ipynb
├── Figuras/
│   └── (gráficos exportados)
├── README.md

## 🎯 Conclusión

Este proyecto representa un ejercicio práctico de análisis de datos aplicados a un contexto laboral real en Ecuador. Permite generar información accionable para diversos actores: profesionales, empresas, investigadores y formuladores de políticas públicas.
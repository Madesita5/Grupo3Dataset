# 📊 Análisis de Ofertas Laborales en Ecuador

Este proyecto tiene como objetivo analizar un conjunto de datos reales sobre ofertas de empleo en Ecuador para identificar patrones relevantes en cuanto a demanda de cargos, ubicación geográfica, y niveles salariales. El análisis se basa en técnicas de limpieza de datos, transformación de variables y visualización exploratoria, todo desarrollado en Python con apoyo de bibliotecas como Pandas, Matplotlib y Seaborn.

---

# 🗂️ Descripción del Dataset

El dataset original (oferta_laboral_ecuador.csv) contiene registros de vacantes laborales publicadas en Ecuador, con variables como:

- **Cargo ofertado**: el puesto o función laboral solicitada.  
- **Ciudad**: ubicación geográfica de la vacante.  
- **Rango de remuneración**: salario mínimo y máximo ofrecido.  
- **Fecha de publicación**: día en que se publicó la oferta.

# 🧹 Limpieza y Transformación
Durante el preprocesamiento del dataset se realizaron las siguientes tareas:

   1. Eliminación de duplicados y valores nulos

   2. Estandarización de nombres de columnas

   3. Conversión de fechas al formato datetime

   4. Extracción del mes de publicación

   5. Transformación de rangos salariales:

        * Se extrajeron los valores numéricos desde strings tipo "USD 600 a USD 900"

        * Se creó una nueva variable: remuneracion_mid, que representa el promedio entre salario mínimo y máximo

# 🔍 Análisis Exploratorio

Con los datos limpios, se realizaron diversos análisis y visualizaciones:

## 📌 Cargos Más Demandados

Se identificaron los puestos más ofertados en el país, revelando los sectores con mayor necesidad de talento.

## 🌆 Ciudades con Más Ofertas

Se analizó la concentración de vacantes por ciudad, destacando Quito y Guayaquil como los principales centros laborales.

## 💰 Distribución de Salarios

Se exploró la variable remuneracion_mid para comprender la variabilidad de los sueldos, detectando también valores atípicos (outliers).

## 📅 Evolución Temporal

Se evaluó la cantidad de publicaciones por mes, identificando picos y caídas en la actividad de contratación.

# 📊 Visualizaciones

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

```
├── data/
│   └── oferta_laboral_ecuador.csv
├── Notebooks/
│   └── analisis_ofertas_ec_colab_completo.ipynb
├── Figuras/
│   └── (gráficos exportados)
└── README.md
```

# 📌 Conclusiones Técnicas del Análisis

1. Concentración de la demanda laboral

    - El análisis de frecuencia por cargos ofertados mostró una clara asimetría positiva, indicando que un número reducido de cargos acumula una alta proporción de vacantes. Esto sugiere la existencia de alta concentración de demanda en perfiles operativos, comerciales o administrativos.

    - Se observa una distribución de tipo Zipfian, típica en fenómenos socioeconómicos donde unos pocos elementos dominan el conjunto.

2. Distribución salarial con outliers

    - La variable remuneracion_mid evidenció una distribución sesgada a la derecha, con la mayoría de los valores concentrados en salarios bajos o medios, y presencia de outliers superiores que distorsionan el promedio.

    - Los boxplots por ciudad y por sector confirman que ciertos sectores como tecnología y salud presentan mayor dispersión y mediana más alta en los salarios.

    - Esta dispersión podría estar influenciada por diferencias en experiencia requerida, ubicación o habilidades técnicas específicas.

3. Análisis por ciudad

      - Quito y Guayaquil concentran la mayor cantidad de vacantes, lo que se alinea con su papel como centros económicos del país.

      - Sin embargo, el análisis cruzado de ciudades con salarios promedio no indica una relación directa entre volumen de vacantes y mejores sueldos. Es decir, no siempre más vacantes significa mejores salarios, lo que implica que el análisis de calidad laboral debe ir más allá de la cantidad.

4. Homogeneidad sectorial

      - El gráfico de barras por sector muestra una distribución desbalanceada: sectores como ventas, servicios, y administración concentran gran parte de las ofertas, mientras que áreas como investigación o educación están subrepresentadas.

      - Este patrón puede tener implicaciones para políticas públicas en formación técnica y redistribución de talento.

5. Calidad de los datos y tratamiento

      - Durante el proceso de limpieza se detectaron múltiples valores atípicos en la columna remuneracion, así como formatos mixtos (rango de texto, strings alfanuméricos, ceros falsos, etc.).

      - Se aplicaron transformaciones como "regex", "split", "replace" y "astype(float)" para estandarizar los salarios y derivar la variable "remuneracion_mid", lo cual fue fundamental para habilitar un análisis cuantitativo robusto.  

## 🎯 Conclusión Final

Este proyecto representa un ejercicio práctico de análisis de datos aplicados a un contexto laboral real en Ecuador. Permite generar información accionable para diversos actores: profesionales, empresas, investigadores y formuladores de políticas públicas.
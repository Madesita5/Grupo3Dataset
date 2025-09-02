# 📊 Análisis de Ofertas Laborales en Ecuador

Este proyecto tiene como objetivo analizar un conjunto de datos de ofertas de empleo en Ecuador, con el fin de extraer información valiosa sobre la **demanda laboral**, los **salarios** y las **tendencias del mercado**. El análisis permite obtener insights que pueden ser útiles tanto para candidatos como para empleadores, ayudando a tomar decisiones estratégicas sobre contratación, búsqueda de empleo y planificación de talento.

---

## 🗂️ Descripción del Dataset

El dataset contiene información detallada sobre ofertas de trabajo publicadas en Ecuador y cuenta con las siguientes variables principales:

- **Cargo ofertado**: el puesto o función laboral solicitada.  
- **Área o sector**: industria o departamento al que pertenece la oferta.  
- **Ciudad**: ubicación geográfica de la vacante.  
- **Rango de remuneración**: salario mínimo y máximo ofrecido.  
- **Fecha de publicación**: día en que se publicó la oferta.

El dataset original se encuentra en `data/oferta_laboral_ecuador.csv`, y después del proceso de limpieza se generó `data/ofertas_ec_limpio.csv` listo para el análisis.

---

## 🧹 Proceso de Limpieza y Transformación de Datos

Para garantizar la calidad y consistencia de la información, se aplicaron los siguientes pasos de preprocesamiento:

1. **Eliminación de valores nulos y duplicados**.  
2. **Normalización de columnas**: estandarización de formatos, especialmente fechas y nombres de variables.  
3. **Creación de nuevas variables**: se calculó la **remuneración promedio** (`remuneracion_mid`) a partir del rango salarial.  
4. **Agrupación de datos**: se consolidó información por **ciudad, cargo y mes** para análisis agregados.  
5. **Corrección de inconsistencias**: unificación de nombres de cargos y sectores para evitar duplicados semánticos.

Este proceso asegura que los análisis estadísticos y visualizaciones sean confiables y significativos.

---

## 📈 Principales Hallazgos

- **🔝 Cargos más frecuentes**: un pequeño grupo de posiciones concentra la mayoría de la demanda laboral, lo que evidencia áreas con alta competitividad y oportunidades.  
- **💰 Distribución de salarios**: la mayoría de las ofertas se encuentra en rangos medios, aunque se detectaron **valores extremos** que podrían reflejar puestos muy especializados o poco representativos.  
- **📅 Tendencia mensual**: la cantidad de ofertas varía a lo largo del año, mostrando **estacionalidad en el mercado laboral**, lo que puede guiar decisiones de búsqueda de empleo y planificación de contratación.

---

## 💡 Conclusiones e Insights

1. Conocer los **cargos más solicitados** permite a los candidatos orientar su formación y a las empresas evaluar la competencia por talento.  
2. Analizar la **distribución salarial** ayuda a establecer expectativas realistas y ajustar políticas de compensación.  
3. Observar la **tendencia temporal de ofertas** revela periodos de mayor actividad laboral, lo que es útil para estrategias de reclutamiento y búsqueda de empleo.  
4. Este análisis puede servir como **base para estudios más profundos** sobre empleabilidad, tendencias por sectores y análisis de salarios en Ecuador.

---

## 📂 Estructura del Repositorio

```
├── data/
│   ├── oferta_laboral_ecuador.csv   # Dataset original
│   └── ofertas_ec_limpio.csv        # Dataset limpio para análisis
├── notebooks/
│   └── analisis_ofertas_ec.ipynb    # Notebook con limpieza, análisis y visualización
├── README.md                        # Documentación del proyecto
```

---

## 🚀 Tecnologías Utilizadas

- **Python**: manipulación de datos y análisis.  
- **Pandas**: limpieza, transformación y análisis de datos.  
- **Seaborn & Matplotlib**: visualizaciones estadísticas.  
- **Plotly**: dashboards interactivos.  
- **Google Colab / Jupyter Notebook**: entornos de ejecución y experimentación.

---

## 📌 Próximos pasos

Este análisis es un **primer paso** para comprender el mercado laboral ecuatoriano. Futuras mejoras pueden incluir:

- Análisis por **sector industrial** y **nivel de experiencia**.  
- Comparaciones **interanuales** de tendencias salariales.  
- Creación de un **dashboard interactivo completo** con filtros por ciudad, sector y cargo.  
- Modelos predictivos para estimar la demanda de determinados perfiles profesionales.
---


Descripción del propósito del dataset

Explicación de los pasos de limpieza y transformación

Principales hallazgos del análisis

Cualquier insight o conclusión relevante

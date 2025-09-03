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

##🌍 Contexto del Proyecto

  -El mercado laboral en Ecuador enfrenta retos relacionados con:
  
  -Alta competencia laboral en áreas urbanas como Quito y Guayaquil.
  
  -Brechas salariales según región, sector y nivel de especialización.
  
  -Transformación digital y nuevas demandas de talento en áreas tecnológicas.
  
  -Dificultades de acceso a información clara sobre empleos y sueldos.

Analizar ofertas laborales ayuda a entender qué sectores demandan más talento, dónde están las mejores oportunidades y cómo evolucionan los salarios. Esto puede ser útil tanto para profesionales que buscan empleo como para empresas, investigadores y formuladores de políticas públicas.


----

## ✅ Ventajas y Desventajas del Dataset  

### Ventajas  
- Información **real y contextualizada** del mercado laboral en Ecuador.  
- Incluye **variables clave** para análisis de demanda y salarios.  
- Útil para **múltiples enfoques analíticos**: economía, sociología, gestión de talento.  
- **Formato estructurado (CSV)**, lo que facilita su uso en Python, R, SQL o Power BI.  

### Desventajas  
- Puede presentar **sesgo geográfico o sectorial** (algunas ciudades/sectores sobre-representados).  
- Datos **limitados**: no incluye experiencia, nivel educativo, tipo de contrato ni beneficios adicionales.  
- Posible **desactualización**: refleja un periodo específico y no necesariamente el presente.  
- Riesgo de **errores humanos** en los anuncios originales.  

----------------------------------------------------------------------------------------------------------------------

## 🧹 Proceso de Limpieza y Transformación de Datos

Para garantizar la calidad y consistencia de la información, se aplicaron los siguientes pasos de preprocesamiento:

1. **Eliminación de valores nulos y duplicados**.  
2. **Normalización de columnas**: estandarización de formatos, especialmente fechas y nombres de variables.  
3. **Creación de nuevas variables**: se calculó la **remuneración promedio** (`remuneracion_mid`) a partir del rango salarial.  
4. **Agrupación de datos**: se consolidó información por **ciudad, cargo y mes** para análisis agregados.  
5. **Corrección de inconsistencias**: unificación de nombres de cargos y sectores para evitar duplicados semánticos.

Este proceso asegura que los análisis estadísticos y visualizaciones sean confiables y significativos.

---

## ✅ Ventajas y Desventajas del Dataset  

### Ventajas  
- Información **real y contextualizada** del mercado laboral en Ecuador.  
- Incluye **variables clave** para análisis de demanda y salarios.  
- Útil para **múltiples enfoques analíticos**: economía, sociología, gestión de talento.  
- **Formato estructurado (CSV)**, lo que facilita su uso en Python, R, SQL o Power BI.  

### Desventajas  
- Puede presentar **sesgo geográfico o sectorial** (algunas ciudades/sectores sobre-representados).  
- Datos **limitados**: no incluye experiencia, nivel educativo, tipo de contrato ni beneficios adicionales.  
- Posible **desactualización**: refleja un periodo específico y no necesariamente el presente.  
- Riesgo de **errores humanos** en los anuncios originales.  

---

## 🔑 Variables Clave

Además de las variables ya mencionadas, se pueden crear nuevas para enriquecer el análisis:

  1. remuneracion_mid: promedio entre salario mínimo y máximo ofrecido.
  
  2. mes_publicacion: mes de la publicación (útil para analizar tendencias temporales).
  
  3. categoria_sector: agrupación de áreas afines (ejemplo: TI, salud, comercio, educación).
  
  4. salario_normalizado: rango salarial ajustado en escala para comparaciones más justas.

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

## 🔎 Análisis Exploratorio de Datos (EDA)  

Algunas de las preguntas exploradas fueron:  

- ¿Cuáles son los sectores con mayor número de ofertas laborales?  
- ¿Qué ciudades concentran más oportunidades de empleo?  
- ¿Cómo varían los salarios según el área o sector?  
- ¿Existen **outliers** en los rangos salariales?  
- ¿Qué patrones se observan en la evolución temporal de las publicaciones?  

📓 El análisis se encuentra documentado en `Notebooks/EDA.ipynb`.  

---
## 💡 Hallazgos e Insights

  -La demanda laboral se concentra en grandes ciudades como Quito y Guayaquil.
  
  -Sectores como tecnología, ventas y salud destacan por la cantidad de ofertas.
  
  -Existen diferencias significativas en los salarios según la ciudad y el área.

  -Algunos anuncios muestran salarios atípicos (muy altos o muy bajos) que deben tratarse como outliers

---

## 📊 Visualizaciones  

Se generaron gráficos informativos y atractivos usando **Matplotlib** y **Seaborn**:  

- **Gráficos de barras** → Sectores con mayor número de vacantes.  
- **Mapas interactivos (Folium)** → Distribución geográfica de ofertas.  
- **Boxplots** → Comparación de salarios entre sectores y ciudades.  
- **Series temporales** → Evolución de publicaciones de empleo por mes.  

--------------------------------------------------------------


## 🚀 Tecnologías Utilizadas

- **Python**: manipulación de datos y análisis.  
- **Pandas**: limpieza, transformación y análisis de datos.  
- **Seaborn & Matplotlib**: visualizaciones estadísticas.  
- **Plotly**: dashboards interactivos.  
- **Google Colab / Jupyter Notebook**: entornos de ejecución y experimentación.

---

## 🎓 Relevancia Académica

Este dataset es especialmente útil en la materia de Tratamiento de Datos, ya que permite aplicar:

  -Técnicas de preprocesamiento y limpieza de datos.

  -Transformación y creación de nuevas variables.

  -Análisis exploratorio con estadísticas descriptivas.

  -Visualización de datos para comunicar hallazgos de forma efectiva.

  -Opcionalmente, el uso de Machine Learning para predicción salarial.

En otras palabras, funciona como un laboratorio práctico que conecta la teoría con un caso real de interés social y económico.


## 🔎 Análisis Exploratorio de Datos (EDA)  

Algunas de las preguntas exploradas fueron:  

- ¿Cuáles son los sectores con mayor número de ofertas laborales?  
- ¿Qué ciudades concentran más oportunidades de empleo?  
- ¿Cómo varían los salarios según el área o sector?  
- ¿Existen **outliers** en los rangos salariales?  
- ¿Qué patrones se observan en la evolución temporal de las publicaciones?  

📓 El análisis se encuentra documentado en `Notebooks/EDA.ipynb`.  

---

## 📊 Visualizaciones  

Se generaron gráficos informativos y atractivos usando **Matplotlib** y **Seaborn**:  

- **Gráficos de barras** → Sectores con mayor número de vacantes.  
- **Mapas interactivos (Folium)** → Distribución geográfica de ofertas.  
- **Boxplots** → Comparación de salarios entre sectores y ciudades.  
- **Series temporales** → Evolución de publicaciones de empleo por mes.  


---

## 📈 Posibles Análisis Avanzados

Además del EDA básico, se pueden explorar:

## Análisis de correlaciones:

  Relación entre ciudad y nivel salarial.
  
  Relación entre sector y rango salarial.

## Modelos predictivos (Machine Learning):

  Regresión lineal para estimar salario según cargo, ciudad y sector.
  
  Clasificación de ofertas por nivel de salario (alto, medio, bajo).

## Análisis geográfico:

  Mapas de calor con Folium mostrando concentración de empleos por provincia.

  Comparación de sueldos promedio entre Sierra, Costa y Amazonía.

## Series temporales:

  Evolución del número de vacantes a lo largo del tiempo.
  
  Impacto de la pandemia u otros eventos en la publicación de ofertas.

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

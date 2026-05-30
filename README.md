# ConnectaTel LATAM - Análisis de Clientes y Uso de Servicios

## Descripción del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel LATAM a partir de información demográfica, planes contratados y patrones de uso de servicios de telecomunicaciones.

El análisis incluye procesos de exploración, limpieza de datos, detección de problemas de calidad, análisis estadístico, visualización, detección de outliers y segmentación de clientes para generar recomendaciones de negocio.

---

## Datasets Utilizados

### plans.csv

Contiene la información de los planes disponibles para los clientes:

* plan_name
* messages_included
* gb_per_month
* minutes_included
* usd_monthly_pay
* usd_per_gb
* usd_per_message
* usd_per_minute

### users_latam.csv

Contiene información de los clientes:

* user_id
* first_name
* last_name
* age
* city
* reg_date
* plan
* churn_date

### usage.csv

Contiene el historial de uso de servicios:

* id
* user_id
* type
* date
* duration
* length

---

## Etapas del Análisis

### 1. Exploración de Datos

* Revisión de estructura de los datasets.
* Análisis de tipos de datos.
* Identificación de valores nulos.
* Revisión de valores inválidos y sentinels.

### 2. Limpieza de Datos

Se identificaron y corrigieron los siguientes problemas:

* Valor inválido -999 en la columna age.
* Valor "?" en la columna city.
* Fechas futuras (2026) en reg_date.
* Revisión de nulos en duration y length.

### 3. Análisis Estadístico

Se calcularon:

* Medidas de tendencia central.
* Medidas de dispersión.
* Distribuciones categóricas.
* Resúmenes por usuario.

### 4. Visualización

Se generaron histogramas para:

* Edad
* Cantidad de mensajes
* Cantidad de llamadas
* Minutos de llamada

También se utilizaron boxplots para detectar valores atípicos.

### 5. Detección de Outliers

Se aplicó el método IQR para identificar valores extremos en:

* cant_mensajes
* cant_llamadas
* cant_minutos_llamada

### 6. Segmentación de Clientes

Se crearon segmentos por:

#### Nivel de Uso

* Bajo uso
* Uso medio
* Alto uso

#### Edad

* Joven
* Adulto
* Adulto Mayor

### 7. Insights y Recomendaciones

Se identificaron oportunidades comerciales relacionadas con:

* Usuarios de alto consumo.
* Migración de clientes hacia planes Premium.
* Segmentación por edad.
* Optimización de ofertas comerciales.

---

## Principales Hallazgos

* El plan Basico concentra aproximadamente el 64.9% de los usuarios.
* El plan Premium representa aproximadamente el 35.1%.
* La mayoría de los clientes pertenece al segmento de Uso Medio.
* Los usuarios Adultos constituyen el grupo de edad más numeroso.
* Existen usuarios con consumos muy elevados de minutos de llamada que representan oportunidades comerciales relevantes.

---

## Cómo Ejecutar el Proyecto

### Google Colab

1. Abrir el notebook `.ipynb`.
2. Cargar los datasets requeridos.
3. Ejecutar las celdas en orden.

### Jupyter Notebook

1. Instalar dependencias:

```python
pip install pandas matplotlib seaborn numpy
```

2. Abrir el notebook.
3. Ejecutar todas las celdas secuencialmente.

---

## Autor

Ana Villanueva

Proyecto desarrollado como parte del programa de Data Analysis en TripleTen.

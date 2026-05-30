# ConnectaTel LATAM - Análisis de Clientes y Uso de Servicios

## Descripción del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel LATAM utilizando información demográfica, Planes contratados y patrones de uso de servicios de telecomunicaciones.

A través de técnicas de limpieza, exploración y análisis de datos, se identifican patrones de comportamiento, segmentos de clientes y oportunidades de negocio para mejorar la oferta de servicios.

---

## Datasets Utilizados

### users_latam.csv
Contiene información de los usuarios:

- user_id
- first_name
- last_name
- age
- city
- reg_date
- plan
- churn_date

### usage.csv
Contiene la actividad de los usuarios:

- id
- user_id
- type
- date
- duration
- length

### plans.csv
Contiene información sobre los planes disponibles:

- plan_name
- messages_included
- gb_per_month
- minutes_included
- usd_monthly_pay
- usd_per_gb
- usd_per_message
- usd_per_minute

---

## Etapas del Análisis

### 1. Exploración Inicial
- Revisión de estructura y tipos de datos.
- Identificación de valores nulos.
- Detección de valores inválidos o sentinels.

### 2. Limpieza de Datos
- Reemplazo del valor sentinel `-999` en la columna `age`.
- Reemplazo de `?` por valores nulos en `city`.
- Corrección de fechas fuera de rango.
- Validación de nulos en las variables de uso.

### 3. Análisis Estadístico
- Resumen estadístico de variables numéricas.
- Distribución de planes contratados.
- Análisis de comportamiento por usuario.

### 4. Visualización de Datos
- Histogramas para:
  - Edad
  - Cantidad de mensajes
  - Cantidad de llamadas
  - Minutos de llamada

- Boxplots para detección de outliers.

### 5. Segmentación de Clientes

#### Segmentación por Uso
- Bajo uso
- Uso medio
- Alto uso

#### Segmentación por Edad
- Joven
- Adulto
- Adulto Mayor

### 6. Insights y Recomendaciones
Se generaron conclusiones orientadas al negocio basadas en los patrones de uso y segmentos identificados.

---

## Principales Hallazgos

- El plan Básico concentra aproximadamente el 65% de los usuarios.
- El plan Premium representa cerca del 35% de los clientes.
- La mayoría de los usuarios pertenece al segmento de uso medio.
- Los adultos representan el grupo de edad más numeroso.
- Se identificaron usuarios con consumos elevados de minutos de llamada que podrían representar oportunidades para planes de mayor valor.

---

## Herramientas Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---


## Autor

Ana Villanueva

Proyecto desarrollado como parte del programa Data Analyst de TripleTen.

## Autor

Ana Villanueva

Proyecto desarrollado como parte del programa de Data Analysis en TripleTen.

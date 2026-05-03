# Case Study: Estrategia de Crecimiento Cyclistic (Chicago)
### Análisis Estadístico Avanzado para la Conversión de Usuarios Casuales a Miembros

Este proyecto es el caso práctico final de la **Certificación de Google Data Analytics**, el cual he perfeccionado aplicando técnicas de **Análisis Exploratorio de Datos (EDA)** y conceptos de **estadística robusta** para obtener insights de negocio más precisos.

---

## 🎯 Objetivo del Proyecto
El propósito principal es analizar los datos históricos de viajes de **Cyclistic** para identificar las diferencias en el comportamiento de uso entre los usuarios **casuales** y los **miembros anuales**. El fin es proporcionar recomendaciones estratégicas basadas en evidencia para convertir a los usuarios ocasionales en suscriptores recurrentes.

---

## 🛠️ Herramientas y Tecnologías
* **Lenguaje:** R
* **Entorno de Reporte:** Quarto (Generación de HTML Interactivo)
* **Librerías Clave:** `tidyverse` (dplyr, ggplot2), `kableExtra`, `knitr`.
* **Procesamiento:** Consolidación de 12 meses de datos y limpieza estadística masiva.

---

## 📊 Metodología y Calidad de Datos
Se trabajó con una muestra de **4,034,328 de registros** correspondientes al periodo comprendido entre **marzo de 2025 y febrero de 2026**.

### Limpieza y Filtrado Estadístico
Durante el EDA, se detectó que el promedio de duración estaba fuertemente sesgado por valores atípicos (viajes de hasta 24 horas por errores operativos).
* **Detección de Outliers:** Se utilizaron **Percentiles (P95/P99)** y el **Rango Intercuartílico (RIC)** para identificar técnicamente los valores extremos.
* **Criterio de Negocio:** Se estableció un filtro de **4 horas (14,400 segundos)** para eliminar ruidos operativos, conservando la integridad del uso recreativo legítimo.

---

## 📈 Hallazgos Estadísticos Clave
Para evitar el sesgo de la media aritmética, el análisis se centró en medidas de tendencia central y dispersión **robustas**:

### 1. El "Usuario Típico" (Mediana)
Se determinó que el viaje típico de un usuario **Casual (12.65 min)** es un **44.5% más largo** que el de un **Miembro (8.75 min)**. Esto confirma un perfil de uso recreativo vs. uno funcional enfocado en la eficiencia del traslado.

### 2. Consistencia y Variabilidad (MAD)
Utilizando la **Desviación Mediana Absoluta (MAD)**:
* **Miembros:** Presentan un comportamiento bastante predecible (MAD de 6.23 min).
* **Casuales:** Presentan el **casi el doble de variabilidad** (MAD de 9.89 min), reflejando un uso heterogéneo y exploratorio.

---
## 💡 Recomendaciones Estratégicas
Basado en los patrones de frecuencia (picos en fines de semana) y duración, se proponen:
1.  **Membresía de Fin de Semana:** Atacar el segmento casual que utiliza el servicio mayoritariamente los sábados y domingos.
2.  **Beneficios por Duración:** Incluir "minutos de cortesía" en viajes largos dentro de la suscripción anual para atraer a quienes valoran el paseo recreativo.
3.  **Marketing Estacional:** Campañas de conversión en primavera para captar la reactivación del uso tras el invierno de Chicago.

---

## 📁 Estructura del Proyecto
* `ciclistic.qmd`: Código fuente en Quarto con el análisis detallado en R.
* `ciclistic.html`: Reporte final interactivo (Publicado en GitHub Pages).
* `data/`: Referencias a la base de datos original de Divvy Trips Chicago.

---
**Autor:** Santiago Gonzalez  

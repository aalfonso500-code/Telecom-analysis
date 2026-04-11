# 📊 Análisis de Comportamiento y Segmentación de Clientes: ConnectaTel 2024

Este proyecto realiza un análisis exploratorio y descriptivo de la base de usuarios de **ConnectaTel**, una empresa de telecomunicaciones, con el fin de identificar patrones de uso, segmentos demográficos clave y oportunidades de optimización de ingresos.

## 🎯 Objetivo del Proyecto
El objetivo principal es transformar datos crudos de telecomunicaciones en **insights accionables** que permitan a la gerencia de ConnectaTel:
* Identificar los segmentos de clientes más valiosos.
* Detectar anomalías de consumo (outliers) y posibles riesgos de fraude.
* Diseñar estrategias de retención para usuarios de bajo uso.
* Optimizar la oferta de planes según la edad y el comportamiento del usuario.

## 💾 Datasets Utilizados
El análisis se basa en el conjunto de dataframes: `user`, `usage` y `plans`, que incluye variables como:
* **Demográficas:** Edad y Grupo de Edad (Joven, Adulto, Adulto Mayor).
* **Comportamiento de Voz:** Cantidad de llamadas y duración total en minutos.
* **Mensajería:** Cantidad de mensajes enviados.
* **Nivel de Uso:** Variable calculada para segmentar a los usuarios en "Bajo", "Medio" y "Alto" uso.

*Nota: Durante el proceso se realizó la limpieza de aproximadamente un 20% de datos nulos en métricas de consumo para asegurar la integridad del reporte.*

## 🛠️ Etapas del Análisis
1.  **Limpieza y Preprocesamiento:** Tratamiento de valores nulos (imputación con 0) y corrección de tipos de datos.
2.  **Ingeniería de Características:** Creación de columnas de segmentación (`grupo_edad` y `grupo_uso`) mediante lógica de negocio y librerías como `NumPy`, `Pandas`, `Seaborn` y `Matplotlib`.
3.  **Análisis Descriptivo:** Evaluación de la distribución demográfica (dominio del 81.3% en segmentos adultos).
4.  **Detección de Outliers:** Identificación de patrones de uso extremo (llamadas > 90 min) mediante visualizaciones y análisis estadístico.
5.  **Cruce de Variables:** Análisis de la relación entre la edad y la intensidad de uso mediante matrices de correlación y heatmaps.

## 🚀 Cómo Ejecutar el Proyecto
Para visualizar y ejecutar el análisis de forma interactiva, sigue estos pasos:

1.  **Google Colab (Recomendado):**
    * Haz clic en el botón "Open in Colab" (si está disponible en el notebook) o sube el archivo `.ipynb` directamente a [Google Colab](https://colab.research.google.com/).
    * Sube el archivo CSV del dataset a la sección de archivos de la izquierda.
2.  **Entorno Local:**
    * Asegúrate de tener instalado Python 3.8+ y las librerías: `pandas`, `numpy`, `matplotlib` y `seaborn`.
    * Ejecuta `jupyter notebook` en tu terminal y abre el archivo correspondiente.

## 🔄 Guía de Reproducción
Para replicar los resultados obtenidos en este repositorio:
1.  Clona este repositorio: `git clone https://github.com/Adrian-Alfonso/telecom-analysis.git`
2.  Carga el DataFrame original.
3.  Ejecuta la celda de **Limpieza de Datos** para tratar los valores `NaN` en las columnas de llamadas y mensajes.
4.  Aplica la función de clasificación `grupo_uso` utilizando el código de vectorización (`np.select` o `np.where`) detallado en el notebook.
5.  Genera las gráficas de distribución utilizando `seaborn` para validar que los porcentajes coincidan con los del reporte (73.2% Uso Medio).

---
**Autor:** Adrian Alfonso  
**Rol:** Junior Data Analyst | Ingeniero Industrial  
**Ubicación:** Querétaro, México

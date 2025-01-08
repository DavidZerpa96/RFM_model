# Modelo RFM con K-Means para Ventas Minoristas

## Resumen
Este proyecto demuestra la aplicación del **análisis RFM** combinado con **clustering K-Means** para segmentar clientes según su comportamiento de compra. El proyecto utiliza un conjunto de datos de transacciones minoristas obtenido de Kaggle.

**Fuente del Dataset:** [Online Retail Listing - Kaggle](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)

---

## ¿Qué es el análisis RFM?
El análisis RFM es un método utilizado en marketing para analizar y segmentar clientes basándose en tres dimensiones clave:

- **Recencia (R):** Cuán recientemente un cliente realizó una compra.
- **Frecuencia (F):** Con qué frecuencia un cliente realiza compras.
- **Valor Monetario (M):** Cuánto dinero gasta un cliente.

Al combinar estas métricas, las empresas pueden clasificar a sus clientes en segmentos significativos para optimizar sus estrategias de marketing y mejorar la retención de clientes.

---

## ¿Qué es el clustering K-Means?
**K-Means** es un algoritmo de aprendizaje no supervisado que particiona un conjunto de datos en `K` clústeres, donde cada punto de datos pertenece al clúster con la media más cercana. Es ampliamente utilizado para:

- Segmentación de clientes.
- Identificación de patrones en los datos.
- Reducción de dimensionalidad en grandes conjuntos de datos.

### Pasos clave en K-Means:
1. Inicializar aleatoriamente los centroides de `K` clústeres.
2. Asignar cada punto de datos al centroide más cercano.
3. Actualizar los centroides en función de la media de los puntos asignados.
4. Repetir hasta que los centroides ya no cambien significativamente.

---

## Flujo de Trabajo del Proyecto
### 1. Preprocesamiento de Datos
- Se cargó el conjunto de datos y se limpiaron duplicados y valores nulos.
- Se convirtieron columnas como `InvoiceDate` a formatos apropiados para cálculos.

### 2. Cálculo RFM
- Se calcularon los valores de Recencia, Frecuencia y Monetario para cada cliente.

### 3. Clustering con K-Means
- Se determinó el número óptimo de clústeres (`K`) utilizando:
  - **Método del Codo**
  - **Puntaje de Silueta**
- Se segmentaron los clientes en 5 clústeres según sus puntajes RFM.

### 4. Análisis de Pareto
- Se aplicó el Principio de Pareto (regla 80/20) para identificar al 20% superior de clientes que contribuyen al 80% de los ingresos.

### 5. Recomendaciones Empresariales
- Se proporcionaron insights accionables para retener a clientes de alto valor y mejorar el compromiso en todos los segmentos.

---

## Resultados Clave
### Segmentos de Clientes
- **Clúster 2:** Clientes de alto valor con alta frecuencia y valores monetarios.
- **Clúster 3:** Clientes leales y valiosos.
- **Clúster 0 y 1:** Clientes promedio con compromiso moderado.
- **Clúster 4:** Clientes nuevos con bajo compromiso.

### Aspectos Destacados del Análisis de Pareto
- El 20% superior de clientes (aproximadamente 1,363 clientes) contribuyen al 80% del ingreso total.

---

## Archivos en el Repositorio
- `RFModelK-means.ipynb`: Notebook Jupyter con todo el análisis.
- `online_retail_listing.csv`: Conjunto de datos utilizado en el proyecto.
- `README.md`: Documentación del proyecto.
- `requirements.txt`: Archivo para importar las bibliotecas necesarias.

---

## Cómo Ejecutar el Notebook
1. Clona el repositorio:
   ```bash
   git clone https://github.com/DavidZerpa96/RFM_model.git
   ```
2. Navega al directorio:
   ```bash
   cd RFM_model
   ```
3. Instala las dependencias (si es necesario):
   ```bash
   pip install -r requirements.txt
   ```
4. Abre el Notebook Jupyter:
   ```bash
   jupyter notebook RFModelK-means.ipynb
   ```

---

## Mejoras Futuras
- Integrar la segmentación de clientes en tiempo real con datos en vivo.
- Utilizar técnicas de clustering adicionales como DBSCAN para comparación.
- Visualizar métricas adicionales como el valor de vida del cliente (CLV).

------------------------------------- ENGLISH VERSION ------------------------------------

# RFM Model with K-Means for Retail Sales

## Overview
This project demonstrates the application of **RFM analysis** combined with **K-Means clustering** to segment customers based on their purchasing behavior. The project uses a dataset of retail transactions sourced from Kaggle.

**Dataset Source:** [Online Retail Listing - Kaggle](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)

---

## What is RFM Analysis?
RFM analysis is a method used in marketing to analyze and segment customers based on three key dimensions:

- **Recency (R):** How recently a customer made a purchase.
- **Frequency (F):** How often a customer makes purchases.
- **Monetary Value (M):** How much money a customer spends.

By combining these metrics, businesses can classify their customers into meaningful segments to optimize their marketing strategies and improve customer retention.

---

## What is K-Means Clustering?
**K-Means** is an unsupervised machine learning algorithm that partitions a dataset into `K` clusters, where each data point belongs to the cluster with the nearest mean. It is widely used for:

- Segmenting customers.
- Identifying patterns in data.
- Reducing the dimensionality of large datasets.

### Key Steps in K-Means:
1. Randomly initialize `K` cluster centroids.
2. Assign each data point to the nearest centroid.
3. Update the centroids based on the mean of the assigned points.
4. Repeat until the centroids no longer change significantly.

---

## Project Workflow
### 1. Data Preprocessing
- Loaded the dataset and cleaned it to remove duplicates and null values.
- Converted columns like `InvoiceDate` to appropriate formats for calculation.

### 2. RFM Calculation
- Calculated Recency, Frequency, and Monetary values for each customer.

### 3. Clustering with K-Means
- Determined the optimal number of clusters (`K`) using:
  - **Elbow Method**
  - **Silhouette Score**
- Segmented customers into 5 clusters based on their RFM scores.

### 4. Pareto Analysis
- Applied the Pareto Principle (80/20 rule) to identify the top 20% of customers contributing to 80% of revenue.

### 5. Business Recommendations
- Provided actionable insights for retaining high-value customers and improving engagement across segments.

---

## Key Results
### Customer Segments
- **Cluster 2:** High-value customers with high frequency and monetary values.
- **Cluster 3:** Loyal and valuable customers.
- **Cluster 0 & 1:** Average customers with moderate engagement.
- **Cluster 4:** New customers with low engagement.

### Pareto Analysis Highlights
- Top 20% of customers (approximately 1,363 customers) contribute to 80% of the total revenue.

---

## Files in the Repository
- `RFModelK-means.ipynb`: Jupyter Notebook containing the entire analysis.
- `online_retail_listing.csv`: Dataset used in the project.
- `README.md`: Documentation for the project.
- `requirements.txt`: To import the necessary libraries.

---

## How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/DavidZerpa96/RFM_model.git
   ```
2. Navigate to the directory:
   ```bash
   cd RFM_model
   ```
3. Install dependencies (if required):
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook RFModelK-means.ipynb
   ```

---

## Future Improvements
- Integrate real-time customer segmentation with live data.
- Use additional clustering techniques (e.g., DBSCAN) for comparison.
- Visualize more metrics such as lifetime value (CLV).

---

## Acknowledgments
Dataset sourced from Kaggle ([link](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)).

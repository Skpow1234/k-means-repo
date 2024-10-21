
# Presentación sobre el Algoritmo K-means

## 1. Introducción al Algoritmo

- **¿Qué es K-means?**  
  K-means es un algoritmo de agrupamiento que tiene como objetivo dividir un conjunto de datos en grupos o "clusters" basados en características similares.  
  Es un algoritmo **no supervisado**, ya que no requiere etiquetas de los datos para realizar el agrupamiento.

- **Propósito principal**:  
  El propósito principal es organizar datos en "clusters" donde los puntos de un mismo grupo son similares entre sí y diferentes de los puntos en otros grupos.

## 2. Funcionamiento del Algoritmo

- **Mecanismo del Algoritmo**:  
  - Inicialmente se seleccionan aleatoriamente K centros de clusters (centroides).
  - Cada punto de datos es asignado al centroide más cercano, formando K clusters.
  - Se recalculan los centroides como la media de todos los puntos dentro de un cluster.
  - El proceso de asignar puntos y recalcular centroides se repite hasta que los centroides no cambian significativamente.

- **Fórmulas clave**:  
  - Distancia Euclidiana: \(d(x, y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}\)  
  - Recalculo del centroide: \(\mu_j = \frac{1}{|C_j|} \sum_{x \in C_j} x\)
    donde \(C_j\) es el conjunto de puntos asignados al cluster \(j\) y \(\mu_j\) es el nuevo centroide.

- **Toma de decisiones**:  
  - Se basa en la distancia entre los puntos de datos y los centroides de los clusters.
  - El algoritmo busca minimizar la suma de las distancias al cuadrado entre los puntos de datos y sus respectivos centroides (inercia).

## 3. Aplicaciones Prácticas

- **Casos de uso reales**:
  - **Segmentación de clientes**: Agrupar clientes en función de características como el comportamiento de compra o datos demográficos.
  - **Compresión de imágenes**: Reducir la cantidad de colores en una imagen representándola con los colores promedio de los clusters.
  - **Agrupamiento de documentos**: Clasificar documentos según similitud de temas.

- **Problemas que puede resolver**:  
  - Detección de patrones en grandes volúmenes de datos.
  - Reducción dimensional de datos agrupando puntos similares.
  - Identificación de grupos homogéneos en estudios de mercado o biología.

## 4. Ventajas y Desventajas

- **Ventajas**:
  - **Simplicidad**: Fácil de entender e implementar.
  - **Escalabilidad**: Funciona bien con grandes volúmenes de datos.
  - **Rápido**: Comparado con otros algoritmos de clustering, K-means es computacionalmente eficiente.

- **Desventajas**:
  - **Sensibilidad a la elección de K**: Se requiere definir el número de clusters de antemano.
  - **Sensibilidad a puntos atípicos**: Outliers pueden distorsionar los resultados.
  - **Forma de los clusters**: Tiende a crear clusters esféricos, lo que puede ser una limitación en datos con estructuras complejas.

## 5. Ejemplo Práctico

- **Conjunto de datos sencillo**:  
  Se puede utilizar un conjunto de datos de puntos bidimensionales para demostrar cómo K-means agrupa los puntos en 3 clusters.

- **Procedimiento**:
  1. Elegir aleatoriamente 3 centroides iniciales.
  2. Asignar cada punto al centroide más cercano.
  3. Recalcular los centroides y repetir hasta la convergencia.

- **Estudio de caso**:  
  Segmentación de clientes en una tienda de comercio electrónico basándose en el valor de compra y la frecuencia de visitas.

## 6. Visualización de Resultados

- **Gráficos**:
  - Gráfico de dispersión mostrando los puntos de datos y sus clusters asignados (diferentes colores para cada cluster).
  - Centroides visualizados como puntos destacados en el gráfico.

- **Gráfico de inercia (codo)** para seleccionar el número óptimo de clusters K, observando dónde se produce una disminución abrupta en la inercia.
- **Comparación** entre los puntos antes y después de aplicar K-means para mostrar cómo el algoritmo agrupa los datos.

# Aplicación de SVD y PCA para Reducción de Dimensionalidad

## 📌 Introducción
Este proyecto presenta un estudio aplicado de la Descomposición en Valores Singulares (SVD) como método base para el desarrollo del Análisis de Componentes Principales (PCA)[cite: 1]. El objetivo principal es evaluar la reducción de dimensionalidad en un conjunto de datos multivariante proveniente de la observación y medición de pétalos y semillas de la especie *Guayaquilensis Triplaris* dentro de la Escuela Superior Politécnica del Litoral[cite: 1]. Se busca mitigar el ruido, aminorar la redundancia y facilitar la compresión de la información sin perder datos vitales[cite: 1].

## ⚙️ Metodología Aplicada
El análisis computacional se implementó utilizando el lenguaje Python, estructurando el proceso en las siguientes fases[cite: 1]:
1. **Preprocesamiento de datos:** Se utilizó la librería `pandas` para estructurar un DataFrame a partir de un archivo `.ods` que contenía medidas mixtas (lineales y polares)[cite: 1]. 
2. **Validación de supuestos:** Se evaluó la linealidad mediante una matriz de correlación y se comprobó la necesidad de escalar y normalizar las variables debido a la distribución desigual de magnitudes[cite: 1].
3. **Aplicación de SVD:** Se utilizó el módulo `numpy.linalg.svd` para factorizar la matriz de datos[cite: 1]. Este método se prefirió por sobre el cálculo explícito de la matriz de covarianza debido a que otorga mayor estabilidad numérica y agiliza el proceso[cite: 1].

## 📊 Resultados
Tras aplicar la transformación proyectiva sobre el nuevo sistema de coordenadas, se obtuvieron los siguientes hallazgos:

* **Dominancia de PC1:** Se comprobó que el sistema puede describirse casi en su totalidad de forma unidimensional[cite: 1]. La primera componente principal (PC1) explica aproximadamente el 97% de la varianza total[cite: 1].
* **Variables angulares:** Dentro de la combinación lineal, las variables angulares (especialmente θ3) dominan el comportamiento de la primera componente principal[cite: 1].
* **Descarte de componentes secundarias:** Componentes como PC2 apenas explican entre el 2% y 3% de la varianza, representando variaciones secundarias asociadas a ruido experimental, por lo que no aportan información relevante adicional[cite: 1].

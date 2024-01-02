# Práctica de Detección de imágenes con Redes Neuronales Convolucionales (CNN) en PyTorch

## Funcionamiento
El código se estructura en torno al entrenamiento y evaluación de un conjunto de tres modelos de red neuronal convolucional avanzada (AdvancedCNN) utilizando la biblioteca PyTorch.
#### 1. Preprocesamiento de Datos:
Se aplican transformaciones a las imágenes, como redimensionamiento y conversión a tensores.
Los datos se dividen en conjuntos de entrenamiento, validación y prueba, con un 70%, y el 30% restante dividido equitativamente entre validación y prueba.
#### 2. Diseño del Modelo:
Se utiliza un modelo CNN avanzado (AdvancedCNN) con capas convolucionales y completamente conectadas.
Se implementan funciones para calcular la precisión del modelo, entrenarlo y aplicar técnicas de regularización L1 y L2.
Se incorpora la estrategia de early stopping para controlar el sobreajuste.
#### 3. Entrenamiento Inicial:
Se entrenan tres modelos AdvancedCNN exclusivamente con el conjunto de entrenamiento.
El conjunto de validación se utiliza para evaluar el rendimiento de cada modelo en cada época y aplicar early stopping.
#### 4. Reentrenamiento:
Se realiza un reentrenamiento exponiendo cada modelo a un conjunto combinado de entrenamiento y validación, representando el 85% del conjunto total.
#### 5. Evaluación Final:
Se evalúan individualmente los tres modelos en el conjunto de prueba (15% restante).
Se lleva a cabo una evaluación de ensemble combinando las predicciones de los tres modelos para obtener una medida agregada de rendimiento.
#### 6. Visualización de Predicciones:
Se incluye una función para visualizar las predicciones de los modelos en imágenes del conjunto de prueba, mostrando etiquetas verdaderas y predicciones.

## WandB y Registro de Métricas:
Durante el entrenamiento y evaluación de un segundo conjunto de datos, se utiliza la biblioteca Weights & Biases (WandB) para registrar y visualizar métricas en tiempo real. Esto proporciona una interfaz interactiva para analizar el rendimiento de los modelos. Algunas de las métricas registradas incluyen:
Pérdida y precisión en el conjunto de entrenamiento y validación en cada época.
Precisión final en el conjunto de prueba para cada modelo y para el ensemble.

## Resultados y Conclusiones
Los modelos son capaces de aprender patrones complejos en los datos de entrenamiento y generalizar de manera efectiva en el conjunto de prueba. La estrategia de reentrenamiento mejora aún más la capacidad de generalización de los modelos, lo que se refleja en un rendimiento robusto en el conjunto de prueba.
La evaluación de ensemble proporciona una medida agregada que aprovecha la diversidad de los modelos individuales, lo que puede resultar en un rendimiento más sólido y confiable en tareas de clasificación.
Los resultados obtenidos a través de WandB permiten una evaluación detallada del rendimiento de los modelos en distintas fases del entrenamiento y validación. La precisión final en el conjunto de prueba, tanto de cada modelo individual como del ensemble, ofrece una visión completa del rendimiento general del sistema.

# Memoria Técnica

## Portada
- **Nombre del Proyecto**: Clasificador de Emociones
- **Fecha**: 13 Diciembre 2024
- **Integrantes**:
  - Juárez Millán Ángel Andrés
  - Lara Bustillos Damaris Aylin
  - Evaristo Ramírez Erik

 

![Emociones](../images/portada-el-cuidado-de-las-emociones-basicas.jpg)

## Índice
- [Portada](#portada)
- [Alcance del proyecto](#alcance-del-proyecto)
  - [Objetivo](#objetivo)
  - [Introducción](#introducción)
- [Fuentes de información y procedimientos aplicados](#fuentes-de-información-y-procedimientos-aplicados)
  - [Construcción del modelo](#construcción-del-modelo)
  - [Resultados modelo](#resultados-modelo)
  - [Pruebas sobre el modelo](#pruebas-sobre-el-modelo)
  - [Conclusiones](#conclusiones)
- [Conclusiones generales](#conclusiones-generales)
- [Anexos](#anexos)
- [Glosario](#glosario)

## Alcance del proyecto

### Objetivo
- Construir un modelo capaz de clasificar emociones comunes como alegría, tristeza, enojo, sorpresa, miedo y neutralidad.
- Evaluar el modelo en un conjunto de datos estándar y analizar su desempeño.

### Introducción
El análisis de emociones a partir de expresiones faciales ha capturado un interés creciente en los últimos años debido a sus aplicaciones prácticas y su relevancia en la interacción humano-computadora. Las emociones no solo son un componente esencial de la comunicación no verbal, sino que también pueden revelar el estado mental y los sentimientos de una persona, lo que resulta invaluable en una variedad de contextos.

Desde asistentes virtuales más empáticos hasta herramientas de diagnóstico en salud mental, el reconocimiento de emociones tiene aplicaciones que abarcan sectores como la atención al cliente, la educación, la psicología y la seguridad. Por ejemplo, en la educación, los sistemas de aprendizaje pueden adaptarse dinámicamente según las emociones del estudiante, mientras que en la atención médica, se pueden diseñar soluciones para detectar signos tempranos de depresión o ansiedad.

A pesar de estos beneficios, el desarrollo de clasificadores de emociones plantea varios desafíos. Factores como las diferencias culturales en la expresión de emociones, las variaciones en condiciones de iluminación y pose en las imágenes, así como la necesidad de equilibrar clases desproporcionadas en los conjuntos de datos, complican la tarea.

## Fuentes de información y procedimientos aplicados

El conjunto de datos, descargado de Kaggle


## Pipeline de Preparación
### 1. Crear Etiquetas 
- Clasificamos las imágenes basándonos en si contienen al menos un trofozoíto.
  ![Distribucion binaria](../images/proportion.png)
### 2. División del Conjunto de Datos
- Los datos se dividen en entrenamiento y validación con proporciones del 80% y 20% respectivamente.

  | Conjunto         | Cantidad de Imágenes |
  |-------------------|----------------------|
  | Entrenamiento     | 2,197               |
  | Validación        | 550                 |
  

  - **Total de imágenes:** 2,747
  - **Etiquetas:**

-**Conclusiones generales**

El modelo seleccionado tiene un buen desempeño global para identificar emociones en imágenes con una exactitud del 79%, pero hay algunas clases que están más confundidas que otras, especialmente la Clase 0 y la Clase 1, lo que podría indicar que esas clases tienen características similares que dificultan su separación.

Podríamos mejorar el modelo si encontramos la forma de utilizar redes pre entrenadas, por ejemplo; o si podemos aumentar significativamente los datos de nuestro modelo. Esta última es la parte más complicada pues se necesitan demasiados datos y los datasets que existen en la red no son tan fiables ya que en muchos casos las categorías son ambiguas, las imágenes que vienen en alguna categoría no necesariamente describen lo que dice esta categoría y revisar cada una de estas, en conjuntos muy grandes, resulta ser una tarea pesada.
También se puede intentar correr en algún entorno mejor, que permita ejecutar redes neuronales pesadas como VGG16 para ver cómo se comporta el modelo.

 
-**Anexos**
-[Repositorio Github](https://github.com/AylinLara/2025-I-proyecto-I/blob/c8c15622e03d37f98cfd2ae5a2e5d09e4225a9af/Clasificador_emociones.ipynb)

- [Conjunto de Datos para la Detección de Conductores Distraídos en Kaggle]()

## Glosario

-**A**

- **Activación (Activation)**: Función matemática que introduce no linealidad a las salidas de una neurona. Ejemplos: ReLU, Sigmoid, Tanh.

-**Arquitectura (Architecture)**: Diseño estructural de la red neuronal, incluyendo las capas y cómo están conectadas.


-**B**

-**Batch Size (Tamaño del Lote)**: Número de muestras procesadas antes de actualizar los pesos del modelo.


-**C**

-**Capas convolucionales (Convolutional Layers)**: Componentes de una CNN que extraen características locales de las imágenes mediante convoluciones.

-**Capas densas o completamente conectadas (Fully Connected Layers)**: Capas donde cada neurona está conectada a todas las neuronas de la capa previa.

-**Convolución (Convolucion)**: Operación matemática que aplica un filtro sobre una imagen para detectar patrones.


-**D**

-**Dropout**: Técnica de regularización que desactiva aleatoriamente neuronas durante el entrenamiento para prevenir sobreajuste.
Dataset: Conjunto de datos utilizado para entrenar, validar y probar el modelo.


-**E**

-**Epoch**: Una iteración completa sobre todo el conjunto de datos durante el entrenamiento.

-**Extracción de características (Feature Extraction)**: Proceso de identificar patrones relevantes en los datos para clasificarlos.


-**F**

-**Filtro (Kernel)**: Matriz pequeña usada en las convoluciones para detectar características específicas.

-**Función de pérdida (Loss Function)**: Métrica utilizada para medir el error entre las predicciones del modelo y las etiquetas verdaderas.


-**G**

-**Gradiente (Gradient)**: Derivada del error respecto a los pesos de la red, utilizada para actualizarlos.

-**Gradiente descendente (Gradient Descent)**: Algoritmo de optimización que minimiza el error ajustando los pesos de la red.


-**H**

-**Hiperparámetros (Hyperparameters)**: Parámetros configurados manualmente antes del entrenamiento, como la tasa de aprendizaje o el número de filtros.

-**Pooling (Submuestreo)**: Reducción del tamaño de las características mediante operaciones como max pooling o average pooling.


-**M**

-**Matriz de confusión (Confusion Matrix)**: Herramienta para evaluar el rendimiento del clasificador mostrando verdaderos positivos, falsos positivos, etc.


-**O**

-**Overfitting (Sobreajuste)**: Problema en el que el modelo aprende demasiado bien el conjunto de entrenamiento pero falla en generalizar a nuevos datos.

-**Optimización**: Proceso de ajustar los pesos para minimizar la función de pérdida.


-**P**

-**Precision (Precisión)**: Proporción de predicciones correctas en las clases positivas.
Preprocesamiento: Transformaciones aplicadas a los datos para hacerlos adecuados para el modelo.


-**R**

-**Red Neuronal Convolucional (CNN)**: Tipo de red neuronal diseñada para procesar datos con estructura de cuadrícula, como imágenes. Las CNN son especialmente eficaces en tareas de visión por computadora, como la clasificación de imágenes, la detección de objetos y la segmentación semántica.

-**ReLU (Rectified Linear Unit)**: Función de activación que convierte valores negativos en ceros, manteniendo valores positivos.
Regularización: Métodos que evitan que el modelo se ajuste demasiado al conjunto de entrenamiento, como L2 o Dropout.


-**S**
-**Stride (Paso)**: Desplazamiento del filtro en una convolución. Un stride mayor reduce el tamaño de la salida.

-**Softmax**: Función utilizada en la última capa de clasificación para convertir salidas en probabilidades.


-**T**

-**Test Set (Conjunto de pruebas)**: Subconjunto de datos utilizado exclusivamente para evaluar el rendimiento del modelo.
Tensor: Arreglo multidimensional de datos, como una extensión de matrices.


-**V**

-**Validación cruzada (Cross-Validation)**: Técnica para evaluar un modelo dividiendo los datos en varios subconjuntos de entrenamiento y validación.

-**Volumen de salida (Output Volume)**: Dimensiones de los datos resultantes después de aplicar una operación en la red (convolución, pooling, etc.).

# Entrenamiento del Modelo

El modelo que vamos a desarrollar se centra en analizar un dataset de **Kaggle** utilizando la metodología **CRISP-DM**, con el objetivo de crear un sistema de aprendizaje automático que prediga el riesgo de desarrollar diabetes.

> **Metodología CRISP-DM:**  
> Este enfoque estructurado en minería de datos abarca desde la comprensión del negocio hasta la implementación del modelo. Su aplicación nos permite extraer conocimiento valioso y construir soluciones predictivas de manera sistemática.

## Objetivo del Proyecto

Desarrollar una **aplicación web** que, a partir del análisis del dataset, evalúe las características de una persona y asigne una puntuación del **0 al 100**, indicando qué tan propensa es a sufrir diabetes.

## Fases del Proceso

1. **Comprensión del negocio:**  
   - Definir los objetivos y el alcance del análisis.
   - Identificar los factores de riesgo y variables relevantes que influyen en la probabilidad de desarrollar diabetes.

2. **Comprensión y preparación de los datos:**  
   - Explorar, limpiar y transformar el dataset para garantizar datos de calidad.
   - Extraer características clave que permitan realizar una predicción precisa.

3. **Modelado y evaluación:**  
   - Desarrollar y optimizar el modelo de aprendizaje automático mediante técnicas de clasificación o regresión.
   - Evaluar el desempeño del modelo para asegurar que la predicción (de 0 a 100) sea fiable.

4. **Implementación:**  
   - Integrar el modelo en una aplicación web que permita a los usuarios ingresar sus datos y recibir una predicción del riesgo de diabetes.
   - Facilitar la toma de decisiones preventivas y el seguimiento personalizado.

## Paso 1
![Entrenamiento del modelo](https://github.com/adiacla/diabetes/blob/main/imagenes/1-entrenamiento.jpg?raw=true)

Para iniciar el entrenamiento del modelo, haz clic en el botón que te dirige a Google Colab, el cual se encuentra en el archivo `Riesgo_Diabetes.ipynb`.

## Paso 2
![Imagen 2](https://github.com/adiacla/diabetes/blob/main/imagenes/2-entrenamiento.jpg?raw=true)
![Imagen 0](https://github.com/adiacla/diabetes/blob/main/imagenes/0-entrenamiento.jpg?raw=true)
![Imagen 3](https://github.com/adiacla/diabetes/blob/main/imagenes/3-entrenamiento.jpg?raw=true)

Antes de comenzar a ejecutar, es importante limpiar cualquier resultado previo para iniciar desde cero. Para ello, cambia el tipo de entorno de ejecución y vuelve a conectarte. Además, revisa la sección de archivos (en la barra lateral izquierda) para asegurarte de que, aparte de la carpeta `sample-Data`, no aparezca ningún archivo adicional.

## Paso 3
![Imagen 4](https://github.com/adiacla/diabetes/blob/main/imagenes/4-entrenamiento.jpg?raw=true)
![Imagen 5](https://github.com/adiacla/diabetes/blob/main/imagenes/5-entrenamiento.jpg?raw=true)

Una vez realizado lo anterior, dirígete a **Entorno de ejecución** y selecciona **Cambiar tipo de entorno de ejecución** para configurar la opción a **GPU T4**. Esto te permitirá disponer de mayor capacidad y ejecutar el archivo en un tiempo más reducido.

## Paso 4
![Imagen 6](https://github.com/adiacla/diabetes/blob/main/imagenes/6-entrenamiento.jpg?raw=true)

Ahora, ejecuta todas las celdas del entorno y espera a que se complete su procesamiento.

## Paso 5
![Imagen 7](https://github.com/adiacla/diabetes/blob/main/imagenes/7-entrenamiento.jpg?raw=true)

Una vez finalizada la ejecución, deberías obtener los siguientes archivos como resultado. Descárgalos.

## Paso 6
![Imagen 8](https://github.com/adiacla/diabetes/blob/main/imagenes/8-entrenamiento.jpg?raw=true)

Estos archivos se guardarán en una carpeta llamada `Diabetes` dentro de la carpeta **Documentos**, y serán utilizados para desarrollar la aplicación web.

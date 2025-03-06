# Entrenamiento del Modelo

El modelo que vamos a trabajar se centra en analizar un dataset de **Kaggle**que contiene 9,538 registros médicos relacionados con el diagnóstico de diabetes y factores de riesgo, ademas de estar ya muy limpio es muy bueno para trabajar con el, para ello, utilizaremos la metodología **CRISP-DM**.

> **Metodología CRISP-DM:**  
> La metodología CRISP-DM es un enfoque estructurado y ampliamente reconocido en el ámbito de la minería de datos. Este proceso se compone de varias fases clave que permiten abordar de manera integral el análisis y modelado de datos.

## Fases del Proceso

1. **Comprensión del negocio:**  
   Definición de objetivos y alcance del análisis, identificando las necesidades y retos específicos del negocio.

2. **Comprensión y preparación de los datos:**  
   Exploración, limpieza y transformación del dataset para asegurar la calidad y relevancia de la información.

3. **Modelado y evaluación:**  
   Desarrollo, optimización y evaluación del modelo predictivo mediante técnicas y métricas rigurosas.

4. **Implementación:**  
   Integración del modelo en un entorno que permita la toma de decisiones informada y la aplicación práctica.

Con este enfoque, buscamos extraer conocimiento valioso del conjunto de datos y construir una solución robusta y escalable que aporte un impacto real en la toma de decisiones del negocio.

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

# Plan de Proyecto: Diagnóstico de Diabetes usando Machine Learning y Streamlit

## 1. Título del Proyecto:
**Predicción de Diagnóstico de Diabetes mediante un Modelo de Machine Learning y su Despliegue Web usando Streamlit.**

---

## 2. Resumen Ejecutivo:
Este proyecto tiene como objetivo desarrollar y desplegar un modelo de clasificación para predecir si una persona tiene diabetes o no, utilizando el *Diabetes Diagnosis Dataset*. El modelo será entrenado con técnicas de machine learning como Random Forest, SVM, y otros. Posteriormente, se creará una aplicación web interactiva utilizando Streamlit donde los usuarios puedan ingresar sus datos médicos para obtener una predicción sobre su riesgo de diabetes.

---

## 3. Objetivos del Proyecto:

### Objetivo General:
Desarrollar un modelo de clasificación con machine learning que prediga el diagnóstico de diabetes utilizando el *Diabetes Diagnosis Dataset*, desplegarlo en una aplicación web con Streamlit y proporcionar una herramienta accesible para la predicción del riesgo de diabetes.

---

### Objetivos Específicos (con metodología SMART):

1. **Objetivo Específico 1: Realizar el análisis exploratorio de datos (EDA)**
   - **Específico:** Analizar el conjunto de datos *Diabetes Diagnosis Dataset*, para limpiar y entender las relaciones entre las características.
   - **Medible:** Realizar visualizaciones de las distribuciones de variables clave como la glucosa, el IMC, la edad, y la presión arterial, además de identificar correlaciones.
   - **Alcanzable:** Utilizar herramientas de Python como pandas y seaborn para la exploración de datos.
   - **Relevante:** La limpieza y el análisis de datos son fundamentales para asegurar que los modelos de clasificación tengan datos de calidad.
   - **Tiempo:** Completar el análisis exploratorio de datos en un plazo de **4 días** (del 6 al 9 de marzo de 2025).

2. **Objetivo Específico 2: Entrenar y evaluar modelos de clasificación**
   - **Específico:** Entrenar al menos tres modelos de clasificación (Random Forest, SVM y Regresión Logística) utilizando el conjunto de entrenamiento.
   - **Medible:** Evaluar cada modelo utilizando métricas como precisión, recall, F1-score, y matriz de confusión.
   - **Alcanzable:** Los modelos de clasificación seleccionados están disponibles en la biblioteca de Scikit-Learn y son adecuados para este tipo de predicción.
   - **Relevante:** Elegir el mejor modelo de clasificación permitirá hacer predicciones de diabetes de manera precisa.
   - **Tiempo:** Completar el entrenamiento y evaluación de los modelos en **6 días** (del 10 al 15 de marzo de 2025).

3. **Objetivo Específico 3: Desarrollar la aplicación web interactiva**
   - **Específico:** Crear una aplicación web en Streamlit que permita a los usuarios ingresar datos médicos y recibir una predicción del riesgo de diabetes.
   - **Medible:** La aplicación debe permitir la entrada de variables como la glucosa, el IMC, la presión arterial, y otros, y debe generar una predicción basada en el modelo entrenado.
   - **Alcanzable:** Streamlit es una herramienta de fácil implementación para crear aplicaciones web interactivas, y ya existen modelos entrenados.
   - **Relevante:** Desplegar el modelo como una aplicación web accesible es esencial para facilitar la predicción del riesgo de diabetes de manera fácil y rápida.
   - **Tiempo:** Completar el desarrollo de la aplicación web en **6 días** (del 16 al 21 de marzo de 2025).

4. **Objetivo Específico 4: Desplegar la aplicación web en un servidor accesible públicamente**
   - **Específico:** Desplegar la aplicación web creada en un servidor web como Heroku o AWS para que sea accesible públicamente.
   - **Medible:** La aplicación debe estar disponible para su uso mediante un enlace en línea, y debe funcionar de manera eficiente.
   - **Alcanzable:** Usaremos servicios gratuitos o de bajo costo como Heroku para desplegar la aplicación.
   - **Relevante:** El despliegue público es fundamental para hacer que la herramienta sea accesible a un público más amplio y facilitar el diagnóstico de diabetes.
   - **Tiempo:** Completar el despliegue en **3 días** (del 22 al 24 de marzo de 2025).

---

## 4. Supuestos del Proyecto:

1. El conjunto de datos *Diabetes Diagnosis Dataset* contiene la información necesaria para entrenar un modelo preciso de clasificación.
2. Los modelos de clasificación seleccionados tienen el rendimiento adecuado para predecir el diagnóstico de diabetes.
3. Los usuarios de la aplicación web cuentan con conocimientos básicos para ingresar sus datos correctamente.
4. El servidor de despliegue podrá manejar la cantidad de tráfico esperado sin caídas ni lentitud.

---

## 5. Metodología:

La metodología será ágil e iterativa. Se utilizarán enfoques de desarrollo incremental con ciclos de retroalimentación y ajuste continuo. Las fases del proyecto incluyen la recolección de datos, análisis exploratorio, modelado, desarrollo de la interfaz web y despliegue.

### Fases del Proyecto:
1. **Fase 1: Recolección y Preparación de Datos (Días 1-4)**
   - Importación y limpieza de datos.
   - Análisis exploratorio y visualización de datos.

2. **Fase 2: Entrenamiento de Modelos (Días 5-10)**
   - Selección y entrenamiento de los modelos de clasificación.
   - Evaluación de los modelos usando métricas de rendimiento.

3. **Fase 3: Desarrollo de la Aplicación Web (Días 11-16)**
   - Creación de la interfaz de usuario con Streamlit.
   - Integración del modelo entrenado con la interfaz.

4. **Fase 4: Despliegue y Pruebas (Días 17-19)**
   - Despliegue de la aplicación en un servidor web.
   - Pruebas de funcionamiento y accesibilidad pública.

---

## 6. Cronograma del Proyecto:

| **Fase**                            | **Duración Estimada** | **Fecha de Inicio** | **Fecha de Finalización** |
|-------------------------------------|----------------------|---------------------|---------------------------|
| **Fase 1: Recolección y Preparación de Datos** | 4 días               | 06/03/2025          | 09/03/2025                |
| **Fase 2: Entrenamiento de Modelos de Machine Learning** | 6 días               | 10/03/2025          | 15/03/2025                |
| **Fase 3: Desarrollo de la Aplicación Web** | 6 días               | 16/03/2025          | 21/03/2025                |
| **Fase 4: Despliegue y Pruebas**  | 3 días               | 22/03/2025          | 24/03/2025                |

---

## 7. Matriz de Riesgo:

| **Riesgo**                           | **Probabilidad** | **Impacto** | **Estrategia de Mitigación**                               |
|--------------------------------------|------------------|-------------|------------------------------------------------------------|
| **Falta de datos limpios y de calidad** | Alta             | Alto        | Realizar un análisis exhaustivo de los datos antes de entrenar el modelo. Limpiar y corregir los datos erróneos. |
| **Sobreajuste del modelo (overfitting)** | Media            | Alto        | Utilizar técnicas de validación cruzada y ajustar los hiperparámetros del modelo. |
| **Falta de capacidad en el servidor para la aplicación web** | Baja             | Medio       | Utilizar un servidor con recursos suficientes y realizar pruebas de carga. |
| **Errores en la interfaz de usuario**  | Baja             | Bajo        | Probar la interfaz con múltiples usuarios antes del despliegue. |
| **Desacuerdo en los resultados del modelo con expertos médicos** | Baja             | Alto        | Colaborar con expertos médicos durante la interpretación de los resultados. |

---

## 8. Recursos Necesarios:

- **Humanos:**
  - Data Scientist / Ingeniero de Machine Learning.
  - Desarrollador Web (Streamlit).
  - Médico/Experto en Diabetes para validación y colaboración.

- **Tecnológicos:**
  - Conjunto de datos *Diabetes Diagnosis Dataset*.
  - Herramientas de desarrollo como Python, Streamlit, Scikit-Learn.
  - Servidor web para despliegue (por ejemplo, Heroku o AWS).

---

## 9. Resultados Esperados:

- Un modelo de clasificación que predice con precisión el riesgo de diabetes para nuevas personas, utilizando parámetros médicos y de estilo de vida.
- Una aplicación web accesible y fácil de usar donde los usuarios puedan ingresar sus datos y obtener una predicción de riesgo de diabetes.
- El despliegue exitoso de la aplicación en un servidor web accesible públicamente.

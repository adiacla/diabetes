# Guia App Web

## 1. Abrir tu proyecto en Visual Studio Code
**Paso 1:** Abre Visual Studio Code y veras la siguiente pantalla

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/PantallaInicioVsC.PNG?raw=true)

**Paso 2:** Una vez dentro de Visual Studio Code abre el folder creado anteriormente de tu proyecto llamado Diabetes

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/AbrirFolderVsc.PNG?raw=true)

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/SeleccionarCarpeta.PNG?raw=true)

Una vez dentro de la carpeta crea un archivo llamado app.py

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/NewFile.PNG?raw=true)

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/PythonFile.PNG?raw=true)

Y copia el siguiente codigo

```bash
import streamlit as st
import numpy as np
import pandas as pd
import joblib

# Cargar modelo y transformadores
model = joblib.load('./AppWeb/random_forest_model.joblib')
scaler = joblib.load('./AppWeb/scaler.joblib')
label_encoders = joblib.load('./AppWeb/label_encoders.joblib')

# ---- Encabezado ----
st.title("Predicción de Diabetes")
st.subheader("Por Alfredo Diaz")

st.markdown(
    """
    <div style="text-align: center;">
        <img src="https://www.insideprecisionmedicine.com/wp-content/uploads/2019/01/360.jpeg" width="300">
    </div>
    """,
    unsafe_allow_html=True
)

st.write("""
### Objetivo y Uso
Esta herramienta permite predecir el riesgo de diabetes con base en datos médicos.
Ingrese sus datos o seleccione un perfil predefinido en el menú lateral.
""")

# ---- Sidebar con perfiles predefinidos ----
st.sidebar.title("Seleccione estados predefinidos")

perfiles = {
    "Joven y Saludable": [30, 1, 24.5, 90, 70, 4.8, 100, 55, 140, 85, 95, 0.85, "No", "Desequilibrada", "No", "No"],
    "Alta Glucosa y Hipertensión": [55, 3, 30.2, 150, 90, 5.9, 120, 45, 180, 95, 105, 0.90, "Si", "Desequilibrada", "Si", "No"],
    "Mayor edad con Alta Glucosa": [65, 2, 28.7, 140, 85, 6.2, 130, 40, 170, 100, 110, 0.92, "Si", "Desequilibrada", "Si", "No"],
    "Joven y sin Factores de Riesgo": [22, 0, 22.1, 85, 65, 4.5, 90, 60, 130, 80, 90, 0.89, "No", "Desequilibrada", "No", "No"],
    "Obeso y Alta Glucosa": [45, 4, 32.5, 160, 95, 6.0, 140, 35, 190, 110, 115, 0.95, "Si", "Equilibrada", "Si", "No"],
    "Edad Media con Riesgo Moderado": [50, 5, 27.5, 130, 80, 5.2, 110, 50, 150, 90, 100, 0.90, "Si", "Desequilibrada", "Si", "No"],
    "Caso Normal": [39, 2, 26.8, 110, 75, 4.9, 105, 55, 145, 88, 98, 0.88, "No", "Desequilibrada", "No", "No"],
    "Anciano con Riesgo Muy Alto": [70, 6, 33.0, 170, 100, 6.5, 150, 30, 200, 120, 125, 1.00, "Si", "Equilibrada", "Si", "No"],
    "Joven con Valores Normales": [29, 1, 23.5, 95, 68, 4.7, 98, 58, 135, 82, 92, 0.86, "No", "Desequilibrada", "No", "No"],
    "Edad Media con Hipertensión": [60, 3, 29.9, 145, 88, 5.8, 125, 42, 175, 98, 108, 0.93, "Si", "Equilibrada", "Si", "No"]
}

perfil_seleccionado = st.sidebar.selectbox("Seleccione un perfil:", list(perfiles.keys()))
valores = perfiles[perfil_seleccionado]

# ---- Formulario ----
st.write("### Ingrese sus datos médicos o edite el perfil seleccionado:")

col1, col2 = st.columns(2)

with col1:
    age = st.number_input("Edad", 18, 90, int(valores[0]))
    pregnancies = st.number_input("Número de embarazos", 0, 16, int(valores[1]))
    bmi = st.number_input("IMC", 15.0, 50.0, float(valores[2]))
    glucose = st.number_input("Glucosa (mg/dL)", 50.0, 250.0, float(valores[3]))
    blood_pressure = st.number_input("Presión Arterial", 60.0, 150.0, float(valores[4]))
    hba1c = st.number_input("HbA1c (%)", 4.0, 7.0, float(valores[5]))
    ldl = st.number_input("LDL (mg/dL)", 0.0, 300.0, float(valores[6]))
    hdl = st.number_input("HDL (mg/dL)", 0.0, 120.0, float(valores[7]))

with col2:
    triglycerides = st.number_input("Triglicéridos", 50.0, 400.0, float(valores[8]))
    waist = st.number_input("Cintura (cm)", 40.0, 200.0, float(valores[9]))
    hip = st.number_input("Cadera (cm)", 50.0, 200.0, float(valores[10]))
    whr = waist / hip
    st.write(f"**Relación Cintura/Cadera (WHR): {whr:.2f}**")

    # Selectores categóricos con índices dinámicos
    family_history = st.selectbox("Historial Familiar", ["No", "Sí"], index=["No", "Si"].index(valores[12]))
    diet_type = st.selectbox("Tipo de Dieta", ["Desequilibrada", "Equilibrada", "Vegana/Vegetariana"], index=["Desequilibrada", "Equilibrada", "Vegana/Vegetariana"].index(valores[13]))
    hypertension = st.selectbox("Hipertensión", ["No", "Sí"], index=["No", "Si"].index(valores[14]))
    medication_use = st.selectbox("Uso de Medicación", ["No", "Sí"], index=["No", "Si"].index(valores[15]))

# ---- Predicción ----
if st.button("Predecir Diabetes"):
# Crear dataframe con los datos ingresados
    input_data = pd.DataFrame({
        'Age': [age], 'Pregnancies': [pregnancies], 'BMI': [bmi], 'Glucose': [glucose],
        'BloodPressure': [blood_pressure], 'HbA1c': [hba1c], 'LDL': [ldl], 'HDL': [hdl],
        'Triglycerides': [triglycerides], 'WaistCircumference': [waist], 'HipCircumference': [hip],
        'WHR': [whr], 'FamilyHistory': [family_history], 'DietType': [diet_type],
        'Hypertension': [hypertension], 'MedicationUse': [medication_use]
    })

    # Mapeo manual según el entrenamiento original
    category_mappings = {
        'FamilyHistory': {"No": 0, "Sí": 1},
        'DietType': {"Desequilibrada": 0, "Equilibrada": 1, "Vegana/Vegetariana": 2},
        'Hypertension': {"No": 0, "Sí": 1},
        'MedicationUse': {"No": 0, "Sí": 1},
    }

    # Convertir texto a valores numéricos
    for col, mapping in category_mappings.items():
        input_data[col] = input_data[col].map(mapping)

    # Aplicar normalización
    input_data_scaled = scaler.transform(input_data)

    # Realizar predicción
    prediction = model.predict(input_data_scaled)
    prob = model.predict_proba(input_data_scaled)[0][1]

    st.subheader("Resultado:")
    if prediction[0] == 1:
        st.error(f"🛑 Alto Riesgo de Diabetes ({prob:.2%})")
    else:
        st.success(f"✅ Bajo Riesgo de Diabetes ({prob:.2%})")

st.markdown("---")
st.markdown('<div style="text-align: center; font-weight: bold;">Smart Region Lab - 2025</div>', unsafe_allow_html=True)
```

**Paso 3:** Entra a la extensiones y descarga la extension de Python

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/ExtensionesVsc.PNG?raw=true)

En la seccion de Buscar escribe Python y dale en el boton de Install

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/PyhtonExtension.PNG?raw=true)

**Paso 4:** Para crear un entorno virtual dale Ctrl+Shift+P y selecciona Create Enviroment

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/Ctrl+Shift+P.png?raw=true)

Selecciona la opcion de Crear un entorno Venv

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/VenvSeleccionar.PNG?raw=true)

Selecciona la opcion de Python 3.10.0

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/Python10.PNG?raw=true)

Para rectificar que se creo correctamente tu entorno virtual, veras una carpeta creada .venv, luego abre la terminal con Ctrl+ñ y escribe el siguiente comando

```bash
pip list
```
Deberias ver lo siguiente

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/PipList.PNG?raw=true)


**Paso 4:** Instalar las dependencias necesarias en la terminal

```bash
pip install scikit-learn
```

```bash
pip install streamlit
```

Para comprobar que se realizaron las instalaciones correctamente utilizamos nuevamente el comando de pip list en el cual deberian aparecer todas esas dependencias que acabamos de descargar

```bash
pip list
```

**Paso 5:** Para ejecutar el codigo recuerden no seleccionar la opcion de ejecutar que tiene visual studio

![diabetes/imagenes](https://github.com/adiacla/diabetes/blob/main/imagenes/NoEjecutar.PNG?raw=true)

Para dejecutar el codigo deberan escribir el siguiente comando en su terminal

```bash
streamlit run app.py
```



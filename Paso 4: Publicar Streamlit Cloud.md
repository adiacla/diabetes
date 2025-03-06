# Guía para Deployment en Streamlit

En este tutorial aprenderás cómo desplegar una aplicación en Streamlit utilizando GitHub. Sigue los pasos detallados a continuación para completar el proceso de manera sencilla.

## 1. Crear una cuenta en GitHub
Dirígete a [GitHub.com](https://github.com) para comenzar. Si aún no tienes una cuenta, haz lo siguiente:

- Haz clic en el botón **Sign Up** ubicado en la esquina superior derecha de la página.

![Imagen 1_1_githubcom](https://github.com/adiacla/diabetes/blob/main/imagenes/1_1_githubcom.png)

## 2. Completar el registro con tus datos
Rellena el formulario de registro ingresando tu correo electrónico y una contraseña segura.

![1_2_type_gmail_password](https://github.com/adiacla/diabetes/blob/main/imagenes/1_2_type_gmail_password.png)

## 3. Verificar tu correo con el código de confirmación
Recibirás un código de verificación en tu correo electrónico. Ingresa este código en la pantalla que se muestra y haz clic en continuar.

![1_6_codigo_gmail_github](https://github.com/adiacla/diabetes/blob/main/imagenes/1_6_codigo_gmail_github.png)

## 4. Iniciar sesión con tu nueva cuenta
Una vez creada la cuenta, inicia sesión ingresando tus credenciales.

![1_7_logearse](https://github.com/adiacla/diabetes/blob/main/imagenes/1_7_logearse.png)

## 5. Hacer un "Fork" del repositorio
Un "Fork" significa crear una copia del repositorio original en tu propia cuenta de GitHub. Para hacerlo:

- Visita el repositorio en https://github.com/adiacla/diabetes.
- Haz clic en el botón **Fork** que encontrarás en la parte superior derecha.

![5_1_2_fork_small](https://github.com/adiacla/diabetes/blob/main/imagenes/5_1_2_fork_small.png)

![5_1_github_fork](https://github.com/adiacla/diabetes/blob/main/imagenes/5_1_github_fork.png)

## 6. Confirmar la creación del "Fork"
En la siguiente pantalla, haz clic en el botón **Create Fork** para finalizar la copia del repositorio a tu cuenta.

![5_2_fork_confirm](https://github.com/adiacla/diabetes/blob/main/imagenes/5_2_fork_confirm.png)

## 7. Acceder a Streamlit
Ahora, dirígete a la página de Streamlit en el siguiente enlace: https://share.streamlit.io/signup?utm_source=streamlit&utm_medium=referral&utm_campaign=main&utm_content=-ss-streamlit-io-topright. 

- Haz clic en el botón **Continue to Sign In** para continuar.

![6_0_1streamlit_continue_signin](https://github.com/adiacla/diabetes/blob/main/imagenes/6_0_1streamlit_continue_signin.png)

## 8. Iniciar sesión con GitHub
En la pantalla de registro de Streamlit, selecciona la opción **Continue with GitHub** para vincular tu cuenta de GitHub.

![6_0_2_streamlit_continue_githubu](https://github.com/adiacla/diabetes/blob/main/imagenes/6_0_2_streamlit_continue_githubu.png)

## 9. Autorizar Streamlit en GitHub
Se te pedirá que permitas a Streamlit acceder a tu cuenta de GitHub. Haz clic en el botón **Authorize Streamlit** para otorgar los permisos necesarios.

![6_1authorize_streamlit_github](https://github.com/adiacla/diabetes/blob/main/imagenes/6_1authorize_streamlit_github.png)

## 10. Confirmar el código enviado a tu correo
Streamlit enviará otro código de verificación a tu correo electrónico. Ingresa este código en el campo correspondiente para continuar.

![6_2streamlit_gmail_code](https://github.com/adiacla/diabetes/blob/main/imagenes/6_2streamlit_gmail_code.png)

## 11. Verificar y confirmar tus datos personales
Revisa la información solicitada en la pantalla (como tu nombre y correo) y haz clic en continuar para avanzar.

![6_3_confirm_personal_data](https://github.com/adiacla/diabetes/blob/main/imagenes/6_3_confirm_personal_data.png)

## 12. Crear una nueva aplicación en Streamlit
Una vez dentro de Streamlit, haz clic en el botón **Create App** para empezar a configurar tu aplicación.

![6_4_click_create_app](https://github.com/adiacla/diabetes/blob/main/imagenes/6_4_click_create_app.png)

## 13. Seleccionar la opción de GitHub
En las opciones disponibles, elige la opcion **Deploy a public app from Github** para vincular tu repositorio.

![6_5_click_github](https://github.com/adiacla/diabetes/blob/main/imagenes/6_5_click_github.png)

## 14. Escoger el repositorio "diabetes"
En el campo "Repository", escribe "diabetes" y selecciona el repositorio de diabetes (O segun el nombre que tenga el repositorio).

![6_6_type_diabetes](https://github.com/adiacla/diabetes/blob/main/imagenes/6_6_type_diabetes.png)

## 15. Configurar el campo "Main File Path"
En el campo **Main File Path**, escribe `AppWeb/app.py` para indicar la ruta del archivo principal de la aplicación.

![6_7_main_file_path.png](https://github.com/adiacla/diabetes/blob/main/imagenes/6_7_main_file_path.png)

Luego, haz clic en **Advanced Settings** para acceder a más opciones.

## 16. Seleccionar la versión de Python
Dentro de **Advanced Settings**, cambia la versión de Python a 3.10 y guarda los cambios.

![6_8_choose_python3_10.png](https://github.com/adiacla/diabetes/blob/main/imagenes/6_8_choose_python3_10.png)

## 17. Personalizar el dominio de la aplicación
En el campo **App URL**, escribe el nombre que desees para el dominio de tu aplicación. 
Ten en cuenta:
- La URL finalizará en `streamlit.app`.
- Deberas usar una URL unica, por lo que "pruebadiabetesunab" no podra ser usada.

![6_9_cambiar_url.png](https://github.com/adiacla/diabetes/blob/main/imagenes/6_9_cambiar_url.png)

## 18. Publicar la aplicación
¡Ya estás listo para lanzar tu aplicación! Haz clic en el botón **Deploy** para publicarla.

Serás redirigido a la URL de tu aplicación en la nube, donde estará lista para usarse **desde cualquier navegador o celular**.

![6_10_app_lista.png.png](https://github.com/adiacla/diabetes/blob/main/imagenes/6_10_app_lista.png)

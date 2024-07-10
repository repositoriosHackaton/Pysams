# Pysams

En este espacio se sube el código creado para el grupo.

## Tabla de contenidos

1. [Nombre](#Nombre)
2. [Descripción](#Descripción)
3. [Arquitectura](#Arquitectura)
4. [Proceso](#Proceso)
5. [Funcionalidades](#Funcionalidades)
6. [Estado del proyecto](#Estado-del-proyecto)
7. [Agradecimientos](#Agradecimientos)

## Nombre

### CLARC, Clasificador de riesgos de ataque al corazón


## Descripción
Clarc es una aplicación web en la cual el usuario ingresa datos médicos y de estilo de vida, y nuestro modelo de IA le clasifica en si tiene, o no tiene riesgo de sufrir un ataque cardíaco.

### Arquitectura del proyecto

**Imagen de la arquitectura del proyecto**  
> Nota: **Poner imagen aquí**

## Proceso

Para desarrollar este proyecto, se llevaron a cabo los siguientes pasos:

1. **Investigación acerca de los factores que determinan un ataque cardíaco**  
   Se investigó en internet y se entrevistó a un cardiólogo para identificar los factores determinantes de un ataque cardíaco.

2. **Investigación del dataset**  
   Se buscó un conjunto de datos que abarcara tanto variables médicas como de estilo de vida del paciente para crear un modelo de IA holístico.  
   **Fuente del dataset:**  
   [Cardiovascular Disease dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset)

3. **Procesamiento de la data**  
   Nuestro dataset de 70,000 registros no tenía valores faltantes ni atípicos, por lo que se procedió a escalar la data.  
   ![Una tabla que se muestra en Google Colab con datos normalizados](imagenes/data_normalizada.jpg)

4. **Entrenamiento del modelo**  
   Se optó por usar el modelo Random Forest debido a su eficacia en tareas de clasificación.

5. **Evaluación de precisión**  
   El modelo obtuvo una precisión del 73.62% con 500 árboles de decisión y una profundidad de 10.
   Nota: poner imagen aquí

6. **Persistencia del modelo**  
   Se guardó el modelo entrenado para su posterior implementación en producción.

7. **Producción**  
   Se investigaron formas para integrar el modelo en un software funcional utilizando el framework de Streamlit para crear una app desde cero y hacer un sencillo despliegue con StreamCloud.

8. **Front-end**  
   Se creó un cuestionario adecuado a los datos necesarios para el modelo, iterando para mejorar la experiencia de usuario.  
   **Imagen de nuestra aplicación web (primera versión)**  
   > Nota: **Poner imagen aquí**

   **Manejo de casos en los cuales el usuario no envía ninguna data**  
   ![Imagen que muestra un mensaje solicitando al usuario que complete el formulario](imagenes/caso_de_no_data_de_usuario.jpg)

   **Manejo de casos en los que el usuario no conoce su presión arterial**  
   ![Imagen que muestra una advertencia donde se le dice al usuario que puede escribir "No sé", en caso de que no conozca su presión arterial](imagenes/caso_de_no_presión_arterial.jpg)

9. **Desarrollo del back-end**  
   Se desarrolló un back-end para procesar los datos del usuario y emitir la respuesta del modelo.

10. **Integración y despliegue**  
    Se integró el formulario con las funciones del back-end y se realizó el despliegue de la webapp. Clarc se encuentra disponible en el siguiente enlace: [Clarc en StreamCloud](https://clarc-jksohzf9zmy8tuacn.streamlit.app/)  
    ![Imagen que muestra una web con un formulario](imagenes/preview_de_la_webapp.jpg)

## Funcionalidades
11. **Funciones adicionales**  
    Se añadió la opción de que la IA generativa de Google proporcione hábitos sencillos de salud basados en los datos ingresados por el usuario, así como un conversor de unidades de libras a kilogramos y de pies a centímetros, por si el usuario lo necesita.  
    **Imagen que destaca la integración con la IA generativa de Google**  
    > Nota: **Poner imagen aquí**

    **Imagen que muestra el conversor de unidades**  
    ![Imagen que muestra un conversor de unidades, de libras a kg y de pies a centímetros](imagenes/conversor_de_unidades.jpg)

12. **Retoques**  
    Se personalizó más la interfaz al mostrar el nombre del proyecto "Clarc", se añadieron emojis y mensajes más específicos para que el usuario no se pierda en el sitio web.
    **Imagen que muestra mensajes que guían al usuario
    > Nota: **Poner imagen aquí**

## Estado del proyecto.

Actualmente el proyecto se encuentra funcionando perfectamente. Sin embargo, el grupo Pysams está trabajando en aumentar la precisión del modelo hasta un 85% para poder proporcionar mejores resultados, especificamente, el equipo está probando con deep learning con la arquitectura de redes neuronales llamada "encoder-decoder".

## Agradecimientos
El equipo Pysams agradece a los profesores/mentores Jenny Remolina y John Mario, así como a todo el personal que hace posible el programa Sangsung Innovation Campus. Finalmente, pero más importante aún, el grupo agradece a todos sus compañeros que son miembros del equipo por el empeño, responsabilidad y pasión por hacer esta idea realidad.
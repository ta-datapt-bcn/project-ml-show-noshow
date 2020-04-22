# Module 3 - Project 2 (ML) - Show | No Show.


1. [Descipción del proyecto](#g1)
2. [Análisis del problema](#g2)
3. [Workflow](#g3)
4. [Resultados](#g4)
5. [Conclusiones](#g5)
6. [Entregas](#g6)


## Descipción del proyecto <a name="g1"></a>

El objetivo de este proyecto es  practicar nuestras habilidades de análisis de datos y probar nuestro conocimiento sobre aprendizaje automático mediante el análisis de un gran conjunto de datos construyendo un modelo capaz de predecir el resultado de una *variable dependiente*.

Dada la naturaleza del conjunto de datos utilizado, este análisis tiene como objetivo describir algunas posibles razones para que el paciente no se presente en las citas programadas.

Los comandos suponen una comprensión básica de las bibliotecas Pandas, Matplotlib y scikit-learn.


## Análisis del problema <a name="g2"></a>
 
1. [Definición del problema](#id1)
2. [Definición del objetivo](#id2)
3. [Contextualización](#id3)
4. [Métricas](#id4)
5. [Aproximación a problemas similares](#id5)
6. [Asunciones previas](#id6)

### Definición del problema <a name="id1"></a>

Personas que reservan una visita con el doctor y no se presentan. Se nos plantea un problema de *clasificación binaria*. 

### Definición del objetivo <a name="id2"></a>

Producir un modelo capaz de predecir la probabilidad de que un paciente se presente a su cita médica:
* ¿Cuándo ocurre?
* ¿Se puede predecir?
* ¿Hay características comunes entre las personas que no se presentan? ¿Cuáles son?


### Contextualización <a name="id3"></a>

Aproximadamente un 20% de la población del dataset no acuden a la visita que han programado con el doctor.  Partiendo de los datos que tenemos crear una muestra para 'entrenamiento' y otra para 'test'. A partir de aqui medir la precisión de nuestro modelo en cuanto a predecir los pacientes que harán No-show.

### Métricas <a name="id4"></a>

110.527 citas médicas  y sus 14 variables asociadas. La variable a predecir es la relacionada con si acude o no a la visita médica.

* **Unnamed: 0** *(int)*: 
* **PatientId** *(float)*: identificación del paciente
* **AppointmentID** *(int)*: identificación de cada cita
* **Gender** *(object)*: masculino o femenino.
* **ScheduledDay** *(object)*: el día de la cita real, cuando tienen que visitar al médico.
* **AppointmentDay** *(object)*: el día que alguien llamó para solicitar la cita y/o fue registrada.
* **Age** *(int)*: años del paciente
* **Neighbourhood** *(object)*: donde se realiza la cita.
* **Scholarship** *(int)*: verdadero de falso. En la wiki del proyecto hay más inforamción relacionada con este campo
* **Hipertension** *(int)*. 1 o 0 según si son hipertensos o no.
* **Diabetes** *(int)*. 1 o 0 según si son diabéticos o no.
* **Alcoholism** *(object)*: según consumo de alcohol.
* **Handcap** *(int)* : Discapacidad.
* **SMS_received** *(int)*: 1 o más mensajes enviados al paciente.
* **No-show** *(object)*: Esta será nuestra variable a predecir. Puede adquirir valores de verdadero o falso.

La base de datos ha sido extraída de [aquí](https://www.kaggle.com/joniarroba/noshowappointments)

### Aproximación a problemas similares <a name="id5"></a>

Problemas similares pueden ser en testeo de calidad {Go, No-go}; clasifiación de películas {Sonido, Mudo}, {Color, B/N}

### Asunciones previas  <a name="id6"></a>

* Si un paciente recibe un SMS es más proble que sea "show" por que no se olvidará de la cita.
* Si un paciente sufre de Hipertensión o Diabetes es más proble que sea "show".
* Si un paciente tiene un Beca Familiar concedida es más proble que sea "show".
* Si un paciente tiene que ir acompañado a la cita es más proble que sea "show".
* El tiempo entre el día programación y el día de la cita, a menor tiempo más probable que sea "show".
* El género, el día programado, el día de la cita, la edad, el vecindario, el handicap, la beca y los SMS recibidos parecen ser las características más importantes a la hora de predecir el resultado de No_Show.

## Workflow <a name="g3"></a>

* **Semana 1:**
    * **Análisis del problema**. Definir el problema, marcar los objetivos y contextualizarlo. Un primer acercamiento a las métricas, a posibles problemas similares y las asunciones previas que podamos tener.
    * **Recuperación de datos**. 
    * **Análisis exploratorio**. Tamaño y tipo de los datos, estudio de cada variable (NaN, outliers, distribuciones), primeras visualizaciones para estudiar posibles correlaciones e identificar posibles transformaciones necesarias. Seleccionar el atributo objetivo.
    
* **Semana 2.**
    - **EDA**.
    - **Manipulación de los datos**.
    
* **Semana 3.**
    - **Selección del modelo**.
    
* **Semana 4.**
    - **Reajuste del modelo**.
    - **Presentación**

## Resultados <a name="g4"></a>

* *show_no_show.csv* - con todos los datos extraídos de Kaggle.
* *main.ipynb* - con todo el código construido para el proyecto.
* *figures* - todas las visualizaciones que respaldan el proyecto.

## Conclusiones <a name="g5"></a>



## Entregas <a name="g6"></a>

* *no_show_show.csv* - Conjunto de datos limpio que contiene toda la información del paciente, incluido si asistieron o no a sus citas médicas.
* Modelo ML capaz de predecir si habrá un Show-Up / No-Show basado en las características del paciente.

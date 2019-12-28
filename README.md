# Practica2
Limpieza y análisis de datos

## 0. INTRODUCCIÓN
Esta práctica se realiza con el juego de datos descargado de "Titanic: Machine Learning from Disaster" (https://www.kaggle.com/c/titanic), en concreto, se realiza la actividad solamente, usando los datos del archivo train.csv, además, nos proponemos el objetivo de limpiar y acondicionar los datos para generar un modelo algorítmico capaz de predecir qué pasajeros sobreviven y cuáles no. Por lo tanto, enfocamos todo el ejercicio práctico de limpieza y análisis para que en una otra actividad, se 

## 1. Descripción del dataset
Para realizar las tareas de limpieza y análisis de datos, la primera tarea es la "descripción del datase". En esta tarea, se carga el conjunto de datos y se visualizan las dimensiones y cantidades de datos respondiendo preguntas como: cuántas variables componen el conjunto de datos, cuántas observaciones o registros hay, se verifica si las variables son numéricas, categóricas, fechas o atributos ID. Y luego, para cada variable, se inspeciona la lógica o información que aporta y se describe un breve argumento sobre los datos que hay detras de cada variable. En este primer paso, se introducen los datos con los que se van a trabajar todas las tareas de limpieza y acondicionamiento y por lo tanto, desvela su importancia porqué a raiz de lo que se introduzca en este primer punto, se desarrollarán todas las otras tareas de limpieza y análisis de datos con una mayor orientación y organización. 

En nuestro caso, hemos cargado el conjunto de datos de TITANIC. Y obsevamos los siguientes aspectos sobre la descrpción de este dataset:
891 observaciones y 12 variables:

- "PassengerId": es el número identidicativo para cada pasajero del Titanic
- "Survived": Supervivencia 0 = No, 1 = Sí
- "Pclass": Ticket de clase 1 = 1 °, 2 = 2 °, 3 = 3 °
- "Name": Nombre del pasajero
- "Sex": hombre o mujer
- "Age": Edad en años
- "SibSp": hermanos / esposas a bordo del Titanic
- "Parch": padres / hijos a bordo del Titanic
- "Ticket": Número de boleto
- "Fare": tarifa Pasajero
- "Cabin": Número de cabina
- "Embarked": puerto de embarque

## 2. Integración y selección de los datos de interés a analizar
En nuestro caso, nos proponemos la limpieza y análisis de datos datos bajo el objetivo de predecir los pasajeros supervivientes del desastre del Titanic. Por esta razón, enfocamos esta segunda tarea con el objetivo de aplicar un algorítmo predictivo como lo es RANDOMFOREST. 
Como sabemos que el uso de RANDOMFOREST nos obliga a trabajar con variables numéricas, en este apartado debemos de seleccionar solamente, aquellas variables numéricas o potencialmente numéricas. En concreto, todas las 12 variables son numéricas excepto: "Name", "Sex", "Ticket", "Cabin" y "Embarked". Definitivamente, la variable del nombre, no nos aporta valor para el modelo predictivo y por lo tanto, la descartamos, pero todas las demás variables, si que es interesante tenerlas en consideración para generar el modelo predictivo y por lo tanto, seleccionamos todas las variables tanto numéricas como categóricas (luego se pueden convertir) y descartamos de la selección la variable "Name".

## 3. Limpieza de los datos
### 3.1 ¿Los datos contienen ceros o elementos vacíos? ¿Cómo gestionarías cada uno de estos casos?






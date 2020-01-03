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
Como sabemos que el uso de RANDOMFOREST nos obliga a trabajar con variables numéricas, en este apartado debemos de seleccionar solamente, aquellas variables numéricas o potencialmente numéricas. En concreto, "Name", "Sex", "Ticket", "Cabin" y "Embarked" son variables categóricas es decir, no nos aporta valor para el modelo predictivo y por lo tanto, las descartamos a excepción de la variable "Sex" que podría convertirse en una variable númerica cambiando los valores "male" por un "1" y "female" por un "2". Todas las demás variables, si que es interesante tenerlas en consideración para generar el modelo predictivo. De las 12 variables, seleccionamos 8:

- "PassengerId"
- "Survived"
- "Pclass"
- "Sex"
- "Age"
- "SibSp"
- "Parch"
- "Fare"


## 3. Limpieza de los datos

### 3.1 ¿Los datos contienen ceros o elementos vacíos? ¿Cómo gestionarías cada uno de estos casos?
Si, en este primer análisis descriptivo detectamos una variable con valores vacíos (NA´s). En concreto, se trata de la variable "Age" con un total de 177 observaciones vacías. 
Esto, comporta un problema ya que si el objetivo es limpiar los datos para que se pueda aplicar el algorítmo predictivo RANDOMFOREST, obligatoriamente necesitamos disponer de todos los campos completos, es decir, que no haya ningún elemento vacío.
Ante esta situación, procedemos a la eliminación de todos los registros con valores vacíos. De este modo, de las iniciales 891 observaciones, obtenemos un total de 714 observaciones

### 3.2. Identificación y tratamiento de valores extremos
En este apartado, seguimos el proceso de acondicionamiento de los datos convirtiendo aquellas variables categóricas en variables numéricas. En concreto, se trata de la variable "Sex", convirtiendo estas variable en numérica, nos permitirá aplicar correctamente el algorítmo predictivo, así como, detectar en el siguiente paso, posibles valores extremos. Lo realizamos mediante el reemplazo de los valores "male" por un "1" y "female" por un "2".
Para analizar la presencia de posibles valores extremos (outliers), realizamos un diagrama de caja (boxplot) para cada una de las variables. En este análisis, se detectan outlers en las variables: "Age", "SibSp", "Parch" y "Fare". Para que la aplicación del algoritmo predictivo sea más eficiente, se deben de eliminar los valores extremos y por lo tanto, acondicionamos estas variables, eliminando sus outlers mediante los boxplots.

## 4. Análisis de los datos

### 4.1 Selección de los grupos de datos que se quieren analizar/comparar
Una vez se han extraido los outlers, agrupamos todas las variables obtenidas en un mismo conjunto de datos del que posteriormente, trabajaremos como datos finales con los que aplicar el algoritmo predictivo y sus análisis previos. 



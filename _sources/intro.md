# UN MODELO HIBRIDO PARA PREDECIR EL RENDIMIENTO ACADEMICO DE LOS ESTUDIANTES DE SECUNDARIA DE DOS ESCUELAS EN PORTUGAL.


RESUMEN

Predecir el rendimiento académico de los estudiantes de secundaria de dos escuelas portuguesas es crucial para que
los profesores apliquen intervenciones didácticas. Los investigadores han prestado
mucha atención a cómo utilizar los registros de comportamiento de los estudiantes para
predecir las calificaciones escolares. Por lo que han existido muchos estudios en donde se han porpuesto varios metodos
de aprendizaje automatico para predecir el rendimiento de los estudiantes de secundaria atraves de registros de aprendizaje.  Sin embargo, uno de los mayores retos actuales es que muchos investigadores ignoran el problema de la
reducción de la precisión de los modelos de predicción debido al desequilibrio de los
datos. Al mismo tiempo, un único clasificador es susceptible a los cambios de datos y
tiene un rendimiento de clasificación inestable. Con este fin, este trabajo propone un enfonque hibrido haciendo pruebas de multiples modelos como Random Lasso Regression,Random Ridge Regression,Random Random Forest,Random Bagging Ensamble,Random XGBoost y Random Stacking Ensamble, haciendo los respectivos estudios para escoger el que mejor prediga el rendimiento academico de los estudiantes de secundaria de dos escuelas en portugal. 

Palabras clave: Predicción del rendimiento académico; aprendizaje automático; Random Lasso Regression;Random Ridge Regression;Random Random Forest;Random Bagging Ensamble;Random XGBoost y Random Stacking Ensamble.


INTRODUCCIÓN

Con el desarrollo de la información educativa, se ha creado un gran número de
datos de los estudiantes, que registran detalladamente su comportamiento y
rendimiento académico.Estos datos de los estudiantes contienen información
potencialmente valiosa, que se utiliza para el análisis del comportamiento de los estudiantes, la predicción de su rendimiento académico, la evaluación personalizada y otras investigaciones.La investigación muestra que el debate
estructurado en línea, la interacción entre profesores y estudiantes, la autoeficacia, los conocimientos previos y la motivación previa son cruciales para el éxito académico. Entre ellos, la predicción del rendimiento académico de los estudiantes ha cobrado especial importancia y ha atraído la atención de los educadores. Ayuda a los profesores a identificar eficazmente a los estudiantes con bajo rendimiento y a guiarlos para que adopten estrategias de estudio adecuadas para mejorar el rendimiento académico. En la actualidad, el aprendizaje
automático es un método de predicción eficaz.
El aprendizaje automatico se aplica ampliamente en diversos campos, como la
predicción médica, la predicción del riesgo bancario y la predicción del flujo de
tráfico, entre otros. El aprendizaje automático para la educación ha ganado
más atención por parte de los investigadores educativos. Los investigadores
suelen aplicar el aprendizaje automático para predecir el rendimiento académico de los
estudiantes basándose en los datos académicos de los estudiantes. Los estudios
han indicado que los modelos de aprendizaje automático pueden identificar con
antelación a los estudiantes con bajo rendimiento académico, ayudando a los
profesores a dar a los estudiantes una orientación adecuada.

En consecuencia este articulo propone un modelo de prediccion para abordar los problemas de investigacion mencionados.

TRABAJOS RELACIONADOS

Muchos modelos tradicionales de aprendizaje automático se han empleado
ampliamente en la construcción de clasificadores para predecir el rendimiento
académico de estudiantes de diferentes niveles. Sin embargo, la mayoría de los
trabajos de clasificación asumen que el espacio de datos es equilibrado y
suficiente.Aunque, de hecho, el problema de los datos desequilibrados existe en
muchas aplicaciones de clasificadores de predicción académica. Por lo tanto, es
necesario modificar los clasificadores tradicionales.38
Para aumentar la precisión de la predicción del rendimiento académico de los
estudiantes, muchos trabajos de investigación se han centrado en el campo de la
clasificación desequilibrada. Sun et al.39 propusieron un método conjunto
novedoso para tratar datos binarios desequilibrados. Zhang et al.40, teniendo en
cuenta las características de los datos desequilibrados, construyeron un conjunto
de datos de entrenamiento etiquetados con equilibrio de clases y aprendieron un
gráfico disperso. Aprovechan el muestreo de puntuación laplaciana y la
representación dispersa. Aunque estos trabajos se centran en el procesamiento de
datos desequilibrados, no tienen en cuenta la limitación de los datos. Los datos
limitados pueden influir en el rendimiento del clasificador de datos
desequilibrados. Para superar el problema de los datos desequilibrados de un
pequeño número de conjuntos de datos, Guarn et al.41 aplicaron técnicas sensibles a los costes a grandes conjuntos de datos. Mientras tanto, el algoritmo
MetaCost42 utilizaba una matriz de costes para especificar los costes relativos de
cada decisión del clasificador. Sin embargo, el conjunto de datos se recopila al
final del periodo académico, por lo que el tiempo de recopilación de datos es
relativamente tardío. Almutairi et al.43 aplicaron la tecnología SMOTE y la
tecnología de clasificación para predecir el rendimiento de todas las
características de los datos de Kalboard 360.

conjunto. Sin embargo, no se utilizaron otros datos de otra escuela para aumentar el
tamaño del conjunto de datos y verificar el modelo. SMOTE es uno de los
métodos populares para mejorar el rendimiento cuando un modelo clasifica datos
desequilibrados añadiendo un pequeño número de muestras generadas para cambiar
la distribución de datos del conjunto de datos desequilibrados. Algunos autores han
utilizado este método en nuestro c o n j u n t o d e datos, por lo que utilizamos la
tecnología SMOTE para tratar conjuntos de datos desequilibrados con el fin de
reducir el impacto del desequilibrio de datos en el rendimiento del modelo.

EXPLICACION SOBRE EL MODELO A UTILIZAR

Grid Ridge Regression



La "Grid Ridge Regression" es una técnica de regresión que se basa en la regresión lineal regularizada conocida como "Ridge Regression" o "Regresión Ridge". La regresión Ridge es una variante de la regresión lineal ordinaria que se utiliza para abordar el problema de la multicolinealidad en los datos y para prevenir la sobreajuste del modelo.

A continuación, se explican los conceptos clave de la Ridge Regression y cómo funciona:

1.Regresión Lineal Ordinaria: En la regresión lineal ordinaria, se busca encontrar los coeficientes (ponderaciones) que mejor ajusten una relación lineal entre las variables predictoras (características) y la variable objetivo (la variable que se está tratando de predecir). El objetivo es minimizar la suma de los errores cuadráticos entre las predicciones del modelo y los valores reales.


2.Multicolinealidad: La multicolinealidad es un problema que ocurre cuando dos o más variables predictoras están altamente correlacionadas entre sí. Esto puede causar inestabilidad en los coeficientes estimados y dificultar la interpretación del modelo.


3.Regresión Ridge: La Regresión Ridge aborda la multicolinealidad al agregar un término de penalización a la función de costo utilizada en la regresión lineal. Este término de penalización, llamado término de regularización L2, penaliza los coeficientes grandes y ayuda a reducir su magnitud. Como resultado, la Regresión Ridge tiende a dar como resultado coeficientes más pequeños y más estables, lo que es útil cuando se tienen variables altamente correlacionadas.


4.Parámetro de Regularización: La Regresión Ridge introduce un parámetro de regularización (lambda o alpha) que controla la cantidad de penalización aplicada a los coeficientes. Un valor más alto de lambda conduce a una mayor penalización y coeficientes más pequeños, lo que puede reducir el riesgo de sobreajuste.


5.Grid Ridge Regression: La "Grid Ridge Regression" es una variante de la Regresión Ridge en la que se realiza una búsqueda en una "rejilla" de valores de lambda para encontrar el mejor valor de regularización. Se prueban varios valores de lambda y se elige el que produce el mejor rendimiento del modelo en función de una métrica de evaluación (como el error cuadrático medio, R cuadrado, etc.).


En resumen, la "Grid Ridge Regression" es un enfoque que utiliza la Regresión Ridge con una búsqueda sistemática de valores de regularización para encontrar el mejor modelo de regresión con el equilibrio adecuado entre ajuste y estabilidad en presencia de multicolinealidad. Este método es útil en la modelización de datos cuando se sospecha o se sabe que las variables predictoras están altamente correlacionadas.


CONJUNTO DE DATOS

Inicialmente la base de datos cuenta con 395 observaciones contenidas en 33 variables de las cuales 16 son de tipo caracter y 17 son numericas, de las 16 variables de tipo caracter se logra identificar que la mayoria de ellas son variables binarias o discretas por lo que se pueden convertir a variables numericas y por tanto pueden ser incluidas en el estudio. 


En este trabajo analizaremos datos reales de dos escuelas de secundaria en portugal como las calificaciones, el numero de ausencias, datos demograficos, entre otros. El objetivo es predecir el rendimiento academico del estudiante e identificar las variables claves que afectan el exito academico.






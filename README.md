# Rusty_Bargain_MLgbm

En este proyecto se crea un modelo para calcular el valor de mercado de un carro usado, de acuerdo con las características compartidas con los vehículos de la base de datos disponible.

Este proyecto requiere atención en tres puntos principales:

- la calidad de la predicción;
- la velocidad de la predicción;
- el tiempo requerido para el entrenamiento

Para cumplir con todos los requisitos, se implementan tecnicas de optimización de gradiente(lightgbm y catboost), estos modelos son mucho más rápidos en su ejecución. Y para medir la velocidad de predicción se trabaja con la libreria 'time'.

Lo primero, como buena practica siempre en los proyectos, es el EDA y el preprocesamiento de los datos. Despues se crean 4 modelos, para el de regresión y el bosque, se aplican tecnicas de codificación para caracteristicas categoricas y escalamiento para los datos numericos. Este preprocesamiento no es necesario para los modelos de gradiente.

Conclusión:
Los diferentes modeos tuvieron sus particularidades. La regresión lineal tuvo el mayor error y la mayor variación pero era el modelo base para comparar los demás. Tanto la regresión lineal como el bosque se tuvieron que procesar para poder implementarse, y el bosque tuvo una mejor puntuación/menor error que la potenciación con LightGBM; Aunque fue el modelo que más tardo y por mucho, en entrenarse y predecir. El modelo más rápido, tuvimos el de LightGBM, pero el menor error de todos fue CatBoost, por lo que es el modelo a elegir en este caso, ya que aun que es un poco más lento que LightGBM, La diferencia en tiempo no es tanta y el error es bastante más bajo.

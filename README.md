# Maximizar Beneficios y Reduccion de Riesgos

<!-- How to make a decision to obtain best benefits and lower risk in a Oil company-->

## Objetivo

Para la compañía petrolera GiantOil se necesita lograr una selección de una región óptima en la cual se deberán operar los pozos petroleros y con ello obtener el mejor margen de beneficios y la mayor reducción de riesgos potenciales.


## Estructura del Proyecto

El repositorio está organizado de la siguiente manera:

- **/datasets**: Contiene los datos brutos (`raw`) y los datos listos para ser procesados para la creacion del modelo(`pre-processed`).
- **/files/documentation**: Almacena la estructura/modelo de datos y notebooks de Jupyter para análisis exploratorio.
- **/files/outputs**: Guarda los resultados del proyecto, como el modelo entrenado (`models`), imagenes (`images`)
- **/src**: Contiene el código fuente modularizado en scripts de Python.
- **`requirements.txt`**: Lista de dependencias del proyecto.
- En la raiz del proyecto se encuentran los archivos principales para la ejecución y prueba del mismo.

## Preparando el ambiente virtual
Por favor considerar el ejecutar las siguientes instrucciones para manejar el workspace dentro de un ambiente virtual:

```
python3 -m venv .venv
source .venv/bin/activate
user$ pip install --upgrade pip
user$ python -m pip install -r requirements.txt
```

## Como ejecutar el proyecto

Se puede controlar las secciones del proceso a ejecutar por medio de variables dentro del modulo **params** en la raiz del proyecto segun se requiera. 

- preprocess_required = True/False
- training_required = True/False

Para la ejecucion del pipeline, es suficiente con la siguiente linea en raiz del proyecto:

```
python project_pipeline.py 

```
## Resultados durante el proyecto

En relacion al entrenamiento de un modelo de datos utilizando un modelo simple de regresion lineal, se generaron los siguientes indicadores:

* Region 0
- RMSE: 37.58 y R2: 0.28

* Region 1
- RMSE: 00.89 y R2: 1.00

* Region 2
- RMSE: 39.96 y R2: 0.20

Para todas, son mejores resultados que la media como prueba de cordura.

De lo anterior resulta tener mejor desempeño para los datos de la region 0.

Los resultados y los datos asociados a la region 1 resultan ser muy dudosos dado el coeficiente de determinacion = 1 obtenido.

El producto promedio de cada Region así como el beneficio calculado para los mejores 200 pozos:

* Producto
R0 = 92.50, R1 = 68.825, R3 = 95.00

* Beneficio para cada region:
R0 = 66350365.68, 
R1 = 24150866.97, 
R2 = 70596329.28

En un principio dado el beneficio generado por las regiones, se podría pensar que la Region 2 debería considerarse para elegir los 200 pozos, sin embargo dado pruebas utilizando la tecnica de bootstrapping dejó ver que el margen de ganancias crece sobre la region 1 donde se puede asumir que el modelo con mejores resultados actua.

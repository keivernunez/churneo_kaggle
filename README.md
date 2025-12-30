
#  Submit final - Competencia Kaggle Gerencial

Esta es la competencia Gerencial de la materia Laboratorio de Implementacion I, edición 2025, Virtual, de la Maestría en Ciencia de Datos, Universidad Austral.
Competencia

### Objetivo ###

El objetivo es predecir que clientes de Paquete Premium de la foto al 30-septiembre-2021 se darán de baja durante noviembre-2021, es decir predecir las BAJA+2 de la foto de 202109

### Objetivos Pedagógicos ###
Conocer los hiperparámetros de un LightGBM y aprender a optimizarlos

Feature Engineering de datos históricos

Entender los conceptos de Data Drifting y Concept Drifting

Aprender a reducir la varianza de los modelos

Manejo de grandes volúmenes de datos en ambiente Cloud

---

###  Características Principales
-  La notebook sube 11 submits a kaggle 
-  Escribe varios archivos en la carpeta del experimento: PARAM.yml, prediccion.txt, modelo.txt, impo.txt, BO_log.txt, modelo.model
-  Dentro del archivo BO_log.txt se encuentran los outputs de la optimización bayesiana realizada.
-  Los hiperparámetros fijos usados para entrenar el modelo fueron:
-     bjective= "binary",
      metric= "auc",
      first_metric_only= TRUE,
      boost_from_average= TRUE,
      feature_pre_filter= FALSE,
      verbosity= -100,
      force_row_wise= TRUE, 
      seed= PARAM$semilla_primigenia,
      max_bin= 31,
      learning_rate= 0.02
      num_iterations= 2048,  
      early_stopping_rounds= 300
  
---

###  Tecnologías Usadas
- Python 3 / R
- LightGBM
- data.table
- mlrMBO
- DiceKriging
- JupyterLab
- Google Cloud

### Evaluation ###

Leaderboard publico y privado
El leaderboard publico contiene aproximadamente el 30% de los registros, y el privado el otro 70% .
La evaluación de la competencia se hace sobre el leaderboard privado, que solo será visible una vez finalizada la competencia (link: https://www.kaggle.com/competitions/labo-i-2025-virtual-gerencial/leaderboard )

Se debe tener cuidado con no hacer overfitting en el leaderboard público.

### Funcion Ganancia ### 
La ganancia esta definida como

ganancia = 117000* "BAJA+2" - 3000*( "BAJA+1" + "CONTINUA" )

### Dataset ###

Los 31 periodos [201901, 202107] tienen la clase completa
El período 202108 solo tiene los BAJA+1
El período 202109 posee campo clase_ternaria completamente vacío, es justamente lo que se debe predecir.

### Ganancia en el leaderboard ### 
La ganancia en el leaderboard está expresada en MILLONES de pesos argentinos.


### Repo en Github ###
En este repositorio encontrará la notebook de google colab que se empleó para el submit final en kaggle. Además encontrará los archivos necesarios que debe cargar a la carpeta datasets de su google drive o jupyterlab antes de ejecutar la notebook de forma exitosa. 

Los archivos son: 

-submit_final_KeiverNunez.ipynb

-gerencial_competencia_2025v_csv.xlsx.

-Indice-FACPCE.xlsx (contiene el coeficiente de ajuste a aplicar en la sección de Data Drifting de la notebook).

Si ejecuta la notebook desde Google Colab recuerde ejecutar la sección 1.1 del código para montar Drive.
Si en cambio ejecuta la notebook desde JupyterLab puede omitir esta primera sección y avanzar a la sección 1.2.

Adicionalmente, se sumó la sección 1.3.2 para ejecutar un sencillo EDA para explorar el dataset. El output de esta sección del código es un archivo html que se guarda en la carpeta del experimento y se puede abrir con cualquier navegador web.

El submit final es el que corresponde al submit KA1012_800.csv subido por mi usuairo keivernuez. Fue subido desde la VM de Google Cloud.

---

## 👤 Autor
**Keiver Nuñez**  

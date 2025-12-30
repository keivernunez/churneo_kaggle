
# 📌 Submit final - Competencia Kaggle Gerencial

En esta carpeta encontrará la notebook de google colab que se empleó para el submit final en kaggle. Además encontrará los archivos necesarios que debe cargar a la carpeta datasets de su google drive o jupyterlab antes de ejecutar la notebook de forma exitosa. 

Los archivos son: 

-submit_final_KeiverNunez.ipynb

-gerencial_competencia_2025v_csv.xlsx.

-Indice-FACPCE.xlsx (contiene el coeficiente de ajuste a aplicar en la sección de Data Drifting de la notebook).

Si ejecuta la notebook desde Google Colab recuerde ejecutar la sección 1.1 del código para montar Drive.
Si en cambio ejecuta la notebook desde JupyterLab puede omitir esta primera sección y avanzar a la sección 1.2.

Adicionalmente, se sumó la sección 1.3.2 para ejecutar un sencillo EDA para explorar el dataset. El output de esta sección del código es un archivo html que se guarda en la carpeta del experimento y se puede abrir con cualquier navegador web.

El submit final es el que corresponde al submit KA1012_800.csv subido por mi usuairo keivernuez. Fue subido desde la VM de Google Cloud, por eso encontrará dos submits en el leaderboard con mi nombre, unos desde Colab y otros desde la VM. 

---

## 🚀 Características Principales
- ✔ La notebook sube 11 submits a kaggle 
- ✔ Escribe varios archivos en la carpeta del experimento: PARAM.yml, prediccion.txt, modelo.txt, impo.txt, BO_log.txt, modelo.model
- ✔ Dentro del archivo BO_log.txt se encuentran los outputs de la optimización bayesiana realizada.
- ✔ Los hiperparámetros fijos usados para entrenar el modelo fueron:
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

## 🧠 Tecnologías Usadas
- Python 3 / R
- LightGBM
- data.table
- mlrMBO
- DiceKriging
- JupyterLab
- Google Cloud

---

## 👤 Autor
**Keiver Nuñez**  

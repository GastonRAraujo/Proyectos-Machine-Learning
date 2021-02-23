# Proyecto Final

En este proyecto se implementaran diferentes técnicas para procesar texto, para luego ser clasificado. Las técnicas utilizadas incluyen Stemming, Lematización, diversos tipos de vectorización, etc.

## Dataset
Se ha utilizado el dataset ["The Hewlett Foundation: Automated Essay Scoring"](https://www.kaggle.com/c/asap-aes). Cuenta con 12948 ensayos de entrenamiento y 4211 de validación.

## Descarga
Para realizar la descarga se debe utilizar la API de Kaggle. Para eso se implementó [DownloadData_wAPI](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/Proyecto_Final/DownloadData_wAPI.ipynb) el cual monta la carpeta de Drive que contiene el archivo ".json" o Token
para luego utilizar la sentecia que nos provee Kaggle para realizar la descarga. Una vez completada, se descomprimen los archivos necesarios y se unifican los archivos que poseen los datos de validación. Por último los archivos son copiados a una carpeta perteneciente a Google Drive, y subibos a GitHub.

## Procesamiento de texto
Para procesar el texto y poder usarlo como input de nuestro modelo debemos realizar los siguientes pasos:

* Tokenizar el texto: convertir el texto en lista de palabras
* Cambiar mayúsculas por minúsculas
* Remover stop words (palabras que no aportan información: the, is, at, which, on, for, this, etc.) y signos de punctuación
* Stemming: método para reducir una palabra a su raíz
* Lematización: proceso lingüístico que consiste en, dada una forma flexionada (es decir, en plural, en femenino, conjugada, etc), hallar el lema correspondiente. Por ejemplo decir es el lema de dije
* Vectorización: convertir nuestro texto tokenizado y procesado en vectores

## Clasificación
Se implementaron 4 variantes que utilizan los modelos: MultinomialNB,	KNeighbors,	LogisticRegression,	SVC,	RF, XGB y	red LSTM. Se utilizaron dos métodos para vectorizar el texto: "CountVectorizer" y "TfidfVectorizer". La diferencia principal entre ambos es que el primero utiliza una codificacion con números enteros (por conteo), mientras que el segundo utiliza decimales (por puntajes). 
A su vez implementó dos variantes para la validación: utilizar como datos de validación los provistos originalmente y por otro lado utilizar una pequeña fracción de los datos de entrenamiento.

### CountVectorizer 
En los siguientes archivos se implementó el vectorizador CountVectorizer:
[CV_1df](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/Proyecto_Final/CV_1df.ipynb) utilizando como datos de validación una fracción del dataset de entrenamiento.
[CV_2df](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/Proyecto_Final/CV_2df.ipynb) utilizando como datos de validación los provisto originalmente.

### TfidfVectorizer
En los siguientes archivos se implementó el vectorizador TfidfVectorizer:
[CV_1df]() utilizando como datos de validación una fracción del dataset de entrenamiento.
[CV_2df](https://github.com/GastonRAraujo/Materia-Ap_Maq/blob/master/Proyecto_Final/CV_2df.ipynb) utilizando como datos de validación los provisto originalmente.

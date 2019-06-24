# Proyecto Integrador sobre Procesamiento de Texto

### Equipo de trabajo
Los integrantes del equipo son:
-  Camila Mejía Quintero
-  Sara Mira Puerta
-  Juan David Jurado Tapias
-  Alirio Rodriguez Mesías

# 1. Primera Entrega
## 1.1 Descripción
En este repositorio se encuentra disponibles los archivos con el código y la respectiva documentación que corresponde al Proyecto Integrador de la Maestría en Analítica y Ciencia de Datos de la cohorte 2019-1 en la  Universidad EAFIT.

## 1.2 Descripción del Problema
A partir de un conjunto muy grande (Big data) de documentos tipo texto (Para este proyecto se cuenta con 980 archivos, habiendo quitando un documento escrito en aleman) y los metadatos sobre dichos documentos, realizar un sistema/aplicación para la ingesta, almacenamiento, indexación, búsqueda, recuperación, navegación y visualización de documentos. 

## 1.3 Descripción de la Solución
Para implementar la solución se establecieron dos fases:

### 1.3.1 Fase 1: Pre-procesamiento
El objetivo es eliminar de cada archivo de texto la mayor cantidad de información que no agrega valor, depurando los datos que se preservan para la siguiente fase. La sección contiene los siguientes archivos ordenados:

*Directorio dataset*
Se encuentran los 980 archivos en formato txt que se obtienen después de realizar la fase de pre-procesamiento.

*Archivo en formato Jupyter Notebook: preprocessing_data.ipynb*
Contiene:
1. Importación de las librerías necesarias: numpy, re, os y collections. 
2. Llamado de los datos input (datasetIn) y se genera una carpeta de outputs "salida" para guardar los datos de texto de menor dimensión (datasetout).
3. Eliminación de la información innecesaria, para lo que se definiero las siguientes reglas:
     a. Eliminar URL o email.<br>
     b. Eliminar cualquier contenido entre paréntesis o corchetes<br>
     c. Eliminar abreviaciones("et al.", "i.i.e.","i.e"), apóstrofes y guiónes<br>
     d  Eliminar los caracteres que NO sean letras o vocales acentuadas<br>
     e. Eliminar palabras o números de un caracter de longitud 1<br>
     
4. Reconstrucción de los datos en formato .txt para su posterior tratamiento en procesamiento. 
5. Guardado de los nuevos datos en la carpeta de salida.
6. Reducción de la información se puede verificar en el archivo .xls generado. 

*Archivo:CleanSummary.csv*<br>
Para cada archivo de texto, se  estableció:
  a. Tamaño del archivo en KB
  b. El número de palabras al momento de iniciar el proceso, con el respectivo calculo de las palabras del vocabulario inicial
  c. Número de palabras depuradas o eliminadas.
  d. Volcabulario obtenido como resultado de la limpieza.
  Con estos datos se pudo calcular un indicador del porcentaje de limpieza de la fase de preprocesamiento, que en promedio es del 19%.
  
### 1.3.2 Fase 2: Procesamiento
El objetivo es eliminar de cada archivo de texto la mayor cantidad de información que no agrega valor, depurando los datos que se preservan para la siguiente fase.   Para esto se implementaron las siguientes reglas de limpieza:
*Archivo: processing_data.ipynb*
1. Carga de las librerías necesarias para el procesamiento de datos: ntkl, pandas, sklearn, CountVectorizer , pickle. 
2. Formación de las reglas para aplicar la tokenización y eliminación de stopwords, entre otros elementos identificados. 
3. Formación de las reglas para aplicar las tecnicas de stemming y lemmatización. 
4. Lectura de los datos .txt guardados en la carpeta de salida, generada en el pre.procesamiento, se seleccionan los archivos en inglés (existe un documento en alemán). 
5. Implementación de las técnicas de tokenización, stemming y lemmatización a los artículos en inglés, 
6. Construcción del vocabulario.
7. Construcción de la bolsa de palabras (Bag of Words - BoW).

# 2. Segunda Entrega
## 2.1 Descripción de la Solución
Dado que la entrega anterior se quedo con el reto de reducir el BoW, se implementaron algunos ajustes a la fase de pre-procesamiento

### 2.1 Fase 1: Pre-procesamiento
*Archivo: simple_conversion_pdf_tika.py*<br>
Para evitar la presencia de caracteres en blanco en medio de palabras, se realizó una conversión de los artículos en formato PDF a formato txt utilizando una libería "Tika (https://tika.apache.org/)", logrando una evitar la pérdida de información.

*Archivo: cleaning_txt.py* <br>
Con los archivos en formato TXT (resultado de la conversión con Tika) se aplica las siguientes reglas:
     a. Eliminar el texto de las referencias bibliográficas, dado que no agrega información en la construcción del BoW.
     b. Eliminar URL o email.<br>
     c. Eliminar cualquier contenido entre paréntesis o corchetes<br>
     d. Eliminar abreviaciones("et al.", "i.i.e.","i.e"), apóstrofes y guiónes<br>
     f  Convertir los caracteres de vocales acentuadas a covales sin acento<br>
     e.  Eliminar los guiones que se utilizan para dividir palabras (eliminando el guión) o para componer (dos palabras unidas por guión y se cambia por un espacio en blanco) conceptos
     g. Eliminar palabras que tengan una longitud de caracteres menor a 3 o mayor a 26<br>

*Archivo: BD_words_to_remove.csv*
Contiene un archivo con

*Archivo: CleanSummary.csv*<br>
Para cada archivo de texto, se  estableció:
  a. Tamaño del archivo en KB
  b. El número de palabras al momento de iniciar el proceso, con el respectivo calculo de las palabras del vocabulario inicial
  c. Número de palabras depuradas o eliminadas.
  d. Volcabulario obtenido como resultado de la limpieza.
  Con estos datos se pudo calcular un indicador del porcentaje de limpieza de la fase de preprocesamiento, que en promedio es del 42%.
  
  
  # 3. Tercera Entrega
  

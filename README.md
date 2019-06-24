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

Para cada archivo de texto, se  estableció el número de palabras antes y después del pre-procesamiento, y se estableció el porcentaje de depuración de palabras, lo que permitió generar un indicador del porcentaje de limpieza de la fase de preprocesamiento, que en promedio es del 19%.

### 1.3.2 Fase 2: Procesamiento
El objetivo es eliminar de cada archivo de texto la mayor cantidad de información que no agrega valor, depurando los datos que se preservan para la siguiente fase.   Para esto se implementaron las siguientes reglas de limpieza:
*Archivo: processing_data.ipynb*
1. Carga de las librerías necesarias para el procesamiento de datos: ntkl, pandas, sklearn, CountVectorizer , pickle. 
2. Formación de las reglas para aplicar la tokenización y eliminación de stopwords, entre otros elementos identificados. 
3. Formación de las reglas para aplicar las tecnicas de stemming y lemmatización. 
4. Lectura de los datos .txt guardados en la carpeta de salida, generada en el pre.procesamiento, se seleccionan los archivos en inglés (existe un documento en alemán). 
5. Implementación de las técnicas de tokenización, stemming y lemmatización a los artículos en inglés, 
6. Construcción del vocabulario.
7. Construcción de Bag of Words.

# 2. Segunda Entrega
## 2.1 Descripción de la Solución
Dado que la entrega anterior se quedo con el reto de reducir el Bag of Word, se implementaron algunos ajustes a la fase de pre-procesamiento

### 2.1 Fase 1: Pre-procesamiento
*Archivo: simple_conversion_pdf_tika.py*
Para evitar la presencia de palabras con caracteres en blanco que las dividen, se realizó una conversión de los artículos en formato PDF a formato txt  utilizando una libería "Tika <a href="https://tika.apache.org/"_blank"></a>" 


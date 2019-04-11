# Proyecto Integrador sobre Procesamiento de Texto

## Introducción
En este repositorio se encuentra disponibles  los archivos con el código y la respectiva documentación que corresponde al Proyecto Integrador de la Maestría en Analítica y Ciencia de Datos de la cohorte 2019-1 en la  Universidad EAFIT.

## Equipo de trabajo
Los integrantes del equipo son:
-  Camila Mejía
-  Sara Mira
-  Juan Jurado
-  Alirio Rodriguez

## Estructura de Directorios
- En la subcarpeta papers-txt del directorio datasets se encuentran los 981 archivos en formato txt que se deben procesar.
- En la subcarpeta salida del directorio datasets se encuentran los 981 archivos en formato txt que se obtienen después de realizar la fase de pre-procesamiento.
- En el directorio raíz están los archivos en formato Jupyter Notebook con las diferentes rutinas para hacer las siguientes operaciones:
  * Archivo preprocessing_data.ipynb, tiene las rutinas del <b>Pre-procesamiento</b> de los archivos de texto, se realizan las siguientes acciones: <br>
    a. Eliminar URL o email.<br>
    b. Eliminar cualquier contenido entre paréntesis o corchetes<br>
    c. Eliminar abreviaciones("et al.", "i.i.e.","i.e"), apóstrofes y guiónes<br>
    d Eliminar los caracteres que NO sean letras o vocales acentuadas<br>
    e. Eliminar palabras o números de un caracter de longitud 1<br>
  Como resultado de este procesamiento se logra en promedio (para los 981 archivos) eliminar aproximadamente el 19% de las palabras en los archivos iniciales.
  * Archivo CleaningData_camila.ipynb, tiene las rutinas del <b>Procesamiento</b> de los archivos de texto, se realizan las siguientes acciones:

# Proyecto Integrador sobre Procesamiento de Texto

### Equipo de trabajo
Los integrantes del equipo son:
-  Camila Mejía Quintero
-  Sara Mira Puerta
-  Juan David Jurado Tapias
-  Alirio Rodriguez Mesías

## I. Descripción
### Introducción
En este repositorio se encuentra disponibles los archivos con el código y la respectiva documentación que corresponde al Proyecto Integrador de la Maestría en Analítica y Ciencia de Datos de la cohorte 2019-1 en la  Universidad EAFIT.

### Descripción del Problema
A partir de un conjunto muy grande (Big data) de documentos tipo texto (Para este proyecto se cuenta con 981 archivos) y los metadatos sobre dichos documentos, realizar un sistema/aplicación para la ingesta, almacenamiento, indexación, búsqueda, recuperación, navegación y visualización de documentos. 

### Descripción de la Solución
Para el primer seguimiento se cubrirá las siguientes fases:
 * Pre-procesamiento: Limpieza de los archivos y generación de métricas.
 * Procesamiento:   <b> Falta completar por parte de Camila </b>
 * Almacenamiento:  <b> Falta completar por parte de Camila </b>


## II. Arquitectura del Código

<b> Falta completar por parte de Sara</b>

## III. Guía de Uso
#### Estructura de Directorios
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
  * Archivo processing_data.ipynb, tiene las rutinas del <b>Procesamiento</b> de los archivos de texto, se realizan las siguientes acciones:
    a. <b> Falta completar por parte de Camila </b><br>
    b. <b> Falta completar por parte de Camila </b><br>
    c. <b> Falta completar por parte de Camila </b><br>
    d. <b> Falta completar por parte de Camila </b><br>
    e. Eliminar palabras o números de un caracter de longitud 1<br>

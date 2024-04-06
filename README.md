# ANALISIS Y GESTIÓN DE LA DATA DE CANCER DE UN ESTUDIO PARA PREVENCIÓN DE CANCER

- Roxana Reina Sanchez.
- Melannie Upegui Vasquez.

## Tabla de Contenidos
- [Descripción de la problematica](#DESCRIPCION)
- [Objetivos](#OBJETIVOS)
- [Contenido del repositorio](#REPOSITORIO)
- [Tecnologias Utilizadas](#TECNOLOGIAS)
  - [Python](#Python)
  - [Jupyter Notebook](#Jupyter)
  - [MySQL](#MySql)
  - [Excel](#Excel)
  - [MySQL Workbench](#MySQL_)
- [Detallez sobre la Cantidad y Naturaleza de los Datos](#Detallez)
  - [Limpieza de datos](#Limpieza)
  - [Manipulación](#Manipulación)
  - [Análisis y Visualización](#Análisis)
- [Conclusiones y valor generado](#Conclusiones)


# DESCRIPCIÓN DE LA PROBLEMATICA
En Colombia, el Instituto Nacional de Cancerología enfatiza la prevención y la detección precoz como estrategias clave para mejorar la calidad de vida de los pacientes y reducir los costos asociados al tratamiento en etapas avanzadas de la enfermedad​ (Cancer.gov)​. 

El proyecto se enfoca en la detección temprana del cáncer en Colombia, un país donde la mayoría de los diagnósticos se hacen en etapas avanzadas, incrementando los costos para las  EPS (Entidades Promotoras de Salud) y el Estado, y reduciendo las probabilidades de un tratamiento exitoso. 

Incorporando análisis de datos, nuestro objetivo es identificar perfiles de riesgo y determinar las edades óptimas para la detección del cáncer. Esto no solo puede disminuir significativamente los costos asociados con tratamientos en etapas avanzadas, sino también mejorar sustancialmente la calidad de vida de los pacientes. Este enfoque se alinea con las estrategias de salud pública que priorizan la prevención y detección precoz como medios eficaces para combatir el cáncer, reflejando la importancia de este trabajo en el contexto colombiano y su potencial para cambiar paradigmas en el manejo de la salud ya que el uso de estas herramientas no solo tiene el potencial de salvar vidas, sino también de modelar prácticas de salud preventiva que pueden ser replicadas en otras regiones con desafíos similares.

 Origen de la data [WebSite](https://www.cancer.gov.co/centro-investigacion/lineas-investigacion/control-del-riesgo-deteccion-precoz-del)

 # OBJETIVOS
- Identificar perfiles de riesgo para el cáncer en la población colombiana
- Determinar las edades óptimas para realizar pruebas de detección temprana.

# CONTENIDO DEL REPOSITORIO
Esta seccion incluye una explicacion de cada uno de los archivos que se encunetran en este repositorio:

- `Limpieza_de_datos.ipynb`: Describe el proceso de limpieza de datos inicial, removiendo datos innecesarios y ajustando el conjunto de datos para eliminar cualquier inconsistencia que pudiera afectar el análisis. Este proceso fue crucial para asegurar la calidad y precisión del análisis posterior.
- `Manipulación_de_datos.ipynb`: Notebook que detalla el proceso de manipulación de datos realizado para preparar el conjunto de datos para un analisis enfocado a bases de datos. Incluye la transformación de el dataframe de pandas a una base de datos llamada ProyectoGestion en la tabla DatosClinicos, y la adecuación de los tipos de datos, ademas de las funciones del CRUD desde python para manipular los datos, y algunas graficas que muestran los reflejos de dichos cambios realizados en el crud.
- `Notebooks de Jupyter`: Contienen el código de análisis de datos, incluyendo limpieza de datos, exploración, visualización, y análisis estadístico. Los notebooks están detalladamente documentados para facilitar la comprensión del proceso.
- `DataLimpia.cvs`: Conjunto de datos resultado de la limpieza de los datos en el proyecto, que se utilizara como material inicial para el funcionamiento del archivo jupiter de Manipulacion de datos.
- `DatosClinicos2020.xlsx`: Conjunto de datos utilizado en el proyecto. Los datos específicos utilizados en este proyecto son sensibles / privados, por lo que aquí se incluye un subconjunto o datos de muestra del estudio total, obtenido de [WebSite](https://www.cancer.gov.co/centro-investigacion/lineas-investigacion/control-del-riesgo-deteccion-precoz-del).
- `README`: Este archivo, que es el guia que proporcionando una visión general del proyecto.

# TECNOLOGIAS UTILIZADAS

## Python
Es fundamental para la ejecucion de este condigo que se encuentre instalado pyhon, para instalarlo se pueden seguir las indicaciones del siguiente [tutorial](https://www.youtube.com/watch?v=i6j8jT_OdEU). En este caso el desarrollo se baso en python 12.1. Se uso para el análisis de datos, utilizando diversas librerias que deben de ser instaladas en el entorno previo a la ejecucion del codigo. A continuacion todas las instalaciones de las librerias correspondientes desde el archivo jupiter:
```bash
%pip install mysql-connector-python
%pip install matplotlib
%pip install numpy
%pip install pandas
%pip install seaborn
```
Si se desea ejecutar directamente desde la terminal seria de la siguiente manera:
```bash
> pip install mysql-connector-python
> pip install matplotlib
> pip install numpy
> pip install pandas
> pip install seaborn
```
Adicional a ello se recomienda tener habilitadas las extensiones correspondientes a python en Visual Studio Code

## Jupyter Notebook
Se utilizo para la documentacion iterativa del analisis. Se recomienda tener instalada y habilitada la extension correspondiente en visual studio Code:
![image](https://github.com/Dev11Rox/PoyectoGestionDeAlmacenamiento/assets/157249748/653b1e3a-0edf-4862-8c06-66c63b55de5b)

## MySql
Fue utilizado para gestionar bases de datos donde se almacenan y consultan los conjuntos de datos utilizados en el proyecto, en este caso se utilizo el servidor mysql 8.0 disponible para la descarga en el siguiente [enlace](https://downloads.mysql.com/archives/installer/).
Posterior a la instalacion es necesario que se cree un susuario y contraseña personal. Por motivos de sgeuridad, en este caso, el usuario y contraseña reales deben de ser reemplazados en el archivo `Manipulación_de_datos.ipynb` para que todo funcione correctamente:
![image](https://github.com/Dev11Rox/PoyectoGestionDeAlmacenamiento/assets/157249748/d230958d-64af-44ed-a013-8e2191efce15)

## MySQL Workbench
Para la interfaz gráfica de usuario que permite la administración de bases de datos MySQL, facilitando la visualización, diseño, creación, y modificación de bases de datos, se utilizo Mysql Workbench, que se puede instalar en el siguiente [enlace](https://dev.mysql.com/downloads/workbench/).

## Excel
Se uso para la manipulación preliminar de datos, es decir, debido a que cuando se exportan los datos desde el archivo de `Limpieza_de_datos.ipynb`, vienen con una columna adicional incial. Es necesario que previo al uso del archivo `Manipulación_de_datos.ipynb`, esta columna sea eliminada con la herramienta excel. Columna a eliminar: 
![image](https://github.com/Dev11Rox/PoyectoGestionDeAlmacenamiento/assets/157249748/c141b039-f43f-4109-94d8-0e4e5425e83a)


# DETALLES SOBRE LA CANTIDAD Y NATURALEZA DE LOS DATOS
## Limpieza de Datos
El proyecto comienza con el proceso de limpieza de datos utilizando Excel, donde se eliminó manualmente la primera columna del conjunto de datos para evitar problemas con el código de manipulación posterior. Este paso fue esencial para preparar los datos para su análisis en Python.

## Manipulación de Datos
Después de la limpieza inicial, se utilizó Python para manipular y transformar los datos desde el servido de mysql. Este proceso incluyó la creación de metodos para graficar y realizar as acciones del CRUD(Create, Read, Update y Delete).

## Análisis y Visualización
Los datos preparados se analizaron para identificar patrones, tendencias y correlaciones. Se emplearon técnicas estadísticas y modelos de machine learning, con el apoyo de visualizaciones generadas a través de Matplotlib y Seaborn, para extraer insights relevantes que informaran nuestras conclusiones y recomendaciones. este analizis se puede ver dentro de el archivo `Limpieza_de_datos.ipynb`. 


# CONCLUSIONES
- La evaluación de la distribución de las edades, el tiempo desde el diagnóstico, y la prevalencia de distintos tipos y subtipos de cáncer, junto con las características demográficas y de comportamiento de los pacientes, como el hábito de fumar y el estado del tratamiento, revela patrones cruciales en la lucha contra el cáncer en Colombia.
- La distribución de edades ligeramente sesgada hacia pacientes mayores y la bimodalidad observada sugieren que ciertos cánceres podrían estar vinculados a etapas específicas de la vida, subrayando la necesidad de estrategias de detección diferenciadas.
- La predominancia de diagnósticos recientes y la existencia de valores atípicos refuerzan la importancia de mejorar los esfuerzos de detección temprana y la gestión de casos a largo plazo.
- La prevalencia de cánceres específicos, como el de mama y pulmón, destaca tanto la universalidad de estos desafíos como la oportunidad de enfocar los recursos hacia donde más se necesitan.
- La variabilidad en la distribución por género y raza, junto con el estado de fumador y el tratamiento, señala disparidades potenciales en el acceso a la atención médica y la eficacia del tratamiento, lo que llama a una revisión de las políticas de salud pública para garantizar una equidad más amplia.
- Aunque se han logrado avances en el diagnóstico y tratamiento del cáncer, aún queda un camino significativo por recorrer hacia la optimización de estrategias de salud pública.
- La identificación de poblaciones en riesgo y la asignación eficiente de recursos hacia programas de prevención y detección temprana podrían transformar el panorama del cáncer en el país. Además, estos insights abren vías para la investigación enfocada en el desarrollo de terapias personalizadas y la mejora de las tasas de supervivencia.
- Finalmente, el análisis subraya la necesidad imperativa de abordar las disparidades en el tratamiento y diagnóstico entre diferentes demografías, asegurando así que todos los ciudadanos tengan igual acceso a cuidados de alta calidad.
- El proyecto no solo contribuye al cuerpo académico de conocimiento sobre el cáncer sino que también proporciona una base empírica para el mejoramiento continuo de las políticas de salud pública, la asignación de recursos, y el desarrollo de tratamientos médicos, apuntando hacia una mayor equidad en la atención sanitaria y mejores resultados para los pacientes.


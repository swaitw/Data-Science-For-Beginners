# Trabajando con Datos: Python y la Biblioteca Pandas

| ![ Sketchnote por [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/07-WorkWithPython.png) |
| :-------------------------------------------------------------------------------------------------------: |
|                 Trabajando Con Python - _Sketchnote por [@nitya](https://twitter.com/nitya)_                 |

[![Video de Introducción](../../../../translated_images/es/video-ds-python.245247dc811db8e4.webp)](https://youtu.be/dZjWOGbsN4Y)

Mientras que las bases de datos ofrecen formas muy eficientes para almacenar datos y consultarlos usando lenguajes de consulta, la manera más flexible de procesar datos es escribiendo tu propio programa para manipularlos. En muchos casos, hacer una consulta en la base de datos sería un método más efectivo. Sin embargo, en algunos casos, cuando se necesita un procesamiento de datos más complejo, no se puede hacer fácilmente usando SQL.
El procesamiento de datos puede programarse en cualquier lenguaje de programación, pero hay ciertos lenguajes que son de más alto nivel respecto a trabajar con datos. Los científicos de datos típicamente prefieren uno de los siguientes lenguajes:

* **[Python](https://www.python.org/)**, un lenguaje de programación de propósito general, que a menudo se considera una de las mejores opciones para principiantes debido a su simplicidad. Python tiene muchas bibliotecas adicionales que pueden ayudarte a resolver muchos problemas prácticos, como extraer tus datos de un archivo ZIP, o convertir una imagen a escala de grises. Además del análisis de datos, Python también se usa frecuentemente para desarrollo web.
* **[R](https://www.r-project.org/)** es una caja de herramientas tradicional desarrollada con el procesamiento estadístico en mente. También contiene un gran repositorio de bibliotecas (CRAN), lo que lo hace una buena elección para procesamiento de datos. Sin embargo, R no es un lenguaje de programación de propósito general, y raramente se usa fuera del dominio de la ciencia de datos.
* **[Julia](https://julialang.org/)** es otro lenguaje desarrollado específicamente para la ciencia de datos. Está pensado para ofrecer mejor rendimiento que Python, convirtiéndolo en una gran herramienta para experimentación científica.

En esta lección, nos enfocaremos en usar Python para procesamiento simple de datos. Supondremos familiaridad básica con el lenguaje. Si quieres un recorrido más profundo por Python, puedes consultar uno de los siguientes recursos:

* [Aprende Python de Manera Divertida con Turtle Graphics y Fractales](https://github.com/shwars/pycourse) - Curso rápido basado en GitHub sobre programación en Python
* [Da tus Primeros Pasos con Python](https://docs.microsoft.com/en-us/learn/paths/python-first-steps/?WT.mc_id=academic-77958-bethanycheum) Ruta de Aprendizaje en [Microsoft Learn](http://learn.microsoft.com/?WT.mc_id=academic-77958-bethanycheum)

Los datos pueden venir en muchas formas. En esta lección, consideraremos tres formas de datos - **datos tabulares**, **texto** e **imágenes**.

Nos centraremos en algunos ejemplos de procesamiento de datos, en lugar de darte una visión completa de todas las bibliotecas relacionadas. Esto te permitirá obtener la idea principal de lo que es posible, y te dejará con una comprensión de dónde encontrar soluciones a tus problemas cuando las necesites.

> **Consejo más útil**. Cuando necesites realizar cierta operación sobre datos que no sabes cómo hacer, intenta buscarla en Internet. [Stackoverflow](https://stackoverflow.com/) usualmente contiene muchos ejemplos útiles de código en Python para muchas tareas típicas.



## [Cuestionario Previo a la Clase](https://ff-quizzes.netlify.app/en/ds/quiz/12)

## Datos Tabulares y Dataframes

Ya te has encontrado con datos tabulares cuando hablamos de bases de datos relacionales. Cuando tienes mucha data y está contenida en muchas tablas vinculadas diferentes, definitivamente tiene sentido usar SQL para trabajar con ella. Sin embargo, hay muchos casos en los que tenemos una tabla de datos y necesitamos obtener algún **entendimiento** o **perspectivas** acerca de esos datos, como la distribución, la correlación entre valores, etc. En la ciencia de datos, hay muchos casos cuando necesitamos realizar algunas transformaciones de los datos originales, seguidas por visualización. Ambos pasos pueden hacerse fácilmente usando Python.

Hay dos bibliotecas muy útiles en Python que pueden ayudarte a manejar datos tabulares:
* **[Pandas](https://pandas.pydata.org/)** te permite manipular los llamados **Dataframes**, que son análogos a tablas relacionales. Puedes tener columnas nombradas y realizar diferentes operaciones sobre filas, columnas y dataframes en general.
* **[Numpy](https://numpy.org/)** es una biblioteca para trabajar con **tenores**, es decir, **arrays** multidimensionales. Un array tiene valores del mismo tipo subyacente y es más simple que un dataframe, pero ofrece más operaciones matemáticas y crea menos sobrecarga.

También hay un par de otras bibliotecas que deberías conocer:
* **[Matplotlib](https://matplotlib.org/)** es una biblioteca usada para visualización de datos y graficar gráficos
* **[SciPy](https://www.scipy.org/)** es una biblioteca con algunas funciones científicas adicionales. Ya nos encontramos con esta biblioteca al hablar de probabilidad y estadística

Aquí hay un fragmento de código que típicamente usarías para importar esas bibliotecas al principio de tu programa Python:
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from scipy import ... # necesitas especificar los sub-paquetes exactos que necesitas
``` 

Pandas se centra en unos pocos conceptos básicos.

### Series

**Series** es una secuencia de valores, similar a una lista o array numpy. La principal diferencia es que una serie también tiene un **índice**, y cuando operamos sobre series (por ejemplo, sumarlas), el índice es tomado en cuenta. El índice puede ser tan simple como el número entero de la fila (es el índice usado por defecto al crear una serie desde una lista o array), o puede tener una estructura compleja, como un intervalo de fechas.

> **Nota**: Hay algo de código introductorio de Pandas en el cuaderno acompañante [`notebook.ipynb`](notebook.ipynb). Solo presentamos algunos ejemplos aquí, y definitivamente eres bienvenido a revisar el cuaderno completo.

Considera un ejemplo: queremos analizar las ventas de nuestra heladería. Generemos una serie de números de ventas (número de artículos vendidos cada día) para un cierto periodo de tiempo:

```python
start_date = "Jan 1, 2020"
end_date = "Mar 31, 2020"
idx = pd.date_range(start_date,end_date)
print(f"Length of index is {len(idx)}")
items_sold = pd.Series(np.random.randint(25,50,size=len(idx)),index=idx)
items_sold.plot()
```
![Gráfico de Serie Temporal](../../../../translated_images/es/timeseries-1.80de678ab1cf727e.webp)

Supón ahora que cada semana organizamos una fiesta para amigos y llevamos 10 paquetes adicionales de helado para la fiesta. Podemos crear otra serie, indexada por semana, para demostrar esto:
```python
additional_items = pd.Series(10,index=pd.date_range(start_date,end_date,freq="W"))
```
Al sumar dos series, obtenemos el número total:
```python
total_items = items_sold.add(additional_items,fill_value=0)
total_items.plot()
```
![Gráfico de Serie Temporal](../../../../translated_images/es/timeseries-2.aae51d575c55181c.webp)

> **Nota** que no estamos usando la sintaxis simple `total_items+additional_items`. Si lo hiciéramos, recibiríamos muchos valores `NaN` (*Not a Number*) en la serie resultante. Esto es porque hay valores faltantes para algunos puntos del índice en la serie `additional_items`, y sumar `NaN` a cualquier cosa resulta en `NaN`. Por lo tanto, necesitamos especificar el parámetro `fill_value` durante la suma.

Con series temporales, también podemos **remuestrear** la serie con diferentes intervalos de tiempo. Por ejemplo, supón que queremos calcular el promedio mensual del volumen de ventas. Podemos usar el siguiente código:
```python
monthly = total_items.resample("1M").mean()
ax = monthly.plot(kind='bar')
```
![Promedios Mensuales de Series Temporales](../../../../translated_images/es/timeseries-3.f3147cbc8c624881.webp)

### DataFrame

Un DataFrame es esencialmente una colección de series con el mismo índice. Podemos combinar varias series en un DataFrame:
```python
a = pd.Series(range(1,10))
b = pd.Series(["I","like","to","play","games","and","will","not","change"],index=range(0,9))
df = pd.DataFrame([a,b])
```
Esto creará una tabla horizontal como esta:
|     | 0   | 1    | 2   | 3   | 4      | 5   | 6      | 7    | 8    |
| --- | --- | ---- | --- | --- | ------ | --- | ------ | ---- | ---- |
| 0   | 1   | 2    | 3   | 4   | 5      | 6   | 7      | 8    | 9    |
| 1   | I   | like | to  | use | Python | and | Pandas | very | much |

También podemos usar Series como columnas y especificar nombres de columnas usando diccionario:
```python
df = pd.DataFrame({ 'A' : a, 'B' : b })
```
Esto nos dará una tabla como esta:

|     | A   | B      |
| --- | --- | ------ |
| 0   | 1   | I      |
| 1   | 2   | like   |
| 2   | 3   | to     |
| 3   | 4   | use    |
| 4   | 5   | Python |
| 5   | 6   | and    |
| 6   | 7   | Pandas |
| 7   | 8   | very   |
| 8   | 9   | much   |

**Nota** que también podemos obtener esta disposición de tabla trasponiendo la tabla anterior, por ejemplo escribiendo 
```python
df = pd.DataFrame([a,b]).T.rename(columns={ 0 : 'A', 1 : 'B' })
```
Aquí `.T` significa la operación de transponer el DataFrame, es decir, cambiar filas y columnas, y la operación `rename` nos permite renombrar columnas para que coincidan con el ejemplo anterior.

Estas son algunas de las operaciones más importantes que podemos realizar en DataFrames:

**Selección de columna**. Podemos seleccionar columnas individuales escribiendo `df['A']` - esta operación devuelve una Serie. También podemos seleccionar un subconjunto de columnas en otro DataFrame escribiendo `df[['B','A']]` - esto devuelve otro DataFrame.

**Filtrar** solo ciertas filas por criterio. Por ejemplo, para dejar solo filas con columna `A` mayor que 5, podemos escribir `df[df['A']>5]`.

> **Nota**: La forma en que funciona el filtrado es la siguiente. La expresión `df['A']<5` devuelve una serie booleana, que indica si la expresión es `True` o `False` para cada elemento de la serie original `df['A']`. Cuando una serie booleana se usa como índice, devuelve el subconjunto de filas en el DataFrame. Por lo tanto, no es posible usar expresiones booleanas arbitrarias de Python, por ejemplo escribir `df[df['A']>5 and df['A']<7]` sería incorrecto. En cambio, debes usar la operación especial `&` en series booleanas, escribiendo `df[(df['A']>5) & (df['A']<7)]` (*los paréntesis son importantes aquí*).

**Crear nuevas columnas computables**. Podemos crear fácilmente nuevas columnas computables para nuestro DataFrame usando expresiones intuitivas como esta:
```python
df['DivA'] = df['A']-df['A'].mean() 
``` 
Este ejemplo calcula la divergencia de A respecto a su valor medio. Lo que realmente ocurre aquí es que estamos computando una serie y luego asignando esta serie al lado izquierdo, creando otra columna. Por lo tanto, no podemos usar operaciones que no sean compatibles con series, por ejemplo, el siguiente código está mal:
```python
# Código incorrecto -> df['ADescr'] = "Bajo" si df['A'] < 5 sino "Alto"
df['LenB'] = len(df['B']) # <- Resultado incorrecto
``` 
El último ejemplo, aunque es sintácticamente correcto, nos da un resultado incorrecto, porque asigna la longitud de la serie `B` a todos los valores en la columna, y no la longitud de los elementos individuales como se pretendía.

Si necesitamos computar expresiones complejas como esta, podemos usar la función `apply`. El último ejemplo puede escribirse así:
```python
df['LenB'] = df['B'].apply(lambda x : len(x))
# o
df['LenB'] = df['B'].apply(len)
```

Después de las operaciones anteriores, terminaremos con el siguiente DataFrame:

|     | A   | B      | DivA | LenB |
| --- | --- | ------ | ---- | ---- |
| 0   | 1   | I      | -4.0 | 1    |
| 1   | 2   | like   | -3.0 | 4    |
| 2   | 3   | to     | -2.0 | 2    |
| 3   | 4   | use    | -1.0 | 3    |
| 4   | 5   | Python | 0.0  | 6    |
| 5   | 6   | and    | 1.0  | 3    |
| 6   | 7   | Pandas | 2.0  | 6    |
| 7   | 8   | very   | 3.0  | 4    |
| 8   | 9   | much   | 4.0  | 4    |

**Seleccionar filas basándose en números** puede hacerse usando la construcción `iloc`. Por ejemplo, para seleccionar las primeras 5 filas del DataFrame:
```python
df.iloc[:5]
```

**Agrupar** se usa a menudo para obtener un resultado similar a las *tablas dinámicas* en Excel. Supongamos que queremos calcular el valor medio de la columna `A` para cada número dado de `LenB`. Entonces podemos agrupar nuestro DataFrame por `LenB`, y llamar a `mean`:
```python
df.groupby(by='LenB')[['A','DivA']].mean()
```
Si necesitamos calcular la media y el número de elementos en el grupo, podemos usar la función más compleja `aggregate`:
```python
df.groupby(by='LenB') \
 .aggregate({ 'DivA' : len, 'A' : lambda x: x.mean() }) \
 .rename(columns={ 'DivA' : 'Count', 'A' : 'Mean'})
```
Esto nos da la siguiente tabla:

| LenB | Count | Mean     |
| ---- | ----- | -------- |
| 1    | 1     | 1.000000 |
| 2    | 1     | 3.000000 |
| 3    | 2     | 5.000000 |
| 4    | 3     | 6.333333 |
| 6    | 2     | 6.000000 |

### Obteniendo Datos


Hemos visto lo fácil que es construir Series y DataFrames a partir de objetos de Python. Sin embargo, los datos usualmente vienen en forma de un archivo de texto o una tabla de Excel. Por suerte, Pandas nos ofrece una forma sencilla de cargar datos desde el disco. Por ejemplo, leer un archivo CSV es tan simple como esto:
```python
df = pd.read_csv('file.csv')
```
Veremos más ejemplos de carga de datos, incluyendo cómo obtenerlos desde sitios web externos, en la sección "Desafío"


### Imprimir y Graficar

Un Científico de Datos a menudo tiene que explorar los datos, por lo tanto es importante poder visualizarlos. Cuando el DataFrame es grande, muchas veces solo queremos asegurarnos de que estamos haciendo todo correctamente imprimiendo las primeras filas. Esto se puede hacer llamando a `df.head()`. Si lo haces desde Jupyter Notebook, imprimirá el DataFrame en una forma tabular agradable.

También hemos visto el uso de la función `plot` para visualizar algunas columnas. Mientras que `plot` es muy útil para muchas tareas y soporta diferentes tipos de gráficos vía el parámetro `kind=`, siempre puedes usar la biblioteca `matplotlib` para graficar algo más complejo. Cubriremos la visualización de datos en detalle en lecciones separadas del curso.

Esta visión general cubre los conceptos más importantes de Pandas, sin embargo, la biblioteca es muy rica, ¡y no hay límite a lo que puedes hacer con ella! Ahora apliquemos este conocimiento para resolver un problema específico.

## 🚀 Desafío 1: Analizando la Propagación del COVID

El primer problema en el que nos enfocaremos es el modelado de la propagación epidémica del COVID-19. Para ello, usaremos los datos sobre el número de individuos infectados en diferentes países, proporcionados por el [Center for Systems Science and Engineering](https://systems.jhu.edu/) (CSSE) de la [Universidad Johns Hopkins](https://jhu.edu/). El conjunto de datos está disponible en [este repositorio de GitHub](https://github.com/CSSEGISandData/COVID-19).

Ya que queremos demostrar cómo trabajar con datos, te invitamos a abrir [`notebook-covidspread.ipynb`](notebook-covidspread.ipynb) y leerlo de arriba a abajo. También puedes ejecutar las celdas y realizar algunos desafíos que hemos dejado para ti al final.

![Propagación del COVID](../../../../translated_images/es/covidspread.f3d131c4f1d260ab.webp)

> Si no sabes cómo ejecutar código en Jupyter Notebook, echa un vistazo a [este artículo](https://soshnikov.com/education/how-to-execute-notebooks-from-github/).

## Trabajando con Datos No Estructurados

Aunque los datos muy a menudo vienen en forma tabular, en algunos casos necesitamos trabajar con datos menos estructurados, por ejemplo, texto o imágenes. En estos casos, para aplicar las técnicas de procesamiento de datos que hemos visto arriba, necesitamos de alguna forma **extraer** datos estructurados. Aquí algunos ejemplos:

* Extraer palabras clave del texto y ver con qué frecuencia aparecen esas palabras clave
* Usar redes neuronales para extraer información sobre objetos en la imagen
* Obtener información sobre emociones de personas en la transmisión de video de una cámara

## 🚀 Desafío 2: Analizando Artículos sobre COVID

En este desafío, continuaremos con el tema de la pandemia de COVID y nos enfocaremos en procesar artículos científicos sobre el tema. Existe el Conjunto de Datos [CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) con más de 7000 (al momento de escribir) artículos sobre COVID, disponible con metadatos y resúmenes (y para aproximadamente la mitad de ellos también se proporciona el texto completo).

Un ejemplo completo de análisis de este conjunto de datos usando el servicio cognitivo [Text Analytics for Health](https://docs.microsoft.com/azure/cognitive-services/text-analytics/how-tos/text-analytics-for-health/?WT.mc_id=academic-77958-bethanycheum) está descrito [en esta publicación de blog](https://soshnikov.com/science/analyzing-medical-papers-with-azure-and-text-analytics-for-health/). Discutiremos una versión simplificada de este análisis.

> **NOTA**: No proporcionamos una copia del conjunto de datos como parte de este repositorio. Primero puede que necesites descargar el archivo [`metadata.csv`](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge?select=metadata.csv) desde [este conjunto de datos en Kaggle](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge). Puede ser necesaria la inscripción en Kaggle. También puedes descargar el conjunto de datos sin registrarte [desde aquí](https://ai2-semanticscholar-cord-19.s3-us-west-2.amazonaws.com/historical_releases.html), pero incluirá todos los textos completos además del archivo de metadatos.

Abre [`notebook-papers.ipynb`](notebook-papers.ipynb) y léelo de arriba a abajo. También puedes ejecutar las celdas y realizar algunos desafíos que hemos dejado para ti al final.

![Tratamiento Médico COVID](../../../../translated_images/es/covidtreat.b2ba59f57ca45fbc.webp)

## Procesamiento de Datos de Imágenes

Recientemente, se han desarrollado modelos de IA muy poderosos que nos permiten comprender imágenes. Hay muchas tareas que pueden resolverse usando redes neuronales preentrenadas o servicios en la nube. Algunos ejemplos incluyen:

* **Clasificación de Imágenes**, que puede ayudarte a categorizar la imagen en una de las clases predefinidas. Puedes entrenar fácilmente tus propios clasificadores de imágenes usando servicios como [Custom Vision](https://azure.microsoft.com/services/cognitive-services/custom-vision-service/?WT.mc_id=academic-77958-bethanycheum)
* **Detección de Objetos** para detectar diferentes objetos en la imagen. Servicios como [computer vision](https://azure.microsoft.com/services/cognitive-services/computer-vision/?WT.mc_id=academic-77958-bethanycheum) pueden detectar varios objetos comunes, y puedes entrenar un modelo [Custom Vision](https://azure.microsoft.com/services/cognitive-services/custom-vision-service/?WT.mc_id=academic-77958-bethanycheum) para detectar algunos objetos específicos de interés.
* **Detección de Rostros**, incluyendo detección de Edad, Género y Emoción. Esto puede hacerse mediante [Face API](https://azure.microsoft.com/services/cognitive-services/face/?WT.mc_id=academic-77958-bethanycheum).

Todos esos servicios en la nube pueden ser llamados usando [SDKs de Python](https://docs.microsoft.com/samples/azure-samples/cognitive-services-python-sdk-samples/cognitive-services-python-sdk-samples/?WT.mc_id=academic-77958-bethanycheum), y así pueden incorporarse fácilmente en tu flujo de trabajo de exploración de datos.

Aquí algunos ejemplos de exploración de datos desde fuentes de datos de imágenes:
* En el post del blog [Cómo aprender ciencia de datos sin programar](https://soshnikov.com/azure/how-to-learn-data-science-without-coding/) exploramos fotos de Instagram, tratando de entender qué hace que las personas den más "me gusta" a una foto. Primero extraemos tanta información como sea posible de las imágenes usando [computer vision](https://azure.microsoft.com/services/cognitive-services/computer-vision/?WT.mc_id=academic-77958-bethanycheum), y luego usamos [Azure Machine Learning AutoML](https://docs.microsoft.com/azure/machine-learning/concept-automated-ml/?WT.mc_id=academic-77958-bethanycheum) para construir un modelo interpretable.
* En [Facial Studies Workshop](https://github.com/CloudAdvocacy/FaceStudies) usamos [Face API](https://azure.microsoft.com/services/cognitive-services/face/?WT.mc_id=academic-77958-bethanycheum) para extraer emociones de personas en fotografías de eventos, con el fin de tratar de entender qué hace felices a las personas.

## Conclusión

Ya sea que ya tengas datos estructurados o no estructurados, usando Python puedes realizar todos los pasos relacionados con el procesamiento y entendimiento de datos. Probablemente es la forma más flexible de procesar datos, y esa es la razón por la que la mayoría de los científicos de datos usan Python como su herramienta principal. Aprender Python en profundidad probablemente sea una buena idea si estás serio en tu camino en ciencia de datos.

## [Examen posterior a la lección](https://ff-quizzes.netlify.app/en/ds/quiz/13)

## Repaso y Autoestudio

**Libros**
* [Wes McKinney. Python para el Análisis de Datos: Manipulación de Datos con Pandas, NumPy e IPython](https://www.amazon.com/gp/product/1491957662)

**Recursos en línea**
* Tutorial oficial [10 minutos para Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
* [Documentación sobre Visualización en Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html)

**Aprender Python**
* [Aprende Python de forma divertida con Turtle Graphics y Fractales](https://github.com/shwars/pycourse)
* [Da tus primeros pasos con Python](https://docs.microsoft.com/learn/paths/python-first-steps/?WT.mc_id=academic-77958-bethanycheum) Camino de aprendizaje en [Microsoft Learn](http://learn.microsoft.com/?WT.mc_id=academic-77958-bethanycheum)

## Tarea

[Realiza un estudio de datos más detallado para los desafíos anteriores](assignment.md)

## Créditos

Esta lección ha sido creada con ♥️ por [Dmitry Soshnikov](http://soshnikov.com)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**Descargo de responsabilidad**:
Este documento ha sido traducido utilizando el servicio de traducción automática [Co-op Translator](https://github.com/Azure/co-op-translator). Aunque nos esforzamos por la precisión, tenga en cuenta que las traducciones automatizadas pueden contener errores o inexactitudes. El documento original en su idioma nativo debe considerarse la fuente autorizada. Para información crítica, se recomienda una traducción profesional humana. No somos responsables de cualquier malentendido o interpretación errónea que surja del uso de esta traducción.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->
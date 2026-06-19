Proyecto de Análisis Exploratorio de Datos (EDA)

Objetivo del proyecto

El objetivo de este proyecto es realizar un proceso completo de preparación, integración y análisis exploratorio de datos a partir de información procedente de una campaña de marketing bancario y de un conjunto de datos complementario con información demográfica y socioeconómica de los clientes.

El análisis busca identificar patrones relevantes en el comportamiento de los clientes y determinar qué factores pueden estar relacionados con la contratación del producto financiero ofertado.

Estructura del proyecto
Proyecto 4 EDA con Python/
│
├── Raw Data/
│   ├── bank-additional.csv
│   └── customer-details.xlsx
│
│── Clean Data/
│   ├── bank_clean.xlsx
│   ├── clientes_clean.xlsx
│   └── df_bank_clientes.xlsx
│
├── Notebooks/
│   └── EDA_Bank_Marketing.ipynb
│
├── README.md
│
└── Informe Proyecto 4 - Eda con Python.pdf


Carpeta Raw Data: Incluye los archivos originales proporcionados para la realización del análisis.

Clean Data: Contiene los datasets resultantes tras las tareas de limpieza, transformación e integración de datos.

Carpeta notebooks: Contiene el notebook utilizado para desarrollar todas las fases del proyecto, incluyendo la limpieza de datos, el análisis exploratorio y la generación de visualizaciones.


Metodología y pasos realizados

1. Carga y exploración inicial

Se cargaron los dos conjuntos de datos proporcionados y se realizó una inspección inicial para comprender su estructura, número de registros, tipos de variables y calidad general de los datos.

Durante esta fase se identificaron variables categóricas, numéricas y temporales, así como posibles problemas de calidad de datos.

2. Limpieza y transformación de datos

Se realizaron las siguientes tareas:

Eliminación de columnas sin utilidad analítica.
Normalización de los nombres de las variables.
Conversión de variables numéricas almacenadas como texto.
Conversión de fechas al formato datetime.
Transformación de variables binarias a formato categórico.
Corrección de tipos de datos inconsistentes.

3. Tratamiento de valores ausentes

Se analizaron los valores nulos presentes en cada variable.

Las variables categóricas fueron tratadas mediante la creación de la categoría "Unknown" cuando resultó apropiado. Para determinadas variables numéricas se utilizó la mediana como método de imputación debido a su mayor robustez frente a valores extremos.

En el caso de la variable Euribor, se estudió previamente el patrón de ausencia para comprobar si existía alguna relación temporal que justificara otro tipo de tratamiento.

4. Integración de datasets

Los dos conjuntos de datos fueron integrados mediante el identificador único del cliente.

Se verificó previamente la ausencia de duplicados y se comprobó la correcta correspondencia entre los identificadores de ambos datasets.

La integración se realizó mediante un merge de tipo left, conservando todos los registros del dataset principal.

5. Análisis exploratorio

Una vez obtenido el dataset final, se realizó un análisis descriptivo de las variables más relevantes mediante estadísticas descriptivas y representaciones gráficas.

Entre los análisis realizados destacan:

Distribución de edades.
Distribución de ingresos.
Distribución de profesiones.
Estado civil.
Nivel educativo.
Duración de las llamadas.
Variables económicas.
Contratación del producto financiero.

6. Análisis de relaciones

Posteriormente se analizaron posibles relaciones entre las variables y la variable objetivo (y), que indica la contratación del producto.

Se estudiaron especialmente:

Edad y contratación.
Ingresos y contratación.
Euribor y contratación.
Profesión y contratación.
Estado civil y contratación.

Finalmente, se elaboró una matriz de correlación para identificar relaciones lineales entre las variables numéricas.


Resultados obtenidos

Perfil de los clientes

La cartera de clientes está compuesta principalmente por adultos de mediana edad, con una edad media cercana a los 40 años.

Los grupos profesionales más frecuentes son los empleados administrativos, los trabajadores manuales y los técnicos.

Asimismo, una proporción significativa de los clientes posee estudios universitarios.

Comportamiento de la campaña

La duración de las llamadas presenta una distribución claramente asimétrica, con la mayoría de contactos concentrados en duraciones relativamente cortas y un número reducido de llamadas excepcionalmente largas.

La mayor parte de los clientes había sido contactada pocas veces durante la campaña y no había participado previamente en campañas comerciales anteriores.

Factores relacionados con la contratación

El análisis mostró que aproximadamente el 11% de los clientes contrató el producto financiero ofertado.

Las variables que mostraron una relación más clara con la contratación fueron:

El nivel del Euribor.
La profesión del cliente.
Determinados indicadores económicos.

Por el contrario, variables como la edad o los ingresos mostraron diferencias reducidas entre los clientes que contrataron y los que no contrataron el producto.

Correlaciones

Las variables macroeconómicas presentaron correlaciones positivas muy elevadas entre sí, destacando especialmente:

Euribor y tasa de variación del empleo.
Euribor y número de empleados.
Tasa de variación del empleo y número de empleados.

Estas relaciones sugieren que dichas variables reflejan aspectos similares del contexto económico.


Conclusiones

A partir del análisis realizado se concluye que la contratación del producto financiero parece estar más relacionada con factores económicos y con determinadas características sociodemográficas que con variables individuales como la edad o el nivel de ingresos.

El Euribor se identifica como una de las variables más relevantes del estudio, observándose una mayor probabilidad de contratación en entornos de tipos de interés reducidos.

Asimismo, estudiantes y jubilados presentan las mayores tasas de contratación, mientras que otros perfiles profesionales muestran una respuesta significativamente menor a la campaña.

En conjunto, los resultados permiten identificar segmentos de clientes con mayor propensión a la contratación y ofrecen información útil para optimizar futuras campañas comerciales.

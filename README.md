![ETL & EDA\Logo PI MLOps STEAM.png](https://github.com/JavierEdgarEsteban77/PI-MLOps---STEAM/blob/ac6b524c83736a49ed22650410ac58ed3172777c/ETL%20%26%20EDA/Logo%20PI%20MLOps%20STEAM.png)

# **Descripción del Proyecto**

Este proyecto consiste en un análisis de datos de juegos de la empresa Steam, con reseñas de usuarios y datos de usuarios.

El objetivo es realizar ingeniería de características, análisis de sentimientos y desarrollo de una API para disponibilizar los datos cuya finalidad es obtener el Producto Mínimo Viable (MVP) y brindar todas las recomendaciones necesarias para brindar información para la toma de decisiones.

## **Requisitos**

- Python 3.12.0
- Pandas
- NLTK
- Matplotlib
- FastAPI.

## **Archivos del Proyecto**

Los archivos JSON con los que trabajaremos para armar nuestros DataFrames de Steam son:

- `steam_games.json`
- `user_reviews.json.gz`
- `users_items.json.gz`

Además, se han creado los siguientes archivos CSV a partir de los DataFrames con los que se ha trabajado y están disponibles en el repositorio clonado:

- `steam_games.csv`
- `user_reviews.csv`
- `users_items.csv`

Los archivos JSON estarán disponibilizados para solo lectura en el siguiente enlace:

## **Proceso a ejecutar el código en este orden:**

1. Importo las bibliotecas necesarias, éstas son: json, pandas, ast, gzip, nltk, vader_lexicon, matplotlib, seaborn, boxplot, os, FastAPI, tqdm.
2. Adapto nuestros dataset en los siguientes D  ataFrames en los que trabajo: `df_steam_games`, `df_user_reviews` y `df_users_items`.
3. Cargo y trabajo los datos de los juegos de Steam, las reseñas de los usuarios y los datos de los usuarios utilizando la función `cargar_datos` para poder procesarlos.
4. Realizo el preprocesamiento y la limpieza de los datos.
5. Realizo el análisis de sentimientos en las reseñas de los usuarios utilizando la biblioteca NLTK.

## **Análisis exploratorio de los datos (EDA)**

Una vez que toda la data es consumible por la API, está lista para consumir por los departamentos de Analytics y Machine Learning, y nuestro EDA nos permite entender bien los datos a los que tenemos acceso.

## **Modelo de aprendizaje automático**

Propuestas de trabajo: 

He elegido el sistema de recomendación, el cual aplica el filtro user-item, esto es tomo un usuario, se encuentran usuarios similares y se recomiendan ítems que a esos usuarios similares les gustaron.

La finalidad es recibir una lista con 5 juegos recomendados para dicho usuario.

En este caso el input es un usuario y el output es una lista de juegos que se le recomienda ese listado a ese usuario, en general se explican como "A usuarios que son similares a tí también les gustó...". 

## **Desarrollo de una API utilizando FastAPI con los siguientes endpoints:**

- developer(desarrollador: str): Este endpoint devuelve la cantidad de items y de contenido Free por año según la empresa desarrolladora.

- userdata(User_id: str): Este endpoint devuelve la cantidad de dinero gastado por el usuario, el porcentaje de recomendación en base a reviews.recommend y la cantidad de items.

- UserForGenre(genero: str): Este endpoint devuelve el usuario que acumula más horas jugadas para el género dado y una lista de la acumulación de horas jugadas por año de lanzamiento.

- best_developer_year(año: int): Este endpoint devuelve el top 3 de desarrolladores con juegos MÁS recomendados por usuarios para el año dado. (reviews.recommend = True y comentarios positivos)

- developer_reviews_analysis(desarrolladora: str): Según el desarrollador, se devuelve un diccionario con el nombre del desarrollador como llave y una lista con la cantidad total de registros de reseñas de usuarios que se encuentren categorizados con un análisis de sentimiento como valor positivo o negativo.

## **Ejecución de la API**

Enlace de fastAPI es: 

## **Video Explicativo**

Enlace al video explicativo:

## **Notas**

Es menester considerar que este proyecto puede ser mejorado y ampliado en el futuro cuya finalidad es brindar información oportuna para la toma de decisiones.

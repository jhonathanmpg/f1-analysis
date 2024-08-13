
# Proyecto de Análisis de Datos de Fórmula 1

Este repositorio contiene el código para el análisis de datos históricos de Fórmula 1, centrado en el periodo 2000-2024. Se utiliza Python y varias bibliotecas de análisis de datos para explorar, limpiar y visualizar la información contenida en archivos CSV y bases de datos SQLite. El análisis principal se realiza en el archivo `main.ipynb`.

## Estructura del Proyecto

- `main.ipynb`: El archivo principal que contiene todo el código de análisis y visualización.
- `data/`: Carpeta que contiene todos los archivos CSV y las bases de datos SQLite utilizados en el análisis.
- `data/reports/`: Carpeta donde se guardan los reportes generados con `Pandas Profiling`.
- `data/circuits.csv`: Archivo CSV generado a partir de la tabla `circuits` de la base de datos.

## Requisitos

Este proyecto requiere las siguientes bibliotecas de Python:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `missingno`
- `plotly`
- `ydata_profiling`
- `sqlite3`

Puedes instalar todas las dependencias utilizando `pip` con el siguiente comando:

```bash
pip install -r requirements.txt
```


## Descripción del Código

1. **Lectura de Datos**:
   - Se leen todos los archivos CSV y bases de datos SQLite ubicados en la carpeta `data/`.
   - Los archivos CSV se cargan en dataframes de pandas, nombrados según el nombre del archivo.
   - Las bases de datos SQLite se conectan para acceder a sus tablas y validar la información contra los CSV.

2. **Validación de Datos**:
   - Se verifica que la información contenida en las bases de datos coincida con los datos de los archivos CSV.
   - Se identifica que la tabla `circuits` no tiene un archivo CSV correspondiente, por lo que se extrae y se guarda en `data/circuits.csv`.

3. **Análisis Exploratorio de Datos (EDA)**:
   - Se generan reportes utilizando `Pandas Profiling` para cada dataframe.
   - Se realizan visualizaciones exploratorias utilizando `matplotlib`, `seaborn` y `plotly`, enfocándose en victorias por pilotos y constructores, entre otros análisis.

4. **Limpieza de Datos**:
   - Se convierten las columnas de fechas a formato datetime.
   - Se rellenan los valores nulos en los dataframes con valores apropiados, como 0 o cadenas vacías.

5. **Visualizaciones**:
   - Se crean gráficos para analizar los resultados de las carreras, incluyendo distribuciones de puntos, posiciones en la parrilla de salida, y más.
   - Se estudian los patrones de las paradas en boxes y su duración a lo largo de las temporadas.

6. **Exportación de Datos**:
   - Se exporta el dataframe `df_circuits` a un archivo CSV para facilitar su uso futuro.

## Ejecución del Proyecto

Para ejecutar el análisis, simplemente abre el archivo `main.ipynb` en un entorno de Jupyter Notebook y sigue las celdas de código. El análisis completo se realizará de forma secuencial, generando los reportes y visualizaciones correspondientes.

## Contribuciones

Si deseas contribuir a este proyecto, siéntete libre de hacer un fork del repositorio y enviar un pull request con tus mejoras o sugerencias. 

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para obtener más detalles.

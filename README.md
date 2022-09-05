# TFMScripts
## English
Repository to store the TFM scripts to be able to reproduce the results obtained.

The repository is divided into 4 sections. Next we will explain the order of execution that must be followed in each of them to correctly reproduce the results.
Within each folder it will be explained more specifically what each notebook does.
* Firstly, the files in the script_generation_dataset folder must be executed. In this folder there are files that allow us, from the raw data,
to obtain for each basin the necessary information of each cyclone. So, first you have to execute the NA_basin, EasternPacific_Basin, WestNorthPacific_Basin, SouthPacific_Basin files
and All_basin. This way for each basin we have a dataset with the data of all the cyclones of the basin.
The next file to be executed is cyclone_files_generator. This file creates folders in which it saves a file for each cyclone. The folders it creates store the data, the precipitation,
the radius and angle of each cyclone. This is necessary to reproduce the results of the script_analysis_variables folder.
Finally the file GroupDataInGross generates the dataset that we will use to build the model. This dataset is the most important that is generated and used in the
of script_matrices_som and script_validation.
* All the necessary datasets are created and the other files can be executed. To follow an order, it is recommended to execute the files of script_analisis_variables, where
collect the results of the influence of variables by basins and globally without applying any model. Then you can run the script_matrices_som files.
In them, the notebook Matrices_SOM_20x20 is the main one and it collects the model and its results. The 3DScatterPlot20x20 file is a mere visual representation
of the characteristics space and how the SOM centroids are distributed in it. Finally, in script_validation we find a single notebook where the validation is collected
of the 95th and 99th percentiles of the model.

## Español
Repositorio para almacenar los scripts del TFM y así poder reproducir los resultados obtenidos.

El repositorio se divide en 4 apartados. A continuación se va a explicar el orden de ejecución que se debe seguir en cada uno de ellos para reprouducir correctamente los resultados.
Dentro de cada carpeta se explicará más en concreto que realiza cada notebook.
* En primer lugar se deben ejecutar los ficheros de la carpeta script_generacion_dataset. En esta carpeta se encuentran ficheros que nos permiten, a partir de los datos en crudo,
obtener para cada cuenca la información necesaria de cada ciclón. Con lo cual se debe ejecutar primero los archivos NA_basin, EasternPacific_Basin, WestNorthPacific_Basin, SouthPacific_Basin
y All_basin. De este modo para cada cuenca tenemos un dataset con los datos de todos los ciclones de la cuenca.
El siguiente fichero en ejecutarse es cyclone_files_generator. Este archivo crea carpetas en las que guarda un fichero por cada ciclón. Las carpetas que crea almacenan los datos, la precipitación,
el radio y el ángulo de cada ciclón. Esto es necesario para reproducir los resultados de la carpeta script_analisis_variables.
Por último el fichero AgruparDatosEnBruto nos genera el dataset que utilizaremos para construir el modelo. Este dataset es el más importante que se genera y se usa en las carpetas
de script_matrices_som y script_validacion.
* Creados todos los dataset necesarios ya se pueden ejecutar los demás archivos. Por seguir un orden, es recomendable ejecutar los archivos de script_analisis_variables, donde se
recogen los resultados de la influencia de variables por cuencas y globalmente sin aplicar ningún modelo. Luego ya se pueden ejecutar los archivos de script_matrices_som.
En ellos se recoge el notebook Matrices_SOM_20x20 que es el principal y recoge el modelo y sus resultados. El archivo 3DScatterPlot20x20 es una mera representación visual
del espacio de características y como se distribuyen en él los centroides de la SOM. Por último, en script_validación encontramos un único notebook donde se recoge la validación
de los percentiles 95 y 99 del modelo.

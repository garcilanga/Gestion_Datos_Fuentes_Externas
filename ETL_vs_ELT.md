# ETL vs ELT

Los **procesos ETL** en general (Extraction, Transform and Load) constituyen uno de los pilares más importantes en la construcción de una solución de BI, representando alrededor del **80% del proyecto**.

## E**T**L

Los procesos ETL se encargan de **extraer datos** de los orígenes o fuentes, **aplicar las transformaciones** necesarias a esos datos para adaptarlos a las necesidades de formato, negocio, etc. y **cargarlos en uno o varios destinos** para su uso y explotación.

En los procesos ETL intervienen diversos elementos:
- Orígenes de datos: bases de datos, webservices, ficheros...
- Herramientas de extracción y transformación.
- Destinos de datos: generalmente bases de datos, aunque también otros.

En los procesos ETL las operaciones de transformación se realizan directamente en la propia herramienta, antes de cargar los datos en la base de datos de destino.

Pero existen ciertas **variaciones conceptuales al proceso ETL que influyen principalmente en el rendimiento** de los procesos de manejo de los datos. Algunas de estas variaciones son **ELT** y **ELTL**.

## EL**T**

Una variante de los procesos ETL son los procesos ELT (Extract, Load and Transform) en los que, básicamente, cambia el orden en el proceso de ejecución. En primer lugar se realiza la extracción da datos del origen u orígenes, luego se cargan los datos en los destinos tal y como están, y ya en el destino (que debería ser una base de datos) se aplican las transformaciones.

**Los procesos ELT proporcionan mayor velocidad de proceso y transformación**

- Mientras que las herramientas de transformación en las ETL evalúan la información registro por registro, en las ELT las transformaciones se realizan directamente en la base de datos, evaluando los registros en lotes.

**Los procesos ELT hacen un mejor uso de los recursos**

Hoy día, las bases de datos, en general, están mejor preparadas para la optimización de los recursos (disco, memoria y proceso).

Además, los avances en el área del procesamiento distribuido han alcanzado tanto a las bases de datos como a los sistemas de procesamiento.
    
Así, bases de datos como **MongoDB** y sistemas de procesamiento como **Hadoop** o **Spark** permiten realizar operaciones de forma distribuida procesando datos en volúmenes y tiempos impensables hasta hace algunos años.

Las ELT realizan los procesos de transformación en la base de datos, aprovechando así el mejor rendimiento que estas herramientas ofrecen.

En cambio, las herramientas de ETL no toman ventaja de configuraciones de disco (RAID) ni de la distribución de la memoria y procesador. También hacen transformaciones temporales y en muchos casos redundantes.

**ELTL**

La variante **ELTL** hace uso de un nuevo elemento, las **_staging area_** (o _landing zone_), espacios temporales de almacenamiento en los que realizar las transformaciones antes de cargar los datos definitivamente en las base de datos de destino.

## ¿Cuál utilizar?

Cada herramienta tiene sus propias ventajas e inconvenientes. Algunas proporcionan mayor facilidad para desarrollar una transformación, aunque el rendimiento no sea el más óptimo. En otras ocasiones sucede al contrario.

En la práctica es importante estar informado y conocer el alcance de los recursos disponibles para poder tomar decisiones correctas y obtener el mejor rendimiento.

Por tanto, no existe a priori un proceso mejor que otro, el resultado final de ambos conceptos es el mismo, la diferencia radica en el rendimiento que se obtiene de la aplicación en cada caso.

La aplicación de un procedimiento u otro en un proyecto determinado dependerá de factores diversos como la complejidad, el volumen de datos, el tiempo de creación, el tiempo de servicio previsto, etc.

# Referencias y más información

- [ETL vs ELT](https://aprendebi.wordpress.com/2017/05/25/etl-vs-elt/)
- [¿ETL o E-LT? ](https://gravitar.biz/bi/etl-elt/)
- [¿Procesos ETL o ELT? 2 ventajas de E-LT sobre ETL](https://blog.powerdata.es/el-valor-de-la-gestion-de-datos/bid/289596/procesos-etl-o-elt-2-ventajas-de-e-lt-sobre-etl)

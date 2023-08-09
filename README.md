# csv_to_mysql_ILS
Migration from csv kaggel bbdd Iowa_Liquor_Sales to mysql bbdd using python (mysql.connector and chunksize)

En este proyecto se desarrolló un procedimiento en python para mover los datos desde un archivo csv de la página kaggel 
llamado Iowa_Liquor_Sales el cual tiene un tamaño de 3.3Gb y 13359716 filas hacia una base de datos mysql, para esto 
se utilizó el paquete de pyhton mysql.connector y la función chunksize del paquete pandas. También se incluye la creación
de una Database y de una Datatable en mysql.

Desafíos para destacar:
1) los tipos de datos int32 y float64 de un dataframe no son compatibles con la base de datos mysql por lo que se
debe pasar la fila del dataframe a una lista y ahí realizar la conversión a los tipos de datos nativos de python
int o float.

desarrollado en:
python 3.11
mysql 8.0.34

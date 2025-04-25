# CoinGecko
Challenge Konfio

Este código utiliza Apache Iceberg para el almacenamiento de datos, por lo que será necesario tenerlo instalado previamente.

1. Se instalan las librerías necesarias que se utilizaran dentro del código, en caso de tenerlas sólo enviara un mensaje que ya cuenta con la correspondiente.
2. Se crea la sesión de Spark con los parámetros necesarios para utilizar Iceberg
3. Se creo una cuenta demo para obtener datos de CoinGecko API, a través de un request con el método get, se trae una lista de CryptoCurrencies
4. La respuesta se guarda en un archivo JSON
5. Se crea un dataframe a partir del JSON creado, se visualiza la información y se verifica que coincidan las cifras del JSON vs Dataframe
6. Se almacena la información dentro de una tabla en Iceberg llamada AllCrytoCurrencies
7. Se obtiene el id que corresponde a la criptomoneda Bitcoin
8. Se obtiene el precio del Bitcoin en dolares del último cuatrimestre del 2024 (1 de septiembre 2024 - 31 de diciembre de 2024)
9. La respuesta se guarda en un archivo JSON
10. Se modifica la fecha para cambiarla de UNIX Timestamp a formato convencional
11. Se visualiza la información para verificar que se encuentra correcta
12. Se crea un dataframe a partir del JSON creado, se visualiza la información y se verifica que coincidan las cifras del JSON vs Dataframe
13. Se almacena la información dentro de una tabla en Iceberg llamada BitCoinsLastQ2024
14. Se usa la función window para obtener la media móvil de 5 días de los datos obtenidos
15. Se realiza un gráfico con dicha información, haciendo el cambio a un pandas dataframe aprovechando que son pocos datos, a través matplotlib 

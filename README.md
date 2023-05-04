Instrucciones de Despliegue
1.	Descargar el proyecto .zip o clonar desde git: 
https://github.com/jorg3lui5/test-prices.git

2.	Ejecutar scripts de base de datos en caso de que no estén creadas las tablas. El archivo con los scripts tiene el nombre: BaseDatos.sql. Los datos de conexión se encuentran en el archivo properties del proyecto.

3.	Contar con la versión de Gradle 7.4.2

4.	Tener java versión 11.

5.	Ejecutar la aplicación con IntelliJ IDEA u otro framework

6.	Compilar con el comando: gradle clean build

Nota: se ejecuta con la Main Class: com.test.demo.OpenAPI2SpringBoot

- Además existe un archivo Dockerfile en la carpeta raíz del proyecto en caso de querer ejecutarlo con DockerFile.

Consumo de servicios
- Para el consumo de servicios se tiene el contrato Open Api, donde se puede consumir dicho servicis. Estos archivos tienen los nombres openapi.yaml o openapi.json

La ruta base de los servicios son: 
- http://localhost:8080/v1/test/

CASOS DE PRUEBA

Curls para los 4 casos de prueba:

- Caso de prueba 1:
curl --location 'http://localhost:8080/v1/test/prices/35455?date=2020-06-14T10%3A00%3A00Z&brandId=1' \
--header 'accept: application/json;charset=UTF-8'

- Caso de prueba 2:
curl --location 'http://localhost:8080/v1/test/prices/35455?date=2020-06-14T16%3A00%3A00Z&brandId=1' \
--header 'accept: application/json;charset=UTF-8'

- Caso de prueba 3:
curl --location 'http://localhost:8080/v1/test/prices/35455?date=2020-06-14T21%3A00%3A00Z&brandId=1' \
--header 'accept: application/json;charset=UTF-8'

- Caso de prueba 4:
curl --location 'http://localhost:8080/v1/test/prices/35455?date=2020-06-15T10%3A00%3A00Z&brandId=1' \
--header 'accept: application/json;charset=UTF-8'

- Caso de prueba 5: 
curl --location 'http://localhost:8080/v1/test/prices/35455?date=2020-06-15T21%3A00%3A00Z&brandId=1' \
--header 'accept: application/json;charset=UTF-8'


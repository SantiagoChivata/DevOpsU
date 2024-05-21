> [!IMPORTANT]
> Para construir la imagen con el archivo Dockerfile se debe ingresar a la carpeta billingApp y ejecutar el siguiente comando  en la consola: ```docker build -t billingapp --no-cache --build-arg JAR_FILE=target/*.jar . ```
>
> Para crear el contenedor de la aplicacion se debe ingresar el siguiente comando en la consola: ``` docker run -d -p 80:80 -p 7080:7080 --name localbillingApp billingapp ```
>
> Para publicar esta imagen en un registry como docker hub (teniendo una cuenta ya creada), debemos etiquetar la imagen con el siguiente comando ```docker tag billingapp santiagochivata/billingapp``` y luego realizar el push hacia docker hub con el siguiente comando ```docker push santiagochivata/billingapp``` en la consola.
esto nos publicara la imagen en la siguiente URL: https://hub.docker.com/repositories/santiagochivata 
>
> Para descargar la imagen que ya tenemos en docker hub ingresamos el siguiente comando en la consola ```docker pull santiagochivata/billingapp:latest```
> Para crear un contenedor a partir de esta imagen ingresamos el siguiiente comando en la consola ```docker run -d -p 80:80 -p 7080:7080 --name localbillingApp santiagochivata/billingapp:latest```
# DevOps de manera práctica con Docker, Pipelines, Jenkins, Orquestar servicios en kubernetes

Este curso es 100% práctico hands-on, donde se aporende todo sobre DevOps, Docker, Jenkins y kubernetes desde cero hasta un nivel profesional.
La aplicacion con la que se realiza la practica la brinta el profesor sotobotero a traves de su curso en Udemy "DevOps con Docker, Jenkins, Kubernetes, git, GitFlow CI y CD"


> [!NOTE]
> Secciones vistas:
> - Seccion 1 : Docker
>   * Crear un contenedor con Docklerfile
>
> [!IMPORTANT]
> para construir la imagen con el archivo Dockerfile se debe ingresar a la carpeta billingApp y ejecutar el siguiente comando  en la consola: ```docker build -t billingapp --no-cache --build-arg JAR_FILE=target/*.jar . ```
>
> para crear el contenedor de la aplicacion se debe ingresar el siguiente comando en la consola: ``` docker run -d -p 80:80 -p 7080:7080 --name localbillingApp billingapp ```
>
> para publicar esta imagen en un registry como docker hub (teniendo una cuenta ya creada), debemos etiquetar la imagen con el siguiente comando ```docker tag billingapp santiagochivata/billingapp``` y luego realizar el push hacia docker hub con el siguiente comando ```docker tag billingapp santiagochivata/billingapp``` en la consola.
esto nos publicara la imagen en la siguiente URL: https://hub.docker.com/repositories/santiagochivata 


Sigue Adelante DevOps!!
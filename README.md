# Desarrollo de una API con el Frameword springboot
## Propiedades de la Aplicación
- `aplication.properties, application.yml` o linea  de comado: Este archivo nos permite gestionar la cnfiguración que tiene el proyecto, por ejeplo mdificar el puerto por donde se ejecuta o el content path de nuestra aplicación
- Posibilidad de añadir propiedades propias como varaible para la configuración
- Gestión de perfiles segun el tipo de despligue, de acuerdo al entorno donde se encuentra nuestro proyecto, podemos crear un perfil que se ejecuta en tiempo de desarrollo y otro perfil que se enfoque en tiempo de producción
    - Para agregar el path del proyecto
        `server.servlet.context-path=/platz-market/api`
    - En archivo `application.property` indicamos con que perfil podemos trabajar utilizando la siguiente instrucción
        `spring.profiles.active=dev`, es decir la palabra que está después del guion 
## Estructura arquitectónica de nuestra aplicación

Es por capas orientada al dominio
- `La primera Capa es la de Dominio` en donde vamos a tener `DTO y objetos de dominios` hacen parte del contexto de nuestra aplicación es decir hacen parte del contexto de un supermercado. Vamos a tener los `servicios` van ha servir de puentes entre los controladores de la API y la capa de persistencia o el repositorio es quien interviene con la base de datos. Tambien vamos a tener la `Específicación de Repositorios` son intefaces o contratatos que debe cumplir la persistencia para intervenir los objetos de dominio y la base de datos
- `La Segunda capa es la WEB`, vamos a tener los controladores de nuestra API 
- Por último vamos a tener la `capa de persistencia` es la que interactúa con la BD

     ![Estructura del proyecto](img/estructura_proyecto.png) 


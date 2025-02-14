# Arquitecturas de Servidores de Aplicaciones, Meta protocolos de objetos, Patrón IoC, Reflexión 💯

En este taller se realizó la contrucción de un servidor Web, tipo apache en java, el cual es capaz de entrregar páginas HTML e imagenes tipo PNG.


## Descripción de la aplicación 📖

La aplicación es un microframework en Java que configura y ejecuta un servidor HTTP simple. Este microframework proporciona una forma sencilla de configurar y ejecutar un servidor HTTP con rutas básicas y soporte para archivos estáticos.

La aplicación es ideal para comprender los fundamentos del desarrollo de frameworks web para servicios REST, permitiendo manejar parámetros de consulta, definir servicios REST y gestionar archivos estáticos.

## Diagrama de Arquitectura 📊

* Usuario (User):

Es quien realiza solicitudes HTTP a través de un navegador web.
* Navegador (Browser):

Actúa como intermediario entre el usuario y el servidor HTTP.
Realiza solicitudes HTTP al servidor en busca de recursos como archivos HTML, JavaScript, CSS o imágenes.
* Servidor HTTP (HttpServer):

Es el servidor que recibe y procesa las solicitudes HTTP enviadas por el navegador.
Se encuentra dentro de un "grupo genérico", lo que indica que puede formar parte de una infraestructura más amplia.

El navegador envía varias solicitudes HTTP al servidor en el puerto 35000 para diferentes rutas:

* /script.js: Solicitud para obtener un archivo de JavaScript.
* /index.html: Solicitud para cargar el archivo principal de la página web.
* /estilos.css: Solicitud para cargar el archivo de estilos CSS.
* /Imagen/Chill.jpg: Solicitud para obtener una imagen ubicada en una ruta específica.
* Recursos (Archivos estáticos): Almacenados en el servidor, servidos a través de rutas específicas.
* Comunicación: Protocolo HTTP entre el cliente y el servidor.

El servidor procesa estas solicitudes y responde con los recursos correspondientes desde su sistema de archivos.

* Servidor HTTP: Clase HttpServer que maneja solicitudes HTTP.
* Manejo de rutas: Clase Route para mapear rutas específicas a manejadores.
* Clases de soporte:
* Request y Response para manejar y estructurar las solicitudes y respuestas.
* Utils con funciones auxiliares
* Archivos estáticos: Recursos en la carpeta resources/Files (HTML, CSS, imágenes, etc.).
* API REST: Endpoints definidos en HttpServer para manejar /api/saludo, /api/fecha, etc.
* Pruebas: Clases de prueba con JUnit para validar el comportamiento del servidor.

![image](https://github.com/user-attachments/assets/ee3336ae-1ca3-40f2-883f-e43ccb439cce)

## Diagrama de Clase 📊

Este diagrama de clases representa la arquitectura de un microframework para servicios REST, dividiendo la funcionalidad en varias clases e interfaces.

Las clases principales (Request, Response, HttpServer) manejan las solicitudes, respuestas y la lógica del servidor, mientras que las interfaces (Route) definen cómo implementar rutas personalizadas.

![image](https://github.com/user-attachments/assets/3416f27c-f056-4eaf-b48e-11aa1c23078c)


## Comenzando 🚀

Las siguientes instrucciones le permitirán obtener una copia del proyecto en funcionamiento en su máquina local para fines de desarrollo y prueba.

### Tecnologías usadas ⚙️

* [Maven](https://maven.apache.org/) : Gestor de dependencias y automatización de construcción para Java.
* [JavaScript](https://nodejs.org/) : Lenguaje de programación para interactividad en la web.
* [Java](https://www.java.com/es/) : Lenguaje de programación robusto para backend y aplicaciones empresariales.
* [html](https://developer.mozilla.org/es/docs/Web/HTML) : Lenguaje de programación que define la estructura de las páginas web

```
* Versión Maven: 3.9.9
* Versión Java: 21
```

### Instalación 📦

Realice los siguientes pasos para clonar el proyecto en su máquina local.

```
git clone https://github.com/Pau993/Taller03.git
cd Taller03
git checkout Taller03
mvn clean compile
```

### Ejecutando la aplicación ⚙️

Para ejecutar la aplicación, ejecute el siguiente comando:

```
mvn exec:java -Dexec.mainClass="com.example.HttpServer"

```
El anterior comando limpiará las contrucciones previas, compilará y empaquetará el código en un jar y luego ejecutará la aplicación.

## Ver la Aplicación: 💿

Diríjase a http://localhost:35000/ en su navegador para ver la aplicación en funcionamiento

## Ejecutando las pruebas ⚙️

Para ejecutar las pruebas, ejecute el siguiente comando:

Las pruebas realizadas en este proyecto se enfocan en la validación y verificación de requisitos relacionados con el proceso de gestión de solicitudes, asegurando su correcto funcionamiento y cumplimiento de especificaciones.

```
mvn test
```
![image](https://github.com/user-attachments/assets/acc5fdc4-897f-492d-96b2-7de303b742da)

## Descripción de las pruebas ✏️

* testHandleApiRequestSaludo 🛠️

Verifica que la solicitud a la ruta /api/saludo responde con HTTP 200 OK y contiene el mensaje JSON esperado.
* testHandleApiRequestFecha 📅

Valida que la solicitud a /api/fecha devuelve HTTP 200 OK y contiene una clave "fecha" en la respuesta.
* testHandleApiRequestNotFound ❌

Comprueba que una ruta inexistente, como /api/desconocido, devuelve HTTP 404 Not Found.
* testHandleApiPostRequest 📤

Evalúa que una solicitud POST a /api/enviar con un cuerpo JSON sea procesada correctamente y responda con HTTP 200 OK y el mensaje

* testHandleApiRequestHello ✏️

Esta prueba verifica que el servidor HTTP maneje correctamente una solicitud a la ruta "/api/hello".

* testHandleApiRequestPi ✏️

Esta prueba verifica que la solicitud al método greeting del controlador GreetingController con un parámetro name devuelve un saludo personalizado.

* testHandleApiRequestGreeting ✏️

Estas pruebas aseguran que los métodos del controlador GreetingController están devolviendo las respuestas correctas cuando se les pasa un parámetro específico.

## Características principales: ⚙️

1. Interfaz moderna y responsiva: 💎

* Interfaz Moderna y Responsiva:
* Diseño minimalista con un esquema de colores sofisticado.
* Adaptable a diferentes dispositivos gracias a su diseño responsivo.
* Gestión de Archivos:
* Botones interactivos para abrir y visualizar archivos clave como JavaScript, CSS, HTML e imágenes.

2. Gestión de archivos: ⚙️

* Incluye botones interactivos que permiten abrir y visualizar archivos clave como:
* Archivos JavaScript (script.js).
* Hojas de estilo CSS (estilos.css).
* Documentos HTML (index.html).
* Imágenes (Chill.jpg).

# Muestra de la aplicación 🧩

https://github.com/user-attachments/assets/228f71e7-3696-413b-8d8a-b19b412c0104

## Autores ✒️

*Paula Natalia Paez Vega* - *Initial work* - [Paulinguis993](https://github.com/Paulinguis993)

## Licencia 📄

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Agradecimientos 🎁

Agradecimientos al profeso Daniel Benavides por brindarme sus conocimientos.

## Arquitectura y organización de carpetas en symfony

La arquitectura de un proyecto Symfony se basa en el patrón de diseño Modelo-Vista-Controlador (MVC), que separa la lógica de la aplicación en tres componentes:

- Modelo: Representa la lógica de negocio y los datos. En Symfony, las entidades y los repositorios dentro de la carpeta src/Entity y src/Repository manejan esta parte.
- Vista: Es la capa de presentación y se encarga de mostrar los datos al usuario. Las plantillas Twig en la carpeta templates se utilizan para definir cómo se presentan los datos.
- Controlador: Actúa como intermediario entre el Modelo y la Vista, procesando la entrada del usuario y llamando a los recursos necesarios. Los controladores se encuentran en src/Controller. 

La estructura de carpetas de un proyecto Symfony típico es la siguiente:

- bin/: Contiene los ejecutables de la aplicación.
- config/: Alberga todos los archivos de configuración.
- public/: Es el directorio raíz de la web y contiene el archivo index.php, que es el punto de entrada de la aplicación.
- src/: Incluye el código PHP de la aplicación, como controladores, servicios y entidades.
- templates/: Guarda las plantillas Twig para la capa de vista.
- tests/: Contiene las pruebas unitarias y funcionales.
- translations/: Almacena los archivos de traducción.
- var/: Incluye archivos generados como caché y logs.
- vendor/: Contiene las dependencias del proyecto gestionadas por Composer.
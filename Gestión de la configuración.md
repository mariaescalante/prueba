# Gestión de la configuración:
-  **Grupo de prácticas:** G5.54
-  **Repositorio:** https://github.com/gii-is-psg2/psg2-2223-g5-54

### Autores:
|Nombre |Correo|Fecha de nacimiento
|----------------|------------------------|-----------------------------|
|**Aguayo Orozco, Sergio**|seraguoro@alum.us.es |28/04/1999|
|**Calero López, Marina**|marcallop7@alum.us.es|05/06/2002|
|**Escalante Ramos, María**|marescram3@alum.us.es|26/09/2002|
|**Rodríguez Cordero, Javier**|javrodcor@gmail.com|25/06/2002|
|**Ruiz Jurado, Ismael**|ismruijur@alum.us.es|27/10/2002|


## Introducción:
Este informe describe detalladamente la gestión de la configuración que emplearemos para realizar homogeneamente el proyecto. Detallaremos información sobre los estándares usados para realizar los commits y la implementación de código, la organización del repositorio de GitHub, el versionado que utilizaremos y cómo estructuraremos las ramas para poder trabajar individualmente de forma organizada.

## Contenido:

### Coding Standards:
Con el fin de implementar toda la funcionalidad necesaria de forma uniforme, llevaremos a cabo las siguientes pautas:
- Se usará el inglés de forma exclusiva para nombrar variables, métodos...
- El código de cada clase se indentará con 1 tab.
- Se usarán las buenas prácticas para la nomenclatura definidas (ver bibliografía 1) 
- No se usarán más de 2 niveles de nesteado (if, for, etc).

### Commit message policies:
-   Se deberá separar el título del cuerpo por una línea vacía.
-   El título no podrá tener más de 50 caracteres.  
-   La primera letra tanto para el título como para el resumen deberá de estar en mayúscula.  
-   No se pondrá un punto al final de cada commit.  
-   Se escribirán todos los commits en inglés.
-   Limitar el resumen a 72 caracteres, si procede.
-   En el caso de que el commit que se va a realizar cierra una issue, se deberá de indicar al final del cuerpo la siguiente expresión:
	-   Fix #XX, donde XX designa el número de la issue que se desea cerrar.
-   En el resumen deberá indicar el qué y el por qué se ha hecho, no el cómo.

### Structure of repositories and default branches:
El repositorio seguirá la siguiente estructura:
-   Directorio raíz: sigue el formato estándar, donde se tiene la carpeta “src” para incluir todo el código de la aplicación, la carpeta “docs” para documentos como el actual y otros, y los archivos frecuentes en un proyecto como lo son “readme.md”, “pom.xml”, entre otros.
    
-   Directorio “src”: Se tiene la carpeta “main”, donde se encuentra toda la parte relacionada con el desarrollo, y la carpeta “test”, donde se hallan los archivos necesarios para realizar las pruebas necesarias para la aplicación.
    
	-   Directorio “main”: Contiene las siguientes carpetas:
	-   ”appengine”: Contiene lo necesario para desplegar la aplicación    
	-   [java/org/springframework/samples/petclinic](https://github.com/gii-is-psg2/psg2-2223-g5-54/tree/main/src/main/java/org/springframework/samples/petclinic): Contiene el código fuente de la aplicación agrupado por entidades, además del inicializador de la aplicación.
	-   ”less”: Contiene los archivos .css para dar estilos a la página web.
	-   ”resources”: Contiene recursos usados por el código como código sql, imágenes, etc.   
	-   ”webapp/WEB-INF”: Contiene las vistas jsp que determinan qué se muestra en la página web.
-   Directorio “test”: Contiene los test agrupados por entidad en [java/org/springframework/samples/petclinic](https://github.com/gii-is-psg2/psg2-2223-g5-54/tree/main/src/main/java/org/springframework/samples/petclinic).

Por otro lado, el repositorio consta de dos ramas por defecto, la rama “main” para realizar el despliegue, y la rama “develop”, en la que se van añadiendo las diferentes implementaciones.

### Branching strategy, based on Git Flow and including peer reviews:
-   Feature: se creará una rama por cada funcionalidad a implementar, con un nombre dado por “feature/” seguido del número de la tarea en GitHub asociada a esa funcionalidad, junto con una palabra que proporcione una idea de qué trata esta. Por ejemplo, en caso de estar implementando una funcionalidad que permite borrar objetos de dominio, se creará una rama con nombre “feature/xx-delete” donde xx sea el número de la tarea en GitHub. 
Una vez el desarrollador acabe con la funcionalidad a implementar, realizará un push a la rama de esta feature, donde podrá crear una pull request. Esta pull request deberá ser examinada por uno o más revisores, que darán el visto bueno en caso de que proceda o comentarán los cambios a realizar por el desarrollador. Una vez la pull request sea aceptada, el desarrollador realizará un merge a la rama principal.

-   Release: esta rama será creada cuando se obtenga una rama developer estable y completa de una versión. El nombre de la rama será “release/xx” donde xx sea la versión a la que pertenece. En esta rama se podrá corregir algún fallo pequeño.

-   Hot-fix: ramas que parten de master y que nos permitirán corregir fallos.

### Versioning policies:
Respecto al versionado del proyecto, se agruparán los commits según lo siguiente:
-   Versión mayor: primer dígito, cambiaremos las versiones con cada entregable del proyecto, puesto que supondrán un gran cambio respecto a la versión entregada en el entregable anterior. Para el primer entregable, asignaremos la versión 1.0.0 al proyecto. Para realizar el segundo entregable obtendremos la versión 2.0.0 del proyecto y así ocurrirá con las sucesivas entregas.

-   Versión menor: segundo dígito, hará referencia a cambios menos significativos de cada entregable de forma que hasta que realicemos el segundo entregable los posibles versionados de la aplicación serán: 1.1.0, 1.2.0, 1.3.0, 1.4.0, etc… Cuando la versión mayor cambie, la versión menor se resetea a 0.

-   Patch: último dígito del versionado, hace referencia a arreglos de fallos, no rompe la compatibilidad. Cuando la versión menor cambie, el patch se resetea a 0.

## Conclusiones:
Utilizando la metodología de gestión de la configuración descrita en este informe.

## Bibliografía:
-   GitHub: [https://github.com/gii-is-psg2/psg2-2223-g5-54](https://github.com/gii-is-psg2/psg2-2223-g5-54)
-   Enseñanza virtual de la Universidad de Sevilla: [https://ev.us.es](https://ev.us.es)

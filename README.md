Harramienta maven


Apache Maven es una herramienta de gestión de proyectos que se utiliza principalmente para simplificar y automatizar el proceso de construcción de software en Java. Su mayor utilidad radica en gestionar las dependencias de un proyecto, manejar el ciclo de vida de construcción, y administrar los plugins necesarios para tareas específicas.

Las fases de maven son:

compile: Genera los archivos .class, compilando las fuentes .java. No termina este en caso de que en algún .class haya un error.

test: Ejecuta los test automáticos de JUnit existentes, abortando el proceso si alguno de ellos falla.

package: Genera el .jar con los .class compilados.

install: Copia los .jar a un directorio en nuestro ordenador, permitiendo que este se pueda usar en otros proyectos maven en la misma máquina.

deploy: Ubica una copia del .jar a un servidor remoto, permitiendo el acceso a este a cualquier otro proyecto maven que tenga acceso a ese servidor.

El ciclo de vida de construcción de Maven consiste en tres etapas: pre-compilación, compilación y post-compilación.

Los plugins en Maven sirven para extender sus capacidades y ejecutar tareas adicionales durante el ciclo de vida del proyecto, como la generación de documentación, pruebas unitarias, o despliegue en un servidor.

El repositorio central de Maven es un repositorio en línea que almacena bibliotecas y componentes de software reutilizables, permitiendo a los desarrolladores acceder y descargar dependencias para sus proyectos de manera fácil y rápida.

CREAR UN PROYECTO CON MAVEN

Para poder crear un proyecto en maven con arquetipos es necesario:

mvn archetype:generate -Dfilter=maven-archetype-quickstart 

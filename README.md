# CVDS - LAB02

## Herramienta maven


Apache Maven es una herramienta de gestión de proyectos que se utiliza principalmente para simplificar y automatizar el proceso de construcción de software en Java. Su mayor utilidad radica en gestionar las dependencias de un proyecto, manejar el ciclo de vida de construcción, y administrar los plugins necesarios para tareas específicas.

## Fases de Maven

Las fases de maven son:

1. Compile: Genera los archivos .class, compilando las fuentes .java. No termina este en caso de que en algún .class haya un error.

2. Test: Ejecuta los test automáticos de JUnit existentes, abortando el proceso si alguno de ellos falla.

3. Package: Genera el .jar con los .class compilados.

4. Install: Copia los .jar a un directorio en nuestro ordenador, permitiendo que este se pueda usar en otros proyectos maven en la misma máquina.

5. Deploy: Ubica una copia del .jar a un servidor remoto, permitiendo el acceso a este a cualquier otro proyecto maven que tenga acceso a ese servidor.

## Ciclo de Vida de Construcción

El ciclo de vida de construcción de Maven consiste en tres etapas: pre-compilación, compilación y post-compilación.

## Plugins en Maven

Los plugins en Maven sirven para extender sus capacidades y ejecutar tareas adicionales durante el ciclo de vida del proyecto, como la generación de documentación, pruebas unitarias, o despliegue en un servidor.

## Repositorio Central de Maven

El repositorio central de Maven es un repositorio en línea que almacena bibliotecas y componentes de software reutilizables, permitiendo a los desarrolladores acceder y descargar dependencias para sus proyectos de manera fácil y rápida.

## CREAR UN PROYECTO CON MAVEN

Para poder crear un proyecto en maven con arquetipos es necesario el siguiete codigo:

```bash
mvn archetype:generate -Dfilter=maven-archetype-quickstart
```
Esto nos generará un proyecto de manera interactiva, lo que después nos solicitará:
* Grupo
* Id del artefacto
* Versión
* Paquete

![image](https://github.com/Santiago0108/LAB2/assets/128636125/43f94a89-65ff-451a-860d-85b04fd2059c)

![image](https://github.com/Santiago0108/LAB2/assets/128636125/78dbe970-2585-4f6b-9c42-19d6a2a4a5b0)

Si nos dirigimos a la carpeta Patterns y escribimos el comando tree,nos mostrara todos los archivos creados por maven:

```bash
tree
```

![image](https://github.com/Santiago0108/LAB2/assets/128636125/133df619-02f2-45d4-931c-fe580faa1051)

## AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO

Modificamos el Pom.xml

![image](https://github.com/Santiago0108/LAB2/assets/128636125/87b1b873-c481-4c91-b661-96871e33a0ab)

## COMPILAR Y EJECUTAR

Para compilar ejecutamos el comando:

```bash
$ mvn package
```

![image](https://github.com/Santiago0108/LAB2/assets/128636125/6e46838c-7e86-4c0b-9267-3c302f387431)

- Busque cuál es el objetivo del parámetro "package" y qué otros parámetros se podrían enviar al comando mvn.
  - El parámetro "package" en el comando Maven (mvn) se utiliza para ejecutar una fase específica del ciclo de vida de construcción de un proyecto Maven. En particular, la fase "package" se encarga de empaquetar el proyecto compilado en un formato específico, como JAR (para proyectos Java), WAR (para proyectos web) o cualquier otro formato de distribución que haya sido configurado en el proyecto.
- Busque cómo ejecutar desde línea de comandos, un proyecto maven y verifique la salida cuando se ejecuta con la clase App.java como parámetro en "mainClass"
  - Para ejecutar el proyecto debe ejecutar el siguiente comando:
    ```bash
    mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.archetype.App"
    ```
- Realice el cambio en la clase App.java para crear un saludo personalizado, basado en los parámetros de entrada a la aplicación.

    ![image](https://github.com/Santiago0108/LAB2/assets/128636125/4638f848-8204-4061-961b-f5f15f2544e0)

    Hicimos estos cambios 

    ![image](https://github.com/Santiago0108/LAB2/assets/128636125/5472b710-f60f-4adf-8c20-e0f4e9ec292a)

    Y aparece esto al hacer la prueba

    ![image](https://github.com/Santiago0108/LAB2/assets/128636125/2f410413-0eb5-42b7-9789-bdaed4f52e15)
  - Ejecutar la clase con su nombre y apellido como parámetro. ¿Qué sucedió?

    ![image](https://github.com/Santiago0108/LAB2/assets/128636125/ae0cd14f-5e8b-46e8-a3d2-36e426cf1604)

## HACER EL ESQUELETO DE LA APLICACIÓN

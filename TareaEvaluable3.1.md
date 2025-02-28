# TE3.1 - Configuración de Eclipse y JetBrains IntelliJ IDEA

En esta tarea de aprendizaje, aprenderás a instalar el JDK y JREs en Windows y Linux, y a configurar Eclipse y JetBrains IntelliJ IDEA.

## Recursos

- [Instalación del JDK en Linux](https://docs.oracle.com/javase/8/docs/technotes/guides/install/linux_jdk.html)
- [Instalación del JDK en Windows](https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html)

### Objetivos

- Conocer cómo instalar el JDK/JRE en Windows y Linux.
- Conocer cómo configurar Eclipse y JetBrains IntelliJ IDEA para utilizar un JDK.
- Conocer cómo configurar Windows y Linux a nivel de sistema para utilizar diferentes versiones de Java.
- Conocer cómo instalar y usar la herramienta SDKMan para instalar diferentes versiones de Java en Linux/MacOS/Windows.

### Recursos

**GIF Videos**

- [Software crear GIFs animados para Windows](https://www.screentogif.com/)
- [Software crear GIFs animados para Linux](https://github.com/phw/peek)
- [Herramienta Online GIF](https://ezgif.com/video-to-gif)

### Entrega

El documento justificativo de la realización de la tarea se realizará en formato `Markdown`, el nombre del fichero será `readme.md` y estará dentro de la carpeta `UT3\TE3.1` dentro del repositorio oficial del alumno para la asignatura.

El fichero `readme.md` debe contener los siguientes apartados:

- Cada uno de los puntos de la tarea.

### 1. Configuración de Java en Windows y Linux

1. Revisa la configuración de tu máquina a través del terminal e indica la versión de Java que tienes instalada.

```bash
# Comprueba la versión de Java instalada
$> java -version
# Comprueba donde está instalado Java
$> where java
# Busca todas las versiones de Java instaladas
$> which java
```

📎 _Adjunta una imagen de los comandos anteriores y responde a las siguientes preguntas_


![Foto.1](Foto.1.png)


    ¿Qué versión de Java tienes instalada?

     ```bash

     Tengo instalada la versión de Java "21.0.5" del 15 de octubre de 2024, que es una versión LTS (Long-Term Support).

      ```

    ¿Cuantas versiones de Java tienes instaladas? ¿ Por qué?

       ```bash

     En este momento, solo tengo una versión de Java instalada en mi máquina. La razón es que no he necesitado múltiples versiones para mis proyectos actuales.
     
      ```

    Si tienes más de una versión indica todas las versiones y rutas de instalación.

    ```bash

     En este caso, solo tengo una versión de Java instalada, ubicada en la ruta /usr/bin/java.

      ```

2. Variables de entorno.

   📎 _Adjunta una imagen de las variables de entorno de tu sistema, tanto a nivel de usuario como a nivel de sistema._

   - Muestra a través de interfaz (Ventana de windows) (Usuarios y sistema) [adjuntar imagen]

     ![Foto.2(1)](Foto.2(1).png)

   - Muestra a nvel de comandos (Solo usuario) (`set`) [adjuntar imagen]

       
       ![Foto.2(2)](Foto.2(2).png)


   - Muestra el contenido de la variable `PATH` (`echo %PATH%`) y de la variable `JAVA_HOME` (`echo %JAVA_HOME%`)

3. Instala el JDK 19 la implementación de Adoptium (Windows)

   - Ves a la página de [Adoptium](https://adoptium.net/) y descarga la versión de Java 19 para Windows y la arquitectura de tu PC (x32/x64).
     (Incluye un gif de la instalación)

         ![Foto.3(1)](Foto.3(1).png)
         ![Foto.3(2)](Foto.3(2).png)

   - Una vez instalado, muestra la versión de Java instalada y la ruta de instalación. (a través de comandos y adjunta una imagen)
     (`java -version` y `where java`)

         ![Foto.3(3)](Foto.3(3).png)

   - ¿ La versión de Java que te muestra es la 19? ¿ Por qué?

    ```bash

     La razón por la cual se muestra la versión 19 de Java después de la instalación es porque acabo de instalar esa versión específica de Java, y la configuración e instalación se realizaron correctamente. Tres fotos hechas.

      ```

4. Configura tu sistema para que utilice la versión de Java 19 como versión por defecto a nivel de usuario. (Si ya lo tienes explica por qué)

   - ¿ Cómo has configurado tu sistema para que utilice la versión de Java 19 como versión por defecto?

### 2. Utilización de SDKMan

```bash

     * He configurado mi sistema para que utilice la versión de Java 19 como predeterminada a nivel de usuario siguiendo estos pasos:
* Definí la variable de entorno JAVA_HOME: Configuré la variable JAVA_HOME para que apunte a la ruta de instalación de Java 19:  /Library/Java/JavaVirtualMachines/temurin-19.jdk/Contents/Home
*    
* Actualicé la variable PATH: Añadí la ruta de JAVA_HOME/bin al inicio de mi variable PATH para garantizar que esta versión de Java tenga prioridad:  export PATH=$JAVA_HOME/bin:$PATH
*    
* Hice los cambios permanentes: Guardé estas configuraciones en el archivo ~/.zshrc (ya que uso el shell Zsh), para que se carguen automáticamente cada vez que inicie sesión.
* Verifiqué la configuración: Ejecuté los comandos java -version y echo $JAVA_HOME para confirmar que mi sistema utiliza Java 19 como la versión predeterminada. Los resultados son:  openjdk version "19.0.2" 2023-01-17
* OpenJDK Runtime Environment Temurin-19.0.2+7 (build 19.0.2+7)
* OpenJDK 64-Bit Server VM Temurin-19.0.2+7 (build 19.0.2+7, mixed mode)
* /Library/Java/JavaVirtualMachines/temurin-19.jdk/Contents/Home 

      ```

5. Instala SDKMan en Windows. (_Para ello puedes seguir la guía disponible [aquí](https://github.com/jssdocente/2425_EEDD_recursos/blob/main/UT3/docs/doc_sdkman.md)

   - Instala SDKMan en Windows e explica los pasos que has seguido, adjunta una captura final de SDK funcionando.

   ![Foto.5(1)](Foto.5(1).png)

   - Muestra la versión de SDKMan instalada

    ![Foto.5(2)](Foto.5(2).png)
     ![Foto.5(3)](Foto.5(3).png)

   - ¿ Dónde se ha instalado SDKMan? ¿ Por qué?

    ```bash

     SDKMAN se ha instalado en el directorio de usuario, específicamente en ~/.sdkman. Esta ubicación es ideal porque:
* No requiere permisos de administrador para modificar archivos del sistema.

      ```

   - Muestra las versiones de Java que tienes instaladas a través de SDKMan

   - ¿ Qué ventajas tiene instalar SDKMan?

   ```bash

    Usar SDKMAN trae consigo numerosas ventajas que hacen que trabajar con diferentes SDKs y lenguajes sea mucho más sencillo. Una de sus características más destacadas es la gestión de versiones, que permite instalar y alternar rápidamente entre distintas versiones de Java u otros SDKs, sin complicaciones. Además, su portabilidad lo convierte en una herramienta compatible con múltiples sistemas operativos, incluyendo macOS, Linux y Windows, lo que amplía considerablemente su alcance.
    
    Otro punto fuerte es la facilidad con la que maneja las actualizaciones. SDKMAN se encarga de gestionar este proceso de manera automática, sin que el usuario tenga que preocuparse por configuraciones adicionales. Finalmente, es ideal para proyectos que requieren versiones específicas, ya que permite cambiar dinámicamente de versión para un proyecto sin que esto afecte a otros. Esto asegura que cada entorno de trabajo esté perfectamente adaptado a las necesidades del desarrollo en curso.

      ```

   - ¿ Instala la versión de Jara 8.0_302-zulu a través de SDKMan ?

    ![Foto.5(4)](Foto.5(4).png)

   - ¿ Instala la versión de Java 11.0.12-zulu a través de SDKMan ?

   ![Foto.5(5)](Foto.5(5).png)

   - ¿ Instala la versión de Java 17.0.0-zulu a través de SDKMan ?

   ![Foto.5(6)](Foto.5(6).png)

6. Configura tu sistema para que utilice la versión de Java 17.0.0 como versión por defecto a nivel de usuario. (Para que las aplicaciones que ejecutes utilicen esta versión de Java)

   - ¿ Qué tienes hacer o comando tienes que utilizar (SDKMAN) para que una aplicación ejecutada desde la interfaz (Windows o Linux) utilize esa versión de Java?

   ```bash

     sdk default java 17.0.0-zulu

      ```

   - ¿ Qué variable de Entorno tienes que modificar para que una aplicación ejecutada desde la interfaz (Windows o Linux) utilize esa versión de Java?

    ```bash

   Debes modificar la variable de entorno JAVA_HOME para que apunte a la ruta donde está instalada la versión 17.0.0-zulu.

      ```

7. Si necesitas compilar una aplicación de Java desde la terminal, fuera del IDE, y necesita compilarse con la version de Java 8, ¿ Cómo lo harías?

 ```bash

   Primero, debes asegurarte de que la terminal esté utilizando la versión de Java 8. Esto se puede lograr con SDKMAN.

      ```

   - ¿ Qué comando de SDKMAN tienes que utilizar para que a nivel de la terminal actual use la versión de Java 8?

   ```bash

   sdk use java 8.0.302-zulu

      ```

   - ¿ Qué comando utilizas para compilar una aplicación de Java ?

    ```bash

  javac Main.java
   
      ```

8. Un proyecto en el que estas trabajando, neceseita la versión de Java 11, pero requieres compilarlo con esa versión, pero no quieres tener siempre que recordar esto, y quieres que se active automáticamente esa versión una vez accedas al directorio del proyecto.

   - ¿ Cómo puedes realizar esto con SDKMAN ? (indica los comandos que tienes que utilizar y la configuración de la herramienta)

   - Haz una captura de pantalla entrando y saliendo del directorio del proyecto, para ver cono se activa y desactiva una versión y otra de Java.

### 3. Utilización de JetBrains IntelliJ IDEA

10. Crea un nuevo proyecto en IntelliJ IDEA (TE21-Paso10) y configura en ese directorio, con SDKMAN para que utilize la versión de Java 11.

- Ahora al abrir IntellJ IDEA, debe activar esa versión automaticamente, pues detectar la configuración. (Incluye una captura de panntalla o GIF de la configuración))

11. Crea un nuevo proyecto en IntelliJ IDEA (TE21-Paso12) que se guarde en la carpeta TE21-Paso12.

- Configura el proyecto para que utilice la versión de Java 17 descargada con SDKMAN. (Muestra una captura de pantalla de la configuración del fichero .sdkmanrc)
- Agrega otro módulo al proyecto, que se guarde en la carpeta Modulo2.
- Agrega otro módulo al proyecto, que se guarde en la carpeta Modulo3.

(Muestra una captura de pantalla de la estructura del proyecto en IntelliJ IDEA)

- Vincula el proyecto principal, con los módulos 2 y 3. (Muestra una captura de pantalla de la configuración de los módulos)

12. En el módulo 2, crea una clase que se llame `Utilidades` y que tenga un método que se llame `calculadora` y que tenga los métodos de suma, resta, multiplicación y división.

(Muestra el código de la clase `Utilidades` con un bloque de código)

13. En el módulo 3, crea una clase llamada `Conversor` que tenga un método que se llame `Texto_to_Uppercase` que convierta un texto a mayúsculas, y otro método que se llame `Texto_to_Lowercase` que convierta un texto a minúsculas.

(Muestra el código de la clase `Conversor` con un bloque de código)

14. En el módulo principal, crea una clase llamada `Principal` que tenga un método `main` que instancie las clases `Utilidades` y `Conversor` y que muestre por consola el resultado de las operaciones de la clase `Utilidades` y el resultado de las operaciones de la clase `Conversor`.

(Muestra un gif donde se muestre la ejecución del programa, en depuración y se visualice que no existen errores de compilación ni ejecución).
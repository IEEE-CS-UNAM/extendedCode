# Práctica 1: Nociones en Git #
Como sabemos, GitHub tiene una gran presencia en la industria debido a su facilidad para gestionar versiones y mantener un orden en el trabajo que estamos realizando.

**Tomemos como ejemplo la siguiente situación**: estamos desarrollando una aplicación para una empresa, y constantemente nos solicitan cambios en el código. Sin embargo, ya hemos progresado significativamente en el proyecto. 
Recordar exactamente en qué punto nos quedamos puede ser complicado y, en algunas ocasiones, resulta imposible. Es en momentos como estos cuando GitHub entra en escena con su sistema de control de versiones, permitiéndonos regresar a la rama deseada (spoiler alert).

El objetivo de esta tarea es que aprendas las nociones básicas de GitHub, incluyendo la creación de una bifurcación (fork) de un repositorio, la creación de una rama local, y la realización de commits de manera efectiva. Sigue los pasos a continuación:

## 1. Bifurcar (*fork*) el Repositorio Principal

1. Abre tu navegador y ve al repositorio al repositorio `IEEE-CS-UNAM/extendedCode` que estamos utilizando para el proyecto: [Repositorio Actual](https://github.com/IEEE-CS-UNAM).

2. En la esquina superior derecha de la página del repositorio, haz clic en el botón "Fork" (Bifurcar). Esto creará una copia del repositorio en tu propia cuenta de GitHub.

Esto bifucará que nos podrá dar una copia del repositorio. Bifurcar un repositorio le permite experimentar libremente con los cambios sin afectar el proyecto original.

## 2. Clonar el Repositorio

La intención de clonar tu repositorio es llevar una copia del repositorio (el tuyo) a tu computadora, esto no es necesario si no deseas trabajar localmente pero es de mucha utilidad dadas las herramientas que tiene la terminal, además de que funciona en entornos más específicos.
Para hacer esto necesitas descargar *Git* en tu computadora [Git page](https://git-scm.com/downloads), la opción de decarga dependerá de tus sistema operativo, la versión la más reciente.
3. Una vez que hayas bifurcado el repositorio, ve a tu propia cuenta de GitHub y encontrarás la copia del repositorio bajo tu perfil.

4. Abre el repositorio bifurcado (tu copia) y copia la URL del repositorio (botón verde). Debería ser algo como: `https://github.com/tu-usuario/repositorio`.

5. Abre tu terminal o línea de comandos y ejecuta el siguiente comando, reemplazando `URL_DEL_REPOSITORIO` con la URL que copiaste en el paso anterior:

   ```shell
   git clone URL_DEL_REPOSITORIO

Esto descargará una copia del repositorio a tu máquina local.
3. Crear una Rama Local

    Navega al directorio del repositorio clonado utilizando el comando cd.

    Crea una nueva rama local utilizando el siguiente comando, reemplazando nombre-de-tu-rama con un nombre descriptivo para tu rama:

    shell

    git checkout -b nombre-de-tu-rama

4. Hacer Commits

    Abre un editor de texto o una herramienta de desarrollo y realiza cambios en los archivos del repositorio según sea necesario.

    Guarda los cambios y luego utiliza los siguientes comandos para realizar un commit. Los commits son una forma de registrar los cambios que has hecho en tu rama:

    shell

    git add .            # Agrega los cambios al área de preparación
    git commit -m "Mensaje descriptivo de tu commit"

    Asegúrate de proporcionar un mensaje descriptivo que explique qué cambios realizaste en este commit. Los mensajes de commit deben ser claros y concisos.

    Si necesitas realizar más cambios, repite los pasos 8 y 9 tantas veces como sea necesario.

5. Empujar Cambios a GitHub

    Una vez que hayas hecho tus commits en tu rama local, debes enviar esos cambios a tu repositorio en GitHub. Utiliza el siguiente comando:

    shell

    git push origin nombre-de-tu-rama

6. Crear una Pull Request

    Ve a la página de tu repositorio en GitHub y cambia a la rama que acabas de crear.

    Haz clic en el botón "New Pull Request" (Nueva Solicitud de Extracción).

    Asegúrate de que la base sea la rama principal del repositorio original (no tu copia) y la comparación sea tu rama recién creada.

    Proporciona una descripción clara de los cambios que has realizado y crea la Pull Request. Las Pull Requests son una forma de proponer tus cambios al dueño del repositorio original

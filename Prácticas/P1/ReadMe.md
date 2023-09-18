# Práctica 1: Nociones en Git y Github

Como sabemos, GitHub tiene una gran presencia en la industria debido a su facilidad para gestionar versiones y mantener un orden en el trabajo que estamos realizando.

**Tomemos como ejemplo la siguiente situación:** estamos desarrollando una aplicación para una empresa, y constantemente nos solicitan cambios en el código. Sin embargo, ya hemos progresado significativamente en el proyecto.

Recordar exactamente en qué punto nos quedamos puede ser complicado y, en algunas ocasiones, resulta imposible. Es en momentos como estos cuando GitHub entra en escena con su sistema de control de versiones, permitiéndonos regresar a la rama deseada (spoiler alert).

El objetivo de esta tarea es que aprendas las nociones básicas de GitHub, incluyendo la creación de una bifurcación (fork) de un repositorio, la creación de una rama local, y la realización de commits de manera efectiva. Sigue los pasos a continuación:

## 1. Bifurcar (*fork*) el Repositorio Principal

1. Abre tu navegador y ve al repositorio `IEEE-CS-UNAM/extendedCode` que estamos utilizando para el proyecto: [Repositorio Actual](https://github.com/IEEE-CS-UNAM).

2. En la esquina superior derecha de la página del repositorio, haz clic en el botón "Fork" (Bifurcar). Esto creará una copia del repositorio en tu propia cuenta de GitHub.

Esto bifurcará que nos podrá dar una copia del repositorio. Bifurcar un repositorio le permite experimentar libremente con los cambios sin afectar el proyecto original.

## 2. Clonar el Repositorio

La intención de clonar tu repositorio es llevar una copia del repositorio (el tuyo) a tu computadora, esto no es necesario si no deseas trabajar localmente pero es de mucha utilidad dadas las herramientas que tiene la terminal, además de que funciona en entornos más específicos.
Para hacer esto necesitas descargar *Git* en tu computadora [Git page](https://git-scm.com/downloads), la opción de decarga dependerá de tus sistema operativo, la versión la más reciente.
1. Una vez que hayas bifurcado el repositorio, ve a tu propia cuenta de GitHub y encontrarás la copia del repositorio bajo tu perfil.

2. Abre el repositorio bifurcado (tu copia) y copia la URL del repositorio (botón verde). Debería ser algo como: `https://github.com/tu-usuario/repositorio`.

3. Abre tu terminal o línea de comandos y ejecuta el siguiente comando, reemplazando `URL_DEL_REPOSITORIO` con la URL que copiaste en el paso anterior:

   ```shell
   git clone URL_DEL_REPOSITORIO
   ```
Ejemplo:
```shell
git clone https://github.com/ "Aquí va el nombre de tu repositorio" /extendedCode.git
```

Esto descargará una copia del repositorio a tu máquina local.
De manera predeterminada guardará el repositorio en la raíz principal y se encontrará con todos los otros repositorios que hayas descargado, con el comando:

```shell
cd extendedCode
```
Cambiaremos de directorio al de nuestro repositorio para poder trabajar en él.

## 3. Configuraciones

Nosotros (los humanos) sabemos que estamos bien cuando no nos sentimos mal, para Git la forma en la cuál saber si todo está bien es con

```shell
git status
```
Muestra el estado del directorio de trabajo y el área de preparación. Le permite ver qué cambios se han preparado, cuáles no y qué archivos no están siendo rastreados por Git. La salida de estado no muestra ninguna información sobre el historial del proyecto comprometido.

Git trae una herramienta llamada git config, que te permite obtener y establecer variables de configuración que controlan el aspecto y funcionamiento de Git.
En prácticas posteriores veremos los distintos tipos de almacenamiento para estás variables, con el comando `--global` Git escribirá específicamente en el usuario que estás trabajando.
Es importante que Git tenga datos mínimos para utilizar esto en los commits que hagas, está información será introducida de manera inmutable en los commits que envíes:

```shell
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```
## 4. ¿Hacer un "commit"?

Después de hacer un cambio, agregar un archivo o cualquier tipo de modificación tenemos que entregarlo. Para hacer esto es siguiendo 3 simples pasos:

```shell
git add
```
Sirve para especificar qué archivos quieres controlar, indica a Git que quieres incluir actualizaciones en un archivo concreto en la próxima confirmación.
Esta acción no afecta al repositorio de manera significativa, solo hasta que se hace un commit.

```shell
git commit
```
Sirve para confirmar una instantánea del directorio del entorno de ensayo en el historial de confirmaciones de los repositorios.
Es importante destacar que al estar comprometiendo cambios se tiene que indicar explícitamente qué se hizo y que los demás usuarios tengan una noción de qué cambio se comprometió.
Asegúrate de proporcionar un mensaje descriptivo que explique qué cambios realizaste en este commit. Los mensajes de commit deben ser claros y concisos.
Utilizando:

```shell
git commit -m "un mensaje cualquiera"
```
Ahora:

```shell
git push
```
Se emplea para enviar los cambios confirmados a repositorios remotos para colaborar. Esto permite a otros miembros del equipo acceder a un conjunto de cambios guardados.
Por lo tanto, una vez que hayas hecho tus commits en tu rama local, debes enviar esos cambios a tu repositorio en GitHub.

## 5. Pull Request

Por último, ya que hayamos comprometido la información, cómo tal los cambios que hiciste siguen estando en tu repositorio. Yo aún no sé qué se hizo y qué no, así que desde tu repositorio **"user"/extendedCode** te aparecerá que estás adelantado al repositorio central: "This branch is 1 commit ahead of unamfi/sistop-2024-1".
Haz clic en Pull request. GitHub te mostrará un resumen de las diferencias entre mi versión y la tuya, y si te parece correcta, te permite seleccionar el botón verde, **Create pull request**.
Las Pull Requests son una forma de proponer tus cambios al dueño del repositorio original.

## Y ahora, ¿Qué tengo que entregar?

Para dar cómo concluida tu práctica tienes que subir una carpeta siguiendo la estructura `ApellidoNombre` dönde en el archivo ReadMe pongas tu biografía hecha en la **Tarea 0** en el directorio `extendedCode/Integrantes/`, aquí subiremos información importante sobre ustedes y su colaboración en los proyectos.
Subir una foto en formato `.png` dónde se muestre su cara y su curriculum (en caso de no tener crear uno, entregar hasta que se tenga).

¡Eso sería todo!


# Guía de comandos Git

## ¿Qué es Git?

Git es un sistema de control de versiones que permite registrar los cambios realizados en los archivos de un proyecto, volver a versiones anteriores y trabajar en equipo.

## ¿Qué es GitHub?

GitHub es una plataforma en línea que permite alojar repositorios Git y compartir proyectos con otras personas.

## ¿Qué es Markdown?

Markdown es un lenguaje de marcado ligero que permite dar formato al texto mediante símbolos. Se utiliza para crear títulos, listas, enlaces, texto en **negrita** y otros elementos. GitHub utiliza Markdown para mostrar los archivos `README.md` con un formato organizado y fácil de leer.

## Comandos de Git

### 1. `git status`

Muestra el estado del repositorio. Permite saber qué archivos fueron modificados, cuáles son nuevos y cuáles están preparados para realizar un commit.

### 2. `git init`

Inicializa un repositorio Git en una carpeta. Crea la estructura interna que Git necesita para registrar los cambios del proyecto.

**¿Por qué puede ser catastrófico usarlo en un repositorio existente?**

Porque puede cambiar la configuración interna del repositorio, especialmente si se utiliza en una carpeta que ya contiene un repositorio. Esto puede causar problemas con la configuración, las referencias o el historial de Git si se usa incorrectamente. Por eso, antes de ejecutarlo, hay que comprobar si la carpeta ya es un repositorio.

### 3. `git add`

Agrega archivos nuevos o modificados al área de preparación (*staging area*), donde se seleccionan los cambios que se incluirán en el próximo commit.

Ejemplo:

`git add .`

Agrega al área de preparación los cambios del directorio actual y sus subdirectorios, respetando las reglas de exclusión de Git.

### 4. `git commit`

Guarda una versión de los cambios preparados en el historial del repositorio local.

Ejemplo:

`git commit -m "Actualizo README"`

El texto entre comillas es un mensaje que describe los cambios realizados.

### 5. `git log`

Muestra el historial de commits del repositorio, incluyendo información como el autor, la fecha, el identificador y el mensaje de cada commit.

### 6. `git push`

Envía los commits del repositorio local al repositorio remoto, por ejemplo, uno alojado en GitHub.

Ejemplo:

`git push`

Permite compartir los cambios realizados con otras personas que trabajan en el proyecto.

### 7. `git pull`

Descarga los cambios del repositorio remoto e intenta integrarlos en la rama local actual. Generalmente, realiza un `git fetch` seguido de una integración mediante *merge* o *rebase*, según la configuración.

**¿Por qué es importante usarlo al trabajar en equipo?**

Porque otras personas pueden haber subido cambios desde la última vez que actualizamos nuestro proyecto. Ejecutar `git pull` al comenzar a trabajar ayuda a mantener la copia local actualizada, evita trabajar con una versión desactualizada y reduce la posibilidad de conflictos al compartir cambios.

### 8. `git clone`

Crea una copia local de un repositorio remoto, descargando sus archivos y el historial de versiones.

Ejemplo:

`git clone https://github.com/usuario/mi-primer-repo.git`

Se utiliza normalmente para obtener un proyecto por primera vez.

## ¿Por qué el archivo se llama README.md?

El nombre `README` significa, en inglés, «léeme». Es un archivo que presenta información importante sobre un proyecto, como su propósito, instrucciones de uso y documentación.

La extensión `.md` significa Markdown. Esto permite que GitHub interprete el formato del archivo y muestre sus títulos, listas, enlaces y textos destacados de forma organizada en la página principal del repositorio.

Por ese motivo, `README.md` es el nombre habitual para el archivo de presentación de un proyecto.

## Conclusión

Git permite controlar las versiones de un proyecto y registrar sus cambios. GitHub permite alojar y compartir esos repositorios en línea. Comandos como `add`, `commit`, `push` y `pull` ayudan a organizar el trabajo y colaborar con otras personas de manera ordenada.

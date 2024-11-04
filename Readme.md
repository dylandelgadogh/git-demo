# Git Demo

**Descripción:**

El contenido está estructurado para cubrir conceptos clave sobre la herramienta Git para gestionar bases de código de manera eficaz y colaborar en entornos de equipo.

---

## 📝 Temas Cubiertos

1. **Introducción al Control de Versiones**: 
   - Comprensión del propósito y beneficios del control de versiones en el desarrollo de software.
2. **Introducción a Git**: 
   - Instalación de Git
   - Configuración de la información del usuario
3. **Comandos Básicos de Git**: 
   - Inicialización de un repositorio
   - Staging y commit de cambios
   - Visualización del historial y diferencias
4. **Branching y Merging**: 
   - Creación y cambio de ramas
   - Comprensión de los flujos de trabajo con ramas
   - Fusionar ramas y resolver conflictos
5. **Buenas Prácticas en Git**: 
   - Uso de `.gitignore`
   - Estrategias de branching

## 💻 Requisitos

- **Git**: Instalar Git [aquí](https://git-scm.com/downloads).
- **Cuenta de GitHub**: Crear una cuenta de GitHub.

## 🎯 Resultados de Aprendizaje

Al final de esta lección, serás capaz de:
- Usar Git para el control de versiones en tus proyectos.
- Navegar con confianza en los comandos básicos de Git.
- Implementar estrategias de branching y merging en Git.
- Colaborar eficazmente con otros en GitHub.

Te invito a revisar a mayor detalle los comandos de git en [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf).

---

# Introducción al control de versiones

Cada vez que se guarda una versión del proyecto (conocido como commit en Git), el sistema registra una "foto" del estado actual de los archivos junto con información sobre quién hizo el cambio, cuándo, y una descripción opcional de lo que se modificó.


Se facilita revertir errores, revisar el historial de cambios y colaborar de manera eficiente con otros desarrolladores.

<div>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJ1MWL23tZLyUn4MhkS7nFmr2EMe8L6zDp2-_GmwO5ioirZ-zqbaFPiHnxYJWX3Whto88&usqp=CAU" width=350 height=350>
</div>

---

# Introducción a Git

## Instalación de Git

 - La instalación del software se puede realizar a través de la página web https://git-scm.com/downloads

## Configuración de la información del usuario 

![Configuración Usuario](/images/config-usuario.png)

---

# Comandos básicos de Git

 - **Inicializar un nuevo repositorio**: Para empezar a utilizar el control de versiones de Git utiliza `git init` dentro del folder que se desee trackear.

  - **Clonar un repositorio**: Para obtener una copia local de un repositorio en GitLab, utiliza el comando `git clone` seguido de la URL del repositorio.

  - **Añadir y confirmar cambios**: Utiliza los comandos `git add` para añadir archivos y cambios al área de preparación, y `git commit` para confirmar los cambios con un mensaje descriptivo.

  - **Enviar cambios al repositorio remoto**: Utiliza el comando `git push` seguido de origin y el nombre de la rama para enviar los cambios confirmados al repositorio remoto en GitLab.

  - **Actualizar el repositorio local con los cambios remotos**: Utiliza el comando `git pull` para actualizar tu repositorio local con los cambios realizados por otros desarrolladores y enviados al repositorio remoto.

  - **Consultar el estado de la rama actual**: Utiliza el comando `git status` para revisar los archivos modificados, agregados o eliminados.

# Branching y merging

## Creación y cambio de ramas

- **Crear una rama**: Utiliza el comando `git branch` seguido del nombre de la nueva rama para crearla.
   - Ejemplo: `git branch feat/example-branch`

- **Listar ramas**: Utiliza el comando `git branch`seguido del flag `--all` o `-a` para listar las ramas del repositorio local y el repositorio remoto.

- **Saltar entre ramas**: Utiliza el comando `git checkout` seguido del nombre de la rama a la que se quiere "Saltar" (Cambiar).
   - Ejemplo: `git checkout feat/example-branch`

> [!TIP]
> El comando `git checkout` también puede ser utilizado para crear ramas. Para esto, se utiliza `git checkout` seguido del flag `-b`, seguido del nombre de la nueva rama.
> - Ejemplo: `git checkout -b feat/another-example-branch`

- **Borrar una rama**: Utiliza el comando `git branch`seguido del flag `--delete` o `-d`, seguido del nombre de la rama que se desea eliminar.
   - Ejemplo: `git branch -d feat/example-branch`

> [!WARNING]
> El comando `git branch -d <nombre-rama>` solo elimina la rama en tu repositorio local. 

## Comprensión de los flujos de trabajo con ramas

El flujo de trabajo incluye ramas específicas para el desarrollo (dev), las pruebas (test) y la producción (main). Asimismo, creamos ramas para las nuevas características de la aplicación (feature).

![Git Workflow](/images/git-workflow.png)

> [!WARNING]
> Cualquier nuevo feature que se desee crear debe ser desde la rama productiva (main). 

## Fusionar ramas y resolver conflictos

## Fusionar ramas
- **Fusionar ramas (Merge)**: Para iniciar una fusión entre ramas se debe seguir lo siguiente.
   1. Saltamos a la rama donde se recibirán los cambios con `git checkout main`.
   2. Indicamos la rama que contiene los cambios que queremos fusionar `git merge feat/example-branch`.
   3. Se creará un commit sobre la fusión de los cambios y utilizamos el comando `git push` para publicarlos al repositorio remoto.

## Conflictos en Git
Un conflicto ocurre cuando Git no puede decidir automáticamente cómo combinar cambios en los mismos archivos o líneas de código. Algunas causas comunes incluyen:

- **Ediciones en la Misma Línea**: Dos ramas tienen cambios en la misma línea de un archivo.
- **Ediciones en la Misma Área del Código**: Cambios cercanos dentro de un archivo que Git no puede resolver automáticamente.
- **Eliminación y Modificación Simultánea**: Un archivo se modifica en una rama y se elimina en otra.
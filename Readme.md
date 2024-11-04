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


# Buenas prácticas de Git

## Uso de .gitignore

 - Si no se requiere realizar el seguimiento de un archivo, se utiliza el archivo .gitignore que se incorpora en la raíz de tu repositorio. 
 - En Git no hay ningún comando explícito para ignorar archivos: en su lugar, cuando tengas nuevos archivos que quieras ignorar, deberás editar y confirmar manualmente el archivo .gitignore. 
 - Ejemplos de archivos que no requerieren seguimiento:
   - Cachés de dependencias, como /node_modules o /packages.
   - Directorios de salida de compilación, como /bin, /out o /target.

## Estrategias de branching

Para incorporar una nueva funcionalidad se deberá crear una nueva rama iniciando con `feat/nombre-funcionalidad`, el nombre de la funcionalidad debe contener `-` en lugar de espacios y no debe contener mayúsculas.

Los repositorios deben contar con las ramas dev (desarrollo), test (pruebas) y main (productivo)
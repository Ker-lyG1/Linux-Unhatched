

# 🐧 Mis Apuntes de Linux Unhatched (NDG / Cisco Networking Academy)

¡Bienvenido/a a mi cuaderno de apuntes sobre **Linux Unhatched**! 🚀  
Aquí registro los comandos, conceptos y arquitectura fundamental del sistema operativo Linux aprendidos en el curso de NDG.

---

## 📌 Tabla de Contenidos

- [1. Introducción a Linux y Código Abierto](#1-introducción-a-linux-y-código-abierto)
- [2. La Interfaz de Línea de Comandos (CLI) y la Shell](#2-la-interfaz-de-línea-de-comandos-cli-y-la-shell)
- [3. Navegación en el Sistema de Archivos](#3-navegación-en-el-sistema-de-archivos)
- [4. Gestión de Archivos y Directorios](#4-gestión-de-archivos-y-directorios)
- [5. Permisos de Archivos y Usuarios](#5-permisos-de-archivos-y-usuarios)
- [6. Banco de Preguntas y Respuestas Clave](#6-banco-de-preguntas-y-respuestas-clave)

---

## 1. Introducción a Linux y Código Abierto 💡

- **¿Qué es Linux?**: Es un sistema operativo libre y de código abierto (*Open Source*) basado en UNIX.
- **Núcleo (Kernel)**: Es el corazón del sistema operativo que gestiona la comunicación entre el hardware del equipo y los programas.
- **Distribuciones (Distros)**: Empaquetan el Kernel de Linux con herramientas del proyecto GNU y software adicional (ej. Ubuntu, Debian, Red Hat, CentOS, Arch Linux).

---

## 2. La Interfaz de Línea de Comandos (CLI) y la Shell 📝

- **Shell**: Es el intérprete de comandos que actúa como interfaz entre el usuario y el sistema operativo (la más popular es `bash`).
- **Prompt o Indicador de Comandos**: Muestra información importante como el usuario actual, el nombre del equipo y el directorio de trabajo.
  - `$` indica un usuario común.
  - `#` indica el usuario administrador (*root*).

### Comandos básicos de información:
- `whoami`: Muestra el nombre del usuario con el que estás autenticado.
- `hostname`: Muestra el nombre del equipo dentro de la red.
- `uname -a`: Muestra información detallada del sistema y la versión del Kernel.
- `clear`: Limpia la pantalla de la terminal.

---

## 3. Navegación en el Sistema de Archivos 🗺️

El sistema de archivos de Linux tiene una estructura de árbol que comienza desde la raíz `/`.

### Comandos clave de navegación:
- `pwd` (*Print Working Directory*): Muestra la ruta completa del directorio actual.
- `ls` (*List*): Muestra el contenido (archivos y carpetas) del directorio actual.
  - `ls -l`: Lista detallada (permisos, dueño, tamaño, fecha).
  - `ls -a`: Muestra todos los archivos, incluyendo los ocultos (los que empiezan con `.`).
- `cd` (*Change Directory*): Cambia de directorio.
  - `cd /`: Va al directorio raíz.
  - `cd ~` o solo `cd`: Va al directorio personal del usuario (*Home*).
  - `cd ..`: Sube un nivel al directorio padre.

---

## 4. Gestión de Archivos y Directorios 📁

### Crear y Eliminar:
- `mkdir nombre_carpeta`: Crea un nuevo directorio.
- `touch nombre_archivo`: Crea un archivo vacío o actualiza la fecha de modificación.
- `rm nombre_archivo`: Elimina un archivo.
- `rmdir carpeta_vacía`: Elimina un directorio vacío.
- `rm -r nombre_carpeta`: Elimina un directorio y todo su contenido de forma recursiva.

### Copiar y Mover:
- `cp origen destino`: Copia un archivo de un lugar a otro.
- `mv origen destino`: Mueve o renombra un archivo/directorio.

### Visualizar Contenido:
- `cat archivo`: Muestra todo el contenido de un archivo en pantalla.
- `head archivo`: Muestra las primeras 10 líneas de un archivo.
- `tail archivo`: Muestra las últimas 10 líneas de un archivo.

---

## 5. Permisos de Archivos y Usuarios 🔒

Linux es un sistema multiusuario, por lo que cada archivo tiene propietarios y permisos definidos.

### Tipos de usuarios:
- **Usuario (u)**: El dueño del archivo.
- **Grupo (g)**: El grupo de usuarios asignado al archivo.
- **Otros (o)**: Todos los demás usuarios del sistema.

### Tipos de permisos:
- `r` (*Read* / Lectura): Permite ver el contenido.
- `w` (*Write* / Escritura): Permite modificar o eliminar.
- `x` (*Execute* / Ejecución): Permite ejecutar el archivo si es un programa o script.

### Cambio de permisos y propietarios:
- `chmod`: Modifica los permisos de lectura, escritura o ejecución.
- `chown`: Cambia el propietario del archivo.
- `sudo`: Ejecuta un comando con privilegios de administrador (*root*).

---

## 6. Banco de Preguntas y Respuestas Clave ❓

> **Q1: ¿Qué comando se utiliza para saber en qué directorio te encuentras actualmente?** > **R:** `pwd` (*Print Working Directory*).

> **Q2: ¿Cuál es la diferencia entre `ls` y `ls -a`?** > **R:** `ls` muestra los archivos visibles, mientras que `ls -a` incluye también los archivos ocultos (que empiezan con un punto `.`).

> **Q3: ¿Qué símbolo representa el directorio personal (Home) del usuario en la línea de comandos?** > **R:** El símbolo de la tilde de la eñe `~`.

> **Q4: ¿Qué comando se usa para crear un directorio nuevo?** > **R:** `mkdir`.

> **Q5: ¿Qué hace el comando `cd ..`?** > **R:** Retrocede un nivel hacia el directorio padre.

> **Q6: ¿Qué comando permite ver las primeras líneas de un archivo de texto?** > **R:** `head`.

> **Q7: ¿Qué significa la opción `-r` al usar el comando `rm`?** > **R:** Indica una eliminación recursiva, necesaria para borrar directorios que contienen archivos u otras carpetas.

> **Q8: ¿Cuál es la función del comando `whoami`?** > **R:** Muestra el nombre del usuario actual del sistema.

> **Q9: ¿Qué usuario posee todos los derechos y privilegios administrativos en un sistema Linux?** > **R:** El usuario `root`.

> **Q10: ¿Qué comando te permite ejecutar tareas con permisos de superusuario o root?** > **R:** `sudo`.

---

🎯 *Notas de Linux Unhatched guardadas y mantenidas desde Termux.*



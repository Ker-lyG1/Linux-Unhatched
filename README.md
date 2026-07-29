
# Apuntes de Linux: Gestión y Ordenación de Archivos

> **Nota:** Los directorios y archivos más grandes pueden mostrarse en Kilobytes, ya que mostrar su tamaño en bytes resultaría en un número demasiado grande. Por lo tanto, en el caso de un directorio, este número podría ser un múltiplo del tamaño de bloque utilizado por el sistema de archivos. El tamaño de bloque es el tamaño de una serie de datos almacenados en el sistema de archivos.

---

## 1. Estructura de la Salida de `ls -l`

### Sello Horario o de Tiempo (*Timestamp*)
Indica la fecha y hora en que el contenido del archivo se modificó por última vez:

```bash
drwxr-xr-x 2 root root 4096 Dec 7 2017

Nombre del Archivo o Directorio
​El campo final contiene el nombre del recurso:

Dec 7 2017 bootstrap.log

En el caso de enlaces simbólicos (un archivo que apunta a otro archivo), el nombre del enlace se mostrará junto a una flecha (->) y la ruta del archivo original:

lrwxrwxrwx. 1 root root 22 Nov 6 2012 /etc/grub.conf -> ../boot/grub/grub.conf

2. Ordenar Archivos con ls
​Por defecto, el resultado del comando ls se muestra ordenado alfabéticamente según el nombre del archivo. Sin embargo, se pueden aplicar diferentes opciones para modificar este comportamiento.
​Las siguientes opciones se combinan con -l para mostrar los detalles relevantes de cada archivo:

Ordenar por Fecha/Sello de Tiempo (-t): Ordena los archivos comenzando por los más recientes (timestamp).

ls -lt /var/log

Ordenar por Tamaño (-S): Ordena los archivos de mayor a menor tamaño (size).

ls -lS /var/log

Invertir el Orden (-r): Invierte el orden de cualquier tipo de clasificación (reverse).

ls -lsr /var/log

Orden Alfabético Inverso (-r): Utilizando únicamente la opción -r, muestra los archivos en orden alfabético de la Z a la A.

(Al usar -r, el orden de los tamaños cambia de descendente a ascendente).

ls -r /var/log


# Linux Unhatched (Cisco)

## Conceptos Básicos
* **GUI:** Interfaz gráfica basada en íconos.
* **CLI:** Línea de comandos; más rápida y eficiente.
* **Comando:** Programa que ejecuta una acción en el sistema.
* **Sintaxis:** `comando [opciones] [argumentos]`
  * **Opciones:** Cambian el comportamiento del comando (ej. `-l`, `-r`). Se pueden combinar (ej. `-lr`).
  * **Argumentos:** El objetivo sobre el que actúa el comando (ej. `ls Documents`).

## Navegación
* `/`: Directorio raíz (nivel superior).
* `~`: Directorio de inicio (*Home*).
* `pwd`: Muestra la ruta actual.
* **Ruta Absoluta:** Inicia siempre con `/` (ej. `/home/sysadmin`).
* **Ruta Relativa:** Depende de la ubicación actual, no empieza con `/` (ej. `cd Documents`).

## Listado de Archivos (`ls`)
* `ls`: Lista el contenido del directorio actual.
* `ls -l`: Muestra el formato detallado (*long*).

### Tipos de archivo (primer carácter en `ls -l`)
* `d`: Directorio
* `-`: Archivo ordinario (texto, imagen, ejecutable, comprimido)
* `l`: Enlace simbólico
* `s`: Socket
* `p`: Tubería (*pipe*)
* `b` / `c`: Dispositivo de bloque / carácter (hardware)

### Campos de `ls -l`
1. Tipo de archivo y permisos (`drwxr-xr-x`)
2. Número de enlaces directos
3. Propietario (usuario creador)
4. Grupo propietario
5. Tamaño (bytes)
6. Sello de tiempo (*timestamp*)
7. Nombre del archivo/directorio



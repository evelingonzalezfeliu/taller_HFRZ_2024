# Taller de Nextflow: Introducción a Linux y Ejecución de un Pipeline

## Objetivo
En este taller, aprenderás los conceptos básicos de Linux y los comandos esenciales para ejecutar un pipeline en Nextflow.

## Contenidos
1. **Introducción a Linux**  
   - ¿Qué es Linux?  
   - La terminal: tu herramienta clave.  

2. **Comandos básicos de Linux (con ejemplos)**  
   - Navegación por el sistema de archivos.  
   - Gestión de archivos.  
   - Visualización de contenido.  
   - Utilidades.  

3. **Instalación y Configuración de Nextflow**  
   - Descarga e instalación.  
   - Configuración básica.  

4. **Ejecución de un Pipeline en Nextflow**  
   - Estructura de un pipeline.  
   - Comando básico: `nextflow run`.  
   - Visualización de resultados.  

5. **Ejercicio Práctico**  

---

## Introducción a Linux

### 1. **¿Qué es Linux?**

Linux es un sistema operativo de código abierto, lo que significa que su código fuente está disponible para que cualquier persona lo utilice, modifique y distribuya. Es ampliamente utilizado en servidores, computadoras personales y dispositivos embebidos debido a su estabilidad, seguridad y flexibilidad.

- **Distribuciones populares**: Ubuntu, CentOS, Fedora, Debian.
- **Áreas de uso**: servidores web, supercomputadoras, sistemas de redes, ciencia de datos, bioinformática, entre otros.

### 2. **La terminal: tu herramienta clave**

La terminal es una interfaz de línea de comandos que permite interactuar directamente con el sistema operativo escribiendo comandos. A diferencia de las interfaces gráficas, la terminal es más poderosa y eficiente para tareas como automatización, manipulación masiva de archivos y ejecución de scripts.

**Ventajas de usar la terminal**:
- **Rapidez**: Realizar tareas con un solo comando.
- **Flexibilidad**: Acceso a opciones y configuraciones avanzadas.
- **Automatización**: Creación de scripts para ejecutar múltiples tareas.

**Ejemplo de una tarea con terminal**:
- Crear un directorio, moverse dentro de él, y crear un archivo en pocos pasos:
  ```bash
  mkdir RUN_BRCA
  cd RUN_BRCA
  touch input.csv

## Comandos básicos de Linux (con ejemplos)

### 1. **Navegación por el sistema de archivos**

 - ```pwd```: Muestra la ruta del directorio actual.
   ```bash
   pwd
   # Salida: /home/usuario/taller_nextflow

- ```ls```: Lista los archivos y directorios.

   ```bash
   ls
   # Salida: documento.txt  directorio1  script.sh

Opciones útiles:

 - ```ls -l```: Lista con detalles adicionales (permisos, tamaño).
 - ```ls -a:``` Incluye archivos ocultos.
 - ```cd```: Cambia de directorio.

   ```bash
   cd directorio1
   pwd
   # Salida: /home/usuario/taller_nextflow/directorio1
   
Volver al directorio anterior:
   ```bash
   cd ..
   pwd
   # Salida: /home/usuario/taller_nextflow
   ```
### 2. **Gestión de archivos**
   
- ```mkdir```: Crea un nuevo directorio.
   ```bash
      mkdir datos
      ls
      # Salida: datos  documento.txt  script.sh

 - ```touch```: Crea un archivo vacío.
   ```bash
   touch archivo_nuevo.txt
   ls
   # Salida: archivo_nuevo.txt  datos  documento.txt

 - ```cp```: Copia archivos o directorios.
   ```bash
   cp documento.txt copia_documento.txt
   ls
   # Salida: archivo_nuevo.txt  copia_documento.txt  documento.txt

 - ```mv```: Mueve o renombra archivos.
   ```bash
   mv copia_documento.txt documentos_backup/

Para renombrar:
   ```bash
   mv archivo_nuevo.txt archivo_renombrado.txt
   ```
 - ```rm```: Elimina archivos o directorios.
   ```bash
   rm archivo_renombrado.txt

Eliminar un directorio y su contenido:
   ```bash
   rm -r datos/
   ```

### 3. **Visualización de contenido**
 - ``cat``: Muestra el contenido completo de un archivo.
   ```bash
   Copiar código
   cat documento.txt

### Salida: (contenido del archivo)
_ ```less```: Permite navegar por el contenido de un archivo grande.
   ```bash
      less documento.txt
   ```
**(Usa las teclas de flecha para desplazarte, presiona 'q' para salir)**

- ```head``` y ```tail```: Muestra las primeras o últimas líneas de un archivo.
   ```bash
   head -n 5 documento.txt  # Primeras 5 líneas
   tail -n 5 documento.txt  # Últimas 5 líneas

### 4. **Utilidades**
 - ```nano```: Abre un editor de texto sencillo.
   ```bash
      Copiar código
      nano documento.txt
   
# Edita el archivo, guarda con Ctrl+O y sal con Ctrl+X.
 - ```man```: Muestra el manual de un comando.
   ```bash
      Copiar código
      man ls
   
**(Lee la descripción del comando 'ls', presiona 'q' para salir)**

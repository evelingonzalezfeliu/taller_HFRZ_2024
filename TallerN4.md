# Taller de Nextflow: Introducción a Linux y Ejecución de un Pipeline

## Objetivo
En este taller, aprenderás los conceptos básicos de Linux y los comandos esenciales para ejecutar un pipeline en Nextflow.

## Contenidos
1. **Introducción a Linux**  
   - ¿Qué es Linux?  
   - Diferencias con otros sistemas operativos.  
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

### 2. **Diferencias con otros sistemas operativos**

| **Característica**       | **Linux**                          | **Windows**                       | **MacOS**                      |
|--------------------------|-------------------------------------|-----------------------------------|---------------------------------|
| **Licencia**             | Código abierto (gratuito)           | Licencia propietaria (pago)       | Licencia propietaria (pago)     |
| **Personalización**      | Altamente personalizable            | Limitada                          | Limitada                        |
| **Interfaz**             | Terminal y entornos gráficos        | Mayormente gráfico                | Mayormente gráfico              |
| **Seguridad**            | Alta, menos vulnerable a virus      | Más susceptible a malware         | Alta                            |
| **Compatibilidad**       | Ideal para servidores y desarrollo  | Más popular en entornos de oficina | Popular en diseño y multimedia  |
| **Actualizaciones**      | Frecuentes, personalizables         | Centralizadas                     | Centralizadas                   |

### 3. **La terminal: tu herramienta clave**

La terminal es una interfaz de línea de comandos que permite interactuar directamente con el sistema operativo escribiendo comandos. A diferencia de las interfaces gráficas, la terminal es más poderosa y eficiente para tareas como automatización, manipulación masiva de archivos y ejecución de scripts.

**Ventajas de usar la terminal**:
- **Rapidez**: Realizar tareas con un solo comando.
- **Flexibilidad**: Acceso a opciones y configuraciones avanzadas.
- **Automatización**: Creación de scripts para ejecutar múltiples tareas.

**Ejemplo de una tarea con terminal**:
- Crear un directorio, moverse dentro de él, y crear un archivo en pocos pasos:
  ```bash
  mkdir proyecto
  cd proyecto
  touch archivo.txt

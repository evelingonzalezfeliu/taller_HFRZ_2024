# Práctico de Llamado de Variantes y Visualización con IGV

## Objetivos

1. Realizar el llamado de variantes en datos genómicos utilizando Strelka y DeepVariant en Galaxy.
2. Comprender qué es un llamado de variantes y cómo interpretar archivos de variantes (VCF).
3. Comparar las variantes detectadas entre Strelka y DeepVariant en una misma muestra.
4. Visualizar y analizar variantes en el genoma de referencia usando IGV.

## Introducción

### ¿Qué es un llamado de variantes?

El llamado de variantes es el proceso de identificar cambios en la secuencia de ADN de un individuo en comparación con un genoma de referencia. Existen diferentes tipos de variantes:
- **SNVs (Single Nucleotide Variants):** Cambios de una sola base.
- **Indels (Inserciones y Deleciones):** Adiciones o eliminaciones de varias bases en la secuencia.

### Herramientas de llamado de variantes: Strelka y DeepVariant

- **Strelka:** Optimizado para el llamado de variantes en secuenciación de alta precisión, especialmente útil para análisis de cáncer.
- **DeepVariant:** Basado en aprendizaje profundo, utiliza redes neuronales para ofrecer alta precisión en el llamado de variantes.

Ambas herramientas generan archivos VCF que podemos comparar y visualizar en IGV.

### Visualización con IGV

**IGV (Integrative Genomics Viewer)** es una herramienta para explorar y visualizar datos genómicos. Permite observar variantes en el contexto del genoma de referencia y comparar múltiples muestras.

- Descarga IGV desde [IGV Download](https://software.broadinstitute.org/software/igv/download)
- IGV es útil para:
  - Ver variantes en regiones específicas del genoma.
  - Comparar múltiples archivos de variantes.
  - Observar cobertura de lectura y calidad de variantes.

## Requisitos

- Acceso a Galaxy.
- IGV instalado.

---

## Instrucciones

### 1. Subida de datos a Galaxy

1. Inicia sesión en Galaxy. [Galaxy](https://usegalaxy.org/). 
2. Selecciona **Upload Data** en el panel izquierdo.
3. Carga tus archivos:
     - Un archivo BAM alineado. [Descargar archivo](CLASE1/data/S11.aln.bam)
     - Un archivo BED con los sitios específicos de BRCA1/2. [Descargar archivo](CLASE1/data/AmpliSeq_BRCA_hg38_new.bed)

### 2. Llamado de variantes con DeepVariant

1. Busca **DeepVariant** en Galaxy.
   ![Upload](CLASE1/images/deepvariant.png)
3. Cargar en galaxy los archivos de entrada (BAM y BED)
   ![Upload](CLASE1/images/deepvariant1.png)
   ![Upload](CLASE1/images/deepvariant2.png)
5. Configura los parámetros y ejecuta DeepVariant.
   ![Upload](CLASE1/images/deepvariant3.png)
   ![Upload](CLASE1/images/deepvariant4.png)
7. Descarga o guarda el archivo VCF generado.
   ![Upload](CLASE1/images/deepvariant5.png)

8. Interpretación de Resultados.Los campos clave en un VCF incluyen:
- **CHROM**: Cromosoma de la variante.
- **POS**: Posición de la variante.
- **REF**: Base de referencia.
- **ALT**: Base alternativa.
- **QUAL**: Calidad de la llamada.
- **INFO**: Información adicional (por ejemplo, profundidad de cobertura y frecuencia alélica).

### 3. Llamado de variantes con Strelka

1. En Galaxy, busca la herramienta **Strelka**.
3. Selecciona el archivo BAM como entrada.
4. Configura los parámetros y ejecuta Strelka.
5. Guarda el archivo VCF generado.

### 4. Visualización en IGV

#### Instalación y Configuración de IGV

1. Descarga IGV desde [IGV Download](https://software.broadinstitute.org/software/igv/download) e instálalo.
2. Descarga la carpeta de drive compartida [drive](https://drive.google.com/drive/folders/1AsFH0l6Q2Hf9og-7FPUAwGZpyhCdeV04?usp=drive_link)
3. Abre IGV y carga el genoma de referencia. **hs38DH.fa**
   ![Upload](CLASE1/images/igv1.png)
   ![Upload](CLASE1/images/igv2.png)

#### Visualización de variantes

1. Carga los archivos VCF de Strelka y DeepVariant en IGV:
   - Selecciona **File > Load from File** y elige cada archivo VCF.
2. Navega a las regiones con variantes detectadas y compara la visualización de las variantes en cada archivo.
   ![Upload](CLASE1/images/igv3.png)
4. Carga las muestras LV y PP, y observa las posición chr17	43093425. Observa y anota las diferencias en la cobertura y la calidad de las variantes.
   ![Upload](CLASE1/images/igv4.png)

### 5. Comparación de variantes

Para comparar las variantes detectadas por Strelka y DeepVariant en la misma muestra, sigue estos pasos:

1. **Descargar los archivos VCF** de Strelka y DeepVariant.
2. **Usar una herramienta de comparación de VCF** (como `bcftools isec` o la herramienta **Compare VCF files** en Galaxy):
   - Esto generará un archivo de salida que muestra las variantes únicas y compartidas entre ambos métodos.
3. **Interpretar los resultados**:
   - Las variantes **compartidas** representan aquellas que ambos métodos detectaron.
   - Las variantes **exclusivas** pueden deberse a diferencias en la sensibilidad y especificidad de cada método.

#### Comparación Final

1. **Identifica variantes compartidas y únicas**:
   - Las variantes únicas pueden indicar diferencias en la precisión de Strelka y DeepVariant.
2. **Visualiza variantes de interés en IGV** para validar y explorar su contexto genómico.

---

Este práctico te guiará para realizar el llamado de variantes, comparar resultados entre Strelka y DeepVariant, y visualizar las variantes en IGV.

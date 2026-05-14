 # MBM-G4
# IDENTIFICACION DE BACTERIAS AMBIENTALES CON GEN HOUSEKEPPING recA  
## Integrantes:
-Helen Correa 
-Joel Malacatus 
-Stephen Sarmiento 
-Christian Valdez     
## Objetivo
## Dataset  
## Flujo de Trabajo  
### 1. Descarga y organización de secuencias
Las secuencias obtenidas mediante secuenciación Sanger fueron descargadas en formato FASTQ. Para organizar el análisis se creó un directorio denominado Secuencias, donde se almacenaron los archivos correspondientes a las muestras 7, 21 y 22 en formato forward y reverse en total 6 secuencias.
mkdir Secuencias
cd Secuencias
ls -l
unzip Secuencias_Fasta_7_21_22.zip
ls -l
### 2. Evaluación inicial de calidad
La calidad de las secuencias fue evaluada utilizando FastQC, generando reportes HTML para cada archivo FASTQ.
eje: fastqc 7fw.fastq
Posteriormente, los archivos HTML fueron abiertos para visualizar los gráficos de calidad,se generaron reportes individuales.
### 3. Preprocesamiento 
La limpieza de secuencias se realizó utilizando Trimmomatic para eliminar regiones de baja calidad y adaptadores.
Primero se verificó la ubicación del programa dentro del sistema:
dpkg -L trimmomatic
java -jar /usr/share/java/trimmomatic-0.39.jar

Posteriormente se ejecutó el trimming individual para cada secuencia.
Ejemplo para la muestra 7 forward:
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 \
7fw.fastq \
7fw_clean.fastq \
ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 \
HEADCROP:15 \
LEADING:20 \
TRAILING:20 \
SLIDINGWINDOW:4:20 \
MINLEN:50
Los parámetros permitieron eliminar adaptadores Illumina, recortar los primeros 15 nucleótidos, remover bases de baja calidad y conservar secuencias mayores a 50 pb mediante control de calidad.

Reevaluación de calidad : Las secuencias limpias fueron nuevamente evaluadas con FastQC,eje:
fastqc 7fw_clean.fastq
xdg-open 7fw_clean_fastqc.html
Posteriormente se realizó el trimming de las secuencias, eliminando regiones de baja calidad y zonas problemáticas.
Los reportes HTML mostraron que las secuencias quedaron aptas para ensamblaje

### 4. Ensamblaje y generación de secuencias consenso 
Antes del ensamblaje se actualizó el sistema e instalaron herramientas bioinformáticas adicionales:
VSEARCH
EMBOSS
Seqtk
Las secuencias limpias fueron convertidas de formato FASTQ a FASTA utilizando Seqtk.
Se generaron correctamente los archivos FASTA a partir de las secuencias limpias, conservando lecturas aptas para el ensamblaje.
El procedimiento fue repetido para las muestras 21 y 22.

Las secuencias forward y reverse fueron ensambladas utilizando la herramienta merger de EMBOSS.
merger -asequence 7fw_clean.fasta \
-bsequence 7re_clean.fasta \
-outfile 7_recA.txt \
-outseq 7_recA_consensus.fasta 
Posteriormente se visualizaron los archivos de alineamiento y las secuencias consenso obtenidas.
El procedimiento fue aplicado a las muestras 7, 21 y 22.

### 5. Identificación taxonómica mediante BLAST
Las secuencias consenso obtenidas fueron analizadas utilizando BLAST en NCBI BLAST
Finalmente se realizó la identificación taxonómica de las secuencias consenso , comparando las muestras 7, 21 y 22 con secuencias registradas en bases de datos para determinar su similitud taxonómica.


## Resultados
## Contribución individual 
## Scripts Reproducibles 
Descargamos las secuencias en formato fastq  
Generamos la carpeta: mkdir Secuencias  
Cambio de director: cd Secuencias  
Revisar contenido de carpeta: ls -l  
Descomprimir: .zip unzip Secuencias Fasta, 7,21,22.zip  
Revisar que las carpetas estén descomprimidas ls -l   
Generacion de .HTMLy visvualizacion con fastq  
Limpieza: dpkg -L trimmomatic  
          java -jar /usr/share/java/trimmomatic-0.39.jar  
          /usr/share/java/trimmomatic-0.39.jar  
•	Limpieza para 7 fw  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 \  7fw.fastq \ 7fw_clean.fastq \ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 \  HEADCROP:15 \LEADING:20 \TRAILING:20 \SLIDINGWINDOW:4:20 \MINLEN:50  
fastqc 7fw_clean.fastq  
xdg-open 7fw_clean_fastqc.html  
Secuencia 7 fw clean  
•	Limpieza para 7 re  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 7re.fastq 7re_clean.fastq ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 HEADCROP:15 LEADING:20 TRAILING:20 SLIDINGWINDOW:4:20 MINLEN:50  
fastqc 7re_clean.fastq  
xdg-open 7re_clean_fastqc.html  
Secuencia 7 re clean  
•	Limpieza para 21fw  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 21fw.fastq 21fw_clean.fastq ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 HEADCROP:15 LEADING:20 TRAILING:20 SLIDINGWINDOW:4:20 MINLEN:50  
fastqc 21fw_clean.fastq  
xdg-open 21fw_clean_fastqc.html  
Secuencia 21 fw clean  
•	Limpieza para 21re  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 21re.fastq 21re_clean.fastq ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 HEADCROP:15 LEADING:20 TRAILING:20 SLIDINGWINDOW:4:20 MINLEN:50  
fastqc 21re_clean.fastq  
xdg-open 21re_clean_fastqc.html  
Secuencia 21 re clean  
•	Limpieza para 22fw  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 22fw.fastq 22fw_clean.fastq ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 HEADCROP:15 LEADING:20 TRAILING:20 SLIDINGWINDOW:4:20 MINLEN:50  
fastqc 22fw_clean.fastq  
xdg-open 22fw_clean_fastqc.html  
Secuencia 22fw clean  
•	Limpieza para 22re  
java -jar /usr/share/java/trimmomatic-0.39.jar SE -phred33 22re.fastq 22re_clean.fastq ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 HEADCROP:15 LEADING:20 TRAILING:20 SLIDINGWINDOW:4:20 MINLEN:50  
fastqc 22re_clean.fastq  
xdg-open 22re_clean_fastqc.html  
Secuencia 22fw clean  

Consensos de Secuencias Limpias  
sudo apt update  
sudo apt install vsearch  
sudo apt install emboss  
sudo apt install seqtk  
# Convertir Fastq a Fasta    
seqtk seq -a 7fw_clean.fastq > 7fw_clean.fasta  
seqtk seq -a 7re_clean.fastq > 7re_clean.fasta  
# Unir con merger  
merger -asequence 7fw_clean.fasta -bsequence 7re_clean.fasta -outfile 7_recA.txt -outseq   7_recA_consensus.fasta  
genera texto y consenso de fw y rv  
less 7_recA.txt  
less 7_recA_consensus.fasta  

## Referencias Bibliograficas  
1.	Durand K, Ogier JC, Nam K. The evaluation of shotgun sequencing and rpoB metabarcoding for taxonomic profiling of bacterial communities. BMC Microbiol. 2025;25:413. doi: 10.1186/s12866-025-04149-3.
2.	Nunes Ramos J, Veloso da Costa L, Viana Vieira V, Lima Brandão ML. Challenges in the Identification of Environmental Bacterial Isolates from a Pharmaceutical Industry Facility by 16S rRNA Gene Sequences. DNA. 2025;5(3):33. doi: 10.3390/dna5030033
3.	Jurvansuu J, Länsivaara A, Palmroth M, Kaarela O, Hyöty H, Oikarinen S, et al. Machine learning-based identification of wastewater treatment plant-specific microbial indicators using 16S rRNA gene sequencing. Sci Rep. 2025;15:23771. doi: 10.1038/s41598-025-07952-0
4.	Valido E, Bertolo A, Stoyanov J. Quantitative profiling of bacterial communities via full length 16S rRNA gene sequencing with internal controls: optimization and validation across diverse human microbiomes. BMC Microbiol. 2025;25:710. doi: 10.1186/s12866-025-04399-1
5.	Wang C, Yang Y, Xu X, Wang D, Shi X, Liu L, et al. The quest for environmental analytical microbiology: absolute quantitative microbiome using cellular internal standards. Microbiome. 2025 Jan 27;13:26. doi: 10.1186/s40168-024-02009-2

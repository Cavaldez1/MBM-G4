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

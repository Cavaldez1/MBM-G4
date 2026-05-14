# IDENTIFICACION DE BACTERIAS AMBIENTALES CON GEN HOUSEKEPPING *recA*
## Integrantes  
 Joel Malacatus  
 Christian Valdez  
 Helen Correa  
 Stephen Sarmiento  
## Objetivo:    
Objetivo general
Identificar molecularmente bacterias marinas mediante el análisis y secuenciación del gen housekeeping recA, con el fin de determinar su clasificación taxonómica y establecer la presencia de bacterias del género Vibrio en muestras ambientales.
## 1. Introducción  
La identificación molecular de bacterias ambientales se ha convertido en una herramienta fundamental para el estudio de la diversidad microbiana y el monitoreo ecológico de distintos ecosistemas. Las bacterias presentes en suelo, agua y sedimentos participan en procesos biogeoquímicos, biodegradación y transferencia genética, influyendo en la estabilidad ambiental y la salud pública. El desarrollo de técnicas moleculares y de secuenciación ha permitido superar las limitaciones de los métodos microbiológicos tradicionales basados en cultivo, facilitando una identificación más precisa de comunidades bacterianas complejas.
Entre los marcadores moleculares utilizados destacan los genes housekeeping, los cuales poseen regiones conservadas y variables útiles para diferenciación taxonómica. El gen recA ha sido ampliamente empleado debido a su función en recombinación homóloga y reparación del ADN bacteriano, además de presentar una mayor resolución filogenética en comparación con otros marcadores convencionales. Su uso permite distinguir especies bacterianas estrechamente relacionadas y fortalecer estudios evolutivos y de clasificación taxonómica.
Actualmente, las tecnologías basadas en PCR, secuenciación de nueva generación y análisis bioinformático han mejorado significativamente la identificación bacteriana en microbiología ambiental. Estas metodologías permiten detectar microorganismos no cultivables, analizar comunidades microbianas complejas e identificar bacterias relacionadas con contaminación ambiental, resistencia antimicrobiana y adaptación ecológica.
En este contexto, el presente proyecto se enfoca en la identificación de bacterias ambientales mediante el análisis molecular del gen housekeeping recA, utilizando herramientas bioinformáticas para el procesamiento, control de calidad y análisis de secuencias bacterianas.
Las muestras ambientales fueron recolectadas bajo condiciones estériles a partir de fuentes naturales seleccionadas de almejas en zona de pesca para el estudio microbiológico. Posteriormente, las muestras fueron transportadas en cadena de frío al laboratorio para su procesamiento dentro de las primeras 24 horas posteriores a la recolección, con el propósito de preservar la viabilidad bacteriana y evitar alteraciones microbiológicas.
## 2. Metodología  
## Aislamiento bacteriano
Las muestras recolectadas fueron sembradas en medios de cultivo apropiados para el crecimiento bacteriano mediante técnicas microbiológicas convencionales. Las placas fueron incubadas bajo condiciones controladas de temperatura y tiempo para favorecer el desarrollo de colonias bacterianas. Posteriormente, se realizó la selección y purificación de colonias con características morfológicas compatibles con bacterias ambientales de interés.
## Extracción de ADN genómico
El ADN bacteriano fue extraído a partir de colonias purificadas utilizando protocolos de extracción molecular estandarizados. La calidad e integridad del ADN obtenido fueron evaluadas mediante técnicas de cuantificación y verificación electroforética antes de proceder con los análisis moleculares posteriores.
## Amplificación del gen recA mediante PCR
La identificación molecular se realizó mediante amplificación del gen housekeeping recA utilizando la técnica de reacción en cadena de la polimerasa (PCR). Para ello se emplearon cebadores específicos dirigidos al gen recA, bajo condiciones optimizadas de amplificación. Los productos obtenidos fueron verificados mediante electroforesis en gel de agarosa.
## Secuenciación genética
Los productos amplificados fueron sometidos a secuenciación nucleotídica para obtener las secuencias correspondientes al gen recA. Las secuencias generadas fueron almacenadas en formatos compatibles para análisis bioinformático posterior.
## Control de calidad inicial
Las secuencias obtenidas fueron sometidas a un control de calidad inicial con el objetivo de evaluar la integridad y confiabilidad de las lecturas generadas. Se analizaron parámetros relacionados con longitud de lectura, presencia de nucleótidos ambiguos y calidad de secuencia.
## Preprocesamiento bioinformático
El preprocesamiento de las secuencias incluyó filtrado, depuración y eliminación de regiones de baja calidad mediante herramientas bioinformáticas especializadas. Las secuencias procesadas fueron organizadas en formatos FASTA y FASTQ para facilitar los análisis posteriores.
## Segundo control de calidad
Posterior al preprocesamiento, las secuencias filtradas fueron sometidas nuevamente a análisis de calidad con el propósito de verificar la mejora en la precisión y confiabilidad de las lecturas utilizadas para identificación molecular.
## Identificación molecular y análisis bioinformático
Las secuencias procesadas fueron comparadas con bases de datos genéticas disponibles en el National Center for Biotechnology Information (NCBI) utilizando la herramienta BLASTn. El análisis de similitud genética permitió determinar correspondencia con bacterias pertenecientes al género Vibrio.
## Gestión y almacenamiento de datos
Todos los datos generados durante el estudio, incluyendo secuencias nucleotídicas, resultados de control de calidad, archivos procesados y documentación metodológica, fueron organizados y almacenados en un repositorio desarrollado en GitHub con el propósito de garantizar la reproducibilidad, trazabilidad y disponibilidad del análisis bioinformático realizado.

## 3. Resultados  
### Resultados del ensamblaje
El ensamblaje de las secuencias forward y reverse mediante EMBOSS merger permitió generar secuencias consenso representativas del gen *recA* para las muestras 7, 21 y 22. Los alineamientos obtenidos mostraron altos porcentajes de identidad y similitud, evidenciando una adecuada correspondencia entre las lecturas analizadas.

| Muestra | Longitud (pb) | Identity (%) | Similarity (%) | Gaps (%) | Score |
|---|---|---|---|---|---|
| 7 | 702 | 88.6 | 88.6 | 11.4 | 3100.0 |
| 21 | 703 | 87.8 | 87.8 | 12.2 | 3085.0 |
| 22 | 702 | 88.0 | 88.0 | 12.0 | 3090.0 |

Estos resultados indican que las secuencias forward y reverse presentan una elevada correspondencia, permitiendo la obtención de secuencias consenso confiables para análisis taxonómicos posteriores. Los porcentajes de identidad cercanos al 88% sugieren la presencia de regiones conservadas del gen *recA*, mientras que los gaps observados podrían asociarse a pequeñas variaciones genéticas, diferencias entre cepas bacterianas o regiones afectadas por el proceso de secuenciación.

### Resultados BLAST
Las secuencias consenso obtenidas fueron analizadas mediante BLAST en NCBI BLAST, obteniéndose coincidencias predominantes con bacterias del género Vibrio.

| Muestra | Principales coincidencias | Similitud (%) |
|---|---|---|
| 7 | *Vibrio sp.*, *Vibrio chaetopteri* | 90.74 – 100 |
| 21 | *Vibrio sp*., *Vibrio ichthyoenteri*, *Vibrio pelagius* | 87.06 – 100 |
| 22 | *Vibrio sp*., *Vibrio frotis* | 87.4 – 100 |

Los resultados sugieren que las muestras analizadas pertenecen a bacterias estrechamente relacionadas con el género *Vibrio*, un grupo ampliamente distribuido en ambientes acuáticos y reconocido por su importancia ecológica y clínica. La presencia de múltiples coincidencias con porcentajes elevados de similitud indica una conservación importante del gen recA entre las especies detectadas.

## 4. Discusión 
El flujo de trabajo bioinformático aplicado permitió obtener secuencias consenso confiables del gen *recA* mediante control de calidad, trimming y ensamblaje de lecturas forward y reverse. La mejora observada en la calidad de las secuencias después del procesamiento permitió reducir regiones problemáticas y obtener lecturas aptas para análisis taxonómicos, aspecto considerado fundamental en estudios de secuenciación bacteriana [Valido, Bertolo, & Stoyanov, 2025](#ref4).

Los ensamblajes obtenidos presentaron porcentajes de identidad cercanos al 88%, permitiendo generar secuencias consenso representativas de las muestras analizadas. Los gaps observados podrían relacionarse con variaciones genéticas entre cepas bacterianas o regiones parcialmente conservadas, fenómeno frecuente en microorganismos ambientales [Durand, Ogier, & Nam, 2025](#ref1).
El análisis mediante BLAST mostró coincidencias predominantes con bacterias del género *Vibrio*, grupo ampliamente distribuido en ambientes acuáticos y caracterizado por una elevada diversidad genética [Jurvansuu et al., 2025](#ref2). Sin embargo, aunque se obtuvieron porcentajes altos de similitud, no fue posible confirmar con precisión la especie bacteriana, posiblemente debido a limitaciones en la cobertura de las bases de datos o a la variabilidad genética de los aislamientos ambientales [Nunes Ramos, Veloso da Costa, Viana Vieira, & Lima Brandão, 2025](#ref3).

Finalmente, el gen *recA* demostró ser un marcador molecular útil para la identificación preliminar de bacterias ambientales y el análisis taxonómico de los aislamientos estudiados [Wang,Yang, et al., 2025](#ref5).

## 5. Conclusiones  
A partir del procedimiento microbiológico y bioinformático realizado, se concluye que fue posible aislar y analizar molecularmente bacterias ambientales mediante el estudio del gen housekeeping *recA*, cumpliendo con los objetivos establecidos en la investigación.
Los análisis de control de calidad realizados con FastQC evidenciaron que las secuencias crudas presentaban regiones de baja calidad en los extremos de lectura, situación común en procesos de secuenciación. Posteriormente, el uso de Trimmomatic permitió eliminar nucleótidos y regiones problemáticas, mejorando la confiabilidad de las secuencias utilizadas en el análisis posterior.
El ensamblaje y procesamiento de las lecturas permitieron generar una secuencia consenso representativa del fragmento amplificado del gen *recA*. Este procedimiento facilitó el análisis molecular del aislamiento bacteriano y demostró la utilidad de las herramientas bioinformáticas para el tratamiento y validación de datos genéticos.
El análisis de similitud mediante BLAST en la base de datos NCBI mostró una identidad aproximada del 88.6 % con secuencias asociadas al género Vibrio. Aunque este porcentaje indica afinidad taxonómica con dicho grupo bacteriano, la coincidencia parcial sugiere la posibilidad de variaciones genéticas, regiones incompletas o la presencia de una cepa poco caracterizada, por lo que no fue posible confirmar con total precisión la especie bacteriana.
El gen *recA* demostró ser un marcador molecular útil para la identificación bacteriana y el análisis filogenético, debido a su conservación entre especies relacionadas y su importancia funcional en procesos de recombinación y reparación del ADN.
En términos generales, el flujo de trabajo aplicado —incluyendo aislamiento bacteriano, extracción de ADN, amplificación por PCR, secuenciación y análisis bioinformático— permitió establecer una identificación molecular preliminar compatible con bacterias del género Vibrio presentes en muestras ambientales. Sin embargo, se recomienda complementar el estudio mediante la secuenciación de otros genes marcadores o mediante una mayor cobertura de secuenciación para confirmar con mayor exactitud la clasificación taxonómica del microorganismo analizado.

## 6. Referencias Bibliograficas
1. Durand, K., Ogier, J.-C., & Nam, K. (2025). The evaluation of shotgun sequencing and rpoB metabarcoding for taxonomic profiling of bacterial communities. BMC Microbiology, 25(1), 413. https://doi.org/10.1186/s12866-025-04149-3
2. Jurvansuu, J., Länsivaara, A., Palmroth, M., Kaarela, O., Hyöty, H., Oikarinen, S., & Lehto, K.-M. (2025). Machine learning-based identification of wastewater treatment plant-specific microbial indicators using 16S rRNA gene sequencing. Scientific Reports, 15(1), 23771. https://doi.org/10.1038/s41598-025-07952-0
3. Nunes Ramos, J., Veloso da Costa, L., Viana Vieira, V., & Lima Brandão, M. L. (2025). Challenges in the Identification of Environmental Bacterial Isolates from a Pharmaceutical Industry Facility by 16S rRNA Gene Sequences. DNA, 5(3), 33. https://doi.org/10.3390/dna5030033
4. Valido, E., Bertolo, A., & Stoyanov, J. (2025). Quantitative profiling of bacterial communities via full length 16S rRNA gene sequencing with internal controls: optimization and validation across diverse human microbiomes. BMC Microbiology, 25(1), 710. https://doi.org/10.1186/s12866-025-04399-1
5. Wang, C., Yang, Y., Xu, X., Wang, D., Shi, X., Liu, L., Deng, Y., Li, L., & Zhang, T. (2025). The quest for environmental analytical microbiology: absolute quantitative microbiome using cellular internal standards. Microbiome, 13(1), 26. https://doi.org/10.1186/s40168-024-02009-2 

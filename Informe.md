#IDENTIFICACION DE BACTERIAS AMBIENTALES CON GEN HOUSEKEPPING recA
## Integrantes  
 Joel Malacatus  
 Christian Valdez  
 Helen Correa  
 Stephen Sarmiento  
## Objetivo:    

## 1. Introducción  

## 2. Metodología  

## 3. Resultados  
### Resultados del ensamblaje
El ensamblaje de las secuencias forward y reverse mediante EMBOSS merger permitió generar secuencias consenso representativas del gen recA para las muestras 7, 21 y 22. Los alineamientos obtenidos mostraron altos porcentajes de identidad y similitud, evidenciando una adecuada correspondencia entre las lecturas analizadas.

| Muestra | Longitud (pb) | Identity (%) | Similarity (%) | Gaps (%) | Score |
|---|---|---|---|---|---|
| 7 | 702 | 88.6 | 88.6 | 11.4 | 3100.0 |
| 21 | 703 | 87.8 | 87.8 | 12.2 | 3085.0 |
| 22 | 702 | 88.0 | 88.0 | 12.0 | 3090.0 |

Estos resulatdos indican que las secuencias forward y reverse presentan una elevada correspondencia, permitiendo la obtención de secuencias consenso confiables para análisis taxonómicos posteriores. Los porcentajes de identidad cercanos al 88% sugieren la presencia de regiones conservadas del gen recA, mientras que los gaps observados podrían asociarse a pequeñas variaciones genéticas, diferencias entre cepas bacterianas o regiones afectadas por el proceso de secuenciación.

### Resultados BLAST
Las secuencias consenso obtenidas fueron analizadas mediante BLAST en NCBI BLAST, obteniéndose coincidencias predominantes con bacterias del género Vibrio.

| Muestra | Principales coincidencias | Similitud (%) |
|---|---|---|
| 7 | Vibrio sp., Vibrio chaetopteri | 90.74 – 100 |
| 21 | Vibrio sp., Vibrio ichthyoenteri, Vibrio pelagius | 87.06 – 100 |
| 22 | Vibrio sp., Vibrio frotis | 87.4 – 100 |

Los resultados sugieren que las muestras analizadas pertenecen a bacterias estrechamente relacionadas con el género Vibrio, un grupo ampliamente distribuido en ambientes acuáticos y reconocido por su importancia ecológica y clínica. La presencia de múltiples coincidencias con porcentajes elevados de similitud indica una conservación importante del gen recA entre las especies identificadas.

## 4. Discusión  
El flujo de trabajo bioinformático aplicado permitió obtener secuencias consenso confiables del gen recA mediante control de calidad, trimming y ensamblaje de lecturas forward y reverse. La mejora observada en la calidad de las secuencias después del procesamiento permitió reducir regiones problemáticas y obtener lecturas aptas para análisis taxonómicos, aspecto considerado fundamental en estudios de secuenciación bacteriana (Valido, Bertolo, & Stoyanov, 2025).

Los ensamblajes obtenidos presentaron porcentajes de identidad cercanos al 88%, permitiendo generar secuencias consenso representativas de las muestras analizadas. Los gaps observados podrían relacionarse con variaciones genéticas entre cepas bacterianas o regiones parcialmente conservadas, fenómeno frecuente en microorganismos ambientales (Durand, Ogier, & Nam, 2025).

El análisis mediante BLAST mostró coincidencias predominantes con bacterias del género Vibrio, grupo ampliamente distribuido en ambientes acuáticos y caracterizado por una elevada diversidad genética (Jurvansuu et al., 2025). Sin embargo, aunque se obtuvieron porcentajes altos de similitud, no fue posible confirmar con precisión la especie bacteriana, posiblemente debido a limitaciones en la cobertura de las bases de datos o a la variabilidad genética de los aislamientos ambientales (Nunes Ramos, Veloso da Costa, Viana Vieira, & Lima Brandão, 2025).

Finalmente, el gen recA demostró ser un marcador molecular útil para la identificación preliminar de bacterias ambientales y el análisis taxonómico de los aislamientos estudiados (Wang et al., 2025).

## 5. Conclusiones  
# 🧬 Discusión

El flujo de trabajo bioinformático aplicado permitió obtener secuencias consenso confiables del gen *recA* mediante control de calidad, trimming y ensamblaje de lecturas forward y reverse. La mejora observada en la calidad de las secuencias después del procesamiento permitió reducir regiones problemáticas y obtener lecturas aptas para análisis taxonómicos, aspecto considerado fundamental en estudios de secuenciación bacteriana [1].

Los ensamblajes obtenidos presentaron porcentajes de identidad cercanos al 88%, permitiendo generar secuencias consenso representativas de las muestras analizadas. Los gaps observados podrían relacionarse con variaciones genéticas entre cepas bacterianas o regiones parcialmente conservadas, fenómeno frecuente en microorganismos ambientales [2].

El análisis mediante BLAST mostró coincidencias predominantes con bacterias del género *Vibrio*, grupo ampliamente distribuido en ambientes acuáticos y caracterizado por una elevada diversidad genética [3]. Sin embargo, aunque se obtuvieron porcentajes altos de similitud, no fue posible confirmar con precisión la especie bacteriana, posiblemente debido a limitaciones en la cobertura de las bases de datos o a la variabilidad genética de los aislamientos ambientales [4].

Finalmente, el gen *recA* demostró ser un marcador molecular útil para la identificación preliminar de bacterias ambientales y el análisis taxonómico de los aislamientos estudiados [5].

## Referencias Bibliograficas

1. Valido E, Bertolo A, Stoyanov J. *Quantitative profiling of bacterial communities via full length 16S rRNA gene sequencing with internal controls: optimization and validation across diverse human microbiomes*. BMC Microbiol. 2025;25:710. doi:10.1186/s12866-025-04399-1

2. Durand K, Ogier JC, Nam K. *The evaluation of shotgun sequencing and rpoB metabarcoding for taxonomic profiling of bacterial communities*. BMC Microbiol. 2025;25:413. doi:10.1186/s12866-025-04149-3

3. Jurvansuu J, Länsivaara A, Palmroth M, Kaarela O, Hyöty H, Oikarinen S, et al. *Machine learning-based identification of wastewater treatment plant-specific microbial indicators using 16S rRNA gene sequencing*. Sci Rep. 2025;15:23771. doi:10.1038/s41598-025-07952-0

4. Nunes Ramos J, Veloso da Costa L, Viana Vieira V, Lima Brandão ML. *Challenges in the Identification of Environmental Bacterial Isolates from a Pharmaceutical Industry Facility by 16S rRNA Gene Sequences*. DNA. 2025;5(3):33. doi:10.3390/dna5030033

5. Wang C, Yang Y, Xu X, Wang D, Shi X, Liu L, et al. *The quest for environmental analytical microbiology: absolute quantitative microbiome using cellular internal standards*. Microbiome. 2025;13:26. doi:10.1186/s40168-024-02009-2



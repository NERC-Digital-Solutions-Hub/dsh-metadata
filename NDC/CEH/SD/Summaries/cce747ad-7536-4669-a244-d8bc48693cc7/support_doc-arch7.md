# Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food). Brunner, F.S., Reynolds, A., Price, S., Atkinson, D.A., Paterson, S., and Plaistow, S.J. (2022)

## Overview
- A factorial laboratory experiment assessing additive genetic variation and plasticity in Daphnia magna across four rearing environments created by crossing two temperatures and two food levels.
- 56 clones (43 UK, 5 French, 8 Danish) sourced from multiple geographic locations; clones reared across multiple temporal blocks (2017–2018).
- Measured thermal tolerance (CTmax) and eight life-history traits per individual, enabling analysis of genotype-by-environment (G×E) interactions and plastic responses.

## Experimental design
- Clones originated from three geographic sources: UK (Brown Moss, Shropshire), France (Camargue), Denmark (Lake Ring).
- Pre-experiment maternal effect reduction: offspring from each clone produced a clutch; one offspring selected and reared for two generations before experimentation.
- Four experimental treatments: crossing two temperatures (24°C and 18°C) with two food levels (2x10^5 and 0.4x10^5 C. vulgaris cells ml^-1 day^-1).
- Each clone assayed in multiple temporal blocks; 3–8 second-clutch neonates per clone allocated to treatments.
- Traits monitored include CTmax and eight life-history metrics (see Data Structure).

## Sampling regime and collection methods
- Individuals photographed at three key life stages: neonate, maturity (first eggs), and after second clutch.
- Measurements:
  - Offspring counts in clutch 1 and 2.
  - Neonate size (5 offspring per clutch) via ImageJ.
  - Body size metrics: length from head to base of tail-spine.
  - Thermal tolerance: CTmax assay with acclimation then ramping from 21°C to 50°C.
- Life-history traits derived: age at maturation, age at second clutch, sizes at various stages, juvenile and adult growth rates, fecundity, and average offspring size.

## Quality control
- All data checked, verified, and processed for analysis.

## Data structure
- Data provided as a comma-separated values (CSV) file.
- Data Set 1: Multivariate plasticity data set.
- Key columns and concepts:
  - Clone, Rep, Block, Tray, T (temperature treatment), food (food treatment), treat (treatment group).
  - cl1No (offspring in clutch 1), cl1moult (moult after clutch 1), cl2No (offspring in clutch 2), cl2moult (moult after clutch 2).
  - agemat (age at maturation), Age1cl (days after first clutch), Age2cl (days after second clutch).
  - Lneo (neonate size), LMat (size at maturation), L2cl (size at second clutch).
  - cl1size, cl2size (mean neonate size for each clutch), Htdate (date of thermal tolerance assay).
  - Tfaint, Timm (temperatures related to loss of motor control and immobility during CTmax).
  - obs (observer initials), clutchpresHT, HTBatch (thermal tolerance batch).
  - aveclNo (mean offspring across clutches), aveoffsize (mean offspring size), grjuv (juvenile growth rate), grad (adult growth rate), Pop (population/origin factor).
- Data capture supports analyses of genetic variation and plasticity across environments.

## Geographic and provenance context (relevance for GIS)
- Origins span three countries, enabling potential spatial analyses of genetic and phenotypic variation by geographic source.
- Experimental design emphasizes environmental manipulation rather than field sampling alone, but the geographic provenance can be integrated with spatial metadata for map-based visualisations of clone origins and their associated trait patterns under different environmental conditions.

## References
- Geerts AN, et al. (2015) Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change.
- Plaistow SJ, Collin H (2014) Phenotypic integration plasticity in Daphnia magna: an integral facet of G × E interactions. J Evol Biol.
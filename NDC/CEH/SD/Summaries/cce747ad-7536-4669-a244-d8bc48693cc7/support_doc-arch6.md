# Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food). Brunner, F.S., Reynolds, A., Price, S., Atkinson, D.A., Paterson, S., and Plaistow, S.J. (2022)

## Overview
- Dataset from a factorial cross experiment on Daphnia magna to compare additive genetic variation and plasticity across environments.
- 56 clones (43 UK, 5 French, 8 Danish) reared in four environments created by crossing two temperature levels and two food levels.
- Measurements focus on life-history traits and thermal tolerance (CT max) at multiple developmental stages.
- Data organized as a CSV with extensive metadata to enable cross-clone and cross-environment analyses.
- Collected across five temporal blocks (2017–2018) to ensure replication across conditions.

## Experimental design
- Clones and origins
  - 56 clones: 43 from Brown Moss (UK, collected 2016), 5 French clones (Camargue, 2007), 8 Danish clones (Lake Ring, 2000).
- Rearing conditions
  - Common lab conditions: 21°C ± 1°C, 14:10 light:dark cycle.
  - Artificial pond water with added organic extracts; high-ration food.
  - Food: batch-cultured Chlorella vulgaris.
- Generational approach to reduce maternal effects
  - From each clone, three females reared and produced a clutch; one offspring from that clutch used for further rearing.
  - In the third generation, 3–8 second-clutch neonates per clone allocated to four treatments.
- Treatments and replication
  - Temperature: 24°C and 18°C.
  - Food levels: 2x10^5 and 0.4x10^5 cells mL^-1 day^-1.
  - Each clone assayed in multiple blocks; experiments conducted in five temporal blocks between Jan 2017 and Mar 2018.
- Sampling and tracking
  - Individuals photographed at neonate stage, maturity, and after second clutch.
  - Daily observations; routine transfers to fresh media and food every other day.

## Sampling regime and data collection
- Photography and measurements
  - Neonates, mature individuals, and post-second-clutch individuals photographed with Canon EOS 350D and Leica MZ6 microscope.
  - Offspring counts per clutch: cl1No and cl2No; 5 neonates per clutch photographed for size estimates.
  - Body size: length from head top to base of tail-spine measured with ImageJ.
- Life-history traits measured per individual
  - Length at maturity (LMat) and at second clutch (L2cl).
  - Age at maturity (agemet) and age at second clutch (Age2cl).
  - Juvenile growth rate (grams per day; calculated as (LMat - Lneo)/agemet).
  - Adult growth rate (mm per day; calculated as (L2cl - LMat)/(Age2cl - agemet)).
  - Average fecundity across clutches 1 and 2 (aveclNo).
  - Average offspring size across clutches 1 and 2 (aveoffsize).
- Thermal tolerance
  - CT max measured after a 15-minute acclimation at 21°C, followed by a ramp from 21°C to 50°C at 40 s/°C.
- Data quality
  - All data were checked, verified, and processed for analysis.

## Data structure
- Data set: Multivariate plasticity data set.
- Key columns (highlights)
  - Clone, Rep (replicate), Block (experimental block), Tray.
  - T (temperature treatment), food (food treatment), treat (treatment group).
  - cl1No, cl1moult; cl2No, cl2moult.
  - agemat; Age1cl; Age2cl.
  - Lneo; LMat; L2cl.
  - cl1size; cl2size; Htdate; Tfaint; Timm.
  - obs; clutchpresHT; HTBatch.
  - aveclNo; aveoffsize; grjuv; grad; Pop.
- Notes
  - Data structure supports analyses of phenotypic plasticity and genetic variation across environment combinations.
- References for methods
  - Geerts et al. (2015) on rapid evolution of thermal tolerance.
  - Plaistow & Collin (2014) on phenotypic integration and G×E interactions.

## Potential uses and implications
- Enables examination of additive genetic variation and plastic responses across temperature and food environments.
- Facilitates analyses of genotype-by-environment interactions in life-history traits and thermal tolerance.
- Data products could include dashboards or summaries of clone-level trait means and plasticity across treatments.
- Supports broader meta-analyses and comparative studies on phenotypic plasticity, adaptation, and life-history evolution in Daphnia.

## References
- Geerts AN, Vanoverbeke J, Vanschoenwinkel B, et al. (2015). Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change, 5: 665-668.
- Plaistow SJ, Collin H (2014). Phenotypic integration plasticity in Daphnia magna: an integral facet of G × E interactions. J Evol Biol, 27: 1913-1920.
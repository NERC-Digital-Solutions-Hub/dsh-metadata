# Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food)

## Objective
- Examine additive genetic variation and its alignment with plasticity by rearing 56 Daphnia magna clones across a factorial cross of temperature and food environments.
- Assess multivariate life-history traits and thermal tolerance to understand environmental responses and genotype-by-environment interactions.

## Experimental design
- Clones: 56 total (43 UK, 5 French, 8 Danish).
  - UK: Resting eggs from Brown Moss, Shropshire (collected 2016).
  - French: 5 clones from Camargue (2007).
  - Danish: 8 clones from Lake Ring (2000).
- Laboratory stock conditions: 21°C ± 1°C; 14:10 light:dark; 200 ml jars with 150 ml artificial pond water (ASTM) plus organic extracts; fed high-ration C. vulgaris.
- Maternal effects reduction: from each clone, three females isolated; offspring reared to third generation to minimize maternal effects; 3–8 second-clutch neonates per clone assigned to treatments.
- Treatments: 4 rearing environments from crossing temperature and food.
  - Temperature: 24°C and 18°C.
  - Food: 2×10^5 and 0.4×10^5 C. vulgaris cells ml^-1 day^-1.
- Experimental blocks: 5 temporal blocks (Jan 2017 – Mar 2018); each clone assayed in multiple blocks.

## Sampling regime and collection methods
- Photography: neonates, maturity (first eggs in brood pouch), and second-clutch release photographed with a Canon EOS 350D and Leica MZ6 microscope.
- Offspring counts: number of neonates in clutch 1 and clutch 2 tallied; 5 neonates per clutch photographed for size estimates.
- Body size: measured as distance from head top to base of tail-spine using ImageJ.
- Thermal tolerance: CT max measured after 15 min acclimation at 21°C; ramp from 21°C to 50°C at 40 s/°C with monitoring of motor function.

## Traits measured
For each individual, eight life-history traits plus thermal tolerance were recorded:
- Length at maturity (LMat)
- Length at second clutch (L2cl)
- Age at maturity (agemet)
- Age at second clutch (Age2cl)
- Juvenile growth rate (grjuv)
- Adult growth rate (grad)
- Average fecundity across clutches 1 and 2 (aveclNo)
- Average offspring size across clutches 1 and 2 (aveoffsize)
- Thermal tolerance (CT max)

## Quality control
- All data were checked, verified, and processed for analysis.

## Data structure
- Data are provided as a comma-separated values (CSV) file with the following structure (Data Set 1 - Multivariate plasticity data set):
  - Clone, Description (sampling period)
  - Rep, Description (replicate within treatment block)
  - Block, Description (experimental block)
  - Tray, Description (tray within incubator)
  - T, Description (temperature treatment)
  - food, Description (food treatment)
  - treat, Description (treatment group)
  - cl1No, cl2No (offspring in clutch 1 and 2)
  - cl1moult, cl2moult (evidence of molt after clutches)
  - agemat (age at maturation)
  - Age1cl, Age2cl (ages after clutches 1 and 2)
  - Lneo (neonate size)
  - LMat, L2cl (size at maturation and size at second clutch)
  - cl1size, cl2size (mean neonate size per clutch)
  - Htdate (date of thermal tolerance assay)
  - Tfaint, Timm (temperatures related to loss of motor control and immobility)
  - obs (observer initials)
  - clutchpresHT, HTBatch (clutch presence during CT assay, CT batch)
  - aveclNo, aveoffsize (mean offspring per clutch; mean offspring size)
  - grjuv (juvenile growth rate)
  - grad (adult growth rate)
  - Pop (population of origin factor)

## References
- Geerts AN, et al. (2015) Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change.
- Plaistow SJ, Collin H (2014) Phenotypic integration plasticity in Daphnia magna: an integral facet of G×E interactions. J Evol Biol.
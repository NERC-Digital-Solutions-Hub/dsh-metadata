# Supporting Document
Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food). Brunner, F.S., Reynolds, A., Price, S., Atkinson, D.A., Paterson, S., and Plaistow, S.J. (2022)

## Experimental design
- Organisms and origin: 56 Daphnia magna clones (43 UK, 5 French, 8 Danish) collected as resting eggs from Brown Moss (UK) in 2016, plus additional clones from France and Denmark. Eggs hatched at 21°C on a 14:10 light:dark cycle; maintained as laboratory stock at 21°C ± 1°C.
- Rearing conditions: 200 mL jars with 150 mL artificial pond water media, enriched with organic extracts, and fed high-ration Chlorella vulgaris (≈200,000 cells mL⁻¹) three times weekly; media refreshed biweekly.
- Experimental design: 56 clones reared across a 2×2 factorial of temperature and food to study additive genetic variation and plasticity. 
  - Maternal effect control: from each clone, three females were isolated to produce a clutch; one offspring from that clutch was raised for two generations to minimize maternal effects.
  - Experimental treatments: in the 3rd generation, 3–8 second-clutch neonates per clone assigned to four rearing treatments created by crossing temperature (24°C vs 18°C) and food levels (high vs low).
  - Temporal structure: five blocks spanning January 2017 to March 2018; each clone assayed in multiple blocks.
- Sampling cadence: daily observations; jars transferred to fresh media/food every other day until second clutch dropped.

## Sampling regime and collection methods
- Imaging: neonates, mature individuals, and those releasing their second clutch photographed with a Canon EOS 350D attached to a Leica MZ6 microscope.
- Reproduction data: counted offspring in first and second clutches; five neonates per clutch photographed to estimate offspring size.
- Growth and size metrics: body size measured as head-to-tail-spine length using ImageJ.
- Thermal tolerance: CTmax measured after second clutch release with a 15-minute acclimation at 21°C, then a ramp from 21°C to 50°C at 40 s/°C.
- Traits measured per individual (8 life-history traits plus CTmax): 
  - Length at maturity
  - Length at second clutch
  - Age at maturity
  - Age at second clutch
  - Juvenile growth rate (length at maturity − length as neonate) / age at maturity
  - Adult growth rate (length at second clutch − length at maturity) / (age at second clutch − age at maturity)
  - Average fecundity (across clutches 1 and 2)
  - Average offspring size (across clutches 1 and 2)
  - Thermal tolerance (CTmax)
  
## Quality control
- All data have been checked, verified, and processed for analysis to ensure accuracy and consistency across blocks, treatments, and measurements.

## Data structure
- Data set: Multivariate plasticity data set (Dataset 1)
- Format: Comma-separated values (CSV)
- Key columns (examples):
  - Clone, Rep (replicate), Block (experimental block), Tray, T (temperature treatment), food (food treatment), treat (treatment group)
  - cl1No, cl1moult, cl2No, cl2moult
  - agemat (age at maturation), Age1cl, Age2cl
  - Lneo (neonate size), LMat (maturity size), L2cl (size at second clutch)
  - cl1size, cl2size (mean neonate size for clutches 1 and 2)
  - Htdate (date of thermal tolerance assay), Tfaint (temperature at loss of motor control), Timm (temperature at immobility)
  - obs (observer initials), clutchpresHT (clutch present during HT), HTBatch
  - aveclNo (mean offspring across clutches 1 & 2), aveoffsize (mean offspring size)
  - grjuv (juvenile growth rate), grad (adult growth rate)
  - Pop (population of origin)
- Purpose: Enables analysis of additive genetic variation and its alignment with plasticity across environments, as well as correlations among life-history traits and thermal tolerance.

## References
- Geerts AN, Vanoverbeke J, Vanschoenwinkel B, Van Doorslaer W, Feuchtmayr H, Atkinson D, Moss B, Davidson TA, Sayer CD, De Meester L (2015) Rapid evolution of thermal tolerance in the water flea Daphnia. Nature Climate Change, 5: 665-668
- Plaistow SJ, Collin H (2014) Phenotypic integration plasticity in Daphnia magna: an integral facet of G × E interactions. J Evol Biol, 27: 1913-1920
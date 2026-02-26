# Multivariate Life-history phenotype of 56 Daphnia magna clones reared in four different environments (Factorial cross of temperature x food)

- The study investigates additive genetic variation and plasticity by rearing 56 Daphnia magna clones across a factorial cross of temperature and food environments (2 temperatures x 2 food levels).
- Clones originate from the UK (43), France (5), and Denmark (8); eggs collected from their natural habitats and reared under controlled laboratory conditions.

## Experimental design

- Clones and origins
  - 43 UK clones; 5 French clones (Camargue); 8 Danish clones (Lake Ring).
  - Clones stored as resting eggs, hatched and maintained in a controlled incubator.
- Generational design to reduce maternal effects
  - From each clone, three females were isolated and reared to produce a clutch.
  - One offspring from that clutch was reared individually for two generations before experimental treatments.
- Treatment structure
  - Four rearing treatments created by crossing:
    - Temperature: 24°C and 18°C
    - Food: 2x10^5 cells ml^-1 day^-1 and 0.4x10^5 cells ml^-1 day^-1 of batch-cultured Chlorella vulgaris
- Replication and blocks
  - 3–8 second-clutch neonates per clone allocated to treatments.
  - Experiments conducted in 5 temporal blocks from January 2017 to March 2018, with each clone assayed in multiple blocks.

## Sampling regime and collection methods

- Timepoints and imaging
  - Neonates photographed at birth, at maturity (first eggs in brood pouch), and after second clutch.
  - Imaging performed with a Canon EOS 350D linked to a Leica MZ6 microscope.
- Reproduction and body measurements
  - Offspring counts in first and second clutches; five neonates per clutch photographed to estimate offspring size.
  - Body size measured as distance from top of head to base of tail-spine using ImageJ.
- Thermal tolerance
  - CT max measured after a 15-minute acclimation at 21°C, followed by a ramp from 21°C to 50°C at 40 seconds per degree.
- Data per individual
  - Eight life-history traits plus thermal tolerance recorded.

## Measurements and traits

- Life-history traits (per individual)
  - Length at maturity
  - Length at second clutch
  - Age at maturity
  - Age at second clutch
  - Juvenile growth rate (mm/day)
  - Adult growth rate (mm/day)
  - Average fecundity (across clutches 1 and 2)
  - Average offspring size (across clutches 1 and 2)
- Thermal tolerance
  - CT max (thermal tolerance limit)

## Data structure and lifecycle

- Data format
  - Data provided as a comma-separated values (CSV) file.
- Data set 1 – Multivariate plasticity data set
  - Key columns include:
    - Clone, Description, Rep, Block, Tray, T (temperature), food, treat
    - cl1No, cl1moult, cl2No, cl2moult
    - agemat, Age1cl, Age2cl
    - Lneo (neonate size), LMat (size at maturity), L2cl (size at second clutch)
    - cl1size, cl2size (mean neonate size per clutch)
    - Htdate (date of thermal tolerance assay), Tfaint, Timm (CT max)
    - obs (observer initials), clutchpresHT, HTBatch
    - aveclNo, aveoffsize, grjuv, grad, Pop (population/origin factor)
- Metadata and provenance
  - Experimental blocks and replications recorded to support G×E and plasticity analyses.
  - References cited for methods and context on rapid thermal adaptation and phenotypic integration.

## Quality control and data management

- All data have been checked, verified, and processed for analysis to ensure reliability of the measurements and trait calculations.

## Dataset provenance and references

- Clonal origins (UK, France, Denmark) and hatch/maintenance protocols described.
- Foundational references:
  - Geerts et al. 2015 on rapid evolution of thermal tolerance in Daphnia
  - Plaistow & Collin 2014 on phenotypic integration and G×E interactions

## Data reuse considerations for data leaders

- End-to-end data lifecycle
  - Clear documentation of clone origins, rearing conditions, treatments, and temporal blocks supports reproducibility and cross-institution collaboration.
- Cross-environment design
  - Factorial temperature x food design enables assessment of genetic variation and plasticity in life-history and thermal traits.
- Comprehensive trait suite
  - Eight life-history traits plus CT max allow integrative analyses of growth, reproduction, and stress tolerance.
- Metadata and discoverability
  - Detailed column definitions and sampling regime facilitate data discovery, integration with other datasets, and meta-analyses.
- Practical governance notes
  - Maternal effects mitigated through generational design; multiple blocks reduce confounding temporal variation; standardized imaging and measurement protocols support consistency across datasets.
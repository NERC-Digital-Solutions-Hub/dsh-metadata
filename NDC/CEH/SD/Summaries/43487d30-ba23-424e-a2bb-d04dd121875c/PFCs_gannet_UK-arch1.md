# PFC data in Gannet eggs from Bass Rock and Ailsa Craig (UK) 1977-2013

## Overview of the dataset
- PFC concentrations reported as ng/g wet weight in egg samples from two UK gannet colonies: Bass Rock and Ailsa Craig.
- Sampling period: 1977–2013; samples were frozen after collection until analysis.
- Samples analyzed by UPLC-QQQ after solid-liquid extraction and cleanup.

## Analytical Method
- Sample preparation:
  - Homogenised whole eggs; 1 g wet weight per sample.
  - Spiked with 13C-labelled internal standards (13C-PFOS and 13C-PFOA).
  - Incubation at 4°C for 18 hours; extraction with acetonitrile; vortexing and ultrasonication repeated three times without solvent exchange.
  - Centrifugation; supernatant dried and reconstituted in acetonitrile.
  - Cleanup with 25 mg activated carbon and 50 µL glacial acetic acid; final centrifugation and dilution with mobile phase.
- Instrumentation:
  - UPLC system (BEH C18 column) connected to a triple quadrupole MS in negative electrospray ionisation.
  - Column setup includes a residue-trap and RP-18e column for separation.
  - Gradient: start 70% A/30% B, ramp to 90% B in 5 minutes, to 100% B quickly, hold briefly, flow 0.4 mL/min.
- Analytes:
  - Ten perfluorinated carboxylic acids (PFCAs) and three perfluorinated sulfonates (PFSs) listed in the study.
- Quality control:
  - Batch blanks; surrogates 13C-PFOA and 13C-PFOS used to assess recovery.
  - Reported recoveries: 72%–144% across compounds.
  - Method detection limits (LOD): PFCAs 0.015–0.107 ng/g; PFOS 0.137 ng/g; PFDS 0.028 ng/g; PFHxS 0.084 ng/g.
  - Target analytes are recovery-corrected.

## Compounds Analysed
- Two groups: Perfluorinated sulfonates (PFSs) and Perfluorinated carboxylic acids (PFCAs).
- PFSs example compounds include PFHxS, PFOS, PFDS.
- PFCAs include PFBA, PFOA, PFNA, PFDA, PFUnA, PFDoA, PFTriDA, PFTeDA, PFPeDA, PFHxA, PFHxA variants, among others.
- Table 1 (as referenced) lists the full set of analysed compounds with abbreviations and carbon chain lengths.

## Data Structure and Availability
- Two CSV files: Results_Ailsa_Craig.csv and Results_Bass_Rock.csv.
- Each file contains 13 columns:
  - Column 1: Location of the sample.
  - Column 2: Year the sample was recovered.
  - Columns 3–10: Results for the PFSs (ng/g wet weight).
  - Columns 11–13: Results for the PFCAs (ng/g wet weight).
- The data are structured to enable temporal (year-by-year) and site-based comparisons, as well as cross-compound correlation analyses.

## Potential Analyses and Considerations for Data Analysts
- Assess temporal trends in specific PFCs and in total PFC burden per colony.
- Compare geographic differences between Bass Rock and Ailsa Craig across years.
- Explore correlations among PFSs and among PFCAs, and between solvents or methodological variables if metadata allow.
- Apply recovery-corrected concentrations and consider LODs when handling non-detects.
- Use the dataset to inform exposure assessments in seabird populations or to calibrate predictive models of PFC transfer to eggs.
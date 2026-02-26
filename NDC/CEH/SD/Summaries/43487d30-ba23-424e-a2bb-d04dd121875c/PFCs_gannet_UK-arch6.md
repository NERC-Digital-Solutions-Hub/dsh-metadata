# PFC data in gannet eggs from Bass Rock and Ailsa Craig

## Overview
- Data described as ng/g wet weight from egg samples of Gannets (Morus Bassanus) collected from two UK colonies: Bass Rock and Ailsa Craig.
- Time span: 1977 to 2013.
- Analytical workflow: PFCs analysed by UPLC-QQQ after extraction in acetonitrile; samples were frozen after collection until analysis.

## Analytical Method
- Sample preparation:
  - Homogenised whole eggs; 1 g wet weight per sample.
  - Spiked with 13C-labelled internal standards (13C-PFOS, 13C-PFOA).
  - Incubation for 18 hours at 4ºC; extraction with acetonitrile and repeated vortex/ultrasound cycles (three cycles without solvent exchange).
  - Centrifugation and evaporation; residue resuspended in acetonitrile with a 10-minute ultrasonic bath.
  - Clean-up with 25 mg activated carbon and 50 µL glacial acetic acid; final centrifugation and dilution with mobile phase.
- Instrumentation:
  - UPLC system (ACQUITY) with BEH C18 column as a residue trap.
  - LC separation on LiChroCART RP-18e column with gradient elution; negative electrospray ionisation Mass Spectrometry (Triple Quadrupole) detection.
- Analytes:
  - Ten perfluorinated carboxylic acids (PFCAs) and three perfluorinated sulfonates (PFSs) listed in Table 1.
- Data produced:
  - Concentrations reported in ng/g wet weight.
- Data handling:
  - Method includes a quality-control blank per batch; recoveries calculated using surrogate standards.

## Quality Control and Detection
- Surrogate standards: 13C-PFOA and 13C-PFOS used for recovery estimation.
- Recovery range: 72% to 144% across compounds.
- Method detection limits (LOD):
  - PFCAs: 0.060 ng/g (range 0.015–0.107 ng/g across compounds).
  - PFSs: 0.028, 0.084, and 0.137 ng/g for PFDS, PFHxS, and PFOS, respectively.
- All target analytes are recovery-corrected based on internal standards.

## Compounds Analysed
- Perfluorinated sulfonates (PFSs): PFOS, PFHxS, PFDS (and related abbreviations as listed in Table 1).
- Perfluorinated carboxylic acids (PFCAs): PFBA, PFOA, PFNA, PFDA, PFUnA, PFDoA, PFTriDA, PFTeDA, PFPeDA, PFHxA, PFHxA (and related entries as listed).

## Data Structure and Availability
- Data files: Results_Ailsa_Craig.csv and Results_Bass_Rock.csv.
- Each CSV contains 13 columns:
  - Column 1: Location of the sample.
  - Column 2: Year of sample recovery.
  - Columns 3–10: Results for the PFSs.
  - Columns 11–13: Results for the PFCAs.
- Units: ng/g wet weight.
- Use-case notes for data support:
  - Useful for cross-site and temporal analyses of PFCs in seabird eggs.
  - Data structure supports merging across colonies for comparative studies, trend analyses, or dashboarding.
  - Consider data completeness by year/location and potential need for quality-filtering based on recovery or LOD considerations.
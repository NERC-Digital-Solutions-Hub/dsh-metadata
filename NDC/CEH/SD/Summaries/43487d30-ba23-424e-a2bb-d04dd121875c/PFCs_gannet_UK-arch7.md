# Overview

- Study aim and scope
  - PFC data reported as ng/g wet weight from eggs of Gannets (Morus bassanus) collected from two UK colonies: Bass Rock and Ailsa Craig.
  - Timeframe: 1977–2013; samples frozen after collection until analysis.
  - Data intended for understanding spatial and temporal trends of PFOS-related compounds in seabird eggs.

- Sampling and data collection
  - Samples taken from two colonies in the UK (Bass Rock and Ailsa Craig).
  - Eggs homogenised (1 g) and analyzed after storage; sample handling included freezing until analysis.

- Analytical method (PFCs)
  - Extraction: solid-liquid extraction from homogenised eggs; spiked with isotopically labelled internal standards (13C-PFOS, 13C-PFOA).
  - Processing: incubation at 4ºC, acetonitrile extraction, vortexing, ultrasonication, repeated cycles, centrifugation.
  - Cleanup: activated carbon and acetic acid, followed by centrifugation.
  - Instrumentation: ACQUITY UPLC coupled to a triple quadrupole mass spectrometer (negative ESI).
  - Chromatography: two-column setup with residue trapping; gradient from 70% A to 100% B; flow 0.4 mL/min.
  - Analytes: 10 perfluorinated carboxylic acids (PFCAs) and 3 perfluorinated sulfonates (PFSs) quantified (specific compounds listed in Table 1).

- Quality control and data quality
  - Blank samples included in each batch.
  - Recovery assessed with isotopically labelled surrogates; recoveries ranged from ~72% to ~144%.
  - Method detection limits (LOD): PFCAs 0.015–0.107 ng/g; PFOS group LODs 0.028–0.137 ng/g (varying by compound).
  - Target analytes recovery-corrected.
  - Method reference: Fernandez-Sanjuan et al., 2010.

- Compounds analyzed
  - Perfluorinated sulfonates (PFSs): examples include PFHxS, PFOS, PFDS, among others.
  - Perfluorinated carboxylic acids (PFCAs): examples include PFBA, PFOA, PFNA, PFDA, PFUnA, PFDoA, PFTriDA, PFTeDA, PFPeDA, PFHxA, etc. (Table 1 lists full set).

- Data structure and formats
  - Two CSV files: Results_Ailsa_Craig.csv and Results_Bass_Rock.csv.
  - Each file contains 13 columns:
    - Column 1: sample location
    - Column 2: year of sample recovery
    - Columns 3–10: results for the perfluorinated sulfonates (PFSs)
    - Columns 11–13: results for the perfluorinated carboxylic acids (PFCAs)
  - Units: ng/g wet weight.
  - Notes: dataset captures both spatial (two colonies) and temporal (1977–2013) dimensions, suitable for GIS layering and time-series analyses.

- GIS considerations and potential uses
  - Spatial mapping: plot concentrations by colony (Bass Rock vs. Ailsa Craig) across years to visualize spatial-temporal trends.
  - Data integration: join with other environmental or ecological layers (e.g., colony location coordinates, seabird exposure data) using location and year as keys.
  - Data quality: account for variability in recoveries and LODs; consider using detection frequency and censoring for non-detects.
  - Visualization ideas:
    - Time-series maps showing colony-specific median/mean concentrations per compound.
    - Compound-specific concentration choropleth maps for selected years.
    - Stacked or multi-variate maps to compare sulfonates vs. carboxylates.

- Practical considerations for GIS workflows
  - Georeferencing: Link sample records to precise colony coordinates for spatial analyses.
  - Data cleaning: address potential missing values and ensure consistent compound ordering across CSVs.
  - Uncertainty handling: incorporate LODs and recovery ranges into visualizations (e.g., confidence bands or uncertainty shading).
  - Data provenance: maintain note of analytical method, QA/QC procedures, and surrogate standards for traceability.
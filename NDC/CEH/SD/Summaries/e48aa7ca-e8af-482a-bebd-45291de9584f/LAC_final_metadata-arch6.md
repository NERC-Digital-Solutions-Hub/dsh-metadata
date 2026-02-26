# Name of datasets

## Overview
- A multi-proxy lake sediment dataset release from the LAC project, comprising seven CSV datasets that cover core data from multiple lakes and resolutions (1 cm and 2 cm where applicable).
- Datasets include a range of paleoenvironmental indicators: LOI, diatoms, biogenic silica, isotopes, XRF elemental scans, macrobiofossils, chironomids, cladocerans, pigments, and pollen.
- Data are prepared to enable self-serve exploration, with detailed metadata, quality controls, and standardized formats.

## Datasets Included
- LAC_Ruppert_1cm_dataset.csv
- LAC_Ruppert_2cm_dataset.csv
- LAC_WBP_dataset.csv
- LAC_Nor1_dataset.csv
- LAC_Nor3_dataset.csv
- LAC_AT2_1cm_dataset.csv
- LAC_AT2_2cm_dataset.csv

## Authorship and Affiliations
- Authors from Geography and Environment, University of Southampton; Environmental Change Research Centre and other UK institutions; plus international collaborators (e.g., University of Regina).
- Institutions involved include University of Southampton, University College London, University of Nottingham, University of Nottingham Malaysia Campus, and Loughborough University, among others.

## Study Design and Sampling
- One sediment sequence collected from the deepest part of each study lake using overlapping drives.
- Cores described with location, depth, coring method, and date; for Ruppert and AT2 sites, XRF scanning performed at high resolution (200 μm or 400 μm).
- Cores were subsampled in the UK into contiguous 1 cm and 2 cm sections for most analyses; some components (e.g., XRF) have fixed resolution.
- Multiple proxies analyzed along the depth axis to create integrated stratigraphies.

## Analytical Methods and Laboratory Techniques
- Loss on Ignition (LOI): 1 cm resolution; dry weight and bulk density estimated; organic matter by LOI at 550°C; carbonate by LOI at 950°C.
- Diatoms: prepared from 1 cm samples; counted with a minimum of 200 valves per sample; identified to species where possible; counts converted to % abundance and concentrations per g dry mass.
- Biogenic Silica (BSi): alkaline extraction with time-course sampling; dissolved silica measured by ICP-MS; BSi calculated from time-course data using reference standards.
- Isotopes: δ13C and δ15N measured via EA-IRMS with standards; expressed as per mil and %C/%N; data presented alongside C and N content.
- XRF Scanning: ITRAX with Mo tube; raw counts normalized by total counts; 1 cm bin averages for major elements (Ca, Fe, Ti, Zr) and Fe:Mn ratios.
- Macrofossils: continuous 1–2 cm sections, >40 μm fractions, identification against standard references; abundance expressed as numbers per 100 ml sediment or abundance scores.
- Chironomids: >40 μm residues processed and identified; counts converted to percentages and fluxes when combined with sedimentation rates.
- Cladocera: same 1–2 cm sections; counts converted to percentages and fluxes using Lycopodium markers for absolute quantification.
- Pollen: standard preparation (KOH, HF, acetylation); counts converted to percentage abundances; diagrams created with appropriate software.
- Pigments: high-performance liquid chromatography (HPLC) to quantify chlorophylls and carotenoids; results used to characterize algal communities.
- Additional proxies: Diatoms, pollen, macrofossil and invertebrate identifications guided by established taxonomic guides and referenced material.

## Data Format and Units
- Data stored as comma-separated values (CSV).
- Column headers reflect running depth (top and bottom), sample IDs, and proxy-specific measurements (e.g., LOI DW%, LOI550%DW, Wet/Dry densities, element counts, isotopic values, pigment concentrations, pollen percentages, macrofossil counts, etc.).
- Units and terminology standardized and documented in the accompanying data tables (e.g., 1 cm and 2 cm resolution datasets; running depth in cm; concentrations in SI units; abundances as percentages or counts per 100 ml as appropriate).

## Format of Stored Data and Column Mapping
- Column naming convention includes: Running_top_cm, Running_bot_cm, SubID, LOI, LOI550_%dw, WetDensity_gcc, DryDensity_gcc, BulkDensity_gcc, Ca_kcps, Fe_kcps, Ti_kcps, Zr_kcps, Fe Mn ratios, Diatoms and Diatom concentrations, DSi/BSi values, δ13C, δ15N, C%, N%, Macrofossil counts, Chydorid counts, Daphnia counts, Sphagnum scores, Pollen taxa abundances, Pigment nmol/g organic mass, and others.
- Abbreviations and units for each column are documented in a dedicated table (Table 2) accompanying the data files.

## Quality Control and Data Validation
- Ongoing checks to ensure values are above detection limits; validation against previous cores from the same locations where available.
- Taxonomic identifications cross-checked with specialist references; uncertain identifications flagged (e.g., cf, unID) in metadata and data sheets.
- QA measures include blanks, reference sediments, and calibrations for isotopes, pigments, and XRF data; cross-core comparisons where possible.

## Data Integration and Usage
- Data designed to be combined into comprehensive stratigraphies by depth, enabling multi-proxy interpretation of past environmental change.
- 1 cm and 2 cm datasets are integrated in some lakes (Nor1, Nor3, Ruppert, AT2) to provide consistent depth resolution across proxies.
- Flux calculations for certain proxies (e.g., diatoms, chironomids, cladocerans, pollen) are intended to be derived using sedimentation rates and core surface area in final analyses.

## References and Methodological Background
- Core preparation, diatom counting, pigment analysis, and pollen techniques are grounded in established methods and key references (e.g., Renberg 1990 for diatoms; Dean 1974 for LOI; Conley & Schelske 2001; Harris et al. 2001; Moore et al. 1991; Grimm 2002; Birks et al.; Sphagnum and macrofossil identification guides).
- Instrumentation and data processing references include ITRAX core scanner methodology (Croudace et al. 2006) and BEIF isotope facility procedures.
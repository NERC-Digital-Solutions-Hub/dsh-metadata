# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

## Overview
- Investigates whether Salmonella Typhimurium and Vibrio cholerae can transfer from plastic mulch (plastics, hay, or culture) to basil and spinach leaves and persist on leaf surfaces.
- Demonstrates persistence on plastic mulch-adhering fragments for up to 14 days and rapid transfer to leaf surfaces within 24 hours.
- Highlights food-safety risks associated with plastic-mediated plastisphere contamination in agricultural systems and the limitations of washing or plastic removal in fully mitigating risk.
- Data accompanying the study are provided as seven CSV files (datasets) and were collected in Oct–Nov 2023.

## Datasets included (CSV files)
- Cholera_Endophytic_CFUs.csv
- Cholera_epiphytic_CFUs.csv
- Cholera_persistence_plastic_hay_CFUs.csv
- Salmonella_Endophytic_CFUs.csv
- Salmonella_Epiphytic_CFUs.csv
- Salmonella_persistence_plastic_hay_CFUs.csv
- STyphimurium_R_squared_Gradient_K_value_D_value.csv

## Data structure, variables, and units
- Sample_ID encodes: plant type (Basil/B spinach) - material (Plastic/Hay/Culture) - leaf surface (Adaxial/Abaxial) - timepoint (days) - replicate.
- Timepoints: 0, 1, 2, 3, 4, 7, 10, 14 days.
- Measured values:
  - Colonies: CFU counts on LB agar with chloramphenicol.
  - Dilution: 10-fold dilution factor used for plating.
  - CFU_per_leaf: CFU per total leaf surface.
  - CFU_per_ml: CFU per millilitre of solution.
  - CFU_per_mm2: CFU per square millimetre (where applicable).
- Data derived from three study components:
  - Endophytic: bacteria inside leaf tissue after surface processing.
  - Epiphytic: bacteria on leaf surface after washing surface material away.
  - Persistence: bacteria recovered from plastic, hay, or culture material.

## Experimental design and data collection
- Basil and spinach leaves placed in petri dishes with wet cotton pads; material applied to leaf surface (via tweezers or pipette) and incubated until designated timepoints.
- Sampling on days 0, 1, 2, 3, 4, 7, 10, and 14; four replicates per timepoint; negative controls included.
- Material analysis (plastic mulch and hay): leaves washed, suspensions serially diluted, plated on LB with chloramphenicol; colonies counted after 24 h at 37°C.
- Epiphytic analysis: leaf surface washes collected, diluted, plated as above.
- Endophytic analysis: leaves washed with 70% ethanol to remove surface bacteria, tissue crushed and resuspended in PBS, then plated.
- All data are reported as CFU counts.

## Quality control and data completeness
- No missing data across datasets; all timepoints present in four replicates.
- Zero CFU interpretations indicate no colonies recovered.
- No SOPs referenced for workflow; data processing converted raw CFU readings to final concentrations per leaf, per mL, or per mm2 as appropriate.

## Data governance, interoperability, and sharing considerations for Data Stewards
- Data are multi-part and multi-material (plastic mulch, hay, culture) with consistent CFU-based measurements across endophytic, epiphytic, and persistence contexts.
- Uniform coding in Sample_ID supports cross-dataset integration but would benefit from a controlled vocabulary and a data dictionary to ensure unambiguous interpretation of codes (B/S, PE/GR/CO, A/B, timepoint, replicate).
- Datasets are CSV-based, facilitating reuse but requiring clear metadata (units, assay conditions, media, incubation details) for interoperability.
- Safety considerations: work involves pathogenic organisms; ensure appropriate handling, licensing, and distribution controls when sharing data beyond research use.
- Publication and citation: data are associated with Heliyon 2024 article by Woodford et al. (doi: 10.1016/j.heliyon.2024.e31343).

## Temporal and collection context
- Temporal coverage: experiments conducted October–November 2023.
- Sampling scheme captures dynamics from immediate exposure (day 0) through day 14 for all three components (endophytic, epiphytic, persistence).

## Key implications for data stewardship and reuse
- The datasets enable analysis of transfer kinetics (rapid transfer within 24 h) and persistence on plastisphere versus plant surfaces, informing risk assessments in agricultural systems.
- For robust reuse, datasets would benefit from:
  - A formal metadata schema including precise material definitions, plant species, leaf surface terminology, and media conditions.
  - Standardized units and a data dictionary detailing each column, including when CFU_per_leaf versus CFU_per_mm2 is used.
  - Clear licensing and accessibility notes, given the safety-sensitive nature of the data.
- The data are linked to a peer-reviewed publication, which aids provenance and reproducibility but additional metadata would enhance discoverability and interoperability across repositories.
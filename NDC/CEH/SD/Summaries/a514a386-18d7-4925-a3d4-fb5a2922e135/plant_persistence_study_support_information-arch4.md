# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

## Overview
- Investigates whether Salmonella Typhimurium and Vibrio cholerae can transfer from plastic mulch (plastisphere) to ready-to-eat basil and spinach leaves and persist on leaf surfaces.
- Key findings:
  - Both pathogens persist on plastic mulch attached to leaves for up to 14 days.
  - Within 24 hours, pathogens can transfer from the plastic to the leaf surface (epiphytic) on both basil and spinach.
  - Washing and removing adhering plastics do not fully eliminate these pathogens, posing food-safety risks.
- Relevance: As use of plastic mulches increases with intensive production, there is an urgent need to understand the co-pollutant pathogen risk in agricultural systems.

## Datasets and data structure
- Seven CSV files capturing bacterial concentrations:
  - Endophytic CFUs (inside leaf tissue)
  - Epiphytic CFUs (surface on leaves)
  - Persistence CFUs on plastic mulch, hay, or culture
  - Separate data for Salmonella Typhimurium and Vibrio cholerae
  - A file with linear decline analysis for Salmonella Typhimurium (R-squared, Gradient, K, D-values)
- Key data elements:
  - Sample_ID encoding: plant type (Basil/Spinach) - material (Plastic/Hay/Culture) - leaf side (Adaxial/Abaxial) - timepoint (days) - replicate
  - Timepoints: 0, 1, 2, 3, 4, 7, 10, 14 days
  - Measurements: CFU counts, CFU_per_leaf, CFU_per_ml, CFU_per_mm2
- File naming and organization:
  - Cholera_Endophytic_CFUs.csv, Cholera_epiphytic_CFUs.csv, Cholera_persistence_plastic_hay_CFUs.csv
  - Salmonella_Endophytic_CFUs.csv, Salmonella_Epiphytic_CFUs.csv, Salmonella_persistence_plastic_hay_CFUs.csv
  - STyphimurium_R_squared_Gradient_K_value_D_value.csv

## Experimental design and data collection
- Plant setup: Basil and spinach leaves placed in petri dishes with wet cotton pads; adaxial or abaxial surface tested.
- Treatments applied: Plastic mulch, hay, or culture material introduced onto leaf surfaces.
- Sampling regime: Days 0, 1, 2, 3, 4, 7, 10, 14; four replicates per timepoint; negative controls included.
- Analytical methods:
  - Plastic/hay samples: PBS wash, serial dilutions, plating on LB agar with chloramphenicol; CFU counted after 24 h at 37°C.
  - Epiphytic (leaf surface) samples: surface wash with PBS, serial dilutions, plating as above.
  - Endophytic samples: ethanol wash to remove residual bacteria, tissue disruption, resuspension in PBS, plating as above.
- Data processing: CFU counts converted to concentrations per ml, per leaf, or per mm² as appropriate.
- Quality controls: No missing data points; 0 CFU indicates no colonies recovered.

## Temporal coverage and scope
- Data collected during October–November 2023.
- Scope covers three interaction types: persistence on materials, epiphytic transfer to leaf surfaces, and endophytic presence within leaves.

## Data quality, standards, and governance
- Comprehensive documentation of data structure and variable definitions (sample codes, timepoints, units).
- Clear, consistent units across datasets (CFU, CFU/ml, CFU/leaf, CFU/mm²).
- No SOP references in the dataset; methodological details provided in accompanying text, enabling reproduction.
- Data integrity indicated by full timepoint coverage, four replicates, and zero-missing datasets.

## Access, reuse, and publication
- Data accompany a peer-reviewed article: Woodford et al. 2024, Heliyon; DOI provided.
- Data structured for reuse: labeled files, explicit variable descriptions, and time-resolved CFU measurements support secondary analyses (e.g., risk assessment, environmental monitoring, modelling decay/transfer dynamics).

## Implications for Data Leaders
- Demonstrates end-to-end data lifecycle:
  - Thoughtful experimental design with clear metadata (plant type, material, leaf surface, timepoint, replicate).
  - Systematic data capture, processing, and conversion to standardized CFU metrics.
  - Integrated data across multiple interaction pathways (endophytic, epiphytic, persistence) for a holistic view of risk.
- Highlights governance needs:
  - Standardized metadata schemas to enable cross-study interoperability (consistent sample coding and units).
  - Transparent documentation of methods and QA to support reproducibility and regulatory considerations in food safety.
  - Clear data provenance linking CSVs to a published study, facilitating discoverability and reuse.
- Practical relevance:
  - Provides a rich, time-resolved dataset for modelling pathogen transfer risks from agricultural plastics to crops.
  - Supports policy and risk assessment efforts by quantifying persistence and transfer timelines, informing wash/disposal guidelines and plastic-use policies in farming.
# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

## Overview
- Investigates whether Salmonella Typhimurium and Vibrio cholerae can move from plastisphere on plastic mulch to ready-to-eat basil and spinach leaves and persist on leaf surfaces.
- Highlights environmental health concern: plastic pollution in agriculture forms a habitat for human pathogens that may contaminate crops.

## Data and file structure
- Seven CSV data files accompany the study:
  - Cholera_Endophytic_CFUs.csv
  - Cholera_epiphytic_CFUs.csv
  - Cholera_persistence_plastic_hay_CFUs.csv
  - Salmonella_Endophytic_CFUs.csv
  - Salmonella_Epiphytic_CFUs.csv
  - Salmonella_persistence_plastic_hay_CFUs.csv
  - STyphimurium_R_squared_Gradient_K_value_D_value.csv
- Data types and units:
  - Endophytic and epiphytic CFUs per leaf, per ml, or per 300 µL as CFU measurements.
  - CFU counts derived from plating on LB agar with chloramphenicol; results reported as CFU.
  - Additional vectors include dilution factors, timepoints (days), leaf surface (adaxial/abaxial), plant type (basil/spinach), and material type (plastic mulch, hay, culture).
  - Regression metrics for Salmonella Typhimurium (R-squared, Gradient, K day⁻¹, D-value) in one file.
- Data provenance: Relevant to environmental monitoring datasets with standardized CFU reporting.

## Experimental design and methods
- Plant material: Basil and spinach leaves; leaves tested on adaxial or abaxial surfaces.
- Contaminants/materials: Plastic mulch, hay, or culture introduced to leaf surfaces.
- Timepoints: 0, 1, 2, 3, 4, 7, 10, and 14 days.
- Replication: Four replicates per condition; negative controls included.
- Procedures:
  - Material analysis: Leaves with adhered plastic/hay washed, serially diluted in PBS, plated on LB agar with chloramphenicol; CFUs counted after 24 hours at 37°C.
  - Epiphytic analysis: Surface washes of leaves collected in PBS, processed similarly.
  - Endophytic analysis: Leaves washed with 70% ethanol to remove residual surface bacteria, crushed, resuspended in PBS, then plated.
- Data processing: Raw CFU data converted to final CFU per ml, per leaf, or per mm² as appropriate.

## Key findings
- Persistence: Salmonella Typhimurium and Vibrio cholerae persisted on plastic mulch fragments adhered to basil and spinach leaves for up to 14 days.
- Transfer: Within 24 hours, both pathogens dissociated from the plastic surface and transferred to the leaf surfaces of both crops.
- Food safety implications: The risk to ready-to-eat crops is heightened because removal of adhering plastics and washing of leaves do not fully eliminate these pathogens.
- Environmental health relevance: Demonstrates a non-quantified co-pollutant pathogen risk associated with plastic pollution in agricultural settings.

## Temporal coverage and sampling resolution
- Experimental window: October–November 2023.
- Sampling schedule: Days 0, 1, 2, 3, 4, 7, 10, and 14 across all three parts of the experiment (material persistence, epiphytic, endophytic).

## Data quality and processing
- Quality control: No missing data points; no processing adjustments required. Zero CFU entries indicate no colonies recovered.
- Data handling: All data stored and organized in structured CSV files; raw colony counts converted to standardized CFU metrics.
- SOPs: The report notes no referenced SOPs and no samples stored as part of the data handling process.

## Implications for environmental monitoring and policy
- Data standardization: Provides time-resolved, comparable CFU data across materials, plant types, and leaf surfaces suitable for integration with environmental health datasets.
- Data-sharing potential: Designed to be accessible as CSV files, enabling reuse for risk assessment and policy performance monitoring related to plastic pollution and food safety.
- Recommendations for monitoring: Emphasizes the need to quantify pathogen risk associated with plastisphere in agricultural systems; fosters broader data linkage to evaluate environmental health and policy outcomes.

## Publication and accessibility
- Published in Heliyon (2024) by Woodford et al.: Salmonella Typhimurium and Vibrio cholerae can be transferred from plastic mulch to basil and spinach salad leaves.
- Reference: https://doi.org/10.1016/j.heliyon.2024.e31343
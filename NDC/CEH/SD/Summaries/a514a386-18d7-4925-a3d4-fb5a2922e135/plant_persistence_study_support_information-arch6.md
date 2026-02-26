# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

## Overview
- Plastic mulch can harbor microbial communities (plastisphere) including human pathogens.
- Study tests transfer of Salmonella Typhimurium and Vibrio cholerae from plastic mulch to basil/spinach leaves and persistence on leaf surfaces.
- Key findings:
  - Pathogens persist on plastic mulch-adhering surfaces for up to 14 days on both basil and spinach leaves.
  - Pathogens can transfer to leaf surfaces within 24 hours, posing a food safety risk even after removing plastics and washing leaves.

## Data assets (files and purpose)
- Seven CSV data files documenting CFU data and decay analyses:
  - Cholera_Endophytic_CFUs.csv
  - Cholera_epiphytic_CFUs.csv
  - Cholera_persistence_plastic_hay_CFUs.csv
  - Salmonella_Endophytic_CFUs.csv
  - Salmonella_Epiphytic_CFUs.csv
  - Salmonella_persistence_plastic_hay_CFUs.csv
  - STyphimurium_R_squared_Gradient_K_value_D_value.csv
- Data focus:
  - Endophytic CFUs: bacteria recovered from inside leaves.
  - Epiphytic CFUs: bacteria recovered from leaf surfaces.
  - Persistence CFUs: bacteria recovered from plastic, hay, or culture materials.
  - Regression metrics for Salmonella Typhimurium (R^2, Gradient, K, D values).

## Data structure and units
- Sample_ID schema: B/S (basil/spinach) - PE/GR/CO (plastic, hay, culture) - A/B (adaxial/abaxial) - Timepoint - replicate.
- Timepoints: days 0, 1, 2, 3, 4, 7, 10, 14.
- Units and measurements:
  - CFU: bacterial colonies counted on LB agar with chloramphenicol.
  - CFU_per_300ul, CFU_per_leaf, CFU_per_ml, CFU_per_mm2: derived concentration metrics.
  - Dilution: 10-fold dilution factors (10^-1 to 10^-4).
  - Data are reported as CFU counts or derived concentrations; zero indicates no colonies recovered.
- Sample processing details:
  - Endophytic: leaves washed with PBS, then ethanol pretreatment, crushed, resuspended, plated.
  - Epiphytic: leaf surfaces washed with PBS and plated.
  - Material persistence: plastic mulch/hay samples vortexed in PBS, serial dilutions plated.

## Experimental design and sampling regime
- Plant material: basil and spinach leaves.
- Treatments: plastic mulch, hay, or culture applied to leaf surfaces.
- Inoculation and setup:
  - Leaves placed adaxial or abaxial side up in petri dishes with wet cotton pads.
  - Materials applied to leaf surface; samples collected at specified timepoints.
- Controls and replication:
  - Negative controls (leaves with no bacteria) included.
  - Four replicates per time point; no data missing across timepoints.
- Processing methodology:
  - Material samples: PBS suspension, serial dilutions, plating on LB agar with chloramphenicol; 24 h at 37°C for CFU counts.
  - Epiphytic samples: leaf wash plated similarly.
  - Endophytic samples: ethanol wash, crushing, resuspension, plating.

## Temporal coverage and data generation
- Temporal window: experiments conducted October–November 2023.
- Timepoints sampled: 0, 1, 2, 3, 4, 7, 10, 14 days.
- Data generation workflow:
  - Raw CFU data recorded in Excel; converted to final concentrations per ml or per leaf.
  - Four replicates per condition and timepoint; data completeness ensured.

## Quality control and data integrity
- No missing data points reported across datasets.
- Data processed uniformly to CFU-based concentrations.
- Zeros indicate absence of detectable colonies on plated media.
- No SOP references; study notes standardized handling and processing to ensure comparability.

## Key findings relevant to data use
- Demonstrated transfer of both pathogens from plastisphere to leafy surfaces within 24 hours.
- Pathogens persisted on plastic mulch and leaf-adhering matrices for up to 14 days.
- Removal of adhering plastics and washing may not fully mitigate contamination risk, underscoring the need for monitoring and mitigation strategies in agricultural systems using plastics.

## Data availability and publication provenance
- Data published in Woodford et al. (2024): Salmonella Typhimurium and Vibrio cholerae can be transferred from plastic mulch to basil and spinach salad leaves. Heliyon 10:e31343. https://doi.org/10.1016/j.heliyon.2024.e31343

## Potential data products and reuse opportunities (data support perspective)
- Time-series dashboards:
  - CFU trends by plant type (basil vs spinach), by material (plastic mulch, hay, culture), and by leaf surface (adaxial vs abaxial).
- Risk modeling inputs:
  - Decay/transfer parameters (K, D-values, gradients) for Salmonella Typhimurium to inform exposure risk assessments.
- Comparative analyses:
  - Endophytic vs epiphytic CFU dynamics across timepoints and materials.
- Data quality and provenance modules:
  - Documentation of processing pipelines, dilution schemes, and plate counts to support auditability and reproducibility.
- Educational and policy outputs:
  - Visualizations illustrating the rapid transfer risk from plastisphere to edible leaves to inform agricultural best practices and policy on plastic use in farming.
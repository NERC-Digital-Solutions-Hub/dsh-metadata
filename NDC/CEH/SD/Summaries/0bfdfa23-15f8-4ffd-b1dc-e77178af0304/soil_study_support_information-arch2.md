# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments.

## Overview
- Dataset quantifies the persistence of Salmonella enterica Serovar Typhimurium on microplastics and glass beads in podzol and loamy soil.
- Includes results from persistence, flooding/leachate, and transfer experiments to assess survival and transfer potential under ambient and flooded conditions.
- Measurements are based on colony forming units (CFUs) recovered after biofilm removal and plating on selective media.
- Four CSV files accompany the dataset, containing CFU data, regression metrics, and transfer results, with data collected between June and August 2023.

## Data Files and Content
- 20230619STyphimurium_persistence_soil_CFUs.csv
  - CFU/g concentrations for samples from the persistence experiment (plastic/glass beads in podzol or loam).
  - Variables include Sample_ID, Sample_type (CC, PE, GB, P, L), Days (1–35), Weight (g), Concentration (CFU/g).
- 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
  - Regression metrics for linear decline analyses across persistence, leachate, and transfer datasets.
  - Variables include Rsquared, Gradient, K(day-1), D-value (days), along with experiment/material/replicate metadata.
- 20230626STyphimurium_leachate_soil_CFUs.csv
  - CFU data from the leachate experiment (and associated soil/plastic materials).
  - Includes notes on N/A values where starting samples were not recovered from leachate or were measured at experiment start.
- 20230626STyphimurium_transfer_CFUs.csv
  - CFU data from the transfer experiment (whether bacteria transferred to virgin material).
  - Includes Sample_ID, Column_ID, Timepoint (0–14 days), sample_type (bottom soil, colonised material, new material), weight (g), CFU_per_ml, CFU_per_g, and related fields.
- All files are in CSV format.

## Experimental Design and Sampling
- Persistence experiment:
  - Plastic and glass beads inoculated with S. Typhimurium embedded in 120 g of podzol or loam soil in jars.
  - Sampling at days 1, 2, 3, 4, 7, 10, 14, 21, 28, 35; four replicates per time point.
  - Beads removed, biofilm detached with PBS, serial dilutions plated on LB agar with chloramphenicol; CFUs quantified.
- Leachate/flooding experiment:
  - Flooding simulated by adding water; leachate collected at sampling times and CFU counts performed as above.
  - Final point included analysis of plastic/glass biofilms remaining in columns.
- Transfer experiment:
  - Virgin plastics placed below contaminated plastics to test transfer to new material; later removed, washed, and biofilm on both contaminated and virgin materials analyzed.
  - Timepoints up to 14 days; four replicates per condition.

## Methods and Unit Details
- CFU counts converted to final concentrations per g (soil/material) or per ml (liquids) from serial dilutions.
- Materials and samples:
  - Podzol (P) and Loam (L) soils; polyethylene (PE) plastics, glass beads (GB), and culture controls (CC).
- Measurements performed by resuspending biofilms in PBS, serial dilutions, plating on LB agar with chloramphenicol, and incubating at 37°C for 24 hours.

## Temporal Coverage
- Experiments conducted from June to August 2023.
- Persistence: days 1–35.
- Leachate and transfer: sampling points within 7–21 days, with additional transfer-related timepoints up to 14 days.

## Data Structure and Variables
- Persistence CFUs: CFU/g concentrations by Sample_ID, Sample_type (CC, PE, GB, P, L), and days.
- Leachate/Transfer: CFU counts and related metrics (per ml, per g, per leachate volume; column/material identifiers; timepoints; replicate info).
- Regression/decline analysis: R^2, Gradient (change in CFU with time), K (day^-1), D-value (days).

## Quality Control and Data Notes
- Some N/A values exist where data could not be recovered (e.g., early transfer samples or starting leachate measurements).
- A noted QC issue: missing values in the transfer dataset for the first 16 samples (pre-mixing stage) were documented as N/A in the sample_type field.
- Raw data were recorded in Excel and converted to standardized CFU per g/ml for analysis.

## Publication and Access
- The dataset is published in: Woodford, L., Fellows, R., White, H.L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environmental Science and Pollution Research, 2024. DOI: 10.1007/s11356-024-34491-4

## Relevance for Environmental Monitoring Analysts
- Provides standardized, machine-readable CFU data across persistence, leachate, and transfer contexts to assess environmental health risks associated with microplastics and soil microbiota.
- Enables calculation of derived parameters (linear decline metrics, decay rates, D-values) to support policy performance and environmental health assessments.
- Data formatting and documentation align with standard monitoring practices: clear experimental context, replicates, and transparency about data processing and QC.
- Highlights the importance of integrating such datasets with broader environmental data to enhance the value and accessibility of monitoring information.
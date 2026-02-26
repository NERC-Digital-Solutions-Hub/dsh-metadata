# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments

## Overview
- Dataset of mesocosm experiments quantifying persistence of Salmonella enterica Serovar Typhimurium (S. Typhimurium) on microplastics and glass beads in podzol and loamy soil.
- Includes persistence, leachate, and transfer experiments with CFU counts to determine survival and transfer potential.
- Sampling: days 1–35 for persistence; 7, 14, 21 days for leachate and transfer; four replicates per time point.
- Methods: biofilm removal, PBS resuspension, serial dilutions, plating on LB agar with chloramphenicol; CFU counts used to express concentrations per g or per ml.
- Temporal coverage: June–August 2023.

## Data files and structure
- Four CSV files:
  - 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
  - 20230626STyphimurium_leachate_soil_CFUs.csv
  - 20230619STyphimurium_persistence_soil_CFUs.csv
  - 20230626STyphimurium_transfer_CFUs.csv
- File contents include:
  - Persistence data: CFUs recovered from plastic/glass beads in podzol/loam over time; sample identifiers indicate material, soil, day, and replicate.
  - Leachate data: CFUs recovered from leachate and materials, with regression metrics (R^2, Gradient, K, D-value) across experiments.
  - Transfer data: CFUs transferred to virgin materials and CFU per ml/g in recovered leachate or material.
- Formats and units are specified within each file (CFU/g, CFU/ml, timepoints in days, etc.).

## Methods and analyses
- Experimental design includes:
  - Persistence: contaminated beads mixed into 120 g of soil (podzol or loam) in jars; destructive sampling at multiple days; CFUs quantified from resuspended biofilms.
  - Leachate: non-destructive flooding with water; leachate collected and analyzed; final analysis of plastics/glass for residual biofilm.
  - Transfer: virgin plastics placed below contaminated plastics to assess transfer to new material.
- Data processing:
  - Serial dilutions converted to final CFU concentrations per g or per ml using standard calculation (example provided: dilution counts scaled to volume/weight).
  - Regression metrics (R^2, Gradient) and process rates (K day^-1) reported for linear decline analyses.
- Quality control notes:
  - Some missing values recorded as N/A; initial sample Type field in transfer dataset noted as pre-mixing and not applicable for those entries.
  - No SOPs referenced; samples not stored; raw data processed in spreadsheet form.

## Experimental design details
- Materials: microplastics and glass beads.
- Soils: podzol and loam.
- Procedures:
  - Destructive sampling in persistence to measure surviving CFUs on materials.
  - Non-destructive leachate sampling with subsequent material analysis at final time point.
  - Transfer assessment via comparison of CFUs on virgin materials versus contaminated materials.
- Replication: four replicates per time point.

## Metadata, accessibility, and governance considerations
- Data are publicly shared as CSV files with explicit naming conventions and descriptive column labels.
- Metadata challenges highlighted:
  - Incomplete or variable metadata across files (e.g., some N/As in sample-type fields).
  - Absence of formal SOP documentation; interpretation relies on descriptive notes.
- Implications for monitoring frameworks:
  - Demonstrates how pathogen persistence and transfer through environmental media (microplastics in soils) can be quantified and monitored.
  - Highlights need for standardized metadata, transparent data governance, and open data sharing to enable reuse and cross-study comparisons.

## Relevance for environmental health monitoring
- Provides concrete measures of:
  - Pathogen persistence on microplastics in agricultural soils.
  - Transfer potential to virgin materials and through leachates, relevant for assessing contamination pathways.
- Supports development of monitoring indicators and risk assessments for soil-associated food safety and water quality.

## Publication and access
- Associated publication: Woodford, L., Fellows, R., White, H.L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environmental Science and Pollution Research, 2024. DOI: 10.1007/s11356-024-34491-4

## Key considerations for policymakers and managers
- Data usefulness hinges on data quality, metadata completeness, and transparent sharing; consider mandating standardized metadata schemas for environmental health datasets.
- The dataset illustrates measurable endpoints (CFU concentrations, persistence over time, leachate transfer) that can inform risk-based monitoring programs and mitigation strategies for soil ecosystems impacted by microplastics.
- Recognize and address data gaps and access issues (as highlighted by the challenges in metadata and SOP documentation) to improve reproducibility and policy relevance.
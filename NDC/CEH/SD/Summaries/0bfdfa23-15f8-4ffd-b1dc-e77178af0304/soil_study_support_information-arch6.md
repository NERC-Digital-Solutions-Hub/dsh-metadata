# Colony forming units of Salmonella Typhimurium recovered from microplastics in two agriculturally relevant soils during persistence, leachate and sample transfer experiments.

## Overview
- A mesocosm dataset quantifying the persistence of Salmonella enterica Serovar Typhimurium on microplastics and glass beads in two soils (podzol and loamy soil).
- Experiments cover persistence, leachate, and transfer under ambient and flooding conditions.
- Surviving bacteria are quantified as CFUs after biofilm removal and plating on selective media.
- Data support potential analyses of decay/persistence dynamics, transfer potential, and leachate impacts.

## Data files and structure
- Four CSV data files:
  - 20230619STyphimurium_persistence_soil_CFUs.csv
    - Concentrations of recovered S. Typhimurium during the persistence experiment.
  - 20230626STyphimurium_leachate_soil_CFUs.csv
    - Recovered CFUs from the leachate experiment (flooding/passage of water through columns).
  - 20230626STyphimurium_transfer_CFUs.csv
    - Transferred CFUs in the transfer (flooding) experiment.
  - 20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv
    - Data for linear decline analyses (R-squared, gradient, K, D-value) across experiments.
- Each file uses standardized naming conventions to indicate experiment type, material, soil type, and replicates.

## Experimental design and methods
- Persistence experiment:
  - Beads (microplastics or glass) colonised with S. Typhimurium mixed into 120 g of podzol or loam soil in glass jars.
  - Samples taken at days 1, 2, 3, 4, 7, 10, 14, 21, 28, 35; four replicates per time point.
  - Biofilm removed by vortexing after resuspension in PBS; serial dilutions plated on LB agar with chloramphenicol; CFUs counted after 24 h at 37°C.
- Leachate and flooding experiment:
  - Water added to simulate flooding; leachate collected and quantified by serial dilution and plating.
  - Final time point involved analysis of plastic/glass to determine retained biofilm.
- Transfer experiment:
  - Virgin plastics placed below contaminated plastics; after the experiment, transferred bacteria to virgin materials were assessed.
- Sample processing:
  - CFU data converted to final concentrations per g or per ml using standard serial-dilution calculations (example provided in dataset documentation).
- Quality control:
  - Some missing values (notably in transfer file) are documented as pre-mixing, with N/A in certain columns.

## Temporal coverage
- Experiments conducted June–August 2023.
- Persistence: 1–35 days.
- Leachate and transfer: measurements at 7, 14, and 21 days (plus initial conditions and final assessments as described).

## Data fields and units
- Persistence CSV (20230619STyphimurium_persistence_soil_CFUs.csv):
  - Sample_ID, Sample_type (CC, PE, GB; P= podzol, L= loam), Days, Weight (g), Concentration (CFU/g).
  - Example encoding: CC-P-1d-01 (culture control in podzol after 1 day, replicate 01).
  - Concentration units: CFU/g.
- Leachate CSV (20230626STyphimurium_leachate_soil_CFUs.csv):
  - Experiment (Persistence, Leachate, Transfer), Material (Plastic, culture, glass), Soil type (Podzol, loam), Replicate (1–4), Soil type codes, Rsquared, Gradient, K(day-1), D-value (days).
  - Timepoints for leachate/transfer included in separate columns (7, 14, 21 days for CFU data; other fields describe per-experiment metrics).
- Transfer CSV (20230626STyphimurium_transfer_CFUs.csv):
  - Sample_ID, Column_ID, Timepoint (0–14 days), Sample_type (Bottom soil, colonised material: plastic/glass or new material: virgin plastic), Weight (g), CFU_per_ml, CFU_per_g, etc.
  - Note: some early samples pre-colonisation are marked N/A.
- R-squared/Gradient/D-value CSV (20230619Soil_persistence_leachate_transfer_R_squared_Gradient_K_value_D_value.csv):
  - Contains statistical descriptors for linear decline models across experiments (R-squared, Gradient, K, D-value).

## Data quality and provenance
- Data were collected via standard microbiological plating and CFU counting, with explicit transformation to concentration per material weight or per volume.
- Missing values documented (e.g., pre-mixing samples, N/A markers) and explained in the dataset notes.
- No explicit SOPs referenced in the collection, analysis, or storage notes; data processing steps are described (dilution calculations, concentration conversion).

## How to use and potential data products
- Reusable for:
  - Modeling persistence curves and decay rates (e.g., estimating K, D-values, and goodness-of-fit via R-squared).
  - Comparing persistence and transfer potential across soil types (podzol vs. loam) and materials (polyethylene, glass beads, virgin plastics).
  - Assessing the impact of flooding on transfer and leachate contamination.
- Data products for end users:
  - Dashboards showing CFU trajectories over time by soil type, material, and experiment type.
  - Self-serve datasets enabling users to reproduce linear decline analyses or fit their own models to persistence/transfer data.
  - Summary charts of transfer potential to virgin plastics under different conditions.

## Publication reference
- Woodford, L., Fellows, R., White, H.L. et al. Survival and transfer potential of Salmonella enterica serovar Typhimurium colonising polyethylene microplastics in contaminated agricultural soils. Environmental Science and Pollution Research, 2024. DOI: 10.1007/s11356-024-34491-4
# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

## Overview
- A model-generated dataset using the SPACSYS model applied to a historic site on the Loess Plateau, China.
- Validated with observed crop yields: winter wheat (1993–2004) and maize (1983–2015).
- Extended to future climate scenarios (2015–2049) to predict daily above-ground dry matter (leaves, stems, grains), soil water content across layers, and soil organic carbon stocks.

## Data content and structure
- The dataset comprises 248 CSV files organized by file naming convention: crop name + 'sim' + weather data name + variable name.
- Crop names: wheat or maize.
- Weather data name: historic or one of six SSP-RCP future scenarios (SSP119, SSP126, SSP245, SSP370, SSP434, SSP585).
- For each combination, five ensemble members: r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1.

## Variables and file types
- Yield.csv
  - harvest_date, yield (grain yield in g/m2).
- DM.csv (above-ground dry matter)
  - date, leaf_DM, stem_DM, grain_DM (daily values in g/m2).
- SW.csv (soil water content)
  - date, 0_10_cm, 10_20_cm, 20_40_cm, 40_60_cm, 60_80_cm, 80_100_cm, 100_140_cm, 140_180_cm, 180_220_cm (proportion of soil water content per soil layer).
- SOM.csv (soil organic carbon stocks)
  - date, 0_40_cm, 40_100_cm (g C/m2) representing topsoil and subsoil stocks.

## Simulation details and management
- Simulation setup includes ploughing before the wheat season (September) and before maize (April) each year.
- Fertiliser application: 20.7 g N/m2 for winter wheat; 14.7 g N/m2 for maize; fertiliser form assumed as urea.
- Complete results for all variables; simulations executed by K Gongadze and H Yang.

## Climate scenarios and validation
- Historical scenario: observed data used for validation.
- Future scenarios: six SSP-RCP climate pathways with five ensemble members each (as listed above), enabling assessment of variability and uncertainty in projections to 2049.

## Data provenance and references
- Model: SPACSYS (integrates 3D root architecture with carbon, nitrogen, and water cycling).
- Reference for model description: Wu, L.; McGechan, M.B.; McRoberts, N.; Baddeley, J.A.; Watson, C.A. (2007). Ecol. Model. 200, 343-359. DOI: 10.1016/j.ecolmodel.2006.08.010.

## Data governance and usage considerations for Data Leaders
- Discoverability and organization: 248 files with a clear naming convention support programmatic access and scalable data management.
- Provenance: links to observed validation data and explicit simulation parameters enhance auditability and reproducibility.
- Metadata and discoverability: file-level structure (dates, layer depths, variable descriptions) supports metadata capture and data quality assessment.
- Versioning and updates: future climate projections are structured by scenario and ensemble member, highlighting the need for version control and provenance tracking as scenarios evolve.
- Cross-domain utility: dataset blends model outputs with agronomic management details, enabling end-to-end data products for decision-support and policy analysis.
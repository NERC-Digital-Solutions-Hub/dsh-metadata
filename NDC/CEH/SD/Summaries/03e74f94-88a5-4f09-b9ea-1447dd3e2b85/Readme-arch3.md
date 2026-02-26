# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

## Overview
- Model-generated dataset using the SPACSYS model applied to a historic site on the Loess Plateau, China.
- Validation used observed yields: winter wheat (1993–2004) and maize (1983–2015).
- Extended simulations cover 2015–2049 under six SSP-RCP climate scenarios with five ensemble members each.
- Outputs include daily metrics for above-ground matter, soil water content by depth, and soil organic carbon stocks.

## Dataset composition and scope
- Crops: winter wheat and maize.
- Predicted variables:
  - Above-ground dry matter (DM) for leaves, stems, grains (daily).
  - Soil water content (SW) by multiple soil layers (daily).
  - Soil organic carbon stocks (SOM) in topsoil and subsoil layers (daily).
- Observations used for validation:
  - Wheat yields: 1993–2004.
  - Maize yields: 1983–2015.

## Simulation setup and inputs
- Management practices simulated:
  - Ploughing: wheat in September (pre-season), maize in April (annual).
  - Fertilizer: total N rate 20.7 g N/m2 for wheat; 14.7 g N/m2 for maize, using urea.
- Outputs are driven by climate scenarios and management assumptions embedded in the SPACSYS model.

## Data files and naming convention
- Total files: 248 CSV files.
- Naming structure: crop name + 'sim' + weather data name + variable name.
  - Weather data name: 'historic' or a SSP-RCP scenario.
  - SSP-RCP scenarios: SSP119, SSP126, SSP245, SSP370, SSP434, SSP585.
  - Ensemble members: r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1.
- Example file: wheatsimhistoricDM.csv (winter wheat, historic climate, daily DM).

## Variable descriptions by file type
- Yield.csv
  - harvest_date: Harvest date (dd/mm/yyyy).
  - yield: Grain yield (dry) in g/m2.
- DM.csv (daily above-ground DM)
  - date: Date (dd/mm/yyyy).
  - leaf_DM: Daily leaf DM (g/m2).
  - stem_DM: Daily stem DM (g/m2).
  - grain_DM: Daily grain DM (g/m2).
- SW.csv (soil water content by depth)
  - date: Date (dd/mm/yyyy).
  - 0_10_cm, 10_20_cm, 20_40_cm, 40_60_cm, 60_80_cm, 80_100_cm, 100_140_cm, 140_180_cm, 180_220_cm: Proportion of soil water content in each layer; layer thickness indicated by the column heading.
- SOM.csv (soil organic carbon stocks)
  - date: Date (dd/mm/yyyy).
  - 0_40_cm: Daily soil organic carbon stocks in topsoil (g C/m2).
  - 40_100_cm: Daily soil organic carbon stocks in subsoil (g C/m2).

## Climate scenarios and structure
- Six SSP-RCP scenarios used for near- to mid-term: SSP119, SSP126, SSP245, SSP370, SSP434, SSP585.
- Each scenario includes five ensemble members to capture variability.
- Historical runs serve as a baseline for comparison against future projections (2015–2049).

## Validation and provenance
- Observational yields from 1993–2004 (wheat) and 1983–2015 (maize) used to validate the SPACSYS model outputs.
- Model description and details of SPACSYS linked to a 2007 publication (Wu et al., Ecol. Model. 200, 343-359).

## Relevance for monitoring frameworks
- Provides a comprehensive, model-based data stream for monitoring agricultural production, soil moisture dynamics, and soil carbon under changing climate conditions.
- Supports evaluation of policy options related to climate adaptation, soil health, water resources, and nutrient management.

## Data governance and implementation considerations
- As a model-generated dataset, ensure thorough metadata for reproducibility and traceability (model version, parameters, input datasets).
- Metadata completeness and documentation of assumptions are essential for usability in monitoring frameworks.
- Data access and sharing: openness depends on dataset originator permissions; clarity on data license and hosting required.
- Data standardization and interoperability: consistent variable naming, units, and depth intervals facilitate integration with other monitoring data.
- Data transformations and lineage: maintain clear records of any post-processing or aggregation steps.
# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

- What the dataset is
  - Model-generated outputs from the SPACSYS model applied to a historic experimental site on the Loess Plateau, China (35.52°N, 107.68°E).
  - Uses observed winter wheat yields (1993–2004) and maize yields (1983–2015) for validation.
  - Projected results under climate scenarios from 2015 to 2049.

- Management and simulation context
  - Agricultural management in simulations: ploughing before wheat (September) and maize (April) each year.
  - Fertiliser application rate: winter wheat 20.7 g N/m2; maize 14.7 g N/m2; fertiliser form assumed to be urea.

- Data scope and outputs
  - Daily simulations of:
    - Above-ground dry matter by component: leaves, stems, grains.
    - Soil water content across layers.
    - Soil organic carbon stocks in topsoil and subsoil.
  - Temporal coverage: 1983–2015 (historical data); 2015–2049 (future projections).

- Dataset structure and contents
  - 248 CSV files in total.
  - File naming convention: crop name + 'sim' + weather data name + variable name.
    - Crop: wheat or maize.
    - Weather data name: historic or one of six SSP-RCP future scenarios (SSP119, SSP126, SSP245, SSP370, SSP434, SSP585).
    - Ensemble members: r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1.
  - Variable groups and file examples:
    - Yield.csv: harvest_date, yield (g/m2).
    - DM.csv: date, leaf_DM (g/m2), stem_DM (g/m2), grain_DM (g/m2).
    - SW.csv: date, depth layers (0_10_cm, 10_20_cm, 20_40_cm, 40_60_cm, 60_80_cm, 80_100_cm, 100_140_cm, 140_180_cm, 180_220_cm) with proportions of soil water content per layer.
    - SOM.csv: date, 0_40_cm (g C/m2), 40_100_cm (g C/m2).
  - Example file: wheatsimhistoricDM.csv.

- Variables and units (as described)
  - Yield: g/m2.
  - Daily dry matter (DM): g/m2 for leaves, stems, grains.
  - Soil water (SW): proportion of soil water content by depth layer.
  - Soil organic carbon stocks (SOM): g C/m2 for 0–40 cm and 40–100 cm layers.

- Validation and reference
  - Model validation against observed yields for winter wheat (1993–2004) and maize (1983–2015).
  - Model reference: SPACSYS model (Wu et al., 2007), description of 3D root architecture integration for carbon, nitrogen, and water cycling.

- Spatial and temporal context
  - Site coordinates and climate context provided; simulations span multiple future climate pathways to support comparative analyses.

- Data governance and stewardship notes for data stewards
  - Clear data organization with standardized file naming to aid discovery and reuse.
  - Comprehensive metadata coverage implied by file contents (dates, layer definitions, variable descriptions), but explicit repository or licensing details are not provided.
  - Large dataset (248 CSV files) necessitates robust data transfer and storage planning; scalable updates would require a defined update mechanism and versioning.
  - Model-based data with fixed management assumptions (ploughing dates, fertiliser rate, urea form) should be clearly documented to inform users about scope and limitations.
  - Potential considerations for users: units are specified; several layers of soil depth are included; multiple climate scenarios and ensemble members enable uncertainty analysis.

- Practical applications
  - Useful for studying biomass production, soil water dynamics, and soil carbon responses under current and future climate conditions.
  - Enables scenario analysis and sensitivity assessments for governance, resource planning, and environmental impact studies.
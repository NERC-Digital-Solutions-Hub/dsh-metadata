# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

- Overview
  - A model-generated, GIS-relevant dataset using the SPACSYS model to simulate crop and soil dynamics at a site on the Loess Plateau, China (35.52°N, 107.68°E).
  - Validated against observed yields: winter wheat yields (1993–2004) and maize yields (1983–2015).
  - Future projections cover 2015–2049 under six SSP-RCP climate scenarios.

- Spatial and temporal scope
  - Location: single experimental site on the Loess Plateau near Changwu, China.
  - Historical period: maize yield data (1983–2015); wheat yield data (1993–2004) used for validation.
  - Projections: daily dynamics through 2049 under six SSP-RCP scenarios with multiple ensemble members.

- Data products and structure
  - Dataset composition: 248 CSV files.
  - File naming pattern: crop name + 'sim' + weather data name + variable name.
    - Crop name: wheat or maize
    - Weather data name: historic or one of six SSP-RCP scenarios (SSP119, SSP126, SSP245, SSP370, SSP434, SSP585)
    - Variable name: Yield, DM, SW, or SOM
  - Example: wheatsimhistoricDM.csv (winter wheat daily above-ground dry matter under historic weather).

- Variables and content
  - Yield.csv
    - harvest_date (dd/mm/yyyy)
    - yield (dry grain yield in g/m^2)
  - DM.csv
    - date (dd/mm/yyyy)
    - leaf_DM (daily leaf dry matter, g/m^2)
    - stem_DM (daily stem dry matter, g/m^2)
    - grain_DM (daily grain dry matter, g/m^2)
  - SW.csv (soil water content by depth)
    - date (dd/mm/yyyy)
    - 0_10_cm, 10_20_cm, 20_40_cm, 40_60_cm, 60_80_cm, 80_100_cm, 100_140_cm, 140_180_cm, 180_220_cm (proportion of soil water content per layer)
  - SOM.csv (soil organic carbon stocks)
    - date (dd/mm/yyyy)
    - 0_40_cm (topsoil + subsoil stocks, g C/m^2)
    - 40_100_cm (additional layer stocks, g C/m^2)
- Management and simulation details
  - Ploughing: wheat in September (before growing season), maize in April.
  - Fertiliser: 20.7 g N/m^2 for winter wheat; 14.7 g N/m^2 for maize; urea assumed.
  - Daily simulations for DM, soil water, and soil organic carbon stocks; results cover both current and future climate conditions.
  - Simulations conducted by K. Gongadze and H. Yang.

- Climate scenarios and ensembles
  - Six SSP-RCP scenarios used for future projections: SSP119, SSP126, SSP245, SSP370, SSP434, SSP585.
  - Each scenario includes five ensemble members (r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1).

- Data quality, provenance, and reference
  - Model-based projections validated with observed wheat and maize yields across the specified historical periods.
  - Model description and integration details cited: Wu et al., SPACSYS model (Ecological Modelling, 2007).
  - Outputs intended for GIS and map-based data visualisation and analysis, enabling exploration of spatially-referenced dynamics at the site and scenario level.
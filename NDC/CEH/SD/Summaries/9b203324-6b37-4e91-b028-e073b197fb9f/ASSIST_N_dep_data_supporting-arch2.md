# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate the annual mean deposition of reduced and oxidised nitrogen over the United Kingdom (UK), with domain covering the UK and Ireland.
- Spatial and temporal scope:
  - 1 km x 1 km grid resolution; 33 vertical layers from ground to 2500 m.
  - Outputs are masked to land cells within the UK.
  - Deposition outputs: wet and dry deposition of NHx (reduced nitrogen) and NOy (oxidised nitrogen).

- Model inputs and data sources
  - Emissions input from UK National Atmospheric Emissions Inventory (NAEI):
    - 160 subsectoral categories, aggregated into 11 SNAP sectors.
    - NH3 from agriculture estimated annually using census data, farming practices, and sector-specific emission data.
    - Emissions mapped to 1 x 1 km grid using land-cover data.
  - Ireland emissions:
    - Sourced from CLRTAP/EMEP and E-PRTR.
    - Spatial distribution for 2016 mapped to 1 x 1 km (MapEire) and scaled to year totals.
  - Wider European boundary conditions (for the UK domain):
    - 50 km x 50 km resolution data from CLRTAP/EMEP.
  - Meteorology and land surface data:
    - Wind: radiosondes or Weather and Research Forecast (WRF) model data.
    - Rain: CHR/Climatology sources (Tanguy et al. 2019; Walsh 2012).
    - Land cover: Land Cover Map 2015 (Rowland et al., 2017).

- Model runs and boundary conditions
  - Eight simulations per year with 45-degree directional resolution to generate boundary concentrations for initializing the UK 1 km x 1 km simulation.

- Deposition modelling approach
  - Dry deposition computed using land-cover-specific deposition velocities; wet deposition derived from precipitation-chemistry coupling.
  - Five land-cover categories used: forest, moorland, grassland, arable, urban.
  - Deposition outputs are produced as:
    - Wet and dry deposition of NHx (NH3 + NH4)
    - Wet and dry deposition of NOy (NO2 + NO3 + HNO3 + PAN)
  - Grid-square deposition is a weighted mean across land-cover types within the square (grid-average).
  - Model evaluation conducted against the UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) network.

- Outputs and data format
  - Outputs provided as annual mean deposition values in kilograms of nitrogen per hectare per year (kg N ha-1 y-1).
  - Data are produced on a 1 km x 1 km grid, masked to terrestrial UK cells.
  - Deposition is provided for:
    - Grid-average (grid_NHx_dry, grid_NOy_dry, grid_NHx_wet, grid_NOy_wet)
    - Forest-only (for_NHx_dry, for_NOy_dry, for_NHx_wet, for_NOy_wet)
    - Moorland-only (mor_NHx_dry, mor_NOy_dry, mor_NHx_wet, mor_NOy_wet)
  - Data set consists of 28 CSV files per year (1990–2017), named ASSIST_N_dep_kgha_xxxx.csv, where xxxx is the year.
  - Each file includes columns for easting, northing, and the various deposition components (dry and wet, NHx and NOy; grid-average and land-cover specific).

- Data structure details (typical fields)
  - x (Easting, meters, OS British National Grid)
  - y (Northing, meters, OS British National Grid)
  - grd_NHx_dry, grd_NOy_dry (grid-average dry NHx and NOy deposition)
  - grd_NHx_wet, grd_NOy_wet (grid-average wet NHx and NOy deposition)
  - for_NHx_dry, for_NOy_dry (forest-only dry NHx/NOy)
  - for_NHx_wet, for_NOy_wet (forest-only wet NHx/NOy)
  - mor_NHx_dry, mor_NOy_dry (moorland dry NHx/NOy)
  - mor_NHx_wet, mor_NOy_wet (moorland wet NHx/NOy)
  - Additional fields follow the same structure for other land-cover combinations as needed.

- Quality control and validation
  - FRAME and its outputs have undergone extensive peer review.
  - Part of Defra model inter-comparison exercises.
  - Widely published in peer-reviewed literature.
  - Validation uses UKEAP network measurements.

- Accessibility, storage and references
  - Outputs are exported from a model output data file and stored as 1 km x 1 km terrestrial grid data.
  - Access to supporting information for UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) is provided via UK-AIR.
  - Core references include Dore et al. on FRAME development and usage, UK emission inventories, land-cover mapping, and inter-comparison/validation studies.
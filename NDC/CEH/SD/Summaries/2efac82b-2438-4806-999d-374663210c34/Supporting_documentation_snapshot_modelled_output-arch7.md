# Supporting documentation

- Purpose and scope
  - Describes model outputs for Great Britain under unmitigated climate change across 8 scenarios.
  - Provides spatially explicit data for arable area, net primary productivity (NPP), runoff, and irrigation demand.
  - Enables analysis of climate, CO2, and irrigation effects on land use using GIS-friendly formats.

- Models and driving data
  - JULES (land surface model)
    - Resolution: 1.5 km x 1.5 km grid over GB.
    - Outputs: NPP, runoff, and irrig_water.
    - File structure: tar files containing 132 files each (11 years of monthly data plus grid coordinates).
    - Variables and units:
      - npp: net primary productivity of biomass (kg m^-2 s^-1); plant types represented by indices 1–5.
      - runoff: grid cell runoff rate (mm s^-1).
      - irrig_water: irrigation water demand (mm s^-1).
  - ECO-AG (econometric agricultural land use model)
    - Resolution: 2 km x 2 km grid over GB.
    - Output: arable land area per grid cell (hectares; up to 400 ha per cell).
    - File structure: ECO_AG_{scenario}.csv containing arable area per grid cell; ECO_AG_grid_2km.csv with grid coordinates and identifiers.

- Scenarios and design
  - 8 scenarios examining combinations of climate, CO2, and irrigation effects.
  - ECO-AG does not incorporate CO2; ECO-AG scenarios labeled with No CO2.
  - JULES scenarios include combinations of Climate (present vs future), CO2 (present vs future), and Irrigation (Yes/No).
  - Climate forcing data derived from Regional Climate Model (RCM) runs at 1.5 km resolution:
    - Present climate: 1998–2008.
    - Future climate: 11-year period around 2100, with CO2 at 936 ppm (RCP8.5).

- Spatial and temporal resolution details
  - JULES outputs are provided as monthly data for 11 years, resulting in 132 monthly files per tar (plus lat/long per file).
  - Future datasets label dates 100 years later to reflect the time shift (e.g., yyyymm corresponding to future period).

- Data structure and file naming
  - JULES_output tar files: {scenario_run}_{variable}_yyyymm.nc
    - Variables: npp, runoff, irrig_water
    - yyyymm reflects present data; future data are labeled as 100 years later.
  - ECO_AG_output: ECO_AG_{scenario_run}.csv
    - Contains grid cell identifier and total arable area (ha).
  - ECO_AG_grid_2km.csv
    - Provides grid cell coordinates (easting, northing; min/max x/y) matching the grid cell identifiers.

- Data provenance and quality control
  - JULES: community-developed model led by UK Met Office and Centre for Ecology & Hydrology; access via the JULES repository (registration required). Model version vn4.9; Rose suite u-ao645.
  - ECO-AG: methodology rooted in Fezzi & Bateman (2011) and UK NEA/Follow-On studies; data built on 2 km grid using June Agricultural Census inputs; widely peer-reviewed (Fezzi et al. 2014; 2015; Bateman et al. 2013, 2014).

- Practical considerations for GIS use
  - Two distinct grids (1.5 km for JULES, 2 km for ECO-AG) require alignment when integrating datasets.
  - Coordinate information is included (lat/long for JULES; easting/northing and grid corners for ECO-AG) to support georeferencing.
  - Units and interpretation:
    - NPP, runoff, and irrigation_w d (JULES) have specified units as noted above.
    - Arable land is reported in hectares per 2 km grid cell.
  - Data extraction and workflow:
    - Extract tar archives to access monthly NetCDF files for JULES.
    - Combine ECO-AG CSV outputs with grid coordinate file for spatial analyses.
  - Accessibility:
    - JULES data requires repository registration; ECO-AG data comes in CSV formats ready for GIS ingestion.

- References
  - Bateman, I. et al., 2014; Bateman, I. J. et al., 2013; Chan, S. C. et al., 2018; Fezzi, C. et al., 2014, 2011, 2015; Kendon, E. J. et al., 2012, 2014; NEA, U., 2011.
# Supporting documentation

## Aim and scope
- Provides model outputs for Great Britain under unmitigated climate change across 8 scenarios, focusing on arable area, Net Primary Productivity (NPP), runoff, and irrigation demand.
- Combines two models: the land surface model JULES and the econometric agricultural land-use model ECO-AG.
- Outputs are produced on high-resolution grids (GB-wide) to analyze climate, CO2, and irrigation effects on land use and productivity.

## Models and driving data
- JULES (land surface model, version vn4.9) developed by the UK Met Office and CEH.
- ECO-AG econometric model, used to derive arable land area outcomes.
- Driving climate data from Regional Climate Model (RCM) runs at 1.5 km grid, daily resolution.
- Present climate constructed from 1998–2008 simulations; future climate from a 11-year period at 2100 with CO2 set to 936 ppm (RCP8.5).

## Scenarios and forcing
- 8 scenarios that isolate or combine effects of climate, CO2, and irrigation.
- ECO-AG scenarios do not include CO2 effects (CO2 column marked as No for ECO-AG in all relevant cases).
- JULES scenarios may include climate, CO2, and irrigation variations; some scenarios include CO2 and/or irrigation as indicated.
- Present-day CO2 concentration around 386.5 ppm; future concentration set to 936 ppm.

## Data outputs and file structure
- JULES outputs:
  - Stored in the JULES_output directory on a 1.5 km x 1.5 km grid.
  - Tar files for each model variable: npp, runoff, irrig_water.
  - Each tar contains 132 files (11 years × 12 months) with monthly grid-cell data plus coordinates.
  - File naming: '{scenario run}_{variable}_yyyymm.nc'.
  - Future climate data labeled as 100 years later than present data.
  - Variables:
    - npp: Net Primary Productivity by plant functional type (kg m-2 s-1) with indices for broadleaf trees, needleleaf trees, C3 grasses, C4 grasses, shrubs.
    - runoff: Grid-cell runoff rate (mm s-1).
    - irrig_water: Irrigation water demand (mm s-1).
- ECO-AG outputs:
  - Stored on a 2 km x 2 km grid over Great Britain.
  - Files named: ECO_AG_{scenario run}.csv, containing grid-cell identifier and total arable area (ha, up to 400 ha).
  - Grid coordinates provided in ECO_AG_grid_2km.csv (easting, northing, and corner coordinates) to map to grid cells.

## Climate data construction and spatial detail
- North and south GB climate data from high-resolution RC models combined with a piecewise linear weighting function to ensure smooth transitions at boundaries.
- Present-day climate uses current CO2 levels; future climate corresponds to conditions at 2100 under RCP8.5.

## Quality control and provenance
- JULES is a community-led model; data produced under a defined configuration (Rose suite u-ao645) with model version vn4.9.
- ECO-AG methodology follows Fezzi & Bateman (2011) and subsequent UK NEA studies; approach widely peer-reviewed.
- Data sources and modeling approaches are documented with references to associated publications.

## Access, reproducibility, and metadata
- JULES outputs are available via the JULES repository (registration required).
- ECO-AG outputs linked to UK National Ecosystem Assessment follow-on studies; grid and scenario metadata included in dedicated CSV files.
- Data are organized to enable replication of analyses, comparisons across scenarios, and identification of spatial patterns in productivity, water use, and land-use change.

## Practical use and considerations for analysts
- Enables exploration of correlations between climate variables, irrigation, CO2, and agricultural land use.
- Facilitates modeling of predicted impacts on arable area, productivity, runoff, and irrigation demand at high spatial resolution across GB.
- Note that ECO-AG does not incorporate CO2 effects; CO2 influence is represented in JULES for applicable scenarios.
- Users should account for potential data access hurdles (repository registration) and align grid mappings using the provided coordinate files.
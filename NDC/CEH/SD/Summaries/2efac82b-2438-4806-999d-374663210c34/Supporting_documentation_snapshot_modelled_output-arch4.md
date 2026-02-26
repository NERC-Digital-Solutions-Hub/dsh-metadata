# Supporting documentation

## Overview
- Presents model outputs from two tools, JULES (land surface model) and ECO-AG (econometric agricultural land use model), at kilometre-scale resolution over Great Britain.
- Covers 8 scenario runs using unmitigated climate change (RCP8.5).
- Outputs include arable area, net primary productivity (NPP), runoff, and irrigation demand.
- Driving climate data come from Regional Climate Model (RCM) runs for 1998–2008 (present) and 11-year future periods around 2100 (future), with CO2 levels of ~386.5 ppm present and ~936 ppm future.

## Models and outputs
- JULES: provides land surface outputs at 1.5 km × 1.5 km grid; outputs are for npp, runoff, and irrig_water.
- ECO-AG: provides arable land data on a 2 km grid over Great Britain.

## Scenarios
- Eight scenario runs combining climate, CO2, and irrigation variations:
  - ECO-AG scenarios reflect Baseline present climate, Climate only, and Climate & Irrigation (CO2 not modeled in ECO-AG; CO2 column shows “No”).
  - JULES scenarios include Present climate with Present CO2 and no irrigation, plus configurations with future climate, future CO2, and irrigation on/off combinations.
- ECO-AG does not incorporate CO2 effects; all ECO-AG results show CO2 set to No.

## Climate driving data and temporal framing
- Driving data: 1.5 km × 1.5 km resolution, daily temporal resolution from Regional Climate Models.
- Present climate: 1998–2008 realisations (Kendon et al. 2012).
- Future climate: 11-year period around 2100 (southern GB and northern GB with a piecewise linear weighting for overlap) corresponding to RCP8.5.
- Present-day CO2 ~386.5 ppm; future CO2 ~936 ppm (RCP8.5).

## Data structure and contents

- JULES_output
  - tar files, each containing data for one variable: npp, runoff, or irrig_water.
  - Each tar contains 132 files (11 years × 12 months) with monthly means for all grid cells plus grid coordinates.
  - File naming: '{scenario run}_{variable}_yyyymm.nc'.
  - Future-climate data files labeled 100 years later than present-climate data.
  - Variables:
    - npp: Net Primary Productivity (kg m-2 s-1) by plant functional type (1–5: broadleaf trees, needleleaf trees, C3 grasses, C4 grasses, shrubs).
    - runoff: Grid cell runoff rate (mm s-1).
    - irrig_water: Irrigation water demand to alleviate all water stress (mm s-1).

- ECO_AG_output
  - 2 km grid arable land data per scenario: ECO_AG_{scenario}.csv
  - Each file contains grid cell identifier and total arable area (hectares; max 400 ha) per grid cell.
  - ECO_AG_grid_2km.csv provides grid coordinates: easting/northing for cell centers and min/max corners, aligned to grid cell identifiers.

## Access, provenance, and quality control

- Data provenance
  - JULES: community-developed, led by UK Met Office and Centre for Ecology and Hydrology; version vn4.9; configuration in Rose suite u-ao645; available via JULES repository (registration required).
  - ECO-AG: methodology from Fezzi & Bateman (2011) and integrated into UK National Ecosystem Assessment workflows; data aligned to 2 km grid and based on June Agricultural Census (GB, 1972–2010).

- Quality control and documentation
  - JULES data require repository registration; detailed model configuration and versioning provided.
  - ECO-AG data built on peer-reviewed approaches and widely cited in related ecosystem service literature.
  - Data formats and grid structures explicitly described to support reproducibility and interoperability.

## Data formats, grids, and coordinates
- Grids
  - JULES: 1.5 km × 1.5 km grid; outputs stored with per-variable tar files.
  - ECO-AG: 2 km × 2 km grid; arable land data plus supplementary grid coordinates.
- Metadata and coordinates
  - Each JULES monthly file includes grid cell coordinates (longitude, latitude).
  - ECO_AG_grid_2km.csv provides easting/northing, and boundary coordinates for each grid cell.

## References
- Bateman, I. et al., 2014. UK National Ecosystem Assessment Follow-on. Work Package Report 3: Economic value of ecosystem services.
- Bateman, I. J. et al., 2013. Bringing ecosystem services into economic decision-making: land use in the United Kingdom. Science.
- Chan, S. C. et al., 2018. Projected changes in extreme precipitation over Scotland and Northern England using a high-resolution regional climate model. Climate Dynamics.
- Fezzi, C. et al., 2014. Valuing provisioning ecosystem services in agriculture: the impact of climate change on food production in the United Kingdom. Environmental and Resource Economics.
- Fezzi, C. & Bateman, I. J., 2011. Structural agricultural land use modeling for spatial agroenvironmental policy analysis. American Journal of Agricultural Economics.
- Fezzi, C. et al., 2015. The environmental impact of climate change adaptation on land use and water quality. Nature Climate Change.
- Kendon, E. J. et al., 2012/2014. Realism of rainfall in high-resolution regional climate models; and Heavier summer downpours with climate change revealed by weather forecast resolution model. Nature Climate Change.
- NEA, U., 2011. The UK national ecosystem assessment technical report. UNEP-WCMC.
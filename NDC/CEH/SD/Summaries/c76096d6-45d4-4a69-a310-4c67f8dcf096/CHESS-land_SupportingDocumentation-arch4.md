# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

## Overview
- Presents a GB-wide assessment of water, energy and carbon balance for 1961–2015 using the JULES land surface model within the CHESS framework.
- CHESS comprises model outputs, ancillary files, and meteorological forcing data (CHESS-met).

## Data sources and inputs
- Meteorology: CHESS-met dataset at 1 km2 resolution; combines daily precipitation (CEH-GEAR) with downscaled other meteorological data from MORECS.
- Land cover: fixed 2000 CEH Land Cover Map (8 categories: broad/needle leaf trees, grass, crops, shrubs, water, bare soil, urban).
- Phenology: monthly prescriptions for deciduous vegetation and crops.
- Soil hydrology: four-layer soil scheme (top 0–0.1 m to 1–3 m) using Darcy–Richards equations.
- Runoff generation: PDM approach with topography from CEH-IHDTM.
- Simulation time step and outputs: 30-second model time step; daily and monthly outputs.
- Documentation and access: MetOffice JULES repository (rose suite u-aixxx); model version jules_vn4.5, branch r3488_albmar_spdm; jules.jchmr.org for access.

## Data formats and structure
- File format: netCDF, CF-compliant, following CEH gridded dataset conventions.
- Time resolutions: monthly (all vars) and daily (subset of vars).
- File organization: yearly files; two data sets:
  - HydEn: hydrology and energy flux variables.
  - BGC: biogeochemistry variables (carbon fluxes).
- Example HydEn variables (selected): surface moisture flux, sensible/latent heat flux, surface temperature, albedo, surface runoff, evapotranspiration components, soil moisture, snow mass, routing flow.
- Example BGC variables (selected): net primary productivity (NPP), gross primary productivity (GPP), plant and soil respiration.
- Dimensionality: z dimension for tile, plant functional type (PFT), or soil layer; explicit mappings for tile, pft, and soil categories.

## Data access and documentation
- Access to driving and model configuration documented in the MetOffice JULES repository and associated rose suite u-aixxx.
- CHESS-met and CHESS-land references provide data provenance and methodological context; full catalog and code are accessible via jules.jchmr.org and the Met Office code repository.

## Usage notes and limitations
- Fixed land cover and prescribed phenology limit representations of dynamic vegetation changes.
- High-resolution meteorology relies on downscaled observational products (CEH-GEAR and MORECS), which may carry biases.
- Model outputs are validated and contextualized in referenced studies (e.g., Blyth et al., Clark & Gedney) with emphasis on evapotranspiration trends and runoff processes.

## Key references
- Best et al. (2011) on JULES model description (energy and water fluxes).
- Blyth et al. (ongoing/under review) on evapotranspiration trends in Great Britain.
- Clark & Gedney (2008) on subgrid soil moisture effects on runoff.
- Fuller et al. (2002) on UK Land Cover Map 2000.
- Keller et al. (2015) on CEH-GEAR rainfall estimates.
- Morris & Flavin (1990) on digital terrain model for hydrology.
- Robinson et al. (2017a, 2017b) on CHESS-met data and trends in atmospheric evaporative demand.
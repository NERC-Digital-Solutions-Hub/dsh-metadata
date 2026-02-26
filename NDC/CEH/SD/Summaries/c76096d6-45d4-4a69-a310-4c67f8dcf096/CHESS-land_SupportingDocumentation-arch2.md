# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

## Overview
- Objective: Assess Great Britain’s water, energy and carbon balance over 1961–2015 using the JULES land surface model driven by CHESS-meteorology data.
- Data package: CHESS-land combines JULES outputs, ancillary files, and meteorological forcing data (CHESS-met) for long-term environmental monitoring and analysis.
- Scope: Provides a consistent, GB-wide view of fluxes and storage changes to support environmental health and policy performance monitoring.

## Data and Modeling Approach
- Meteorological forcing (CHESS-met): 1 km2 resolution; precipitation from observations (CEH-GEAR) with downscaled MORES data for other variables; covers 1961–2015.
- Land cover: Fixed vegetation map from CEH Landcover2000 (2000) across 8 categories (broadleaf trees, needleleaf trees, grass, crops, shrubs, water, bare soil, urban).
- Phenology: Monthly prescribed for deciduous vegetation and crops.
- Soil hydrology: Darcy–Richards equations with four layers (0.0–0.1 m; 0.1–0.35 m; 0.35–1 m; 1–3 m); soil-type dependent parameters.
- Runoff generation: PDM approach with topography dependent on CEH-IHDTM data.
- Time step and outputs: 30-second model time step; daily and monthly outputs.
- Configuration and access: Model version jules_vn4.5; branch r3488_albmar_spdm; rose suite u-aixxx; access via MetOffice JULES repository and jules.jchmr.org.

## Data Outputs and Structure
- File format: NetCDF, CF-compliant, CEH gridded dataset conventions.
- Time resolutions: Daily and monthly outputs; yearly file organization.
- Data sets: HydEn (hydrology and energy variables) and BGC (biogeochemistry variables) sets.
- Example variables (HydEn): gridbox moisture flux (fqw_gb), surface sensible/latent heat flux (ftl_gb, le), surface/soil evapotranspiration (ei_gb, esoil_gb), surface runoff (surf_roff), soil moisture, snow mass, net/latent heat fluxes, and related surface/soil fluxes.
- Example variables (BGC): net/gross primary productivity (npp_gb, gpp_gb), plant and soil respiration (resp_p_gb, resp_s_gb).
- Dimensional structure: z dimension denotes tile type, plant functional type (pft), or soil layer (e.g., tiles: broadleaf, needleleaf, grass, crops, shrubs, water, bare soil, urban; PFTs; soil layers).

## Access and Reuse
- Data and model configurations are documented and accessible via:
  - MetOffice JULES repository (jules.jchmr.org)
  - Rose suite: u-aixxx
  - JULES version and branch: jules_vn4.5, r3488_albmar_spdm
- CHESS-met and CHESS-land data establish a reproducible forcing and flux framework for GB-scale environmental monitoring.

## Reproducibility and References
- Core components:
  - JULES model description and energy–water fluxes (Best et al., 2011)
  - CHESS-met dataset developments and GB trend analyses (Robinson et al., 2017a, 2017b)
  - Land cover and terrain data (CEH Land Cover Map 2000; Morris & Flavin, 1990)
  - Subgrid soil moisture representation and runoff (Clark & Gedney, 2008)
- Key datasets and methods underpinning the GB-wide flux assessment (1961–2015) and the associated methodological references are listed in the accompanying documentation.
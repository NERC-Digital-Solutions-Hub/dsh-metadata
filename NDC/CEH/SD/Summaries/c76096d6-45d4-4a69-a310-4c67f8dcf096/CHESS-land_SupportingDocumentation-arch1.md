# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

## Overview
- Assessment of Great Britain's water, energy, and carbon balance over 1961–2015 using the JULES land surface model integrated with CHESS meteorology forcing (CHESS-land).
- CHESS (Climate, Hydrological and Ecological research Support System) data and model outputs form a cohesive dataset used in a science paper (Blyth et al, under review).

## Data sources and forcing
- Meteorological forcing: CHESS-met dataset with 1 km2 spatial resolution.
- Precipitation: observations-based areal rainfall (CEH-GEAR) and downscaled data from MORECS for non-precipitation variables.
- Land cover: fixed 2000 vegetation map (CEH Landcover2000) across eight land-cover categories.
- Phenology: monthly prescription for deciduous vegetation and crops.
- Spatial data: topography from CEH-IHDTM database.

## Model configuration (JULES)
- Land surface processes: JULES model (v4.5) describing energy, water, and carbon fluxes.
- Soil hydrology: Darcy–Richards formulation with four vertical layers (0.0–0.1 m; 0.1–0.35 m; 0.35–1 m; 1–3 m).
- Runoff generation: PDM approach with topography-dependent parameters.
- Time step: 30 seconds; outputs provided as daily and monthly averages.
- Configuration access: MetOffice JULES repository (rose suite u-aixxx); instructions at jules.jchmr.org.
- Branches/versions: jules_vn4.5, branch r3488_albmar_spdm.

## Output data and file formats
- Format: netCDF, CF-compliant, CEH gridded dataset conventions.
- Temporal resolution: daily and monthly (two time-averaging levels).
- File organization: yearly files; data split into two sets:
  - HydEn set: hydrology and energy variables.
  - BGC set: biogeochemistry (carbon fluxes).
- Z-dimension: may denote tile (surface type), plant functional type (PFT), or soil layer.

## Variables (selected examples)
- HydEn set (surface and energy fluxes):
  - fqw_gb, ftl_gb, tstar_gb: gridbox moisture flux, surface sensible heat flux, surface temperature.
  - albedo_land, fsmc_gb, latent_heat, snow_mass_gb.
  - ecan_gb, esoil_gb, ei_gb: evaporation and sublimation components.
  - surf_roff, sub_surf_roff, rflow: surface and sub-surface runoff, routing.
  - le, ftl: tile latent and sensible heat fluxes for land tiles.
  - t_soil, smcl: sub-surface temperature and soil moisture content per layer.
- BGC set (carbon fluxes):
  - npp_gb, gpp_gb, resp_p_gb: net and gross primary productivity, plant respiration.
  - resp_s_gb: soil respiration.
  - npp, gpp, resp_p: per Plant Functional Type (PFT) equivalents.
- Z-dimensions:
  - tile: 1–8 (land cover types like broad leaf trees, grasses, crops, urban, etc.).
  - pft: 1–5 (tree, grass, crops, shrubs, etc.).
  - soil: 1–4 (soil layer depths).

## Spatial and temporal scope
- Spatial: Great Britain, 1 km2 grid resolution.
- Temporal: 1961–2015 (55 years).
- Outputs: daily and monthly aggregates; yearly netCDF files.

## Access and reproducibility
- Model and data access: CHESS-met/CHESS-land resources; MetOffice JULES repository; jules.jchmr.org.
- Data provenance: extensive references documenting model components, forcing data, land cover, and soil/runoff parameterizations.

## References
- Best et al. (2011): JULES model description, Part 1: Energy and water fluxes.
- Blyth et al.: Trends in evapotranspiration and drivers in Great Britain (to 2015).
- Clark & Gedney (2008): Subgrid soil moisture variability and runoff representation.
- Fuller et al. (2002): UK Land Cover Map 2000.
- Keller et al. (2015): CEH-GEAR rainfall estimates.
- Martinez-de la Torre et al./Robinson et al.: CHESS-met and CHESS-land datasets; related methodology.
- Morris & Flavin (1990): Digital terrain model for hydrology.
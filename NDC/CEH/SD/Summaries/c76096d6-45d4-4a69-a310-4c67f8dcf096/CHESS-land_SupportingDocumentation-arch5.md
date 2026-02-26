# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

## Overview
- Long-term GB-wide assessment (1961–2015) of water, energy and carbon fluxes using the JULES land surface model with meteorological forcing from CHESS.
- Outputs, ancillary data, and forcing data collectively referred to as CHESS (Climate, Hydrological and Ecological research Support System) in the describing paper.
- Data and methods are documented and versioned within the Met Office JULES repository and CHESS framework.

## Data and Methods

- Meteorological forcing (CHESS-met): 1 km2 resolution; combines observed daily precipitation (CEH-GEAR) and downscaled other data from MORECS.
- Land cover: fixed vegetation map from CEH Landcover2000 (2000) describing eight categories (broadleaf trees, needleleaf trees, grass, crops, shrubs, water, bare soil, urban).
- Phenology: monthly prescriptions for deciduous vegetation and crops.
- Soil hydrology: Darcy–Richards equations with four vertical layers (0.0–0.1 m, 0.1–0.35 m, 0.35–1 m, 1–3 m) with soil-type–dependent parameters.
- Runoff generation: PDM approach with topography dependence from CEH-IHDTM.
- Time step and outputs: 30-second model time step; daily and monthly output averages.
- Model configuration: jules_vn4.5, branch r3488_albmar_spdm; detailed instructions and configuration are maintained in the Met Office JULES repository (rose suite u-aixxx).
- Access and documentation: instructions available at jules.jchmr.org and via the Met Office JULES repository.

## Data Format and Structure

- File formats: netCDF, CF-compliant; follows CEH gridded dataset conventions.
- Time resolutions: monthly (full variable set) and daily (subset of variables).
- File organization: yearly files; two variable sets:
  - HydEn set: hydrology and energy variables.
  - BGC set: biogeochemistry variables (carbon fluxes).
- Example variables (HydEn set): fqw_gb, ftl_gb, tstar_gb, albedo_land, fsmc_gb, latent_heat, snow_mass_gb, ecan_gb, esoil_gb, ei_gb, fqw_soil_gb, fqw_veg_gb, surf_roff, sub_surf_roff, rflow, le, ftl, t_soil, smcl.
- Example variables (BGC set): npp_gb, gpp_gb, resp_p_gb, resp_s_gb, npp, gpp, resp_p.
- Dimensions: z may indicate tile (surface type), pft (plant functional type), or soil layer (0.0–3 m). Tile mappings include eight land-cover types.

## Data Access, Provenance and Documentation

- CHESS-met: described in Robinson et al. (2017a, 2017b); v1.2 referenced.
- JULES configuration and outputs: documented in the Met Office JULES repository; access via rose suite u-aixxx; JULES version and branch details provided (vn4.5, r3488_albmar_spdm).
- References for model components and forcing data are provided (e.g., Best et al. 2011; Clark & Gedney 2008; Fuller et al. 2002; Keller et al. 2015; Morris & Flavin 1990; Robinson et al. 2017a,b; Tanguy et al. 2016).

## Practical Considerations for Data Stewards

- Standards and interoperability: data are CF-compliant and CEH conventions-driven, with clear metadata and documentation in the JULES/CHESS repositories.
- Data governance: modular dataset structure (HydEn vs BGC) supports controlled access, updates, and potential embargo management; versioned configurations and branches documented.
- Metadata and provenance: thorough references, data sources, and model configurations are provided to support traceability and reproducibility.
- Operational considerations: large data volumes due to high-resolution forcing and long temporal span; ensure appropriate storage and transfer capabilities; ensure consistency of year-by-year file organization.

## References

- Best, M. J., et al. 2011. The Joint UK Land Environment Simulator (JULES), model description - Part 1: Energy and water fluxes.
- Blyth, E., Martínez-de la Torre, A., and Robinson, E.L. 2017–. Trends in evapotranspiration and its drivers in Great Britain: 1961 to 2015.
- Clark, D.B. and Gedney, N. 2008. Representing subgrid variability of soil moisture on runoff in a land surface model.
- Fuller, R. M., et al. 2002. The UK Land Cover Map 2000.
- Keller, V. D. J., et al. 2015. CEH-GEAR: 1 km resolution areal rainfall estimates for the UK.
- Martinez-de la Torre, A., Blyth, E., and Robinson, E. 2020 (under review). Improving river flow generation over Great Britain in a land surface model.
- Morris, D. G., and Flavin, R. W. 1990. A digital terrain model for hydrology.
- Robinson, E.L., et al. 2017a. CHESS-met meteorology dataset for Great Britain (1961–2015) v1.2.
- Robinson, E.L., et al. 2017b. Trends in atmospheric evaporative demand in Great Britain using high-resolution meteorological data.
- Tanguy, M., et al. 2016. CEH-GEAR: daily and monthly areal rainfall estimates for the UK (1890–2015).
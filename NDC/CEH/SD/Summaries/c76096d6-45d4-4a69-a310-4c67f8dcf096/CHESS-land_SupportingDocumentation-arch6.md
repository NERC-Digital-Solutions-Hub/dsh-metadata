# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

## Overview
- Objective: assess the Great Britain-wide water, energy and carbon balance over 1961–2015 using the JULES Land Surface Model forced by CHESS meteorology.
- CHESS-met data: 1 km2 resolution meteorological forcing; combines observed precipitation (CEH-GEAR) and downscaled other data from MORECS.
- CHESS-land: model outputs, ancillary files, and meteorological forcing collectively described in Blyth et al. (under review).

## Data and Methods
- Forcing data: CHESS-met (Robinson et al., 2017a,b) with daily precipitation and downscaled meteorological fields.
- Land cover and phenology: fixed vegetation map from CEH Landcover2000 (8 categories) with monthly phenology for deciduous vegetation and crops.
- Soil and hydrology: Darcy–Richards soil hydrology with four vertical layers; PDM runoff using topography from CEH-IHDTM.
- Model configuration: JULES v4.5, branch r3488_albmar_spdm; 30-second model time step; outputs as daily and monthly averages.
- Access and documentation: configuration and access via MetOffice JULES repository (rose suite u-aixxx); website jules.jchmr.org.

## Data Format and Content
- Format: netCDF, CF-compliant, following CEH gridded data conventions.
- Time resolutions: monthly (all variables) and daily (subset of variables).
- File structure: yearly files; two variable sets:
  - HydEn: hydrology and energy flux variables (e.g., moisture flux, surface fluxes, surface temperature, albedo, evapotranspiration, runoff, soil moisture, snow, etc.).
  - BGC: biogeochemistry variables (e.g., net primary productivity, gross primary productivity, plant and soil respiration).
- Example HydEn variables (selected):
  - fqw_gb, ftl_gb, tstar_gb, albedo_land, fsmc_gb, latent_heat, snow_mass_gb, ecan_gb, esoil_gb, ei_gb, fqw_soil_gb, fqw_veg_gb, surf_roff, sub_surf_roff, rflow, le, ftl, t_soil, smcl.
- Example BGC variables (selected):
  - npp_gb, gpp_gb, resp_p_gb, resp_s_gb, npp, gpp, resp_p, and related plant functional type (PFT) variables.
- Dimensionality: z-dimension may indicate tile (surface type), pft (plant functional type) or soil layer.
- Dimensional labels:
  - tile: 1=broad leaf trees, 2=needle leaf trees, 3=grass, 4=crops, 5=shrubs, 6=open water, 7=bare soil, 8=urban
  - pft: 1=broad leaf trees, 2=needle leaf trees, 3=grass, 4=crops, 5=shrubs
  - soil: 1=top layer (0.0–0.1 m), 2=second layer (0.1–0.35 m), 3=third layer (0.35–1 m), 4=bottom layer (1–3 m)

## Accessibility and Usage
- Access to configuration and data: MetOffice JULES repository (rose suite u-aixxx); JULES website for access instructions.
- Intended use: enabling end users to explore, analyse, and possibly self-serve the GB water/energy/carbon balance through CHESS-land outputs and CHESS-met forcing data.
- Documentation and evaluation: described in the associated MetOffice JULES repository and related references (see references section).

## Notes and Considerations
- Vegetation and land-cover are fixed to the 2000 map; dynamic land-cover changes are not represented.
- Model specifics and parameterizations (e.g., runoff representation, subgrid moisture effects) are embedded within the JULES configuration and CHESS framework.
- Full methodological details and evaluation are available in the MetOffice JULES repository and accompanying papers.

## References
- Best, M. J., Pryor, M., Clark, D. B., et al. The Joint UK Land Environment Simulator (JULES), model description - Part 1: Energy and water fluxes. Geosci. Model Dev., 4, 677-699, 2011.
- Blyth, E., Martínez-de la Torre, A., and Robinson, E.L.: Trends in evapotranspiration and its drivers in Great Britain: 1961 to 2015, Hydrol. Earth Syst. Sci., under review.
- Clark, D.B., and Gedney, N.: Representing subgrid variability of soil moisture on runoff in a land surface model. J. Geophys. Res. Atmos., 113(D10), 2008.
- Fuller, R. M., Smith, G. M., et al.: The UK Land Cover Map 2000. Cartographic Journal, 2002.
- Keller, V. D. J., Tanguy, M., et al.: CEH-GEAR: areal rainfall estimates for the UK, Earth Syst. Sci. Data, 2015.
- Martínez-de la Torre, A., Blyth, E., and Robinson, E.: Improving river flow generation in a land surface model, Hydrol. Earth Syst. Sci., under review.
- Morris, D. G., and Flavin, R. W.: A digital terrain model for hydrology. Proceedings, 1990.
- Robinson, E.L., Blyth, E., Clark, D.B., et al.: CHESS-met meteorology dataset for Great Britain (1961–2015) [CHESS-met] v1.2, 2017.
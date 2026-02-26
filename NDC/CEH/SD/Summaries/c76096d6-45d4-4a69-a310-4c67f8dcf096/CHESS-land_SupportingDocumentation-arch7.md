# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

- Overview
  - Simulates water, energy, and carbon fluxes for Great Britain over 1961–2015 using the JULES land surface model driven by CHESS-met meteorology data.
  - CHESS-land outputs, ancillary files, and forcing data are collectively referred to as CHESS in the accompanying science paper.

- Data sources and inputs
  - CHESS-met meteorology dataset (1 km2 resolution): combines CEH-GEAR daily precipitation with downscaled MORECS data.
  - Land cover: CEH Landcover2000 (8 vegetation categories) used to prescribe land-cover fractions.
  - Topography: CEH-IHDTM digital terrain model for runoff parameterization.
  - Vegetation phenology: monthly prescriptions for deciduous vegetation and crops.
  - Soil hydrology: Darcy–Richards equations with a four-layer soil profile.
  - Model setup and forcing details are described in the MetOffice JULES repository (rose suite u-aixxx).

- Model configuration
  - JULES version: jules_vn4.5, branch r3488_albmar_spdm.
  - Time step: 30 seconds; outputs provided as daily and monthly averages.
  - Land cover and phenology fixed from year 2000 data; topography and soil parameters influence hydrology and runoff.
  - Output ecosystem/land surface processes include surface fluxes, evapotranspiration, and carbon fluxes.

- Output format and data structure
  - File formats: NetCDF, CF-compliant, following CEH gridded dataset conventions.
  - Time resolutions: Monthly and daily (daily variables may be limited).
  - Spatial structure: Gridded 1 km2 dataset; yearly files.
  - Data sets:
    - HydEn set: hydrology and energy variables.
    - BGC set: biogeochemistry variables (carbon fluxes).
  - Variables (illustrative, with typical examples):
    - HydEn variables (daily and monthly where present): gridbox moisture flux, sensible/latent heat flux, surface temperature, albedo, soil moisture measures, various runoff terms, evapotranspiration components, surface and soil temperatures, soil moisture in layers.
    - BGC variables (daily and monthly where present): net primary productivity (npp_gb, npp), gross primary productivity (gpp_gb, gpp), plant and soil respiration (resp_p_gb, resp_s_gb; resp_p, resp_s), carbon fluxes by plant functional types (PFTs).
  - Dimensionality: z-dimension may represent tile (surface type), pft (plant functional type), or soil layer (0–3 m depth), with explicit level mappings provided for tile, pft, and soil.

- Temporal coverage and resolution
  - Coverage: 1961–2015 (55 years).
  - Outputs: daily and monthly averages; 30-second model time step driving data.

- Accessibility and access notes
  - Access instructions and repository details provided:
    - MetOffice JULES repository: https://code.metoffice.gov.uk/trac/jules
    - Access instructions: jules.jchmr.org
  - Data referencing and usage details are described in the CHESS-land documentation and associated paper (Blyth et al., under review).

- References (selected)
  - JULES model description and validation papers (Best et al., 2011; Clark & Gedney, 2008; Fuller et al., 2002; Morris & Flavin, 1990; Keller et al., 2015; Robinson et al., 2017a,b; Tanguy et al., 2016).
  - CHESS-met dataset documentation (Robinson et al., 2017a,b) and CEH-GEAR data descriptions (Keller et al., 2015).
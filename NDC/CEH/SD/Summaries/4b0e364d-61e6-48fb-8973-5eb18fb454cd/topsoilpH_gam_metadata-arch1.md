# Topsoil pH estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

- Purpose and scope
  - Provides modelled estimates of topsoil pH (0–15 cm depth) across Great Britain at 1 km2 resolution for 2007.
  - Improves on earlier simple models by incorporating climate, atmospheric deposition, habitat, soil, and spatial variables.
  - Based on Countryside Survey data from 2446 locations, with a random effect to account for nesting within 1 km2 survey squares.

- Modelling approach
  - Generalized Additive Mixed Model (GAMM) using a Tweedie distribution (variance power ≈ 1.01) due to non-Gaussian data characteristics.
  - Non-linear smooths for climate and atmospheric deposition; two-dimensional tensor product smooths for spatial coordinates (latitude/longitude) to capture large-scale spatial variation.
  - Random intercept for 1 km2 survey squares to account for clustering of samples.
  - Implementation details described in Thomas et al. 2020; full modelling details available in related CS studies.

- Data and coverage
  - Depth: 0–15 cm topsoil.
  - Spatial resolution: 1 km2 across Great Britain.
  - Sample size: 2446 locations (soil pH data used for model fitting).
  - Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
  - Dataset: CS_topsoil_ph_gam.nc
    - Soil_pH: mean pH value for 2007 modelled using GAM.
    - VAR: standard error associated with Soil_pH divided by the predicted mean (ratio).
    - x, y: Easting and Northing coordinates; supports mapping and GIS integration.
    - transverse_mercator: coordinate reference system metadata.

- Variables and data attributes (key predictors and data structure)
  - Climate-related smooth terms:
    - s(5 year mean winter temperature)
    - s(5 year mean spring temperature)
    - s(5 year mean summer temperature)
    - s(5 year mean autumn temperature)
    - s(5 year mean winter precipitation)
    - s(5 year mean spring precipitation)
    - s(5 year mean summer precipitation)
  - Atmospheric deposition terms:
    - s(3 year mean NO3 deposition)
    - s(3 year mean NH4 deposition)
    - s(3 year mean SO4 deposition)
  - Spatial terms:
    - te(Easting, Northing) with multiple configurations (1 km and others)
  - Other covariates:
    - Broad Habitat
    - CACO3 Rank
    - Soil Group
  - Data attributes include units (pH, mm, degrees Celsius, kg ha-1 yr-1), and coordinate system details.

- Sampling, calibration, and quality control
  - Field sampling following the Countryside Survey protocol:
    - Soil cores 15 cm long, 5 cm diameter.
    - 10 g field-moist soil mixed with 25 ml de-ionised water (soil to water ratio 1:2.5 by weight) for pH measurement.
  - Quality control and methodological references:
    - Emmett et al. (2008, 2010) provide full soil sampling and analytical procedures.
    - Data preparation and methodology aligned with Defra/NERC Joint Codes of Practice.

- Data sources and supporting references
  - Primary data: Countryside Survey (CS) 2007 soil pH observations (Reynolds et al. 2013).
  - Climate data: Met Office (various sources; 5 km resolution, 2003–07)
  - Atmospheric deposition data: CBED (2005), NOx/NHx/SO4 deposition estimates
  - Land Cover Map 2007 (Morton et al. 2014)
  - Soil and parent material references from British Geological Survey
  - Related methodological details in Thomas et al. (2020)

- How to use and interpret outputs
  - Provides spatially explicit estimates of topsoil pH across GB at 1 km2 resolution for 2007.
  - Output includes mean pH and the VAR ratio (uncertainty measure) per grid cell.
  - Suitable for analyses linking pH with biodiversity, nutrient availability, and land-use change at regional scales.
  - The full analytical framework and carbon-related analyses are described in Thomas et al. (2020).

- Limitations and considerations for analysts
  - Based on 2007 data; temporal applicability may be limited for current conditions.
  - Depth restricted to 0–15 cm; results do not represent deeper soil pH profiles.
  - Model relies on multiple external datasets (climate, deposition, land cover); uncertainties propagate through to pH estimates.
  - Spatial smoothing and random effects address large-scale patterns but may obscure very localized variability.
  - Access to metadata and reproducibility relies on references and potentially requires GIS tools to work with the CS_topsoil_ph_gam.nc dataset.
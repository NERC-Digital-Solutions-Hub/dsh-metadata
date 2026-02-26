# Topsoil carbon concentration estimates from the Countryside Survey of Great Britain, 2007 using a Generalized Additive Model

## Overview
- Presents modelled estimates of topsoil carbon concentration (g kg-1) in the 0–15 cm soil depth across Great Britain for 2007.
- Output derived from Countryside Survey (CS) data using a Generalized Additive Mixed Model (GAMM) with non-linear and spatial components.
- Model built from 2,446 sampling locations and includes a random effect to account for nesting within 1 km² CS survey squares.
- Model type: Tweedie distribution (variance power = 1.99) fitted via mgcv in R; full details in Thomas et al. 2020.
- Outputs are designed for standardised environmental monitoring and can be stored in datasets and disseminated via portals.

## Model framework and inputs
- Core approach: Generalized Additive Mixed Model (GAMM) incorporating climate, atmospheric deposition, habitat, soil, and spatial variables.
- Spatial structure: two-dimensional tensor product smooths for latitude/longitude to capture large-scale spatial variation.
- Non-linear terms: smoothed functions applied to climate and deposition predictors.
- Temporal and spatial scales: 5-year means for summer temperature/precipitation, 5-year winter temperature, and 3-year deposition metrics for NH4 and NO3; spatial resolution targeted at 1 km and 5 km for different terms.
- Data sources integrated:
  - Met Office climate data (summer/winter temperatures, precipitation)
  - Atmospheric deposition data (NH4, NO3, SO4)
  - Land cover and habitat datasets (Land Cover Map 2007, broad habitat classes)
  - Soil and parent material information (British Geological Survey)
  - Other supporting spatial datasets (e.g., 1 km CS survey square structure)

## Data attributes and outputs
- Primary dataset: CS_topsoil_carbon_gam.nc
  - Soil_OrgC_Conc: Mean soil carbon concentration in 2007 (g kg⁻¹)
  - VAR: Standard Error relative to the predicted mean (ratio)
  - x, y: Easting and Northing coordinates (OSGB 1936 / British National Grid, meters)
  - transverse_mercator: coordinate reference system indicator
- Spatial resolution and coverage: modeled estimates across Great Britain at approximately 1 km² resolution.
- Modeling outputs include maps and charts suitable for monitoring environmental health and policy performance.

## Sampling, calibration, and quality control
- Field sampling: Soil carbon measured from 15 cm long by 5 cm diameter cores; samples air-dried to 2 mm sieve.
- Laboratory analysis: Loss-on-ignition (LOI) used to estimate organic content; LOI (%) converted to carbon concentration by multiplying by a factor of 0.55.
- Standards and accreditation: CEH UKAS accredited method SOP3102; Defra/NERC Joint Codes of Practice followed.
- Foundational references for methods: Emmett et al. (2008, 2010) CS soils manuals; Reynolds et al. (2013) for CS soil change; Henrys et al. (2012) for earlier model estimates.

## Data provenance and references
- Supporting documents and data sources underpinning the model and its inputs:
  - Reynolds et al. (2013): Countryside Survey “Soil Change” (1978–2007) for topsoils
  - Emmett et al. (2008, 2010): CS soils manuals and 2007 soils report
  - Henrys et al. (2012): Model estimates of topsoil carbon
  - Met Office (2014): UK climate projections data
  - Morton et al. (2014): Land Cover Map 2007
  - Dore et al. (2015): Atmospheric deposition model inter-comparison
  - Thomas et al. (2020): Patterns and trends of topsoil carbon in the UK
  - British Geological Survey: Soil Parent Material Model
- Full methodological details are provided in Thomas et al. (2020).

## Relevance to monitoring and data stewardship
- Aligns with the Analysts Monitoring the Environment aim to present consistent, quality-assured environmental indicators.
- Demonstrates data verification, cleaning, and transformation from established sources.
- Delivers standardised outputs (maps, charts, reports) and ensures datasets are stored for portal access, facilitating broader reuse.
- Addresses challenges of: (1) increasing the value of monitoring datasets by integrating with additional data, and (2) enabling access to underlying data used to create outputs.
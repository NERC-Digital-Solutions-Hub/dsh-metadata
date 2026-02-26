# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

- Purpose: Provide high-resolution, daily UK soil moisture maps to support understanding of hydrological and ecological processes, with quantified uncertainty and a transparent modelling approach. Outputs are updated daily with a lag of about one week.
- Scope: UK and Ireland at 2-km resolution, covering 2016–2023, focusing on topsoil moisture (roughly 15–30 cm, depth varies with soil wetness).

## Data inputs and sources

- COSMOS-UK network
  - Cosmic-ray neutron sensors measure soil moisture in the top 15–30 cm over footprints ~100–240 m radius.
  - Provides the primary calibration dataset (about 61,225 daily observations after quality filtering).
- Soils data
  - Porosity estimates using bulk density and soil organic carbon, with UK-specific and rest-of-domain methodologies to derive porosity.
- Meteorological data
  - Precipitation from Met Office NIMROD, assimilated into the UKV high-resolution weather model (2-km, frequent updates; bias corrections applied).
  - Other variables from UKV for model development (e.g., vapour pressure deficit implications).
- SCAT-SAR Soil Water Index (SWI)
  - Fusion of Sentinel-1 SAR soil moisture with ASCAT scatterometer data, providing high-temporal and high-spatial-resolution SSM info (daily, ~1 km over Europe).
- NRFA data
  - Daily river discharge and catchment precipitation from the UK National River Flow Archive, used to capture spatial variation in precipitation–storage relationships across ~1,212 catchments (hydrometric areas).

## Modelling approach

- Core model
  - Simple hierarchical Bayesian model linking soil moisture to EMA precipitation, vapour pressure deficit, and SCAT-SAR SWI.
  - Random intercepts for site-level non-independence; site-specific deviations b_s.
  - Predictive structure: moisture deficit from saturation is modelled as a function of precipitation, D, and I, with uncertainty quantified via posterior distributions.
- Parameter calibration and spatial variation
  - Regional variation in precipitation response (β_P) inferred using NRFA-derived estimates of change in soil storage, ΔS, linked to EMA precipitation changes.
  - β_P,s scaled by local slope m_s relative to the nationwide mean m̄, enabling spatial heterogeneity in the precipitation response.
- Spatial extrapolation
  - 2-km grid predictions via kriging using a Matérn covariance model to interpolate β_P,s across space.
  - Bayesian kriging accounts for uncertainty in the variogram parameters (σ, φ, ν) with uniform priors; geoR package used for implementation.
- Uncertainty and quality control
  - Bayesian Hamiltonian MCMC used to estimate parameter and prediction distributions, providing robust uncertainty quantification.
  - Uncertainty also propagated through the spatial extrapolation (variogram uncertainty).
  - Data gaps in Met Office NWP-UKV data are not filled; days with missing data are excluded from the deposited dataset.

## Outputs and data structure

- Format and grid
  - Outputs stored as GeoTIFF raster files on a 2-km UK/Ireland grid (704 rows × 548 columns; OS GB coordinates; 385,792 cells total).
- Variables and units
  - Daily volumetric soil moisture: m3 water per m3 soil (dimensionless volume fraction).
  - Depth corresponds to a top-soil layer whose thickness varies with soil moisture (about 15–30 cm, decreasing exponentially with distance from sensors).

## Data quality, completeness, and limitations

- Data completeness
  - Some periods have missing Met Office NWP-UKV data; such days are omitted from the deposited dataset.
- Model limitations
  - Absolute soil moisture values over large regions are inferred via spatial extrapolation rather than direct measurement; depth z is unknown, so relative changes are emphasized.
  - SCAT-SAR and porosity estimates introduce uncertainties in regional predictions.
- Depth variability
  - The effective measurement depth varies with soil moisture, complicating direct comparisons across locations with different soil properties.

## Applications and relevance for environmental monitoring

- Hydrology and flood risk
  - High-resolution soil moisture informs runoff generation and catchment response to precipitation events.
- Agriculture and irrigation
  - Provides near-real-time indicators of soil water availability to guide irrigation planning and crop management.
- Ecology and greenhouse gas emissions
  - Soil moisture influences microbial processes affecting nitrous oxide and methane fluxes.
- Drought and front-tracking
  - Daily maps capture short-term variations due to weather fronts and prolonged droughts, supporting drought assessment and response.

## Data availability and accessibility

- Repository and access
  - Data are stored and deposited via the Centre for Environmental Data Analysis (CEDA).
  - Daily outputs incorporate inputs from COSMOS-UK, soils, meteorology, SCAT-SAR SWI, and NRFA data.
- Update policy
  - Predictions and inputs are updated daily, lagging real time by about one week.

## Key challenges and future directions

- Data value and integration
  - Increasing the value of these datasets by combining with additional relevant datasets beyond the current inputs.
- Data accessibility
  - Enhancing access to the underlying datasets and provenance to support broader reuse and cross-study analyses.

## References and methodological context

- Highlights of data sources, modeling choices, and statistical methods are anchored in cosmopolitan literature on soil moisture remote sensing, kriging, and Bayesian hierarchical modelling (COSMOS-UK, CRN literature, kriging methodology, geoR, and related datasets).
- Notable components include EMA precipitation, Cartesian integration of SWI, and Bayesian spatial inference to quantify uncertainty.
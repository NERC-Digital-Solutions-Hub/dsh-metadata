# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

- Purpose and scope
  - Develop and provide daily maps of soil moisture for the UK at 2-km resolution (2016–2023) to support hydrological and ecological decision-making.
  - Address limitations of existing remotely sensed soil moisture by using a simple, transparent empirical model calibrated with in-situ observations and multiple data streams.
  - Produce predictions with quantified uncertainty and near-real-time timeliness (updates daily, lagging ~1 week).

- Data sources and inputs
  - COSMOS-UK network: cosmic-ray neutron sensors measuring soil moisture in the top ~15–30 cm; ~40 sites contributing ~60k observations after quality filtering.
  - Soils data: porosity derived from bulk density and soil carbon (GB and rest of domain) to estimate soil-water retention properties.
  - Meteorology: precipitation from Met Office NIMROD-based UKV high-resolution model (2-km radar-satellite rainfall data with bias corrections); additional meteorological variables from UKV.
  - SCAT-SAR SWI: fusion of Sentinel-1 SAR soil moisture and ASCAT SCAT data; provides daily, high-resolution (1 km) soil moisture index.
  - NRFA data: daily river flow and catchment precipitation across ~1212 gauging sites, grouped into hydrometric areas; used to inform spatial variation in model parameters.
  - Missing data: some periods with gaps in Met Office data; gaps are not filled.

- Modelling approach
  - Simple statistical model in a Bayesian hierarchical framework to explain daily soil moisture at time t and site s.
  - Core equation uses: exponentially weighted moving average (EMA) of precipitation, vapour pressure deficit, and SCAT-SAR soil wetness index, plus site-specific random effects.
  - Local site deviations (random intercepts) account for within-site correlation.
  - Spatial variation in a key precipitation sensitivity parameter (βP) is informed by NRFA-derived estimates of soil-water storage change (ΔS) in catchments, mapped to relative βP_s across sites.
  - βP,s is derived by scaling a global βP with the NRFA-based slope ratio (m_s / mean m), linking changes in soil storage to changes in precipitation.
  - Spatial extrapolation to the 2-km UK grid via kriging using the Matérn covariance model; parameters treated in a Bayesian manner to incorporate uncertainty.

- Uncertainty and quality control
  - Bayesian calibration (Hamiltonian MCMC) used to quantify uncertainty in parameters and predictions.
  - Uncertainty in the variogram model (kriging) is incorporated via posterior sampling (Bayesian kriging with geoR).
  - Multiple realisations reflect parameter and spatial-model uncertainty.
  - Quality control of COSMOS data is described in prior work; missing data periods are excluded from the deposited dataset.

- Data structure and outputs
  - Outputs stored as TIFF rasters on a 2-km grid covering the UK and Ireland.
  - Grid: 704 rows × 548 columns (OSGB coordinate system).
  - Recorded values: volumetric soil moisture (m3 water per m3 soil) for a variable soil depth between ~15–30 cm (depth changes with soil moisture, decaying with distance from the surface).

- Key findings and performance
  - The simple empirical model explains about 70% of the variance in daily COSMOS soil-moisture observations.
  - Capable of reproducing fine-scale, short-term variations driven by sporadic precipitation, including orographic and convective rainfall patterns.
  - 2016–2023 predictions show realistic front propagation and drought responses.
  - Outputs update daily with a lag of roughly one week and require negligible computation time for generation.

- Implications for monitoring and policy
  - Provides a high-resolution, near-real-time soil moisture product that can inform flood risk assessment, irrigation planning, crop management, and ecological modeling.
  - Combines multiple data streams (in-situ COSMOS, satellite SWI, radar rainfall, river flow) to yield a robust monitoring variable with quantified uncertainty.
  - The Bayesian framework explicitly represents uncertainty in parameters, spatial extrapolation, and predictions, supporting risk-based decision-making.
  - Encourages data provenance and governance considerations (transparent methods, reproducible uncertainty quantification, and clear data structure).

- Limitations and considerations for data governance
  - Gaps in input data periods reduce completeness; gaps are not imputed.
  - Porosity estimates and depth-of-sensing variability introduce model-related uncertainties.
  - Spatial extrapolation relies on NRFA catchments; accuracy depends on the representativeness of gauge data.
  - Ensuring metadata, versioning, and openness of underlying data and methods is important to avoid barriers to data sharing and reuse.

- Access and availability
  - Data are provided as raster TIFF files on a 2-km grid (704 × 548) over the UK and Ireland.
  - Depth is a responsive top-soil layer (15–30 cm) with depth varying by soil moisture and location.
  - Updates are produced daily with a ~1-week lag; methodology and uncertainty quantification are embedded in the analysis.
# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

- Purpose: to produce daily, high-resolution maps of UK soil moisture (2-km grid) using a simple empirical model calibrated with COSMOS-UK cosmic-ray neutron sensor data.
- Key finding: the model explains approximately 70% of the daily variance in COSMOS observations and can reproduce patterns from more complex process-based models.
- Outputs: daily SMUK predictions with high temporal and spatial detail, capturing weather-front passages and drought periods; updates lag about one week behind real time.
- Practical value: enables detailed understanding of soil moisture dynamics for hydrology, ecology, flood risk, crop and irrigation planning, and greenhouse gas-relevant processes.

## Abstract
- They present an empirical, Bayesian-calibrated model to map soil moisture across the UK at 2-km resolution, driven by precipitation, humidity, a remotely-sensed soil water index, and soil porosity.
- Calibration uses five years of COSMOS-UK observations from ~40 sites.
- The model captures small-scale and short-term moisture variability and provides quantified predictive uncertainty.

## Data sources
- COSMOS network: cosmic-ray neutron sensors providing near-surface soil moisture (top 15–30 cm) with ~100–240 m footprint; used as the primary calibration dataset (61225 daily observations after quality filtering).
- Soils data: porosity estimated from bulk density and soil organic carbon for GB and analogous mapped data for Ireland/edge of Europe; methods account for organic soils with porosity >70%.
- Meteorological data: precipitation from Met Office NIMROD system and other variables from the UKV high-resolution forecast model; 2-km, high-temporal-resolution precipitation data (every five minutes).
- SCAT-SAR: fusion of Sentinel-1 SAR soil moisture with ASCAT scatterometer data to produce high-resolution daily SWI (1 km over Europe) with radiometric and temporal smoothing.
- NRFA data: daily river flow and catchment precipitation across ~1212 gauging sites; used to derive spatially varying responses via catchment-scale water balance estimates.
- Data organization and quality: data stored on a 2-km grid; missing periods in Met Office data are not filled.

## Model development
- Model form: a simple hierarchical statistical model predicting soil moisture at time t and site s based on an exponential moving average (EMA) of precipitation, vapour pressure deficit, and SCAT-SAR Soil Wetness Index, with a site-specific random intercept.
- Core equation: theta_t_s' = beta0 + beta_s(P_t_s) + beta_b(D_t_s) + beta1(I_t_s) + b_s + epsilon_t_s; theta_t_s = theta_max,s - theta_t_s'
- Spatial variation: use NRFA catchment data to inform spatial variation in precipitation response (beta_P). Estimate local slope m_s from regression of changes in estimated soil storage against changes in EMA precipitation; relate beta_P,s to global beta_P adjusted by m_s/mean(m).
- Parameter estimation: Bayesian calibration (MCMC) to obtain posterior distributions for parameters and predictions; uncertainty is explicitly quantified.
- Spatial extrapolation: kriging with a Matérn covariance model to predict beta_P across the UK grid; Bayesian kriging accounts for variogram uncertainty via posterior sampling.
- Software: geoR package in R used for Bayesian kriging; prior distributions are uniform for key variogram parameters.

## Spatial extrapolation of beta_P
- Objective: transform site-level beta_P estimates into 2-km grid predictions across the UK.
- Approach: Bayesian kriging with Matérn covariance, sampling from posterior variogram parameters to propagate uncertainty into spatial predictions.

## Quality control
- COSMOS data quality control follows prior work; model calibration uses Hamiltonian Monte Carlo to quantify parameter uncertainty.
- Uncertainty in the semivariogram is incorporated by treating variogram parameters as distributions rather than fixed values, with posterior sampling to reflect this in predictions.
- Missing data handling: periods with missing Met Office data are not interpolated; records for days with missing soil moisture calculations are removed from deposited datasets.

## Missing data
- Some periods in the Met Office NWP-UKV data are missing; these gaps are not filled, so the soil moisture dataset is not complete for those days.
- Data for days without calculated soil moisture are removed from the public dataset.

## Details of data structure
- Data format: TIFF files with raster data on a 2-km UK/Ireland grid.
- Grid dimensions: 704 rows × 548 columns (ncell ~385,792).
- Projection: OS GB coordinate system (Transverse Mercator).
- Example: metadata provided for a sample file (e.g., 1 July 2023).

## Nature and units of recorded values
- Variable: volumetric soil moisture (m3 water per m3 soil).
- Depth: effectively a variable soil layer depth between 15–30 cm, deepest in dry conditions and shallower in wet conditions, with exponential decline of footprint sensitivity with radius.
# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

## Executive overview
- Introduces SMUK, a daily 2-km UK soil moisture map produced with a simple empirical model calibrated to COSMOS-UK cosmic-ray neutron sensor data (~40 sites) from 2016–2023.
- Model inputs: precipitation (EMA), vapour pressure deficit, SCAT-SAR Soil Water Index, and soil porosity.
- Predicts volumetric soil moisture with ~70% variance explained relative to observations; captures fine-scale, short-term variations due to precipitation, including orographic and convective effects.
- Spatial variation in precipitation response (βP) is informed by NRFA catchment data; predictions are extrapolated to a 2-km grid via Bayesian kriging with a Matérn covariance.
- Parameter and prediction uncertainty are quantified via Bayesian calibration (MCMC) and Bayesian kriging; updates are daily with about a one-week lag.
- Data are stored as 2-km raster TIFFs; depth corresponds to a variable top-soil layer (roughly 15–30 cm, depth adjusts with soil moisture).

## Data sources and inputs
- COSMOS-UK: network of cosmic-ray neutron sensors, ~61,225 daily observations after quality filtering; footprints ~100–240 m; sensitive to top 15–30 cm soil moisture.
- Soils data: porosity estimated from bulk density and soil organic carbon; GB and rest-of-domain differences accounted for; LUCAS-based covariates used.
- Meteorological data: Met Office NIMROD-derived precipitation at 2-km resolution, with high-resolution UKV model inputs; radar-based precipitation corrected for bias.
- SCAT-SAR: fusion of Sentinel-1 SAR soil moisture and ASCAT data, daily 1-km SWI with SNR-based weighting and normalization.
- NRFA data: daily river flow and catchment precipitation across ~1,212 gauging locations, grouped into ~100 hydrometric areas.

## Modelling approach
- Hierarchical model with site-specific random intercepts to account for non-independence within COSMOS sites.
- θ_t_s′ (model-estimated soil moisture deviation) is driven by:
  - EMA precipitation (P_t_s)
  - vapour pressure deficit (D_t_s)
  - SCAT-SAR SWI (I_t_s)
- Relationship to actual soil moisture θ_t_s via θ_max,s − θ_t_s′; βP derived from NRFA-based slopes to capture spatial variation in precipitation response.
- Use of NRFA catchment data to estimate relative spatial variation in βP:
  - Compute ΔŜ per catchment from P − Q − Epot
  - Regress ΔŜ on Δ⟨P⟩ to obtain m_s, scale βP by m_s/mean(m)
- Spatial extrapolation to a 2-km grid via kriging with a Matérn covariance; implemented in a Bayesian framework (geoR) to propagate variogram uncertainty.

## Quality control and uncertainty
- Data quality control for COSMOS data described in prior work; uncertainty explicitly quantified via Hamiltonian MCMC (Bayesian) to produce posterior parameter and prediction distributions.
- Uncertainty also propagated through the Bayesian kriging step, treating variogram parameters as distributions.
- Missing data periods in Met Office NWP-UKV data are not filled; days lacking calculable soil moisture are removed from the deposited dataset.

## Data product structure and access
- Data stored as raster TIFFs on a 2-km grid over the UK and Ireland (704 rows × 548 columns; OS GB coordinate system).
- Each file corresponds to a timestamp (e.g., 1 July 2023) with header metadata.
- Recorded values: volumetric soil moisture (m3 water per m3 soil); depth corresponds to a dynamic surface layer (15–30 cm, varying with soil moisture).

## Key results and implications
- Predictive performance: model explains ~70% of daily soil moisture variance observed by COSMOS.
- Temporal and spatial detail: high input resolution enables realistic representation of weather-front passages and droughts.
- Computationally efficient: very low compute time for inputs and predictions; suitable for near-real-time updates with a modest lag.
- Data integration demonstrates effective cross-system data fusion (in-situ sensors, satellite indices, meteorology, river data, and soil properties).

## Relevance for data leadership and strategy
- Data integration and atlas-style products:
  - Combines diverse data streams (in-situ, satellite, radar, catchment, soil properties) into a coherent, gridded product.
  - Demonstrates governance around multi-source data provenance, alignment of spatial and temporal scales, and traceability of data lineage.
- Uncertainty-aware analytics:
  - Provides full posterior distributions for model parameters and predictions; important for risk-aware decision making in hydrology, agriculture, and climate impacts.
- Data quality, metadata, and discoverability:
  - Clear data structure (TIFFs with headers), documented inputs, and an explicit missing-data policy; data deposited in a centralized repository (CEDA) to support discoverability.
- Operational and strategic value:
  - Near-real-time soil moisture mapping supports flood risk assessment, irrigation planning, crop management, and ecological studies.
  - The approach offers a blueprint for building resilient, auditable data products that surface uncertainty and enable cross-sector collaboration.

## Limitations and considerations for future work
- Depth variability: top-soil depth is dynamic and device-to-site dependent; potential refinements to fixed-depth assumptions.
- Data gaps: periods with missing NWP-UKV data remain unfilled, limiting continuous coverage.
- Spatial density of ground truth: calibration relies on ~40 COSMOS sites; expanding sensor networks could improve spatial inference and reduce uncertainty.
- Generalizability: method tuned to UK conditions; adaptation required for other regions with different data ecosystems.
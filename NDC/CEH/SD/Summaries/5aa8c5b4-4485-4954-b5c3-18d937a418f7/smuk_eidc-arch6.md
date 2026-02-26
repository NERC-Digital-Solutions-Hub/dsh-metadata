# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

## Overview
- Introduces a simple empirical, Bayesian-calibrated model to produce daily UK soil moisture maps at 2-km resolution (SMUK) using COSMOS-UK neutron sensors, satellite and meteorological inputs.
- Explains about 70% of the variance in daily COSMOS observations is explained by the model.
- High spatial (2-km) and temporal (daily) resolution enables detailed capture of precipitation-driven soil moisture dynamics, including orographic and convective rainfall patterns.
- Outputs update daily with a lag of about one week and require negligible computation time.

## Data sources
- COSMOS-UK network: cosmic-ray neutron sensors measuring soil moisture in the top ~15–30 cm (footprint ~100–240 m); provides daily moisture observations.
- Soils data: soil porosity estimated from UK Countryside Survey (GB) and other sources for Ireland/edge Europe; porosity derived from bulk density and carbon data; used to compute porosity for the model.
- Meteorological data: precipitation from Met Office NIMROD system, assimilated into UKV high-resolution forecast; other variables from UKV model.
- SCAT-SAR: SCAT-SAR SWI combining Sentinel-1 SAR and ASCAT scatterometer data to deliver high-resolution daily soil moisture (1 km, Europe-wide since 2015).
- NRFA data: UK National River Flow Archive provides daily river discharge and catchment precipitation data across ~1,212 catchments; used to inform spatial variation of precipitation response.
  
## Model development
- Structure: simple hierarchical Bayesian model predicting volumetric soil moisture θt,s at time t and site s, using:
  - EMA (exponential moving average) of precipitation Pt,s
  - Vapour pressure deficit Dt,s
  - SCAT-SAR Soil Wetness Index It,s
  - Local site effects bs
- Core equation (conceptual):
  - θt,s′ = β0 + βs(Pt,s) + βbDt,s + β1It,s + bs + εt,s; bs ∼ N(0,Ψ), εt,s ∼ N(0,σ2)
  - Actual soil moisture θt,s = θmax,s − θt,s′
- Spatial variation: use NRFA catchment data to estimate how the precipitation response parameter βP varies spatially:
  - Compute ΔŜ ≈ P − Q − Epot for each NRFA catchment
  - Fit ΔŜ = e + m Δ⟨P⟩; relate βP,s to global βP via βP,s = βP (ms / m̄)
- Addressing depth uncertainty: m relates to change in soil water storage; absolute moisture depends on depth z, which is unknown; spatial patterns used as a proxy for βP variation.

## Spatial extrapolation (kriging)
- Goal: Predict βP,s across a 2-km UK grid from 1,212 NRFA-informed estimates.
- Approach: Bayesian kriging with Matérn covariance to model spatial correlation; predictions weighted by semivariogram.
- Software: geoR package in R; Bayesian treatment accounts for uncertainty in variogram parameters (σ, φ, ν) with uniform priors; multiple realizations used to represent uncertainty.

## Quality control
- Data quality: COSMOS data quality control as per prior work; Bayesian MCMC (Hamiltonian) used to estimate parameter posteriors and predictive uncertainty.
- Uncertainty: both parameter and spatial predictions represented via posterior distributions; variogram uncertainty incorporated through Bayesian kriging.
- Missing data: some NWP-UKV periods have missing data; such days are omitted from the deposited dataset (no imputation for those days).

## Missing data handling
- Gaps in Met Office NWP-UKV data exist; no imputation performed, leading to incomplete daily soil moisture records for some days.
- Deposited data exclude days with no calculable soil moisture output.

## Data structure and delivery
- Format: TIFF rasters on a 2-km grid for UK and Ireland.
- Grid: 704 × 548 cells; OsGB Transverse Mercator projection; 2-km resolution.
- Example: header excerpt shown indicates 704×548×385,792 data cells.
- Units: volumetric soil moisture (m3 water per m3 soil); effectively a shallow, surface layer whose depth (15–30 cm) varies with soil moisture.

## Nature and units of recorded values
- Values represent volumetric soil moisture in the topsoil layer; depth changes with soil moisture (shallower when wet, deeper when dry), modeled as an exponential depth decay within 15–30 cm range.

## Applications and implications
- Enables near-real-time monitoring of soil moisture for hydrology, flood risk assessment, plant growth, irrigation planning, and soil-atmosphere studies.
- Provides a scalable, high-resolution dataset that can be used to study weather-front dynamics, drought periods, and their ecological and agricultural impacts.
- Uncertainty quantification supports risk-based decision making and transparent communication of model confidence.

## Accessibility and reuse
- Data are stored as standardized 2-km TIFF rasters covering the UK and Ireland; updated daily with about a one-week lag.
- Methodology combines multiple data streams (COSMOS, SCAT-SAR, radar-rainfall, NRFA) within a transparent Bayesian framework, enabling reproducibility and extension.
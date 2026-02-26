# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

## Overview
- Presents SMUK, a daily, high-resolution (2-km) UK soil moisture map series (2016–2023) built from a simple empirical model calibrated with COSMOS-UK cosmic-ray neutron sensor data.
- Aims to produce near-real-time, spatially detailed soil moisture estimates with quantified uncertainty, capable of capturing short-term and small-scale hydrological variability.
- Updates are daily with a lag of about one week; computation is lightweight, enabling timely predictions.

## Data sources and inputs
- COSMOS-UK network: provides daily soil moisture observations (top 15–30 cm) from cosmic-ray sensors; footprint ~100–240 m.
- Soils data: porosity estimates derived from bulk density and soil carbon maps; GB and rest of domain use region-specific data.
- Meteorological data: precipitation from Met Office NIMROD assimilated into UKV model; additional meteorological inputs from UKV for model development.
- SCAT-SAR Soil Water Index: fusion of Sentinel-1 SAR and ASCAT data for high-resolution soil moisture information.
- NRFA data: daily river flow and catchment precipitation across GB, used to inform spatial variation of model parameters.
- Data are stored as 2-km TIFF rasters covering the UK and Ireland.

## Model approach
- Simple Bayesian hierarchical model predicting soil moisture at time t and site s via:
  - EMA-processed precipitation (P)
  - Vapour pressure deficit (D)
  - SCAT-SAR Soil Water Index (I)
  - Site-specific random effects
- Parameters (β) include βP, βD, βI with a maximum soil moisture reference (θmax) and a deviation term.
- Spatial variation in βP is inferred indirectly using NRFA catchment data:
  - Compute ΔS estimates from P, Q, and Epot; derive slope m_s relating ΔS to changes in EMA precipitation.
  - Scale global βP by the ratio m_s/mean(m) to obtain site-level βP,s.
- Spatial extrapolation to 2-km grid via kriging with a Matérn covariance, implemented in a Bayesian framework.

## Spatial extrapolation and uncertainty
- Geostatistical extrapolation (kriging) accounts for spatial dependence and provides unbiased, minimum-variance estimates.
- Uncertainty in the semivariogram is incorporated via Bayesian kriging (geoR), with uninformative priors for σ, φ, ν.
- Uncertainty propagation through both parameter estimation (MCMC) and spatial prediction to quantify predictive uncertainty.

## Quality control and data handling
- Quality control of COSMOS inputs referenced and applied during model calibration.
- Bayesian methods (Hamiltonian MCMC) used to estimate parameter distributions and prediction uncertainty.
- Missing data: some periods in the Met Office NWP-UKV dataset exist; days with missing soil moisture predictions are removed from deposited data (no imputation for gaps).
- Missing days are excluded to maintain dataset integrity and reproducibility.

## Data structure and units
- Outputs stored as 2-km-resolution TIFF rasters.
- Grid: 704 rows × 548 columns (OSGB Transverse Mercator projection).
- Recorded values: volumetric soil moisture (m3 water per m3 soil).
- Depth of measurement varies with soil moisture; typically 15–30 cm depth, depth adapting to moisture conditions.

## Practical implications for data stewardship
- Data provenance: multiple, heterogeneous data sources (COSMOS, soils, Met Office, SCAT-SAR, NRFA) require clear metadata and lineage tracking.
- Standardization: harmonization of inputs (units, depth, temporal resolution) essential for interoperability and reuse.
- Metadata and documentation: explicit articulation of model assumptions, parameter estimation, uncertainty quantification, and data gaps.
- Reproducibility: Bayesian calibration and kriging steps documented and implementable via R (geoR) to enable auditability.
- Access and sharing: deposition in data archive with explicit data gaps handling; updated outputs enable near-real-time applications in hydrology, ecology, flood risk, agriculture, and climate research.
- Governance considerations: management of large, multi-source datasets, update cycles, and transparency around uncertainty and methodological choices.

## Limitations and challenges
- Incomplete picture of some input data and missing periods in NWP-UKV require careful handling and documented gaps.
- Data creators and multiple systems/formats present interoperability challenges; bespoke handling needed for porosity and SCAT-SAR inputs.
- Large, high-resolution datasets and cross-border coverage demand robust storage, metadata, and update workflows.

## Endnotes
- The methodology demonstrates that a relatively simple, Bayesian, data-driven model can emulate more complex process-based soil moisture dynamics while delivering high-resolution, timely maps with quantified uncertainty.
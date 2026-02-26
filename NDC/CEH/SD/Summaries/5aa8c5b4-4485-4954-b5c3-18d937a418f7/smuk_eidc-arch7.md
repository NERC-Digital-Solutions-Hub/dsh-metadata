# Daily soil moisture maps for the UK (2016-2023) at 2 km resolution

- Purpose: Present a high-resolution, daily UK soil moisture map product (SMUK) at 2-km resolution, suitable for map-based GIS analyses and environmental decision-making. The approach provides quantified predictive uncertainty and captures detailed spatial-temporal variability.

## Data sources and inputs (used to drive the model)

- COSMOS-UK cosmic-ray neutron sensors: ground-truth daily soil moisture observations at ~40 sites (61225 measurements after quality filtering).
- Soils and porosity: site-specific porosity estimates derived from UK Countryside Survey data (GB) and LUCAS-based maps (rest of domain).
- Meteorological data: precipitation from Met Office NIMROD integrated with UKV atmospheric model; additional meteorological variables from UKV.
- SCAT-SAR SWI: daily 1 km Soil Water Index product from SCAT-SAR fusion (Sentinel-1 SAR + ASCAT).
- NRFA river flow data: daily catchment-scale precipitation and discharge data across ~1212 catchments (used to inform spatial variation of precipitation response).
- Missing days: periods with missing Met Office data are excluded from the dataset.

## Modelling approach

- Simple Bayesian hierarchical model to link daily soil moisture to predictors:
  - θ_t_s' = β0 + β_s(P_t_s) + β_b D_t_s + β1 I_t_s + b_s + ε_t_s
  - where θ is soil moisture deviation from saturation, P is EMA precipitation, D is vapour pressure deficit, I is SCAT-SAR SWI, b_s is a site-specific random intercept.
- Spatial variation in rainfall response β_P is inferred using NRFA-based estimates:
  - ΔŜ ≈ P − Q − E_pot; slope m_s relates ΔŜ to Δ⟨P⟩; β_P,s = β_P × (m_s / mean(m)).
- Spatial extrapolation to a 2-km UK-wide grid via kriging with a Matérn covariance model, implemented in a Bayesian framework (geoR in R).
- Uncertainty: full posterior distributions for parameters and spatial predictions are quantified via Hamiltonian MCMC; variogram parameters also estimated with uncertainty (Bayesian kriging).

## Output structure and data products

- Data are stored as raster TIF files on a 2-km grid over the UK and Ireland.
- Grid: 704 × 548 cells in OS GB coordinate system (Transverse Mercator).
- Output units: volumetric soil moisture (m3 water per m3 soil); depth corresponds to a shallow surface layer, effectively varying between ~15–30 cm depending on soil moisture.
- Temporal coverage: daily maps for 2016–2023; updates lag real time by about one week; some days removed when data gaps existed.

## Quality control and data gaps

- COSMOS data quality-controlled; Bayesian MCMC used for robust parameter and predictive uncertainty estimation.
- Missing data: some days have no soil moisture estimates due to NWP-UKV data gaps; these days are excluded from the deposited data.

## Key characteristics and implications for GIS use

- Resolution and responsiveness: 2-km spatial resolution with daily updates suitable for event-driven mapping (e.g., fronts, droughts) and large-scale hydrological or ecological analyses.
- Uncertainty aware: predictive uncertainty is explicitly quantified and propagated in the spatial estimates.
- Data fusion: integrates satellite (SCAT-SAR SWI), radar-derived precipitation, ground observations, and catchment-scale water balance data for robust spatial patterns.
- Computational efficiency: model has negligible computation time, enabling regular updates.

## Practical considerations for GIS specialists

- Data format: single-band TIF rasters with georeferenced 2-km grid; consistent 704 × 548 grid layout.
- Projection: OS GB Transverse Mercator; easy to align with other UK GIS layers.
- Spatial variability: β_P s values are regionally informed via NRFA-based slopes, improving predictions in data-sparse areas.
- Use cases: flood risk assessment, drought monitoring, agricultural planning, ecosystem and greenhouse gas interaction studies, policy reporting at national/regional scales.

## Limitations and caveats

- Absolute soil moisture values are model-derived and dependent on calibration to COSMOS observations; thus, uncertainty is inherent and explicitly modeled.
- Some Day-to-day persistence depends on the quality and coverage of input data (e.g., SCAT-SAR SWI and NRFA-based refinements).
- The depth of the moisture estimate is variable with soil conditions, so applications requiring precise depth-specific moisture should consider the provided depth interpretation.

## References and further information

- SMUK methodology, data sources, and validation are described in the associated study and Citations within the document (COSMOS-UK, SCAT-SAR SWI, NRFA, and Met Office data sources).
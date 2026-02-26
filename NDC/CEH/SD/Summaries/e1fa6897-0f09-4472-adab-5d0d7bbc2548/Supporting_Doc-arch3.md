# Snow water equivalent estimates using cosmic-ray neutron sensors in the United Kingdom (2014-2019)

## Overview
- This dataset provides daily estimates of Snow Water Equivalent (SWE) for the United Kingdom using cosmic-ray neutron sensors (CRNS) and, where available, supporting sensors.
- Primary SWE estimates come from multiple methods:
  - CRNS-based SWE: SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3
  - SnowFox buried-sensor SWE: SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3
  - Snowmelt model SWE: SWE_MODEL (PACK snowmelt model)
  - Depth-based SWE: SWE_DEPTH
- Inputs include CRNS/SnowFox count rates, snow-free rate estimates, soil moisture considerations, albedo, temperature, precipitation, and snow depth measurements.
- Albedo is used to identify snow onset/retreat; daily 24-hour SWE estimates are provided with uncertainty estimates.

## Data structure, sites, and coverage
- Timeframe: data collected up to the 2018/19 winter season; daily SWE estimates are provided for each snow day.
- Sites: originally 50 COSMOS-UK sites; after quality checks, 44 sites contribute data (forest-dominated sites excluded due to footprint complexities; some sites had no detected snow).
- Snow events: 263 snow events recorded across the dataset; per-event figures are provided to assess reliability.
- Metadata: site identifiers, coordinates, installation dates, decommission dates, SNOW_SITE flags (presence of SnowFox/depth sensors), and data provenance are included.
- Outputs: for each snow event at each site, a figure summarises SWE estimates, precipitation, temperature, count rates, and albedo.

## SWE estimation methods in detail
- CRNS-based SWE (SWE_CRNS_1, SWE_CRNS_2, SWE_CRNS_3)
  - Inputs: CTS_CRNS (daily average corrected CRNS count rate), CTS_SNOWFREE_1/2/3 (snow-free rate estimates), N_WAT (CRNS count rate over infinite depth of water).
  - Snow-free rate estimation methods:
    - Method 1: adjust only if lower than current rate to avoid negative SWE.
    - Method 2: also accounts for soil moisture variation using two local probes.
    - Method 3: uses the minimum soil moisture change to reduce artefacts from probe data.
  - Recommendation: Method 3 often marginally most accurate, though added complexity may not always be justified.
- SnowFox SWE (SWE_SNOWFOX_1, SWE_SNOWFOX_2, SWE_SNOWFOX_3)
  - Inputs: SnowFox count rate normalised by snow-free rate (CTS_SNOWFOX_SNOWFREE_1/2/3); attenuation curve applied.
  - Note: SnowFox footprint is small, making results more sensitive to snowpack inhomogeneity.
  - Bias: SnowFox SWE estimates tend to be about 1.7 times larger than other methods (not corrected in data).
- Snowmelt model SWE (SWE_MODEL)
  - Based on PACK snowmelt model (Moore et al., 1999) using local air temperature and precipitation; snow vs. rain determined by temperature threshold.
  - Data quality: precipitation input filtered; suspicious precipitation leads to removal of some snow events (e.g., 29 events removed; additional removals for suspicious values).
- Depth-based SWE (SWE_DEPTH)
  - Inputs: daily median snow-depth from sonic sensors (30-minute data); background height subtracted using a robust method.
  - Conversion: 0.1 g/cm3 density assumed for fresh snow to convert depth to SWE.
  - Quality control: days with significant depth decrease (>20% from max) are excluded from SWE_DEPTH; some depths removed after manual checks.
- Albedo (ALBEDO)
  - Mean albedo between 10:00 and 14:00 GMT used to detect snow presence; snow events start when albedo > 0.5 and end when albedo < 0.35.
  - Two snow-free days are required to end an event to avoid misclassification due to short-term albedo fluctuations.
  - Site-specific considerations: Hollin Hill posed challenges due to slope and radiometer orientation; cross-checked with phenocams.
- Uncertainty estimates
  - CRNS and SnowFox: typical one-standard-deviation uncertainties ≈ 4 mm; slightly higher later in the event; dependence on soil moisture noted.
  - Depth-based SWE: uncertainties ≈ 4 mm.
  - Snowmelt model: uncertainties around 5 mm; model uncertainties may increase as the event progresses.
  - For CRNS, uncertainties UNCERT_CRNS_1/2/3 reflect method choice due to soil moisture dependence; for SnowFox, UNCERT_SNOWFOX_1/2/3 show weaker soil-moisture dependence.

## Data quality, processing, and governance
- Data processing includes quality assurance, data cleaning, and transformation into usable SWE estimates; figures accompany each snow event to aid assessment of reliability.
- Data availability and open governance
  - Open Government Licence; data accessible via DOI; citation requirements specified.
  - Clear documentation of methods, inputs, and QC steps supports reuse and evaluation in monitoring frameworks.
- Practical considerations and caveats
  - SnowFox bias (larger SWE estimates) and method-dependent uncertainties should be considered when using the dataset for policy monitoring or trend analysis.
  - Precipitation input quality directly affects Snowmelt model outputs; some events are excluded due to data quality concerns.
  - The multi-method approach (CRNS, SnowFox, model, depth) provides cross-validation potential but requires careful interpretation of inter-method differences.

## Relevance for monitoring frameworks and policy evaluation
- Demonstrates how multiple complementary sensors and models can be combined to produce robust environmental health indicators (SWE) across a broad footprint, improving representativeness for heterogeneous snowpacks.
- Highlights the importance of:
  - Metadata completeness and standardization (site details, installation/decommission dates, SNOW_SITE flags).
  - Transparent data processing workflows and explicit uncertainty quantification to inform decision-making.
  - Clear data governance and licensing to enable reuse in monitoring programs.
  - Per-event visualization and documentation to support rapid assessment of measurement reliability.
- Provides a concrete example of handling data gaps, quality controls, and disclosure of potential biases (e.g., SnowFox bias) within a monitoring framework.
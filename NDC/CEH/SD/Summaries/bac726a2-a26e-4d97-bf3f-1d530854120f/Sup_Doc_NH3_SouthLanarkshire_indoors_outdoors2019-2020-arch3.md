# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two sites in a rural area of South Lanarkshire: one indoor (hall of dwelling) and one outdoor (garden of dwelling) adjacent to grassland and a large dairy farm.
- Local site operator: dwelling owner; analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.
- Use of CEH ALPHA® passive samplers to measure NH3 concentrations; sampling occurs in monthly cycles at the beginning of each month.

## Sampling and Analysis Method
- CEH ALPHA® sampler: passive NH3 sampler with a citric acid coated filter and a white PTFE membrane; membrane faces downward during exposure.
- Replicates used per site to improve reliability; samplers mounted on shelters on posts at ~1.5 m above ground.
- Analysis workflow: exposed samplers extracted into deionised water; ammonium quantified by SEAL AA3 colorimetry; ammonium concentration converted to ambient NH3 concentration using a known uptake rate of 0.003241315 m³ h⁻¹ and the exposure duration.
- Data represent monthly average NH3 concentrations (µg NH3 m⁻³) for each site.

## Data Quality and Flags
- Raw data are flagged for concerns; quality checks applied.
- QA rules:
  - Coefficient of variation (CV) of replicate samplers: CV < 15% considered valid; >15% prompts evaluation of replicates.
  - Some results exceed calibration range but are still considered valid if remeasurement isn’t possible.
  - Missing data are flagged (-9999) where measurement or metadata is unavailable.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv; includes site names, spatial identifiers, and data flags.
- Data status and flags are complemented by detailed EMEP coding to convey verification, calibration, and quality concerns.

## Dataset contents and structure
- Each row represents one month of data for a single site.
- Columns include:
  - Station name (site name)
  - Unique site identifier
  - network_id
  - parameter_id (alpha_NH3_g)
  - measurement start date and time (exposure start)
  - measurement end date and time (exposure end)
  - measurement (ammonia concentration; units: µg NH3 m⁻³)
  - less than (indicator if value is below detection limit)
  - verification id
  - unit id (µg NH3 m⁻³)
  - Data capture (percentage)
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status code)
  - Month-Year (mm-yy)

## Site Information
- Inside
  - Start date: 01/01/17; End: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in hall of dwelling
- Outside
  - Start date: 01/01/17; End: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in garden of dwelling

## Data governance and accessibility
- Data are structured for transparency with explicit metadata and flags to aid verification and interpretation.
- Dataset fields and site identifiers are documented (pages referenced in the source) to support data sharing and reproducibility.
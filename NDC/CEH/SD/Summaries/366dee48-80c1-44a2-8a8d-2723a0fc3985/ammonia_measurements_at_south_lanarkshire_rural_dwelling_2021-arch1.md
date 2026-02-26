# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

- Two sites in a rural dwelling in South Lanarkshire: inside (hall) and outside (garden), with garden adjoining grassland from a large dairy farm.
- Operator: dwelling owner (site duties); analysis conducted by Centre for Ecology and Hydrology Edinburgh.
- Sampling design: UKCEH ALPHA® passive samplers exposed monthly, with replicate samplers to improve reliability.
- Timeframe and scope: data are presented for indoor and outdoor NH3 measurements; final dataset named NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv; the document title references 2021 but the dataset covers 2019–2020 (data collection includes ongoing series since 2017).

## Methodology

- Sampler design: UKCEH ALPHA® passive sampler using a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter and faces downward during exposure.
- Deployment: samplers mounted on a shelter on a pole at about 1.5 m above ground; replicates used per site for robust concentration estimation.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 using colorimetry on the resulting ammonium concentration.
- Concentration calculation: ammonium concentration converted to average NH3 in air using a known sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Data handling: data flagged for concerns; quality assessed with criteria described below; final dataset includes site name, exposure period, and NH3 concentration (µg NH3 m-3).

## Data quality and flags

- Quality rule: coefficient of variation (CV) across replicates must be <15% to consider the measurement valid; CV >15% leads to evaluation of replicates, and data can still be valid and flagged (103) if deemed representative.
- Calibration considerations: values greater than calibration range can be considered valid if remeasurement/dilution was not possible due to instrument failures.
- Missing data: represented as -9999 for measurement or meta data when not available.
- Data status: final dataset uses coded fields for verification (e.g., Verified, Preliminary Verified), data capture percentage, and validity status.
- EMEP/UK-Polar flag codes: extensive flag mapping is provided to annotate data quality issues (e.g., detection limits, contamination, sampling anomalies, nearby activities) and may appear in the EMEP code field.
- Data flags and notes sources: details are documented in the data quality section (e.g., page 4) and within the EMEP flag explanations.

## Dataset structure and contents

- Final dataset name: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv.
- Each row represents one month of data for a single site.
- Core fields include:
  - Site id and Site name
  - Network id (RSW)
  - Parameter id (alpha_NH3_g)
  - Measurement start date/time; measurement end date/time
  - Measurement (NH3 concentration in µg NH3 m-3)
  - Less than flag (whether value is below detection limit)
  - Verification id (quality verification status)
  - Unit id (µg NH3 m-3)
  - Data capture percentage
  - Validity id (valid or not valid)
  - EMEP data status code and constituent flags
  - Month-Year of measurement (mmm-yy)
  - Comments on data
- Data fields provide granular metadata to support traceability and reuse, including calibration notes and data status.

## Site context and metadata

- Inside site: located in hall of dwelling; coordinates 55.64072, -3.59705; air inlet height 1.5 m; start date 01/01/17; end date ongoing.
- Outside site: located in garden of dwelling; same coordinates and inlet height (1.5 m); start date 01/01/17; end date ongoing.
- Spatial context: indoor and outdoor measurements share the same dwelling coordinates, with the outdoor site backed by grassland near a large dairy operation.

## Data provenance, access, and usage notes

- Data provenance: collected with UKCEH ALPHA samplers; analysis conducted by CEH Edinburgh; data are prepared with standardized metadata and are intended to be discoverable via portals with full metadata.
- Practical use: useful for examining correlations and trends in indoor vs. outdoor NH3 concentrations at a rural dwelling, with attention to data quality flags and local source influences (nearby dairy farm).
- Cautions for analysts: account for potential data gaps or flagged quality concerns, CV-based validity decisions, calibration range limitations, and the need to consult the EMEP/flag documentation for specific data issues.
# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Two sampling sites in a rural area of South Lanarkshire: one inside the hall of a dwelling, one outside in the dwelling’s garden.
- Local site operator duties are carried out by the dwelling owner; analysis is performed by the Centre for Ecology and Hydrology (CEH) Edinburgh.
- Data collected using CEH ALPHA® passive samplers to measure ammonia concentrations in air; samplers exposed monthly at the start of each month.
- Locations are near grassland that forms part of a large dairy farm.

## Sampling Method and Analysis (GIS context)
- CEH ALPHA® samplers use a citric acid coated filter to capture NH3; protected by a white PTFE membrane that allows diffusion of gaseous ammonia.
- Samplers are mounted on shelters at about 1.5 m above ground; replicates are used to improve reliability.
- Analysis involves extracting samplers into deionised water and measuring ammonium colorimetrically with SEAL AA3; results converted to average NH3 concentration in air using a known uptake rate (0.003241315 m³ h⁻¹) and exposure duration.
- Units: micrograms of NH3 per cubic metre of air (µg NH3 m⁻3).

## Data Quality and Flags
- Data have been flagged to indicate concerns; quality checks include:
  - Coefficient of variation (CV) of replicates must be ≤ 15% to be considered valid.
  - Some samples exceed calibration range but are still deemed valid due to practical constraints.
  - Missing data are marked with -9999 in the field.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv, with data values and appropriate flags.
- Data quality and status are encoded with a detailed flag system (including verification, data capture, validity, and EMEP-related codes).

## Dataset Structure (Spatial and Temporal Context)
- The final dataset contains one row per month per site, identified by site name, with fields including:
  - Station name, unique site identifier, network_id
  - Parameter type (alpha_NH3_g)
  - Measurement start and end dates/times (exposure period)
  - Ammonia concentration (µg NH3 m⁻³)
  - Flags: less than detection, verification status, unit id, data capture percentage, validity_id, EMEP data status
  - Month-Year (MMM-YY)
- EMEP flag codes accompany measurements to indicate data treatment and metadata status.

## Site Information
- Inside site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072, Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the hall of the dwelling
- Outside site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072, Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the garden of the dwelling

## Potential GIS Uses
- Map monthly NH3 concentrations for the two proximal sites (inside vs. outside) over the 2019–2020 period.
- Compare spatial context and data quality flags to identify reliable months for mapping.
- Join NH3 data with site polygon/point features using the provided coordinates and site identifiers for visualization and analysis in GIS workflows.
- Incorporate QC flags (CV, detection limit, data capture, validity) into metadata layers to inform map symbology and data confidence.
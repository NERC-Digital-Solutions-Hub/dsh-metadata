# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

## Overview
- Atmospheric ammonia concentrations measured at five moss sites (Fenn's, Whixall, Bettisfield, Wem, Cadney Mosses SAC/SSSI) as part of LIFE project within SNAP.
- Local site operator duties by Natural England; analysis by CEH Lancaster; data processing by CEH Edinburgh.
- Sampling occurred in monthly exposure cycles initiated at the beginning of each month in 2018.
- Data products produced: final accepted dataset FWBWC_ammonia_measurements_2018.csv with site-specific monthly ammonia concentrations (units: µg NH3 m-3).

## Sampling Method (CEH ALPHA samplers)
- CEH ALPHA passive sampler uses a citric acid coated filter to capture NH3; protected by a white PTFE membrane.
- Membrane oriented downwards during exposure; samplers mounted ~1.5 m above ground on shelters.
- Replicates used per site to improve reliability; samplers kept in protective plastic containers.
- Exposed monthly; sampling period aligned to monthly cycle.

## Analysis and Data Processing
- Analysis: exposed samplers are extracted into deionised water and analyzed by SEAL AA3 colorimetric ammonium assay.
- Concentration in air calculated from sampler concentration using a fixed uptake rate: 0.0028986 m3 hr-1 (UKEAP 2018 uptake rate for UK) and the exposure duration in hours.
- Data quality checks applied to raw data:
  - Coefficient of variation (CV) of replicates must be < 15%; otherwise evaluated for discarding replicates or marking data as valid with notes.
  - Missing samplers coded as -9999.00 and marked invalid (-1).
  - Deviations in exposure duration (long/short) flagged.
  - Local contamination or deviations noted by site operator; non-representative results discarded.
- Final dataset: FWBWC_ammonia_measurements_2018.csv containing accepted values with appropriate flags; accompanying metadata describes site identifiers and spatial identifiers.

## Data Structure and Variables (Dataset Contents)
- Each row represents one month of data for a single site.
- Core columns include:
  - Site name and unique site identifier; network_id (UWT); parameter_id (alpha_NH3_g).
  - Measurement start date/time and end date/time (exposure period).
  - Ammonia concentration (units: µg NH3 m-3).
  - Flags for detection limit (<) and verification status; unit_id (24 = µg NH3 m-3).
  - Data capture percentage; validity_id (1 = valid, -1 = not valid).
  - EMEP code with multiple data-status flags (data capture, validity, and contamination/other reasons).
  - Month-Year of measurement (MMM-YY).
- The document provides a detailed tabular description for these fields and the interpretation of EMEP flags.

## EMEP Flags and Data Quality Indicators
- EMEP flag system encodes data capture status and reasons for validity or invalidity, including:
  - Missing measurements, below detection limit, below detection/quantification, representative sampling periods, contamination reasons (agricultural, industrial, dust, etc.), and CV-related validity.
  - Examples include codes indicating missing measurements, detection-limit values, sampling period deviations, and contamination signals; many codes indicate data considered valid with the stated caveats.
- Users should consult the EMEP codes to interpret data quality and any caveats attached to individual measurements.

## Spatial Information
- Site Information examples included:
  - MM01: start_date 01/07/2018; End date Ongoing; Latitude 52.925; Longitude -2.777; Inlet height 1.5 m.
  - MM02: start_date 01/07/2018; End date Ongoing; Latitude 52.932; Longitude -2.751; Inlet height 1.5 m.
  - MM03: start_date 01/07/2018; End date Ongoing; Latitude 52.924; Longitude -2.758; Inlet height 1.5 m.
- Spatial identifiers enable GIS mapping of monitoring locations and integration with other spatial datasets.

## Practical Notes for GIS Specialists
- Data are monthly, site-specific ammonia concentrations with accompanying quality and validity flags; units are µg NH3 m-3.
- The dataset supports map-based visualization of spatial NH3 patterns and time-series analyses by site and month.
- Apply quality filters using CV, data capture, validity flags, and EMEP codes to ensure robust GIS analyses.
- The dataset name to reference: FWBWC_ammonia_measurements_2018.csv; site names and coordinates are provided, enabling geospatial joins and mapping.
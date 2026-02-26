# Sup_Doc_NH3_UWT_Cuilcagh

## Overview
- Data describe ammonia (NH3) monitoring around Cuilcagh, Ireland and Northern Ireland to assess local NH3 impacts on vegetation.
- Operators: Ulster Wildlife Trust (site operation) and UK Centre for Ecology and Hydrology Edinburgh (analysis).
- Method: UK CEH ALPHA® passive samplers deployed monthly, typically at 1.5 m above ground, with replicate samplers for each site.

## Sampling Method
- Passive sampling with citric acid coated filter to capture ammonia; PTFE membrane protects the filter and faces downward during exposure.
- Replicate samplers attached to shelters on poles, about 1.5 m high; triplicate sampling used for reliability.
- Devices housed in plastic containers for protection; exposure occurs in monthly cycles at the start of each month.

## Analysis Method
- Exposed samplers are extracted with deionised water and analyzed (SEAL AA3) via colorimetry to determine ammonium concentration.
- NH3 concentration in air calculated from ammonium concentration using a fixed uptake rate of 0.003241315 m3 h-1, exposure duration, and lab blanks.
- Data are flagged for concerns where applicable.

## Data Quality and Validation
- Raw data screened using predefined quality rules; results are flagged and evaluated for acceptance.
- Validation rules:
  - Coefficient of variation (replicates) < 15%: accepted; if >15%, assess discarding replicates; if deemed representative, data flagged as valid (103).
  - Values above calibration range may be valid if re-measurement wasn't possible due to instrument issues.
  - Missing data or meta data marked with -9999; missing timestamps prevent calculation of concentration.

## Dataset Structure and Flags
- Final dataset: NH3_Cuilcagh2020.csv containing accepted values with associated flags; includes site identifiers and spatial data.
- Columns and meanings (selected):
  - Site name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Less-than flag, verification id (1=Verified, 2= Preliminary verified, 3= Not verified)
  - Unit id (24 = µg NH3 m-3), data capture percentage, Validity_id (1=valid, -1=not valid)
  - EMEP code and data status codes
  - Month-Year, Comments
- EMEP flags provide detail on data quality and context (e.g., below detection limit, calibration range issues, nearby sources, contamination).
  - Examples: 103 (CV of replicates >15% but valid), 781/780 (values at or near detection/quantification limits but valid), 653/654 (sampling period deemed representative), 559/557/556 (valid with various contamination considerations), 593/591 (industrial/agricultural contamination deemed invalid).

## Site Information
- Boardwalk: start 01/02/2020; end ongoing; Lat 54.218694, Lon -7.823424; inlet height 1.5 m.
- Eshvagh: start 01/02/2020; end ongoing; Lat 54.190490, Lon -7.846421; inlet height 1.5 m.
- Corcashel: start 01/02/2020; end ongoing; Lat 54.187536, Lon -7.973599; inlet height 1.5 m.
- Grouse Project: start 01/02/2020; end ongoing; Lat 54.130905, Lon -7.896038; inlet height 1.5 m.
- Shridrinagh: start 01/02/2020; end ongoing; Lat 54.119063, Lon -7.995085; inlet height 1.5 m.

## Relevance for Monitoring Frameworks
- Demonstrates end-to-end monitoring workflow: site operations, sampling design (triplicate passive samplers), laboratory analysis, data processing, and quality assurance.
- Provides a structured data schema with explicit metadata, data capture metrics, and standardized flags (including extensive EMEP-related flags) to support interoperability and cross-dataset comparability.
- Highlights governance aspects: need for clear data provenance, documentation of methods, transparency of quality controls, and the potential data-sharing barriers related to metadata completeness and openness.
- Addresses common framework challenges: data gaps, silos, and metadata shortcomings; underscores the importance of data governance, timeliness, and public access to underlying data and metadata.
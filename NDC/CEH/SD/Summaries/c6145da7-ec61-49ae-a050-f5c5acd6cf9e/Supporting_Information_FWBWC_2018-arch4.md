# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

## Overview
- Data accompany ammonia measurements collected with CEH ALPHA samplers during the LIFE project’s Site Nitrogen Action Plan (SNAP) implementation on Fenn ' s, Whixall, Bettisfield, Wem and Cadney Mosses SAC, SSSI.
- Local site operator duties are performed by Natural England (NE); analysis by Centre for Ecology and Hydrology (CEH) Lancaster; data processing by CEH Edinburgh.
- Samplers are exposed in monthly cycles at the beginning of each month.

## Sampling and Analysis Method
- CEH ALPHA ® sampler is a passive device using a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter.
- Membrane oriented downwards during exposure; samplers mounted on a shelter on a pole at about 1.5 m above ground.
- Replicate samplers used to improve reliability; samples stored in protective plastic containers.
- Analysis involves extracting exposed samplers into deionised water, then using SEAL AA3 colorimetric detection to determine ammonia concentration.
- Converts sampler concentration to an average air concentration for the exposure period using a known uptake rate (0.0028986 m³ h⁻¹; UKEAP 2018) and exposure duration.

## Quality Control and Data Validation
- Data quality checks applied to raw data:
  - Coefficient of variation (CV) across replicates must be < 15%; otherwise replicates are reassessed; valid results flagged as 103 if representative.
  - Missing samplers are set to -9999.00 and marked invalid (-1).
  - Sampler durations longer or shorter than the typical monthly cycle are flagged.
  - Local contamination or non-representative deviations noted; affected samplers may be discarded; reported data is the average of remaining results.
- Final dataset is the accepted values, with appropriate flags.

## Dataset and Structure
- Final dataset: FWBWC_ammonia_measurements_2018.csv
- Each row represents one month’s data for a single site; columns include:
  - Site name and unique site identifier
  - network_id (UWT)
  - parameter_id (alpha_NH3_g)
  - Measurement start and end dates and times
  - Exposure ammonia concentration (units: µg NH3 m⁻³)
  - Less than detection flag
  - Verification id
  - Unit id (24 = µg NH3 m⁻³)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP data status code
  - Month-Year (mmm-yy)
- Dataset contents and field meanings are detailed in the accompanying documentation (site names with spatial identifiers provided on page 5; page 3 lists column contents).

## Data Flags and Codes (EMEP Flags)
- Data capture and validity are governed by EMEP flags, indicating reasons such as:
  - Missing measurement or data capture issues
  - Values below detection limit or below quantification limit
  - Valid/invalid indicators and accompanying reasoning
  - Sampling period alterations (longer/shorter than normal) still considered valid if representative
  - Contamination or local influences (e.g., agricultural or industrial sources, dust, smoke)
- A comprehensive mapping of flags to data status and rationale is included (e.g., 99 9 for missing capture; 78 1 for valid with value below detection limit; various codes for contamination and sampling period conditions).

## Site Information
- Monitoring sites (MM01, MM02, MM03) with:
  - Start date: 01/07/2018
  - End date: Ongoing
  - Geographic coordinates (Latitude and Longitude)
  - Inlet height above ground: 1.5 m
- Example entries:
  - MM01: Lat 52.925, Lon -2.777
  - MM02: Lat 52.932, Lon -2.751
  - MM03: Lat 52.924, Lon -2.758
- All sites share the same exposure height and ongoing data collection status.

## Data Stewardship and Accessibility
- Roles clearly defined: NE (site operator), CEH Lancaster (analysis), CEH Edinburgh (data processing).
- Data are organized to support discoverability and reuse, with detailed metadata and standardized fields to facilitate integration into broader data systems.
- The dataset supports ongoing analysis under the SNAP LIFE project and can support data-driven decisions and cross-network data collaboration, with explicit attention to data quality, provenance, and user needs.
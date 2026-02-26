# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

## Overview
- Data arising from atmospheric ammonia monitoring with CEH ALPHA samplers during the Site Nitrogen Action Plan (SNAP) implementation on Fenn ' s, Whixall, Bettisfield, Wem and Cadney Mosses SAC, SSSI as part of the LIFE project.
- Responsibilities: Natural England (NE) as local site operator; Centre for Ecology and Hydrology (CEH) Lancaster handles analysis; data processing by CEH Edinburgh.
- Samplers deployed monthly in replicates to estimate ambient NH3 concentrations.

## CEH ALPHA sampler method
- Passive sampling device using a citric acid coated filter to capture ammonia; white PTFE membrane protects the filter and allows NH3 diffusion.
- Orientation: membrane end facing downwards during exposure; protected cap when not exposed.
- Setup: replicate samplers mounted on a shelter on a pole at ~1.5 m above ground; samplers stored in protective plastic containers.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetric method; results converted to average ambient NH3 concentration for the exposure period using a known uptake rate (0.0028986 m3 h-1, UK uptake rate from UKEAP 2018) and exposure duration.

## Data processing and quality assurance
- Data quality checks applied to raw measurements:
  - Coefficient of variation (CV) < 15% across replicates; CVs > 15% trigger review of replicates; if replicates are not discarded and the average is considered representative, the data are valid and flagged as 103.
  - Missing samplers: replaced by -9999.00 and marked invalid (-1).
  - Sampler duration mismatch: data flagged when exposure duration is longer or shorter than the usual monthly cycle.
  - Local contamination or influences: site operator notes used to evaluate and potentially discard non-representative results; reported as the average of remaining results.
- The final dataset contains accepted data values, flagged appropriately for quality issues.

## Dataset content and structure
- Final dataset file name: FWBWC_ammonia_measurements_2018.csv
- Structure: each row corresponds to one month’s data for a single site; columns include site name, start/end dates, ammonia concentration for the exposure period, and a data flag, plus extensive metadata.
- Concentration units: micrograms of ammonia per cubic meter of air (µg NH3 m-3).
- Key columns (with purpose):
  - Site information: site name, unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g).
  - Temporal: measurement start date/time, measurement end date/time, month-year.
  - Measurement: ammonia concentration; less than flag (indicates values below detection limit of 0.03).
  - Verification: verification id; unit id (24 = µg NH3 m-3); data capture percentage; validity_id (1 = valid, -1 = not valid).
  - Data status: EMEP code and related EMEP flags describing data status and quality (e.g., contamination, detection limits, sampling period adjustments).

## Data format and identifiers
- Columns include: station name, unique site identifier, network_id, parameter_id, measurement start date and time, measurement end date and time, exposure start and end, ammonia concentration, less than flag, verification id, unit id, data capture (%), validity_id, EMEP code, and Month-Year.
- EMEP flags provide a standardized set of statuses and reasons (e.g., missing data, below detection limit, valid measurement with estimation, contamination, atypical sampling duration).

## EMEP flags and data status (summary)
- EMEP flag structure encodes:
  - Data capture percentage and validity (valid/invald status).
  - Reasoning for any data issues (e.g., missing measurements, below detection limit, contamination, irregular sampling duration, nearby activities).
- Examples of statuses include:
  - Values below detection/quantification limits or requiring estimation.
  - Missing or contaminated data due to local influences.
  - Sampling period longer or shorter than normal but considered representative.
- These flags enable users to assess data reliability and suitability for analysis or integration with other datasets.

## Site information (examples)
- MM01: start 01/07/2018; end ongoing; coordinates ~52.925 N, -2.777 W; inlet height 1.5 m.
- MM02: start 01/07/2018; end ongoing; coordinates ~52.932 N, -2.751 W; inlet height 1.5 m.
- MM03: start 01/07/2018; end ongoing; coordinates ~52.924 N, -2.758 W; inlet height 1.5 m.

## Usage notes
- Data reflect monthly-average ambient NH3 concentrations derived from replicated ALPHA samplers.
- Units are µg NH3 m-3; data include quality flags to indicate validity and any caveats.
- Data processing and quality assurance are documented to support traceability and re-use in broader analyses and reporting.
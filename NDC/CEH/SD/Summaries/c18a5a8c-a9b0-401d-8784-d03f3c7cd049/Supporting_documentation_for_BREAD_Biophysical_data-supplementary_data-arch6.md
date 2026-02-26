# IPORE Soil EC, Water Content, and Temperature Data Collection Protocol

## Overview
- Protocol describes experimental design, sampling, calibration, and quality control for soil water content, pore water conductivity (ECp), and soil temperature data collected in Konicha and 1st Choroko, Ethiopia.
- Data collected with a W.E.T sensor across multiple households and fertility zones to capture spatial and temporal variability.

## Experimental design and sampling regime
- Within each household, three fertility zones are sampled: Home, Near, and Far from the house.
- Sampling locations span two kebeles (Konicha and 1st Choroko) with varying farmer wealth status (poor, medium, rich).
- Position of soil samples within each area is random; three replicates are taken from each fertility zone/area.
- Depths for measurements: 0–5 cm, 5–10 cm, and 10–15 cm.
- Fertility zones around each household: three (Home, Near, Far); measurement sites total per configuration: 108, 216 across the stated regimes (leading to 324–648 total samples across configurations).
- Measured variables across time: monthly measurements from January to July (seven months) for each site/depth/replicate.

## Calibration and sensor configuration
- W.E.T sensor calibrated for soil water content using a two-point approach to derive parameters b0 and b1, enabling field water content calculation from soil permittivity.
- Field calibration steps include:
  - Collecting damp soil, measuring permittivity when wet, then oven-drying and re-measuring when dry.
  - Calculating calibration coefficients b0 and b1 and entering them into the W.E.T. soil type (Custom 1).
  - Repeating a separate calibration for pore water conductivity (ECp) using a soil slurry and solution measurements to derive relevant parameters, then entering into the sensor’s Custom 1 soil parameters.
- In the field, always select Custom 1 soil type for measurements.
- Measurements collected at three depths per area to reflect vertical variation.

## Measurement procedures and data collection
- Field measurement procedure uses random placement of measurements within each fertility zone and household.
- Depths sampled: 0–5 cm, 5–10 cm, 10–15 cm.
- Parameters recorded per site: pore water conductivity (ECp), volumetric water content (VWC), and soil temperature for each month (January–July).
- Data capture and storage:
  - Data collected via the W.E.T sensor and uploaded in real time to a tablet using ODK to minimize data loss and mislabeling.
  - Site labeling and replication controlled to minimize spatial misassignment.

## Quality control
- Randomized replication: three samples per site to account for spatial variability.
- Regular sensor checks in saline solution to verify accuracy; two experienced soil scientists conducted operations.
- Documentation and calibration references available in sensor user manual.
- Sample labeling: some minor loss (<5%) due to label eligibility; overall data integrity maintained.
- Laboratory analyses and broader data handling follow Standard Operating Procedures and regular calibration of sensors and equipment.
- Data analyzed for normal distribution to ensure statistical appropriateness.

## Data files and structure
- IPORE-Soil EC.csv
  - Columns: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July pore water conductivity (mS m^-1).
- IPORE-Soil water.csv
  - Columns: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July volumetric water content (%).
- IPORE-Soil temperature.csv
  - Columns: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July soil temperature (°C).
- Each file includes the same metadata fields (household, location, zone, depth, replicate) plus the corresponding monthly measurement values.

## Data use and potential products
- Rich, multi-dimensional time-series data enabling:
  - Spatial comparison of soil moisture and ECp across Home/Near/Far zones and wealth strata.
  - Depth-wise analysis of soil moisture and temperature dynamics across months.
  - Correlation analyses between VWC, ECp, and soil temperature to study soil health and fertility dynamics.
  - Dashboard or pivot-table style self-serve data products for end users (e.g., policymakers, researchers, extension agents).
- Potential data products:
  - Interactive dashboards showing monthly VWC and ECp by fertility zone and depth.
  - Reports summarizing soil moisture trends by kebele and household wealth status.
  - Geographically contextualized summaries combining kebele data with household metadata.

## Limitations and notes
- Some labeling losses occurred; dataset includes measures to minimize misassignment, but users should account for minor data gaps.
- The sampling framework assumes randomization within zones; interpretations should consider potential residual biases if any zones or households were underrepresented.
- Calibration relies on two-point methods; users should review calibration documentation and sensor accuracy specifications (approx. 5% for VWC, 1.5 °C for temperature, 10 mS m^-1 for EC).
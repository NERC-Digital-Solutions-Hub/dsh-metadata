# Experimental design/Sampling regime

- Objective and scope
  - Collect soil health indicators (pore water conductivity, volumetric water content, and soil temperature) to compare management effects and spatial variability around households.
  - Sampling occurs across multiple households within two kebeles, covering gradients of proximity to the residence.

- Sampling design
  - Three fertility zones per household:
    - Home: land close to the house with intensive management and higher-value crops.
    - Near: field between home and far zone.
    - Far: field furthest from the house with typically more extensive production.
  - Spatial and socioeconomic context:
    - Fields and measurements taken from farmers with varying wealth status (poor, medium, rich).
    - Conducted in two kebeles (Konicha and 1st Choroko).
  - Randomization and replication:
    - Position of soil samples within each fertility zone is random.
    - Three replicates per fertility zone.
  - Overall structure (household and site counts) are provided in the data framework, with replication and site totals increasing across configurations (e.g., measurement sites: 108 → 216; households: 36 → 72; resulting sample totals: 324 → 648).

- Measurement scheme and depth
  - Depths per measurement: 0–5 cm, 5–10 cm, 10–15 cm.
  - Variables measured and frequency:
    - Pore water conductivity (ECp) via W.E.T sensor, monthly from January to July.
    - Volumetric water content (VWC) via W.E.T sensor, monthly from January to July.
    - Soil temperature, monthly from January to July.

- Instruments and field procedure
  - Instrument: W.E.T soil moisture/EC sensor, chosen for simultaneous measurement of water content, temperature, and conductivity; field operation by two experienced soil scientists.
  - Field procedure:
    - Randomly positioned measurements within each fertility zone.
    - Three replicates per area; measurements for each depth interval (0–5, 5–10, 10–15 cm).
    - Fields categorized by wealth status and located in 2 kebeles.
  - Data capture:
    - Readings entered into a Tablet via an ODK file to reduce data misplacement and loss.

- Calibration and data processing
  - Soil water content calibration:
    - Two-point calibration using damp soil and oven-dried soil cores.
    - Derive calibration constants b0 and b1 and embed into the W.E.T. custom soil type (Custom 1).
    - Instructions provided for activation and parameter entry on the W.E.T. device.
  - Pore water conductivity calibration:
    - Calibration to determine ECp parameters (ECp and related readings) by preparing soil-water mixtures and measuring in solution and in soil.
    - Enter calibrated parameter into the W.E.T. Custom 1 soil type to enable field calculations.
  - Field usage notes:
    - Always select Custom 1 soil type during measurements.
    - Electrical conductivity reported as ECp in the field.

- Quality control and data management
  - Randomized, replicated sampling (three replicates) to account for spatial variability.
  - Periodic checks of the WET sensor in saline solution to ensure accuracy.
  - Personnel: two experienced soil scientists with prior related project experience.
  - Data integrity measures:
    - Immediate data upload to tablet with defined input variables to minimize location mix-ups and data loss.
    - Labeling of soil samples; some minor loss (<5%) due to label eligibility issues.
  - Analytical and data quality standards:
    - Laboratory analyses follow standard procedures with strict QA/QC and SOPs.
    - Regular calibration of sensors and equipment; calibration checks for nutrient analyses and pH measurements.
    - Statistical checks indicating normally distributed data.

- Data outputs and structure
  - Data files and schemas:
    - IPORE-Soil EC.csv: columnar data for sample metadata and monthly pore water conductivity (mS/m) from January to July.
      - Key columns: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July ECp.
    - IPORE-Soil water.csv: similar structure for volumetric water content (%), January–July.
    - IPORE-Soil temperature.csv: similar structure for soil temperature (°C), January–July.
  - Shared metadata fields across files:
    - S. no., HH no., Kebele (PA), HH ID, Fertility Zone, Top depth, Bottom depth, Replicates.
  - Data usage note:
    - Data are organized to allow analysis of spatial (home/near/far), depth, month, and kebele effects on soil moisture, salinity (ECp), and temperature.

- Relevance to monitoring framework goals
  - Demonstrates an end-to-end monitoring approach from experimental design and sampling strategy to field instrumentation, calibration, QA/QC, and structured data outputs.
  - Produces quantifiable environmental health indicators (soil moisture, salinity, temperature) across management and spatial gradients to inform policy decisions, monitoring priorities, and future data collection improvements.
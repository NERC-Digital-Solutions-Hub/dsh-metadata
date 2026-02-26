# Holder A.J. and Hayes, F.

## Overview
- Experimental study conducted at the UK Centre for Ecology & Hydrology’s air pollution facility to assess the impact of ozone (O3) on sweet potato growth.
- Plants grown in 25 L tubs inside three heated solardomes with ambient + 6°C conditions; randomised into Low, Medium, and High O3 treatments to simulate varying pollution levels.
- Measurements tracked weekly (2019–2020) including leaf stomatal conductance, leaf temperature, light; plus chlorophyll content and soil moisture; final tuber harvest weight recorded.
- Four csv data files accompany the study, with detailed metadata to enable data reuse.

## Experimental Design and Conditions
- Location: Abergwyngregyn, North Wales, UK.
- Plant material: Sweet potato varieties Erato orange, Beauregard, and Murasaki grown from plug plants in 25 L pots.
- Growth environment: Three solardomes (3 m diameter, 2.1 m high); each dome hosts four replicates.
- O3 treatments:
  - Low: 30 ppb (daytime maximum)
  - Medium: 80 ppb
  - High: 110 ppb
  - Episodic exposure: two days per week across all domes at Low to represent episodic pollution.
- Measurements (weekly): stomatal conductance (gs), leaf temperature (TLeaf), light; chlorophyll content index; soil moisture.
- Harvest: end-of-season fresh weight of tubers measured.
- Planting and harvest timing spans 2019–2021 (explicit start, end, and harvest dates provided in Table 1 for each variety).

## Quality Control and Data Processing
- O3 monitoring: two calibrated analyzers (API 400A and Thermo 49i) measured every 30 minutes; matched calibration ensured.
- Instrument calibration: porometer calibrated with curve error ≤ ~10%.
- Data screening: outliers removed (gs > 1500 mmol H2O m-2 s-1; light > 2100 µmol m-2 s-1); graphical checks for anomalies.
- Data integrity: missing measurements marked as NA; datasets prepared with consistent time stamps (Date, Time/Hour, DayOfYear, etc.).

## Data Files Provided
- Treatment_Data.csv: mean hourly O3 treatment concentrations with fields for Date, DayOfYear, Hour, Treatment, O3_ppb.
- SwtPot_gs_ci.csv: measurements per plant (gs, Light, TLeaf, Soil_moisture, Chlorophyll, Tair, RH) plus metadata (Date, Time, Treatment, PlantID, Leaf_side).
- SwtPot_gs_ci_alongVine.csv: along-vine measurements (gs, Light, TLeaf, Soil_moisture, Chlorophyll, Leaf_No) with PlantID, Date, Time, Treatment, Leaf_side.
- SwtPot_yield.csv: harvest data (Date, Variety, Treatment, PlantID, Fresh_weight, No_tubers).
- All data include clear column descriptions, units, and NA indicators for missing values.

## Metadata and Data Governance
- Each file includes comprehensive descriptions of columns, measurement methods, and units to facilitate interpretation and reuse.
- Emphasizes transparency and traceability of measurements, enabling verification and secondary analyses.

## Relevance to Monitoring and Policy Frameworks
- Demonstrates end-to-end monitoring data lifecycle: study design, standardized data collection, quality control, data management, and documentation.
- Highlights practical challenges relevant to environmental monitoring programs:
  - Robust data collection in controlled but policy-relevant settings.
  - Need for clear metadata to enable data sharing and reuse.
  - Consistency in data formats and units to support cross-study comparisons.
- Provides a model for structuring monitoring datasets to support scrutiny of policy interventions (e.g., pollution exposure scenarios) and inform future decisions.
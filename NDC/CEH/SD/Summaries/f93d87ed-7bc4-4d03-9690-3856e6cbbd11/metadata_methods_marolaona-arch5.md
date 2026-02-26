# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Dataset from the 31.7 ha Marolaona catchment in the Ankeniheny Zahamena Corridor, Madagascar (lat/long provided in text) covering 2015–2016.
- Includes hydrometric measurements (rainfall, streamflow, perched groundwater, soil moisture) and stable isotope data (δ18O, δ2H, and deuterium excess) from multiple locations and plots.
- Aims to support understanding of rainfall–runoff and hillslope moisture dynamics under long-term slash-and-burn practices.
- Data described in two CSV files: HydrometricData_Marolaona.csv and IsotopeData_Marolaona.csv; summary of contents provided in Tables 1 and 2.

## Data files and structure
- HydrometricData_Marolaona.csv
  - Time interval: 5-minute records from Feb 3, 2015 to Mar 3, 2016.
  - Columns cover: rainfall at downstream/upstream gauges (amount and hourly intensity), streamflow at downstream/upstream weirs, perched water tables (TF2, EUC, TSF, TF1), volumetric soil moisture (SMC) at TF2, EUC, TSF, TF1 with depths (5, 15, 30 cm), and soil temperatures at those depths; and corresponding groundwater levels.
  - Missing data represented as NaN.
  - Perched water tables are expressed as height above the low-permeability layer (300 mm below surface).
  - Data gaps noted (e.g., upstream rainfall gauge data lost July 1–Aug 17, 2015).
  - Column details provided in Table 1 (names, units, explanations) and associated text.
- IsotopeData_Marolaona.csv
  - Samples from streamflow (upstream of weirs) and overland flow (TF2, EUC, TSF plots) with rainfall sampling during wet season.
  - Isotopes measured: δ18O, δ2H, and deuterium excess (DEx) via CRDS (Picarro L2130-i) at University of Freiburg.
  - Sampling metadata: Location, Water_type (rainfall, streamflow, or plot runoff/overland flow), DateTime, Delta18O, Delta2H, DEx.
  - Measurement precision: ±0.16‰ for δ18O and ±0.6‰ for δ2H.
  - Content described in Table 2.
- Background references provide context for methods and rating curves (supplementary materials referenced for detailed rating-curve equations).

## Data collection and measurement details
- Rainfall
  - Two tipping-bucket gauges (Rain Collector II, Davis) with 0.2 mm tip, connected to HOBO loggers; installed ~1.2 m above soil to minimize ground-splash.
  - Locations: downstream and upstream at ~1.2 m above ground; data converted to 5-minute totals (00:00–00:05 period corresponds to 00:00 hour).
  - Data gap: upstream gauge lacked data July 1–Aug 17, 2015 due to battery failure.
- Streamflow
  - Weirs at the catchment outlet (31.7 ha) and upper sub-catchment (7.11 ha); water level recorded at 5-minute intervals.
  - Upper weir modified to a 90° V-notch in the 1960s; lower weir rated via salt-dilution-slug-injection method across varying flows.
  - Data periods with sensors functioning: Feb 15–May 13, 2015 (CTD-10 sensor) and Dec 12, 2015–Mar 3, 2016 (STS/DL sensor). Data gaps due to sensor failure.
  - Rating curves described in detail in Zwartendijk et al. (2023) and supplementary materials.
- Soil moisture
  - Measurements at three hillslopes: TF2 (young tree fallow), EUC (coppiced eucalyptus and degraded grassland), TSF (terraced shrub fallow).
  - Sensor types: Decagon ECHO-EC-TM (5 cm, 15 cm) and ECHO-TM-5 (30 cm); accuracy ±3%; resolution 0.1%.
  - Depths: 5, 15, 30 cm; data logged at 1-minute intervals with 5-minute averages stored.
  - Sensor placement relative to plot boundaries described to capture upslope/downstream moisture dynamics.
- Perched groundwater
  - Fully screened wells at TF1, EUC, TSF (and TF2 adjacent to moisture plots).
  - Water levels recorded with Decagon CTD-10 sensors (minute-level) and 5-minute averages stored; some wells used Keller DCX-18 sensors (5-minute sampling).
- Isotope sampling
  - Water samples from streamflow and overland flow; rainfall samples collected daily during wet season (TF2 gauge) and event-based sequential sampler sampling (every ~13 mm of rainfall).
  - Samples analyzed for δ18O, δ2H, and DEx; results expressed relative to VSMOW.

## Data quality, standards, and governance
- Data are provided with explicit time stamps and units; NaN indicates missing data.
- Metadata includes detailed column descriptions (Table 1 and Table 2), locations, sampling schemes, sensor types, depths, and measurement intervals.
- Isotope data include analytical precision and delta notation references to VSMOW standard.
- Documentation references prior publications for background, data interpretation, and rating-curve details (Zwartendijk et al. 2020, 2023; Moore 2004, 2005; Bos 1989; Kennedy et al. 1979; etc.).
- Data sharing and reuse considerations:
  - Data are stored in CSV format with clear definitions for each column; potential updates or corrections would follow documented provenance.
  - The dataset is part of a broader study on rainfall–runoff responses in upland tropical catchments under slash-and-burn practices, implying careful attention to standardization and interoperability across related datasets.

## Provisional challenges and considerations for data stewards
- Incomplete picture of user needs and priorities may affect dataset discoverability and reuse focus.
- Timely acquisition of data from field teams can be challenging; battery/failure incidences caused data gaps.
- Harmonizing metadata across multiple systems and formats (rain gauges, weirs, soil moisture sensors, groundwater wells) can be complex.
- Large datasets from high-frequency measurements (5-minute rainfall/streamflow, minute-level groundwater and soil moisture) require robust storage, versioning, and update workflows.
- Outdated or bespoke systems may hinder interoperability; documentation and supplementary materials are essential for future reuse.

## For scientists and data users
- Use HydrometricData_Marolaona.csv for high-resolution rainfall, streamflow, soil moisture, and groundwater dynamics; refer to Table 1 for variable definitions and units.
- Use IsotopeData_Marolaona.csv for hydrological source tracing and isotope-based mixing analyses; refer to Table 2 for sample metadata and isotope variables.
- Cross-check with the cited methodological sources for rating curves, measurement techniques, and calibration procedures when performing hydrological analyses.
- Consider data gaps when performing time-series analyses; document data completeness in any reuse study.

## Contact and authorship
- Corresponding author: Bob Zwartendijk (bob.zwartendijk@inholland.nl), Inholland University of Applied Sciences, Alkmaar, The Netherlands.

## References (contextual)
- Key methodological and historical references for measurement techniques, rating curves, and prior related studies are provided (e.g., Moore 2004, 2005; Bos 1989; Zwartendijk et al. 2020, 2023).
# Exotic Plantations Increase Risk of Flooding in Mountainous Landscapes

## Overview of the dataset
- Two main components:
  - DailyRainDischarge2014to2016.csv: daily rainfall and discharge for eight small catchments with land cover data in the Upper Nilgiris (May 2014 – December 2016). Rainfall from tipping bucket gauges (tips per minute converted to mm); water levels from stilling wells with capacitance loggers.
  - KSatLandCovers.csv: hydraulic conductivity under major land covers in the Upper Nilgiris (2013–2016), measured with a mini-disk infiltrometer.
- Geographic and temporal scope:
  - Collected in the Upper Nilgiris Reserve Forest, Tamil Nadu, part of the Western Ghats; headwaters of the Bhavani river.
  - Data collection started in 2013 and continued through at least May 2020 as part of ecohydrology projects involving multiple partners.

## Fieldwork and instrumentation

- Rainfall (section 2.1)
  - Tipping bucket, wired Rainwise gauges installed on ridges and grasslands in roughly a 1x1 km grid.
  - Data recorded at 1-minute intervals; retrieved ~every two weeks.
  - Location coordinates provided for each gauge (Table 1).

- Discharge (section 2.2)
  - Water levels measured at five-minute intervals in eleven streams using stilling wells and capacitance loggers.
  - Discharge converted from stage via velocity-area (all units except 101); unit 101 used a compound weir with standard discharge equations.
  - Stream catchment boundaries derived from SRTM; locations provided (Table 2).

- Infiltration (section 2.3)
  - Saturated hydraulic conductivity (Ksat) measured at multiple sites under patches of land cover using a mini-disk infiltrometer.
  - GPS accuracy around 20 m; coordinates for Shola, Grassland, Pine, and Wattle patches recorded (Table 3).

## Calibration and quality assurance

- Calibration
  - Rain gauges calibrated yearly by pouring fixed volumes at ~3–4 tips/min; average water-per-tip used.
  - Water level recorders calibrated per manufacturer instructions.
  - Mini-disk infiltrometer methods followed the manufacturer’s manual.

- Quality assurance and control
  - Logs checked for power and contact issues; problematic intervals replaced with NULL values.
  - Stilling wells paired with permanent scales to correct placement errors.
  - Salt-dilution gauging (slug and constant release) performed in parallel with velocity-area calculations for QA.
  - Infiltrometer readings: at least three consecutive readings per sample; air-leak readings discarded.

## Data processing and reproducibility

- Data processing
  - All data imported into R and aggregated to daily time steps.
  - Daily, 1-minute through 15-day aggregation supported by a suite of processing steps.

- Scripts and workflow
  - A comprehensive set of R scripts and functions documented to process rainfall, water level, and discharge data, including calibration, gap filling, aggregation, and plotting.
  - Master scripts coordinate the sequencing of processing steps; detailed descriptions of each script/function are provided (e.g., tbrg_nlg.R, wlr.nlg.R, dis.control.R, etc.).

- Reproducibility notes
  - The processing workflow is explicitly documented, enabling replication of data preparation and analyses from raw logs to daily time series and figures.

## Data structure and variables

- Rain/runoff dataset (Table 5 description)
  - Core fields include:
    - dt.tm: timestamp (IST) for each sample
    - wlr: water level recorder number
    - Discharge: discharge in m3/s
    - DepthDischarge: depth of discharge in mm
    - flowD: daily flow in mm
    - mm: daily rainfall (mm)
    - PeakDischarge: daily peak discharge (m3/s)
    - PeakDepthDischarge: depth at peak discharge
    - AMI: antecedent moisture index (past 14 days)
    - Area: catchment area (hectares)
    - CircularityIndex, slopeSteep, drainDensity: catchment descriptors
    - catchment: land cover category (Wattle, grasslands, shola)
- Saturated hydraulic conductivity data (Table 6)
  - Fields include:
    - Date: sample date
    - Land.Cover: land-cover type
    - LSAT: saturated hydraulic conductivity
    - K: hydraulic conductivity (ms-1)

## Study design and governance considerations for data stewards

- Provenance and collaboration
  - Data collected across multiple partner organizations over a multi-year program, with clear documentation of instrumentation, calibration, and QA processes.
  - Multiple data types (rainfall, discharge, land cover, hydraulic conductivity) collected to support ecohydrology analyses.

- Metadata and standards
  - Detailed site-level coordinates, instrument types, calibration procedures, and data processing steps are recorded to support discoverability and reuse.
  - Metadata includes data collection period, measurement intervals, and data transformations (e.g., tips to mm, stage to discharge conversions).

- Data accessibility and reuse
  - Scripts and functions used for data processing are provided, enabling reproducibility and reuse for similar hydrological studies.
  - Dataset designed to be uploaded to relevant portals and catalogues; maintains linkage between raw measurements and processed daily time series.

- Limitations and considerations for reuse
  - Dry-season data are excluded to focus on extreme rainfall events; users should consider seasonal completeness.
  - Infiltration data have GPS accuracy limitations (~20 m) for some patches.
  - Some metadata references (e.g., certain environmental parameters) are noted as requiring external references; users should consult accompanying documentation for complete context.

## References and methodological context
- Methods and instrumentation follow established standards for tipping-bucket rainfall, capacitance water level logging, velocity-area discharge estimation, and mini-disk infiltrometry.
- The study is framed within ecohydrology research on land-cover effects on rain-runoff, carbon sequestration, and nutrient/sediment discharge, with relevant methodological references provided in the dataset documentation.
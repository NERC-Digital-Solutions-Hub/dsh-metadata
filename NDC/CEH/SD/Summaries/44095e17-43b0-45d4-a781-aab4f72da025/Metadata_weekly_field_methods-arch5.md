# SAMPLING

## Overview
- A multi-dataset environmental sampling record covering rainfall, cloud, stream water, groundwater, throughfall, and stemflow.
- Each dataset lists metadata on collection methods, devices, measurement types, sampling frequency, time coverage, and filtration approach.
- Time coverage spans from the early 1980s through ongoing periods for several datasets, with some ends in the 1990s and others continuing.

## Datasets and key metadata

- Rainfall (first period)
  - COLLECTION METHOD: Bulk sample
  - COLLECTION DEVICE: Continuously open, 15 cm diameter PVC collector with anti-bird protection and coarse neck filter
  - FLOW/VOLUME: Tanllwyth met site ground level raingauge
  - FIELD MEASUREMENTS: Air temperature (glass thermometer and thermistor)
  - SAMPLING INTERVAL: Weekly/daily
  - START: 10-May-1983
  - FINISH: 18-May-1999
  - FILTRATION: Lab

- Rainfall (second period)
  - COLLECTION METHOD: Bulk sample
  - COLLECTION DEVICE: Continuously open, Warren Spring pattern collector with anti-bird protection and coarse neck filter
  - FLOW/VOLUME: Tanllwyth met site ground level raingauge
  - FIELD MEASUREMENTS: Air temperature (glass thermometer and thermistor)
  - SAMPLING INTERVAL: Weekly/daily
  - START: 25-May-1999
  - FINISH: Cont.
  - FILTRATION: Lab

- Cloud
  - COLLECTION METHOD: Bulk sample
  - COLLECTION DEVICE: CEH (Edinburgh) pattern lidded harp type passive collector
  - FLOW/VOLUME: Weight of sample
  - FIELD MEASUREMENTS: None
  - SAMPLING INTERVAL: Weekly
  - START: 25-Sep-1990
  - FINISH: Cont.
  - FILTRATION: Lab

- Stream water
  - COLLECTION METHOD: Grab samples
  - COLLECTION DEVICE: Plastic bucket attached to plastic cord; sample taken near middle of stream
  - FLOW/VOLUME: CEH stream (flume) gauges; if not sampled by flumes, flow record provided by nearest flume
  - FIELD MEASUREMENTS: Stream temperature (glass thermometer/thermistor), electrical conductivity (field meters, corrected to 25°C)
  - SAMPLING INTERVAL: Weekly/Daily
  - START: 10-May-1983
  - FINISH: Cont.
  - FILTRATION: Field

- Groundwater
  - COLLECTION METHOD: Grab samples after flushing of boreholes
  - COLLECTION DEVICE: BGS borehole sampler
  - FLOW/VOLUME: Dip level recorder; depth referenced to datum of borehole cover
  - FIELD MEASUREMENTS: Groundwater temperature, electrical conductivity (field meters, corrected to 25°C)
  - SAMPLING INTERVAL: Monthly/fortnightly/weekly
  - START: 24-Apr-1994
  - FINISH: 14-Feb-2001
  - FILTRATION: Field

- Throughfall
  - COLLECTION METHOD: Bulk sample
  - COLLECTION DEVICE: Trough collector
  - FLOW/VOLUME: Volume of sample
  - FIELD MEASUREMENTS: None
  - SAMPLING INTERVAL: Fortnightly
  - START: 06-Feb-1984
  - FINISH: 02-Sep-1991
  - FILTRATION: Lab

- Stemflow
  - COLLECTION METHOD: Bulk sample
  - COLLECTION DEVICE: Plastic tubing wrapped around trees and carboy collector
  - FLOW/VOLUME: Volume of sample
  - FIELD MEASUREMENTS: None
  - SAMPLING INTERVAL: Fortnightly
  - START: 06-Feb-1984
  - FINISH: 02-Sep-1991
  - FILTRATION: Lab

## Common themes and governance considerations for Data Stewards
- Diverse collection methods and devices across datasets require careful standardization of terms, units, and metadata to enable interoperability.
- Multiple data streams include both field-based and lab-based processing (filtration), suggesting need for clear data lineage and processing workflows.
- Temporal coverage varies by dataset, with some ongoing (“Cont.”) periods; ensure mechanisms are in place for updating and discovering new records.
- Data quality factors to monitor:
  - Consistency and completeness of metadata (collection method, device, measurements).
  - Calibration and unit consistency for field measurements (e.g., temperature, conductivity).
  - Documentation of any methodological changes (e.g., different rainfall collectors) that could affect comparability.
- Data access and provenance considerations:
  - Observed affiliations (CEH, BGS) imply institutional governance; ensure proper data provenance, stewardship, and access controls are in place.
  - Filtration type (Lab vs Field) should be clearly logged for downstream data users.
- Actionable items for maintaining the dataset:
  - Harmonize naming and coding schemes for devices and methods across datasets.
  - Confirm ongoing data intake processes for continuing periods and update portals/catalogues accordingly.
  - Provide clear metadata templates to capture similar details for any future additions or updates.
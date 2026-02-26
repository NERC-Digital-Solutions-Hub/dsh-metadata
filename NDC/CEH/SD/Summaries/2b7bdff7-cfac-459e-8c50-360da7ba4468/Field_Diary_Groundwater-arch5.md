# Bore Hole monitoring

## Overview
- Longitudinal monitoring of water levels across five boreholes near Tyn y Bryn farm.
- Monitoring period: 03/08/2005 to 03/03/2008 (with last entry noting diver downloaded and wire left in hole).
- Data collected using divers/barodivers, with frequent updates on deployments, readings, and data handling.
- Measurements include water depth, measuring point offset above ground, and whether the diver was in or out of the borehole, affecting actual water level calculations.

## Borehole details and data characteristics
- Borehole 1
  - Total depth: 11.6 m.
  - Example readings span 03/08/2005 to 03/03/2008, with water levels ranging roughly from 185 cm to 360 cm depending on date and diver status.
  - Notable events: diver deployments and later barodiver installation in 2008; series of readings adjusted by ground-level offset to obtain actual water level.
- Borehole 2
  - Total depth: 5.5 m.
  - Readings recorded from 03/08/2005 through 03/03/2008, with water levels broadly between about 39 cm and 117 cm (values vary with diver in/out and diver condition).
  - Observations include multiple diver removals during downloads, occasional 10 cm jumps between downloads, and diver cleanliness affecting readings.
- Borehole 3 (Bowl)
  - Total depth: 5.89 m.
  - Extensive logs of readings from 03/08/2005 onward, including periods where diver position (in/out) and reinstallation affected measurements.
  - Barodiver installed in this borehole on 03/03/2008; numerous diver re-installations and manual readings prior to that.
- Borehole 4 (Above shelterbelt)
  - Total depth: 1208.5 cm.
  - Readings show consistent depths around 1100–1150 cm, with many “not possible to read when diver was in bore hole” notes.
  - Diver deployment and retrieval times frequent; multiple instances of readings with diver in vs diver out and adjustments to measurement offset.
- Borehole 5 (Below shelterbelt)
  - Readings from 03/08/2005 show water levels around 700–800 cm, with values fluctuating over time as diver presence changed.
  - Notable issues include diver reliability concerns, device changes, and notes to delete diver data post-download; multiple instances of manual checks and recalibrations (diver in/out, and occasional reinstallation below or above shelterbelt).

## Instrumentation, data handling, and metadata
- Measurement devices include diver (dipper) and barodiver; installations and removals documented.
- Key data points per measurement:
  - Timestamp (GMT)
  - Borehole identifier
  - Water level measurement (cm)
  - Measuring point offset above ground (cm)
  - Diver status (in/out)
  - Note on data handling (e.g., diver downloaded, wire left in hole, manual readings, 30-minute sampling)
- Data handling notes emphasize:
  - Adjustments to convert measured depth to actual water level using the offset above ground.
  - Occasional data gaps due to diver in the borehole or equipment issues.
  - Instances of data quality concerns (diver dirty, reliability concerns, and jumps in measurements between downloads).

## Data quality challenges and considerations for data stewards
- Incomplete or intermittent readings due to diver presence in boreholes.
- Variability in data quality: readings labeled as unreliable (e.g., diver dirty, readings not possible when diver in), occasional sudden jumps between downloads (~10 cm).
- System heterogeneity: different boreholes used different devices over time (divers, barodivers) and multiple re-installations.
- Calibration and provenance: frequent notes about diver deployments, re-installations, and equipment swaps require robust metadata to maintain data lineage.
- Data hygiene: reminders to delete diver data after download; occasional notes about mechanical issues (e.g., screw problems, cables) affecting data capture.

## Data governance, sharing, and lifecycle implications
- Data should be stored with rich metadata capturing:
  - Borehole ID, total depth, measurement methods, device type (diver/barodiver), deployment dates, and any changes in instrumentation.
  - For each measurement: timestamp, raw depth, offset, diver status, and any corrections applied.
  - Provenance notes documenting when readings were manual, when diver mounting was altered, and when readings were not possible.
- Standardization needs:
  - Consistent units (cm for water level, GMT for timestamps).
  - Clear flags for data quality (e.g., diver in/out, readings with known issues).
  - Versioning and audit trails for data updates or reprocessing after equipment changes.
- Sharing and discovery:
  - The dataset is suitable for portals or catalogues that support time-series water level data with per-measurement metadata.
  - Document data gaps and instrument-change events so data users understand context and limitations.
- End-of-life considerations:
  - The monitoring activity as described ends with a diver download and wire left in the bowl borehole on 03/03/2008, marking a need for archival storage, data reassessment, and potential data migration to a centralized repository with complete provenance.

## Key takeaways for Data Stewards
- This document represents a rich, multi-borehole time-series dataset with extensive event-level metadata about instrumentation, diver usage, and data handling.
- Ensure robust metadata schema to capture device type, deployment events, reading conditions (diver in/out), measurement offsets, and data quality flags.
- Anticipate and manage data gaps, measurement anomalies, and equipment changes when integrating this dataset into a larger data catalogue.
- Maintain clear data provenance and versioning to support reproducibility and future re-use by researchers or practitioners monitoring groundwater or hydrological conditions.
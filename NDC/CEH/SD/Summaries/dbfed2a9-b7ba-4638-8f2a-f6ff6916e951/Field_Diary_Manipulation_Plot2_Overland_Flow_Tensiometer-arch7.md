# Rhos2: Notes from field visits for tensiometers and OLF

- Purpose and scope
  - A longitudinal field log documenting tensiometer and OLF (likely open-lattice field) monitoring activities across multiple plots.
  - Dates span from 2004 to 2009, recording daily maintenance, sensor readings, modifications, and incidents affecting data collection.

- Instrumentation and data types
  - Tensiometers deployed at multiple depths (commonly 10 cm, with 30 cm and 50 cm noted in several entries).
  - OLF systems with traps, gutters, sump pits, and associated sensors (float switches, tipping buckets, pumps).
  - Data loggers and sensors mentioned include Delta-T loggers, Tinytags, TinyTag calibrations, read switches, and various batteries (including desiccants) and desiccant status.
  - Supporting activities: soil sampling, trenching, grass cutting, weed control, and structural adjustments to plots (edging, covers, drainage).

- Data collection realities and quality issues
  - Recurrent sensor anomalies attributed to external events (e.g., storm-induced electrical surges) causing widespread nonsensical readings across many loggers.
  - Data integrity challenges due to: pump battery depletion, clogged gutters, water in traps, and miscalibrated or damaged sensors.
  - Widespread wildlife interference (voles) causing damaged wiring, chewed cables, and disrupted readings; frequent notes to ignore data during or after suspected damage periods.
  - Issues requiring data exclusion or caution: “ignore tips” periods, double tipping from certain tensiometers, and periods with suspected faulty readings or wiring problems.
  - Calibration and maintenance cycles: repeated degassing of tensiometers, recalibration of tipping buckets, replacement of tensiometers and read switches, and occasional reassignment of loggers to different channels or plots due to faults.
  - Data gaps and irregularities documented alongside corrective actions (replacements, re-installations, resealing, trench digging, and rerouting of water away from sensors).

- Maintenance, repairs, and field actions
  - Sensor maintenance: degassing tensiometers, changing wiring, replacing tensiometers at specific depths, resealing and desiccant replacement, and re-installation of sensors into new holes or adjusted depths.
  - OLF system upkeep: pump repairs, replacement of float switches, gutter cover replacements, sump maintenance, and trench modifications to manage water flow and prevent sensor submersion.
  - Data collection workflow adjustments: re-tightening connections, recalibrating Tak T/B (tipping buckets) readings, re-setting tiny tags, and altering sampling schedules to align with sensor capabilities.
  - Physical plot management: grass cutting, lawn edging repairs, trenching for water diversion, and structural changes to protect sensors and data collection infrastructure.

- Temporal and spatial scope relevant to GIS
  - Data are tied to multiple plots (e.g., plot 1, plot 2, plot 3) with depth-specific measurements and a variety of sensor types, indicating potential for multi-layer GIS mapping (locations, depths, sensor type, status, and data quality flags).
  - Frequent events affect data quality across plots, suggesting the need for metadata layers capturing sensor health, calibration events, and data validity windows.
  - Occasional relocation or replacement of sensors (including different channels and loggers) implies a non-static sensor network over time, requiring temporal geospatial tracking for accurate historical visualization.

- Implications for GIS-based data products
  - Data quality flags are essential: annotate readings with quality indicators (e.g., storm-affected, dodgy data, ignored periods, sensor replaced, recalibrated) to enable reliable map-based analyses.
  - Metadata richness is critical: record sensor IDs, depths, plot associations, equipment types, calibration events, maintenance dates, and observed issues to support reproducibility and traceability in maps and time-series visualizations.
  - Handling data gaps and inconsistencies: design workflows to interpolate, flag, or exclude data with documented faults; maintain clear provenance for any imputed values.
  - Spatial-temporal integration: align sensor readings across plots and depths in a coherent time axis; support queries by plot, depth, and sensor type to facilitate targeted GIS visualizations (e.g., time-series maps, depth profiles, anomaly detection).
  - Data standardization needs: the log highlights varied equipment and practices over years; a standardized schema for recording observations, readings, and issues would aid future GIS analyses and interoperability with other datasets.

- Key challenges highlighted for GIS specialists
  - Proactive data quality management in the face of multiple disruption sources (weather, wildlife, hardware failures).
  - Integrating heterogeneous data streams (tensiometers, OLF sensors, loggers) with consistent metadata.
  - Packaging and presenting large, complex field datasets in accessible map-based formats while preserving data provenance and quality context.
  - Ensuring robust, repeatable data cleaning and annotation processes to support reliable spatial analyses over time.
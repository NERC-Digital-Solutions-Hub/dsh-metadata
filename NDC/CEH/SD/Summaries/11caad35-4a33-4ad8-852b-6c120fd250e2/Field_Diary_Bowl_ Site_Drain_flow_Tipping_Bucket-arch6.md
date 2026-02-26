# Drain flow data logging and calibration notes (2005-2009)

- Purpose and setup
  - Monitoring drain flow using tipping buckets (TB) and weir boxes; transducers and TinyTag logger used.
  - Data logging interval adjusted from 10 minutes to 5 minutes to align with an overland flow trap.
  - Data streams include drain flow, weir box measurements, and outflow (OLF) indicators; calibration and alignment events are recorded.

- Data collection and provenance
  - Regular downloads of drain flow data and OLF data; notes track data integrity and events affecting data capture.
  - Calibration and testing events documented, including TB calibration runs and magnet/tip-volume adjustments.
  - Time stamps noted as sometimes inconsistent (GMT/BST shifts) requiring adjustments in analyzed data.

- Data quality issues and cleaning actions
  - Periods flagged as invalid or ignore-worthy (e.g., calibration periods, data during diversions, and anomalous timestamps).
  - Entries indicating data corruption or sensor issues (e.g., TB tip misalignment, transducer positioning, battery failures, sensor box moisture, gunk in TB).
  - Specific instances to ignore data include calibration events (e.g., ~08:54–12:00 GMT during calibration) and suspected misreads (e.g., “ignore tips” time windows, “ignore data” during weir box calibration).

- Calibration, measurement integrity and adjustments
  - TB calibration procedures established (e.g., 30 L through TB yields 11 tips; this implies ~2.91 L per tip).
  - After initial calibration, a linear incremental adjustment to tip volume was applied to account for measurement differences over time.
  - Recalibration activities and updates to TB volume were performed (e.g., recalibration due to algae/gunk, magnet reattachment, and TB reinstallation).

- Maintenance and operational disruptions
  - Multiple maintenance events: TB/magnet repairs, TB reinstallation, weir box servicing, PT checks, battery changes, desiccants, seals, and wiring/connector checks.
  - Physical adjustments to the drain setup during field work (reinstallations, pipe alignment, and water diversion for calibration).
  - Occasional data gaps or unusable periods due to equipment issues (e.g., system frozen, tubes not reinstalled properly, or data channels not recording).

- Data integration and outputs
  - Data were consolidated from drain flow and OLF measurements to enable analysis and interpretation.
  - Calibration notes and timestamp corrections are essential for accurate integration and subsequent self-serve analysis (dashboards, reports, charts).

- Key takeaways for data users
  - Expect intermittent data quality issues tied to calibration, maintenance, and timestamp synchronization.
  - Use the documented calibration factors (e.g., 2.91 L per TB tip; 30 L → 11 tips) and note periods of data that should be ignored.
  - Maintain awareness of time-zone adjustments (GMT/BST) to align timestamps across datasets.
  - Regularly reference maintenance logs to understand data gaps and sensor health, and apply these when cleaning and aggregating data for analyses.
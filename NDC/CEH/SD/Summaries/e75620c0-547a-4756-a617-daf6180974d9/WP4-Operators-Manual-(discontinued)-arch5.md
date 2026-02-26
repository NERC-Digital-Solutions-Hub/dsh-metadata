# WP4 Dewpoint PotentiaMeter Operator's Manual

## Overview and purpose
- Instrument for measuring water potential using the chilled-mirror dewpoint technique.
- Two models: WP4 (standard) and WP4-T (temperature-controlled).
- Delivers readings of water potential (Megapascals, MPa) and sample temperature in near real time (under five minutes); supports pF readings in some modes.
- Data and system status are displayed on an LCD and can be exported via RS-232 to a computer.

## Data produced and metadata
- Primary data outputs:
  - Water potential (MPa; 0 to -300 MPa) and measurement temperature (°C) for each reading.
  - Optional pF (in certain modes).
  - Time since chamber was closed (timestamp), printed to console when connected to a computer.
- Metadata and context:
  - Model version (WP4 v3.0 main menu shown at startup; WP4-T variant available).
  - Sample preparation details (cup size, fill level, rim cleanliness, lid for storage).
  - Temperature information: chamber/block temperatures, Ts (sample) and Tb (block) temperatures, Ts-Tb difference critical for accuracy.
  - Calibration and verification status, including use of verification standards (0.5 M KCl) and any zero-offset adjustments.
  - Operational mode (normal vs continuous) and beeper/LED notification settings.

## Data interfaces, formats, and storage
- Interfaces:
  - RS-232 computer interface for live data logging with Hyperterminal (Windows 98/2000 instructions provided).
  - Data format includes time, sample temperature, water potential, and pF.
- Data storage and logging:
  - In continuous mode, data can be logged to a connected computer; instructions exist for capturing and exporting data to spreadsheets or text editors.
  - Calibration and verification data should be logged for traceability.

## Calibration, verification, and quality control
- Calibration basics:
  - Calibration slope fixed at factory; user resets zero offset.
  - Regular verification with Decagon’s KCl verification standards recommended before each use; if unavailable, a saturated salt solution can be prepared (Appendix A guidance).
- Verification standards:
  - KCl standards provide known water potentials at specified temperatures (e.g., -2.19 MPa at 20°C, -2.22 MPa at 25°C; 4.35 pF in pF mode at 20–25°C).
  - Use fresh KCl solution, equilibrate to sample temperature, and verify readings against known values.
- Calibration procedure:
  - If readings drift beyond ±0.1 MPa (or ±0.1 for KCl reference), clean the chamber and repeat verification; if drift persists, adjust the zero offset in the calibration menu as directed.
  - Cleaning and recalibration instructions are in later chapters; if issues persist after cleaning, contact Decagon support.
- Temperature considerations:
  - Ts-Tb accuracy is crucial; temperature equilibration times impact read times and accuracy.
  - For WP4-T, setpoint temperature and equilibration time can be adjusted to optimize accuracy.

## Data quality and governance considerations
- Temperature control and equilibration:
  - Temperature differences between sample and instrument (Ts-Tb) must be minimized for accurate readings; large gradients increase read times and error.
- Contamination risks:
  - Mirror, thermopile, and chamber contamination degrade accuracy; regular cleaning and calibration checks are essential.
  - Proper sample preparation (avoid overfilling, clean cup rims, cover samples if stored) minimizes carryover and sensor contamination.
- Operational notes affecting data:
  - Field portability and power considerations (inverter use) but require stable temperature to ensure comparability with lab measurements.
  - Condensation risks from warm samples or large ambient temperature fluctuations can bias readings.
- Documentation and traceability:
  - Maintain logs of calibration verifications, cleaning events, instrument configuration changes, and any repairs.
  - Record model (WP4 or WP4-T), firmware/configuration settings, calibration state, and operator identity for reproducibility.

## Operational workflow (summary)
- Setup and warm-up:
  - Place WP4 on a stable, temperature-controlled surface; allow ~30 minutes warm-up before use.
- Sample preparation:
  - Use disposable cups, fill up to half full, ensure rim is clean, cover for short-term storage if needed.
- Taking readings:
  - Load sample in drawer, monitor sample temperature, ensure Ts-Tb is within acceptable range, then read.
  - Readings appear after ~40 seconds; in continuous mode, readings proceed automatically with status indicators (LED/beeper).
- Data capture and export:
  - Use RS-232 connection to log time, sample temperature, water potential, and pF.
  - Save or print data for records; use software to store time-stamped results.
- Maintenance and troubleshooting:
  - Regular cleaning of chamber, mirror, thermopile, and sensors as described; re-check calibration with KCl standards.
  - If problems arise (e.g., mirror dirty, block ROM failure, TE set missing in WP4-T), follow troubleshooting steps or contact Decagon support.
- Field and service considerations:
  - For field use, ensure power stability; bring spacer and insulation to minimize temperature gradients.
  - When repairs are needed, ship per specified instructions; warranty coverage is 1 year for parts and labor with a 30-day satisfaction guarantee.

## Maintenance, cleaning, and repair (highlights)
- Cleaning procedures:
  - Use Kimwipe tissues with cleaning solution; avoid cotton swabs and ensure mirror, optical sensors, thermopile, and chamber interior are clean.
  - Follow steps to access and clean the block, mirror, and sensors; reassemble carefully.
- Calibration after cleaning:
  - Re-check calibration with KCl standard; if drift remains, adjust zero offset or seek service.
- Repairs and servicing:
  - Contact Decagon support; include serial number, description of issue, and repair preferences.
  - Shipping guidelines emphasize original packaging or sturdy replacement with adequate padding; avoid shipping power cord.
- Troubleshooting focus:
  - Common issues include power/connectivity, slow readings, abnormal KCl readings, sample dryness, mirror condition, and block ROM errors.
  - Component performance screen (accessible during startup) provides quick diagnostics for thermocouple, thermopile, block temperature, and mirror reflectance.

## Appendix and references (data stewardship context)
- Verification standards and calibration details outline procedures to ensure data quality and comparability across sessions and users.
- Salt solution preparation guidance (for in-house verification) provides method to generate reference potentials, though Decagon standards are recommended for high accuracy.
- Application notes and further reading offer additional data contexts (soil moisture, leaf water potential, field portability) that can inform dataset documentation and metadata schemas.

Note: This summary highlights data production, quality control, data management, and governance considerations relevant to Data Stewards responsible for datasets generated with the WP4 Dewpoint PotentiaMeter, including calibration, verification, data formats, and data provenance practices.
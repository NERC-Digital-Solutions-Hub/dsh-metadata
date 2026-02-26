# WP4 Dewpoint PotentiaMeter for models WP4 and WP4-T Operator' s Manual Version 5

- Overview
  - Fast, accurate instrument for measuring water potential using the chilled-mirror dewpoint technique.
  - Two models: WP4 (standard) and WP4-T (temperature-controlled).
  - Outputs water potential in MPa (0 to -300 MPa) with typical accuracy of ±0.1 MPa (0 to -10 MPa) and ±1% (-10 to -300 MPa).
  - Readings include sample temperature and dewpoint-based water potential, displayed in MPa and pF; can be logged to a computer via RS-232.

- Key Features and Outputs
  - Dewpoint-based measurement with rapid (<5 minutes) results.
  - Internal fan for faster equilibration; simultaneous measurement of dewpoint and sample temperature.
  - Temperature control option in WP4-T to stabilize chamber and/or sample temperature.
  - Continuous and normal sampling modes; optional data logging when connected to a computer.
  - Calibration verification using Decagon’s 0.5 molal KCl standards; optional calibration adjustment (zero offset).

- Models, Setup, and Location
  - WP4: standard model; WP4-T: temperature-controlled model with selectable internal temperature.
  - Place on a level, stable surface away from temperature shocks (vents, windows, heat sources).
  - Warm-up: allow ~30 minutes after power-on for stable readings.
  - Field portability: can operate from a vehicle power source with a 12V inverter; use insulating measures to minimize temperature gradients.

- Operation Modes and User Interface
  - Main display shows water potential and sample temperature; drawer loaded with disposable cups.
  - Languages: multiple on-screen language options; switchable when not reading.
  - Normal sampling: one measurement per drawer read; optional beeper and LED signals.
  - Continuous mode: ongoing measurements; useful for long-term monitoring; data can be logged to a computer.
  - System configuration: adjust beeper, enter calibration menu, and (in WP4-T) set sample chamber temperature and equilibration time (0, 1, or 2).
  - Sample equilibration screen: monitor Ts vs Tb to gauge condensation risk and reading stability.

- Calibration, Verification, and Data Integrity
  - Verification standards: use Decagon’s KCl standards for calibration checks and drift correction; avoid using distilled water for calibration checks.
  - Calibrate by adjusting the zero offset to match known KCl values at the sample temperature (e.g., around -2.19 MPa at 20°C or -2.22 MPa at 25°C).
  - Calibration should be checked before each use for batch processing; drift suggests chamber contamination or sensor changes.
  - If calibration drift persists after cleaning, contact Decagon for guidance.
  - Data can be collected via RS-232 using Hyperterminal (Windows 98/2000) or equivalent terminal programs; data format includes time, sample temperature, water potential, and pF.

- Temperature Effects and Sample Handling
  - Temperature difference (Ts - Tb) critically affects accuracy; aim for minimal lag between sample and chamber temperature.
  - Condensation risk: large positive Ts-Tb can cause condensation; cooling or delaying sampling may be required.
  - 0.1°C accuracy in temperature difference is needed for 0.1 MPa precision; best results when sample is near chamber temperature.
  - For KPIs, use WP4-T to stabilize temperature and reduce variability due to ambient changes.

- Sample Preparation and Reading Process
  - Prepare samples in disposable cups; cover bottom to maximize contact area and speed reach to vapor equilibrium.
  - Do not overfill cups; ensure rims are clean to maintain a proper vapor seal with the sensor block.
  - Seal cups with lids for short-term storage; avoid spills in the chamber.
  - Steps to take a reading: load sample, monitor Ts with the sample temperature screen, close the drawer to READ, observe beeper/LED signals, and view the reading in ~40 seconds.
  - Dry samples: if extremely dry, WP4 may indicate “Sample too dry”; mirror and chamber contamination can also cause false low readings.

- Cleaning, Maintenance, and Calibration Verification
  - Regular cleaning is essential for accuracy; follow detailed cleaning procedures for mirror, optical sensor, thermopile sensor, and interior chamber.
  - Do not use cotton swabs; use Kimwipe and Decagon cleaning solution or distilled water as directed.
  - After cleaning, re-check calibration with the KCl standard; recalibrate if necessary.
  - Component performance screen (accessible at startup): checks thermocouple, thermopile, block temperature, and mirror reflectance voltage to diagnose issues.
  - If persistent problems occur (e.g., mirror contamination, dirty sensors, or failed components), contact Decagon for service.

- Troubleshooting and Support
  - Common issues include power/turn-on failures, slow or inconsistent readings, calibration drift, “sample too dry,” mirror contamination (triangle indicator), Block ROM failures, and TE set issues.
  - Each issue has recommended corrective actions, from cleaning routines to hardware checks and when to seek service.
  - Warranty: 1-year warranty on parts and labor; fungal or wear-related damage excluded.
  - Repair, shipping, and loaner services available; international users to contact local distributors as applicable.

- Data Management and Governance Considerations
  - Calibrations and verification standards provide traceable data for quality assurance; log calibration events and standard readings to maintain an audit trail.
  - RS-232 interface enables time-stamped data capture for integration with lab information systems or analysis pipelines.
  - Documented maintenance, cleaning, and calibration practices support reproducibility and data integrity across teams and sites.

- Appendix and Additional Resources
  - Appendix A: preparation guidance for saturated salt solutions; table of water potential values for NaCl and KCl at 20°C.
  - Application notes and downloadable resources available from Decagon (e.g., soil moisture characteristics, leaf water potential, field portability, seed priming, expansive soils classification).
  - Contact details for technical support and repair services provided in the manual.
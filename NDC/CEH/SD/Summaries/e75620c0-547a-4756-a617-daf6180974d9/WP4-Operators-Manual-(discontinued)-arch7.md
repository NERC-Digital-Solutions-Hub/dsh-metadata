# WP4 Dewpoint PotentiaMeter Operator' s Manual

- A high-precision instrument for measuring water potential using the chilled-mirror dewpoint technique.
- Models: WP4 (standard) and WP4-T (temperature-controlled).
- Outputs readings in MegaPascal (MPa) and pF, with sample temperature; rapid readings (typically <5 minutes).
- Primary audience: scientists and technicians requiring accurate, map-relevant water-potential data across sites or experiments.

## Key capabilities and data characteristics (GIS-relevant)

- Direct data outputs for GIS workflows:
  - Main display shows water potential (MPa) and sample temperature; pF also available.
  - Computer interface via RS-232 for logging to a computer or database; data can be exported to spreadsheets for GIS tagging.
  - Data stream format (example): time since chamber closed, sample temperature, water potential, and sample pF.
- Measurement precision and ranges:
  - 0 to -10 MPa: ±0.1 MPa
  - -10 to -300 MPa: ±1%
  - Accurate temperature-difference measurements are critical (Ts-Tb); best results when sample temperature is near chamber temperature.
- Sampling modes:
  - Normal sampling: single measurement per read.
  - Continuous mode: ongoing readings, useful for long-term monitoring (e.g., leaves, tissues).

## Instrument models and how they affect data collection

- WP4: Standard model; fast, accurate readings without external bath.
- WP4-T: Temperature-controlled model; maintains a set chamber temperature to reduce temperature-induced variability; valuable for temperature-controlled studies and reducing ambient-temperature effects on data.
- Temperature equilibration and control:
  - For WP4-T, setpoint temperature and equilibration timing can be adjusted to balance speed and stability.
  - Temperature differences between sample and chamber (Ts-Tb) influence reading stability and condensation risk.

## Operation and workflow (data quality focus)

- Location and setup:
  - Place on a level, stable surface away from temperature flux (vents, open doors) to minimize data drift.
  - Warm-up ~30 minutes after powering on before taking readings.
- Sample preparation (to ensure clean sensor data for GIS datasets):
  - Use disposable cups; don’t overfill; clean rims to avoid contamination of sensor chamber.
  - If storing for later reads, cap the cup to limit water transfer.
  - Dry samples near instrument limits may yield errors; field samples require careful handling to avoid condensation.
- Taking readings:
  - Load sample, seal with chamber, and start read cycle.
  - In ~40 seconds the first measurement is displayed; reading involves repeating dewpoint checks to ensure accuracy.
  - Watch sample vs. chamber temperature difference to anticipate condensation risk.
- Data management implications:
  - For GIS workflows, ensure time stamps, sample temperature, water potential (MPa), and pF are captured consistently.
  - In continuous mode, data logging can be performed to external software or spreadsheets for time-series mapping and analysis.

## Calibration and verification (data quality assurance)

- Verification standards:
  - Use Decagon's 0.5 M KCl verification standards for calibration checks.
  - Calibration slope is fixed; only zero offset is adjustable by the user.
  - Calibrate before use or after cleaning; if drift observed, adjust zero to match standard.
- Calibration workflow:
  - Load a KCl standard, read twice, ensure readings are within ±0.1 MPa of expected values (e.g., -2.19 MPa at 20°C or -2.22 MPa at 25°C; ~4.35 pF in pF mode).
  - If misfit persists after cleaning, contact support for guidance.
- Verification standards and Appendix A:
  - Appendix A provides methods for preparing saturated salt solutions if verification standards aren’t available.
  - Regular verification helps detect chamber contamination or sensor drift, which is critical for GIS-derived data integrity.

## Sample handling, temperature, and measurement considerations

- Sample preparation and handling:
  - Adequate surface area improves reading speed and sensor stability.
  - Avoid rim contamination; ensure initial sealing of the sample cup against the sensor block.
- Temperature considerations:
  - Temperature difference Ts-Tb must be controlled; errors of 1°C in Ts-Tb can produce large MPa errors.
  - The dewpoint-based approach requires accurate temperature measurements; for field GIS data, aim for near-room-temperature samples or use WP4-T to stabilize chamber conditions.
- Field portability:
  - Optional portable power via 12V inverter; warm-up still required; maintain stable field temperatures to avoid data drift.
  - Use insulation or a Styrofoam box to minimize temperature fluctuations during field measurements.

## Cleaning, maintenance, and calibration checks (to preserve data quality)

- Cleaning:
  - Regular cleaning of the mirror, sensor block, and chamber is essential to prevent data drift.
  - Use Kimwipe tissues with cleaning solution or distilled water; avoid cotton swabs and contaminants.
  - Reassemble carefully; verify ribbon cables and connections after cleaning.
- Calibration checks after cleaning:
  - Re-check calibration with the KCl standard and adjust if necessary.
  - If readings remain inconsistent, consult support for service or potential component issues.
- Maintenance and spare services:
  - Troubleshooting and repair support details are provided, including shipping instructions and loaner service availability.

## Troubleshooting and common data-quality issues (GIS data flags)

- Common issues affecting data:
  - Won’t turn on: check power cord and fuses; address blown fuse or faulty components.
  - Slow or inconsistent readings: dirty sample chamber, slow desorption/adsorption, or broken chamber fan blade.
  - KCl calibration deviations: contaminated thermopile or non-equilibrated verification salt solution.
  - “Sample too dry” warnings: sample moisture insufficient; mirror/chamber may be dirty.
  - Mirror warning triangle: mirror performance degraded; clean chamber/mirror thoroughly.
  - “Block ROM failed” or “TE set” missing: hardware connection or temperature control module fault; service required.
- Component performance screen:
  - Accesses diagnostic values (thermocouple, thermopile, block temperature, mirror voltage) to assess instrument health; used to guide repairs with support.

## GIS-focused takeaways for data products

- Data integrity:
  - Record MPa, sample temperature, pF, and timestamps with each reading; document calibration status and temperature controls for traceability in maps.
- Metadata and standards:
  - Maintain model (WP4 or WP4-T), calibration date, verification standard used, sample cup details, and field conditions to enable reproducibility on maps.
- Data integration:
  - Use RS-232 exports or manual entry into GIS-compatible databases; structure data for time-series mapping and spatial correlation with site metadata.
- Quality flags:
  - Include flags for temperature drift (Ts-Tb), mirror contamination, or calibration drift to inform data consumers about reliability.
- Applications:
  - Potential to generate soil moisture potential maps, leaf/wisdom potential fields, or field-portable salinity/temperature impact studies by aggregating MWa (MPa) data across samples and times.

## Appendices and references (for deeper GIS-informed data handling)

- Preparation of verification standards and salt solutions (Appendix A).
- Reference readings and theory related to water potential and the dewpoint technique.
- Application notes and additional data-generation methods available from Decagon for broader GIS analyses.

- Contact and support:
  - Decagon support and repair contacts for maintenance, calibration, and data integrity questions.
  - Warranty and service terms included in the manual.
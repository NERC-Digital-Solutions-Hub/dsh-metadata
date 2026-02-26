# WP Dewpoint PotentiaMeter for models WP4 and WP4-T Operator' s Manual Version 5

## Purpose andscope
- Instrument and manual for measuring plant/soil water potential using the chilled-mirror dewpoint method.
- Two models: WP4 (standard) and WP4-T (temperature-controlled).
- Designed for fast, accurate, standardized data suitable for environmental monitoring and policy assessment.

## What the WP4 measures and outputs
- Water potential (Ψ) directly in MPa and user-configurable units (pF) with output values displayed alongside sample temperature.
- Measurement time: typically under five minutes per read.
- Outputs include:
  - Water potential (MPa or pF)
  - Sample temperature (°C)
  - Temperature difference screens (sample vs. chamber)
  - Optional continuous data logging when connected to a computer via RS-232

## How it works (key concepts)
- Dewpoint/condensation technique: equilibrates sample liquid water with headspace vapor; condensation on a chilled mirror is detected and related to water potential.
- Internal sensors: dewpoint mirror with photodetector, thermocouple for mirror temperature, thermopile for sample temperature, and an infrared thermometer for boundary-layer temperature.
- Temperature control: WP4-T maintains a set chamber temperature to reduce temperature-driven variability; standard WP4 requires stable ambient temperatures for best accuracy.

## Calibration, verification, and data quality
- Calibration basics:
  - Calibration slope is factory-set; user adjusts zero offset.
  - Verification uses Decagon’s 0.5 molal KCl standards; preferred verification standard for accuracy.
  - Calibration should be checked before each use with the KCl standard (not distilled water).
- Verification standards:
  - Ready-to-use KCl standards recommended for minimizing error; shelf-stable for one year.
  - If using non-Decagon salt solutions, ensure the solution is at equilibrium and adjust if readings drift.
- Typical verification values:
  - At 20 °C: ~-2.19 MPa; at 25 °C: ~-2.22 MPa (in MPa mode; 4.35 pF in pF mode).
- Calibration workflow:
  - Load KCl standard, run read, confirm read within ±0.1 MPa of expected value.
  - If drift occurs, clean the chamber and repeat; if drift persists, adjust calibration via the calibration menu and re-test with KCl.
- Ongoing accuracy:
  - Normal operation accuracy: ±0.1 MPa from 0 to -10 MPa; ±1% from -10 to -300 MPa.
  - For highest accuracy (up to ±0.05 MPa), ensure precise temperature control, minimize ambient fluctuations, and consider continuous 0.5 KCl calibration checks.

## Data handling and portability
- Data capture and logging:
  - Data can be logged to a connected computer via RS-232; in continuous mode, data can be logged over time.
  - Example data format from Hyperterminal: time since chamber closed, sample temperature, water potential, and pF.
- Data formats and access:
  - Data accessible for export to spreadsheets or text editors; can be printed or saved from terminal software.
- Field usability:
  - Portable operation with vehicle power via an inverter; recommended to insulate and allow for a 30-minute warm-up in field setups.

## Modes and user interface
- Normal sampling mode: single measurement per read; LED and optional beeper indicate status.
- Continuous mode: measurements run continuously until the drawer is opened; useful for long-term monitoring.
- Language support: English by default; multiple language options available (e.g., German, French, Spanish, Italian, etc.).
- Beeper settings: three options (no beep, four short beeps, continuous beeps).

## Sample preparation and measurement protocol
- Sample preparation:
  - Use disposable cups; fill to about half-full; avoid contamination on cup rims.
  - Cap samples for short-term storage; avoid spills that contaminate the chamber.
- Reading steps:
  - Load sample drawer, close gently, monitor sample temperature difference (Ts - Tb screen).
  - Seal and start read cycle; read displayed in ~40 seconds for first measurement.
- Temperature equilibration:
  - Aim for Ts ≈ Tb; large Ts-Tb differences can cause condensation or slow/erroneous readings.
  - For WP4-T, set equilibration behavior (0, 1, or 2) to control how closely the sample must equilibrate before final reading.

## Temperature considerations and accuracy
- Temperature differences drive potential measurement error; require temperature-difference accuracy around 0.005 °C for 0.1 MPa precision.
- Best results when samples are near chamber temperature; condensation risks increase with larger Ts-Tb differences.

## Cleaning, maintenance, and upkeep
- Regular cleaning is critical to maintain accuracy:
  - Use non-linting wipes (Kimwipe) and Decagon cleaning solution or distilled water/alcohol as appropriate.
  - Clean the mirror, optical sensor, thermopile sensor, and interior chamber; protect the fan blades.
- Access and disassembly:
  - Disconnect power, remove lid, access block, and follow cleaning procedures for all surfaces.
- Post-cleaning checks:
  - Re-check calibration with the KCl standard; recalibrate if readings drift after cleaning.

## Troubleshooting and common issues
- Common problems include: instrument won’t turn on, slow or inconsistent reads, drift in KCl verification, sample too dry, mirror contamination (triangle warning), block ROM failure, TE set option missing (WP4-T).
- Remedies include: reseating connections, replacing fuses, cleaning mirrors and sensors, verifying or recalibrating with KCl standards, and servicing if hardware faults are suspected.

## Maintenance of data integrity and environment monitoring relevance
- The WP4’s standardized measurement protocol, calibration/verifications, and data export capabilities support consistent, auditable environmental data over time.
- By using standardized verification standards and documenting calibration, analysts can compare datasets across time and locations, facilitating scrutiny of environmental health and policy performance.

## References and supplementary notes
- Theory and practical notes on water potential, dewpoint measurement, and data interpretation are provided to support standardized environmental data collection and interpretation.
- Application notes and appendix materials available from Decagon for advanced use cases (e.g., soil moisture curves, leaf water potential, field portability).
# WP4 Dewpoint PotentiaMeter for models WP4 and WP4-T Operator' s Manual Version 5

- Purpose and scope
  - Decagon WP4 is a dewpoint-based instrument for measuring water potential (Ψ) in samples.
  - Two models: WP4 (standard) and WP4-T (temperature-controlled).
  - Delivers readings in MegaPascals (MPa) quickly (typically under five minutes) with high accuracy.
  - Measures the sum of osmotic and matric potentials in a sample.

- Key specifications
  - Measurement range: 0 to -300 MPa.
  - Accuracy: ±0.1 MPa from 0 to -10 MPa; ±1% from -10 to -300 MPa.
  - Temperature control options: WP4-T includes a thermoelectric (Peltier) chamber for temperature stability.
  - Dewpoint/development: uses chilled-mirror dewpoint technique, with a photodetector to detect condensation, a fan for equilibration, and an infrared thermometer for sample temperature.

- Models and options
  - WP4: standard model suitable for most uses.
  - WP4-T: temperature-controlled model with internal setpoint control (15°C to 50°C; 0.1°C increments) and optional equilibration time settings.

- How it works (conceptual)
  - Equilibrates sample water with the headspace vapor in a sealed chamber.
  - Condensation on a temperature-controlled mirror is detected to determine dewpoint, which, with sample temperature, yields water potential.
  - Internal fan accelerates equilibration and reduces measurement time; simultaneous dewpoint and temperature readings minimize full thermal equilibration needs.

- Setup, location, and startup
  - Place on a level, stable surface away from HVAC vents and temperature fluctuations.
  - Warm-up: allow about 30 minutes after powering on for optimal accuracy.
  - Sample drawer: use disposable cups; avoid overfilling; ensure rims are clean to seal properly.
  - Language options: English default; multiple languages selectable via the main menu.

- Getting started and operation modes
  - Normal sampling mode: single measurement per read.
  - Continuous mode: continuous readings for long-term monitoring; useful for dynamic samples (e.g., leaves, plants); can log data to a computer.
  - Main menu and system configuration: adjust beeper behavior, enter calibration, and configure WP4-T setpoints.
  - Beeper options: none, four beeps, or continuous beeps after each reading.
  - Temperature equilibration policy (WP4-T): set equilibration level (0, 1, or 2) determining how close Ts must be to Tb before reading begins.
  - Sample equilibration screen: monitors Ts - Tb to avoid condensation and condensation-related errors.

- Sample preparation and handling
  - Use a cup with adequate sample surface area; cover bottom but avoid overfilling.
  - Clean cup rims and outside to avoid sensor contamination.
  - Lid the cup for short storage; seal for longer storage with Parafilm.
  - Dry samples: readings may be unavailable if Ψ is beyond instrument detection (e.g., -300 MPa or drier); WP4 displays an error when too dry.

- Reading the sample
  - Load sample: open the drawer, place prepared cup, reseal, then activate the read cycle.
  - Read time: first display typically within ~40 seconds once sealed.
  - Temperature and dewpoint data: watch Ts and Tb on the sample temperature screen; monitor Ts-Tb (0 to -0.5°C is ideal for fast readings; larger differences increase equilibration time).
  - Condensation and condensation-related cautions: warm samples can cause condensation if placed in a cooled chamber.

- Data display and computer interface
  - RS-232 interface included for computer data capture.
  - In Hyperterminal (Windows 98/2000), data stream outputs: time (since chamber closed), sample temperature, water potential, and pF.
  - Data can be printed or transferred to spreadsheets; include a device file for capture.

- Calibration and verification
  - Calibration slope is fixed by factory calibration; zero offset can be reset.
  - Regular calibration verification using Decagon’s KCl verification standards (preferred) or saturated salt solutions if standards are unavailable.
  - Calibrate before use to account for drift due to chamber contamination; check with fresh 0.5 M KCl at the sample temperature.
  - Procedure: place KCl standard in drawer, read twice; adjust zero offset to align with known values (-2.19 MPa at 20°C; -2.22 MPa at 25°C; or corresponding pF values).
  - If readings drift outside ±0.1 MPa after cleaning or verification, recalibrate; persistent issues may require service.

- Verification standards and Appendix references
  - Decagon’s KCl verification standards are recommended for accuracy and repeatability.
  - Appendix A provides preparing salt solutions and an AOAC-style procedure for saturated solutions; includes a table of water potentials for NaCl and KCl at 20°C.
  - Verification standards are shelf-stable for one year and are used to detect drift and contamination.

- Temperature effects and accuracy improvements
  - Temperature difference measurement Ts-Tb is critical; a 1°C error could yield ~8 MPa error.
  - Best accuracy when sample is near chamber temperature; for higher accuracy, use WP4-T to control chamber temperature and minimize ambient variation.
  - Condensation risks increase with near-saturation samples; Ts-Tb guidance and equilibration settings help mitigate.

- Cleaning, maintenance, and care
  - Regular cleaning is essential to maintain accuracy.
  - Cleaning tools: Kimwipe tissues, gentle cleaning solutions; avoid cotton swabs.
  - Cleaning process covers mirror, optical sensor, thermopile sensor, inside chamber, and case.
  - Mirror and optical components require careful cleaning to prevent measurement errors; damaged or contaminated components should be serviced.
  - After cleaning, re-check calibration using KCl standard.

- Troubleshooting and diagnostics
  - Common problems: instrument won’t turn on, long read times, calibration drift, “sample too dry,” mirror contamination (triangle symbol), Block ROM failed, TE set not available (WP4-T problem).
  - Solutions include checking power and fuses, cleaning sensors and chamber, verifying equilibrium with standards, reseating cables, and consulting support if hardware failure is suspected.
  - Component performance screen can display sensor temperatures, block temperature, and mirror reflectance to diagnose issues (non-adjustable).

- Repair, shipping, and support
  - Contact Decagon support for repairs, service, and warranty questions.
  - Warranty: 30-day satisfaction guarantee; one-year warranty on parts and labor.
  - Repair costs: warranty repairs free; non-warranty repairs billed (minimum $50); rush charges may apply.
  - Loaner service available on a limited basis during repair.
  - Shipping back to Decagon: use original packaging if possible; do not ship with power cord; include contact information and a problem description.

- Additional resources and references
  - Application notes available on Decagon’s site (soil moisture, leaf water potential, field portability, seed priming, seed longevity, expansive soils).
  - References to foundational works on water potential and dewpoint methods.

- Appendix and supporting content
  - Appendix A includes preparation of salt solutions and detailed steps for saturated salts for verification.
  - The manual also contains tables and figures supporting calibration, verification, and measurement theory.
# WP4 Dewpoint PotentiaMeter for models WP4 and WP4-T Operator's Manual

- Purpose: A research standard for measuring water potential using the chilled-mirror dewpoint technique; designed for scientists and students to obtain fast, accurate readings to inform environmental monitoring and policy decisions.

- Models: Two configurations
  - WP4: Standard model for most water potential needs
  - WP4-T: Temperature-controlled model with internal thermoelectric control; allows setpoint temperature and equilibration adjustments

- What it measures and outputs
  - Water potential (Ψ) directly in MPa and also in pF
  - Sample temperature (Ts) in °C
  - Read times typically under five minutes
  - Accuracy: ±0.1 MPa from 0 to -10 MPa; ±1% from -10 to -300 MPa
  - Outputs displayed on main LCD; data can be exported via RS-232 to PC (Hyperterminal instructions provided)

- How the WP4 works
  - Uses chilled-mirror dewpoint method: sample equilibrates with headspace in a sealed chamber; condensation on a mirror is detected photometrically
  - Mirror temperature controlled by Peltier cooler; dewpoint and sample temperature determine water potential
  - Internal fan speeds up equilibrium and reduces boundary-layer effects
  - For WP4-T, internal temperature control maintains a user-set chamber temperature to study temperature effects or reduce ambient fluctuations

- Key components and setup
  - Main unit, calibration certificate, power cord, RS-232 cable, disposable sample cups, KCl verification standards, cleaning kit
  - Location: level surface, stable temperature away from vents or rapid fluctuations
  - Warm-up: ~30 minutes after power-up for best accuracy
  - Sample preparation: cup filled to about half; rim and exterior cleaned to avoid contamination; lid used for short-term storage

- Measuring process (Taking a Reading)
  - Preparation: load sample cup into drawer; confirm cleanliness of cup rim
  - Temperature checks: monitor Ts-Tb via sample temperature screen
  - Read cycle: close drawer to seal; instrument beeps/LED signals when reading begins; first display appears in about 40 seconds
  - Modes: Normal sampling (one reading per load) and Continuous mode (continuous readings with logging capability)

- Temperature considerations and equilibration
  - Temperature differences between sample and chamber (Ts-Tb) strongly affect accuracy
  - Ts-Tb within 0 to -0.5 °C yields faster, reliable readings; larger gaps slow or bias readings
  - Condensation risk: if sample is warmer than the chamber, condensation inside the chamber can occur; use cooling or adjust sample handling
  - For higher accuracy, align sample temperature with chamber temperature; TS-Tb influences reading time and stability

- Calibration and verification
  - Verification standards: Decagon-provided KCl standards (0.1 MPa precision target; typically -2.19 MPa at 20°C and -2.22 MPa at 25°C; or 4.35 pF in pF mode)
  - Calibration: fixed slope; user resets zero offset using KCl standards
  - When to verify: before each use for best accuracy; regular checks for batch processing
  - If readings drift beyond ±0.1 MPa after cleaning or cleaning procedures, recalibrate (calibration menu guides this process)
  - Appendix/Appendix A and application notes provide additional salt solutions and verification guidance

- Data interface and interpretation
  - RS-232 interface for computer logging; Hyperterminal setup instructions included for Windows 98/2000
  - Output format: time since chamber closure, sample temperature, sample water potential, and pF
  - Data management: capture text for storage; suitable for integration into larger monitoring datasets

- Sample preparation and handling guidance
  - Use disposable cups; ensure full bottom coverage when possible to optimize readings
  - Do not overfill; wipe cup rims; cap for short-term storage to limit moisture transfer
  - For very dry or very wet samples, readings may be affected; ensure adequate moisture for dewpoint formation

- Cleaning, maintenance, and care
  - Regular cleaning to prevent sensor contamination; uses Kimwipe tissues, cleaning solution, and, if needed, isopropanol
  - Accessing block and mirror carefully to avoid damaging the fan or sensors
  - Cleaning steps cover the mirror, optical sensor, thermopile sensor, and internal chamber
  - After cleaning, re-check calibration with KCl standard; consult technical support if readings remain off

- Troubleshooting and diagnostic guidance
  - Common issues include slow readings, mirror contamination, block ROM failures, TE set removal, or triangle warning icons indicating mirror performance problems
  - Step-by-step remedies reference cleaning, calibration checks, and component integrity
  - Component performance screen provides live readings for thermocouple, thermopile, block temperature, and mirror reflectance to diagnose problems

- Repair, support, and logistics
  - Contact Decagon for repairs, with details on warranty, repair costs, shipping, and loaner options
  - Shipping instructions emphasize preserving instrument integrity; avoid shipping power cord in the box
  - Loaner instruments available on a first-come, first-served basis to minimize downtime

- Additional resources
  - Application notes available on Decagon’s site (soil moisture characteristics, leaf water potential, field portability, seed priming, etc.)
  - Appendix A and calibration verification references provide supplementary methods and conversion values
  - References to foundational literature on water potential measurement and dewpoint methods

- Overall takeaway for monitoring framework authors
  - WP4 provides a robust, calibrated, and documented method for obtaining water potential data with explicit QA/QC procedures (verification standards, calibration checks, and standardized procedures)
  - Data quality hinges on proper calibration, consistent sample preparation, temperature control, and timely maintenance
  - The device supports data capture and integration into monitoring programs, with clear guidance on data export, calibration traceability, and operational constraints relevant to policy-informed environmental health assessment
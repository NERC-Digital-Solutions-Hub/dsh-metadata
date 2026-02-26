# WP4 PotentiaMeter Operator's Manual

- Purpose: Decagon WP4 PotentiaMeter (models WP4 and WP4-T) is the dewpoint-based instrument for measuring water potential. It outputs direct measurements in MPa (0 to -300 MPa) and can display or log related data (pF and temperature) for analysis and reporting.

- What it measures and outputs
  - Water potential (Ψ) from 0 to -300 MPa; accuracy ≈ ±0.1 MPa from 0 to -10 MPa and ±1% from -10 to -300 MPa
  - pF (in alternative units) when in pF mode
  - Sample temperature (Ts) and chamber temperature (Tb)
  - Data packet includes time since chamber closed, sample temperature, water potential, and pF (via RS-232)
  - Display shows water potential and sample temperature on the main menu; optional computer logging via RS-232

- Data collection modes and workflow
  - Normal sampling: one measurement per read
  - Continuous mode: continual readings with optional data logging to a computer
  - Temperature considerations: Ts should equilibrate with Tb; large Ts-Tb differences slow or bias readings; WP4-T allows active chamber temperature control to stabilize measurements
  - Sample preparation and handling influence data quality (avoid spills, contamination, and condensation)

- Calibration and verification (data quality safeguards)
  - Calibration verification using Decagon’s 0.5 molal KCl standards is essential before use; the slope is fixed; the zero offset is adjustable
  - Do not rely on distilled water for calibration due to humidity effects
  - If readings drift, clean the chamber and mirror, then re-verify with KCl; if drift persists, recalibrate as guided
  - Calibration targets at 20°C (-2.19 MPa) and 25°C (-2.22 MPa) for KCl standards; in pF mode target ~4.35 pF at these temperatures

- Data interface and software usage
  - RS-232 interface provided for direct computer data capture
  - Hyperterminal (Windows 98/2000) workflow described for establishing a connection and capturing time, temperature, Ψ, and pF data
  - Data can be printed, pasted into spreadsheets, or captured via the RS-232 transfer function
  - Continuous mode can support real-time logging; data integrity relies on proper calibration and clean sensors

- Sample preparation and temperature considerations (data quality impact)
  - Use disposable cups; fill no more than half full; keep rims clean to maintain sensor seals
  - For samples read later, cap the cup to limit moisture exchange
  - Dry samples (Ψ beyond instrument detection) yield “Sample too dry” messages
  - Ts-Tb temperature difference: aim for small differences; large differences cause condensation and measurement errors
  - For WP4-T, set and stabilize chamber temperature; equilibrate ~30 minutes after power-up

- Operation and data integrity tips
  - Warm-up: allow ~30 minutes for stable readings
  - Avoid moving the instrument or leaving a loaded sample unattended to prevent contamination
  - Use the sample equilibration screen to monitor Ts-Tb before reading
  - Mirror and chamber contamination degrade accuracy; clean per guidelines to maintain data integrity

- Maintenance, cleaning, and calibration verification (data reliability)
  - Regular cleaning of the mirror, optical sensor, thermopile, and chamber interior is critical for data accuracy
  - After cleaning, re-check calibration with the KCl standard and adjust if necessary
  - Component performance screen provides status of sensors and should be used if suspecting degraded data quality

- Troubleshooting and common issues (data-related guidance)
  - Won’t turn on: check power cord, fuses, and potential internal faults
  - Slow or inconsistent readings: clean chamber, address slow moisture desorption, or replace fan if needed
  - KCl calibration out of range: clean thermopile, verify salt standard equilibrium
  - “Sample too dry” or mirror-triangle warnings: clean mirror and chamber; address sample dryness or condensation issues
  - Block ROM failed or TE set disappear: likely hardware fault; contact Decagon for service
  - Temperature control module failure (TE Set unavailable on WP4-T): service required

- Data integrity and reporting considerations
  - Use KCl verification standards for consistent calibration; keep records of calibration results and dates
  - Report data with units (MPa and pF) and include temperature context (Ts, Tb)
  - If logging data, ensure proper transfer settings and save formats; verify data post-download for completeness

- Additional resources and references
  - Theory and Measurement background: theory of water potential and dewpoint-based measurement
  - Application notes and supporting materials available from Decagon (e.g., soil moisture, leaf water potential, field portability)
  - Appendix A and salt solution preparation guidance for verification standards (NaCl/KCl table of Ψ vs concentration)

- Model overview and key options
  - WP4: standard model for most Ψ measurements
  - WP4-T: temperature-controlled model using thermoelectric control to stabilize chamber temperature and improve measurement precision

- Getting help and warranty
  - 30-day satisfaction guarantee; 1-year parts and labor warranty
  - Contact information and service procedures provided for repairs, shipping, and technical support
# Operation Manual HYPROP

- HYPROP is a fully automated system to determine hydraulic properties of soil samples, measuring water tension at two depths with two tensio shafts to derive soil water retention (pF/WC) and unsaturated hydraulic conductivity (Ku) curves during evaporation.
- Data and evaluation are handled with HYPROP-VIEW (data logging and device management) and HYPROP-FIT (curve fitting and export).
- Measurement duration varies by soil type (roughly 2 days to 10 days) and can be run in two modes: multi balance (one balance per sensor unit) or single balance (one balance for up to 20 sensor units).

## What HYPROP Measures
- Water tension (matrix potential) in two depths (h1 and h2) during evaporation.
- Mass change of the soil sample over time to compute water content changes.
- Medial pF value derived from h1 and h2; medial θ(h) from mass change; volumetric water content (VWC) and hydraulic conductivity K(h) calculated via Darcy’s equation.
- Output: discrete data points forming the pF/WC and Ku curves; optional integration of WP4 data for combined analysis.

## System Components and Scope
- HYPROP hardware: sensor unit with two tensio shafts, saturation and sample handling accessories, and a balance interface.
- Accessories and software: HYPROP-VIEW (device manager, measurement display, configuration wizard), HYPROP-FIT (data fitting/evaluation), Refill Unit (vacuum degassing), syringes for degassing, and various adapters and spare parts.
- Modes: Multi balance mode (one balance per sensor unit) and Single balance mode (one balance for multiple sensor units; up to 20 samples).

## Intended Use and Safety
- Intended use: measure water retention and unsaturated hydraulic conductivity of soil as a function of tension/ content.
- Safety: follow electrical and EMC requirements; IP65 protected sensor unit; handle degassing gear and vacuum equipment carefully; avoid damage to ceramic tensio shaft tips and pressure sensors.
- Warranty: minimum 12 months; excludes misuse or external damage.

## Data and Outputs
- Outputs include tensions h1 and h2, sample mass, and derived medial pF(h) and θ(h) values.
- Time points: default interpolation to 100 time points for curve generation.
- Software outputs: HYPROP-FIT models (e.g., van Genuchten, Brooks-Corey, Kosugi, PDI variants) and integral fit approaches; ability to export data and fit results.
- WP4 data can be added post-measurement for enhanced data sets and re-weighted in HYPROP-FIT.

## Software and Workflow
- HYPROP-VIEW: initial setup, device management, measurement configuration (wizard), display of connected devices, and live measurement graphs.
- HYPROP-FIT: data evaluation, fitting of θ(h) and K(h) curves, model selection, and export of results.
- Data processing: raw data are interpolated (Hermitian splines) to fixed time points; θ(h) derived from mass and dry mass; K(h) derived from water flow between two time points and tension gradient.
- Documentation and help: built-in help and linked manuals for HYPROP-FIT and related methods.

## Measuring Procedure (High-Level)
- Prepare soil sample in a 250 ml ring; saturate and cap to prevent evaporation losses during setup.
- Saturation: capillary saturation with controlled water addition; saturation times depend on soil texture.
- Degassing: remove dissolved air from water and tensio shafts either with the HYPROP Refill Unit (vacuum) or with syringes; ensure bubble-free, fully degassed water in tensio shafts and sensor unit.
- Implement tensio shafts: fill shafts with degassed water and install into sensor unit; monitor pressure rise to ensure correct seating and prevent sensor damage.
- Attach sample to the sensor unit and balance system; ensure no air gaps and proper zeroing.
- Weighing: in multi balance mode, weights are logged automatically; in single balance mode, weigh each sample manually (typically twice daily).
- Measuring: evaporation drives tensions; HYPROP automatically logs tensions and mass over time.
- Finishing: stop when appropriate (e.g., cavitation phase or air entry conditions) and proceed to dry-weight determination.
- Drying and weighing: determine the dry soil mass post-measurement for accurate θ(h) calculations.

## Degassing and Filling Details (Summary)
- Refill Unit: use vacuum to degas water and fill tensio shafts; monitor for leaks; ensure proper vacuum levels and avoid dynamic shock to sensors.
- Syringes: manual degassing and filling, with bubble-free water; follow step-by-step filling to avoid air entrapment.
- Sensor unit filling and tensio shaft installation require careful handling to prevent air bubbles and ensure proper O-ring seals.

## Finishing a Measurement and Data Evaluation
- End conditions: cease measurement at cavitation or use air-entry point for calculated medial values if appropriate.
- Dry weight: weigh the dry soil mass after measurement to allow accurate conversion to volumetric water content.
- Evaluation: HYPROP-FIT performs nonlinear regression to fit θ(h) and K(h); multiple models and integral fitting are available; detailed evaluation steps are documented in the HYPROP-FIT manual.
- Data integration: WP4 data can be incorporated into HYPROP-FIT evaluation for enhanced data interpretation.

## Typical Curves and Interpretation
- The manual provides typical curves for various soils (sand, loam, clayey substrates) and discusses features such as bubble point, air entry, cavitation, and evaporation-driven behavior.
- Curve shapes inform about pore size distribution and hydraulic conductivity characteristics; model selection (e.g., van Genuchten, Brooks-Corey, Kosugi, Simmons-Fayer) depends on soil type.

## Maintenance, Troubleshooting, and Storage
- Cleaning: sensor unit is IP65; clean under running water with the unit inverted to avoid soil ingress; do not remove tensio shafts during cleaning.
- O-ring maintenance: replace red O-rings if leakage is detected or tensions flatten/droop prematurely.
- Storage: prevent algae growth for long-term storage.
- Spare parts and accessories: extensive list of HYPROP extensions, beaker mounts, extension sets, tensio shafts, and related components.

## Notes and References
- The manual includes technical data, measurement ranges, and conversion notes for soil water terms (pF, hPa, kPa, MPa, bar, psi, %rF).
- Foundational literature and prior method descriptions related to HYPROP measurement are cited for further reading.
# Operation Manual HYPROP

- HYPROP is a fully automated measuring and evaluation system to determine the hydraulic properties of soil samples (water retention function and hydraulic conductivity as a function of water tension or water content).
- Based on Schindler’s method; measures water tension at two depths with two tensio shafts; correlates weight loss to pF/WC curves; uses HYPROP-FIT for evaluation.

## What HYPROP includes and how it works

- Hardware: sensor unit with tensio shafts, saturation plate, reservoirs, hoses, and related accessories; options for degassing via Refill Unit or syringes.
- Software: HYPROP-VIEW for data logging and device management; HYPROP-FIT for evaluation, fitting, and export.
- Two measurement modes:
  - Multi balance mode: one balance per sensor unit.
  - Single balance mode: one balance for multiple sensor units (up to 20 samples).
- Measurements yield the retention (θ(h)) and conductivity (K(h)) curves through an evaporation-based approach.

## Preparing and starting HYPROP

- Install HYPROP-VIEW and HYPROP-FIT on a computer; connect HYPROP balance to USB; ensure each sensor unit has a unique device ID.
- Prepare to weigh samples and enter sample metadata via the software wizard or directly in the manager.

## General measuring procedure (overview)

- Steps: soil sampling and preparation → saturating the soil sample → preparing the measuring system → assembling the sample on the system and starting measurement → evaluating results with HYPROP-FIT.

## Saturating the soil sample

- Use sample rings; prepare top and bottom surfaces to minimize soil loss.
- Saturate by capillary action: place soil in a tray with degassed water, keep air venting (cap off loosely), and saturate until the surface shines.
- Saturation times vary by soil type (longer for finer textures; up to weeks for clay).

## Filling the device and degassing

- Tensio shafts must be filled with degassed water; avoid air bubbles; do not touch ceramic tips with bare fingers.
- Two degassing methods:
  - HYPROP Refill Unit: use vacuum to degas water and fill tensio shafts; monitor for leaks; recommended with timing to extend pump life.
  - Syringes: manually degas water in reservoirs and tensio shafts; more hands-on but effective.
- Steps include connecting the refilling attachment, ensuring bubble-free filling, and achieving a vacuum in the sensor unit before measuring.

## Implementing the tensio shafts in the sensor unit

- Attach tensio shafts filled with degassed water to the sensor unit; monitor tensions during installation to avoid sensor damage.
- After installation, verify zero pressure and response speed; ensure no air gaps remain.

## Attaching the dirt protection and preparation for measurement

- Install dirt protection, cover tips with silicone tubes, and fill with degassed water; ensure all connections are bubble-free.

## Balances and measurement setup

- Choose multi balance or single balance mode; prepare a vibration-free workspace.
- Weighing:
  - Multi balance: automated mass measurement alongside tension data.
  - Single balance: weigh each sample manually, typically twice daily; monitor and manage tare components.
- Ensure proper cable management and that the magnet cable loops do not constrain movement.

## Optimal measuring curve and phases

- Four phases when air-free filling is achieved:
  - Phase 1: regular measurement range (tension rises).
  - Phase 2: boiling delay phase (if fully air-free).
  - Phase 3: cavitation phase (water vapor forms; tension drops).
  - Phase 4: air entry phase (air replaces water; tension drops to zero).
- Endpoints and data interpretation may use either complete or partial phases depending on data quality.

## Finishing a measurement

- End when the upper tensio shaft reaches cavitation or when the air-entry point is reached and a reliable medial value can be computed.
- HYPROP-FIT can interpolate between phases to compute medial tension values if one shaft has entered cavitation earlier than the other.

## Determining the dry weight and evaluating results

- After measurement, determine the dry mass by oven-drying the soil sample and weighing, ensuring the sample ring is fully recovered and free of adhering soil.
- HYPROP-FIT evaluates the data by fitting θ(h) and K(h) together; input the dry mass for precise volumetric water content; models available include van Genuchten, Kosugi, Brooks-Corey, and PDI variants.
- Data interpolation uses Hermitian splines to create a fixed number of time points (default around 100) for curve fitting.

## HYPROP software and data handling

- HYPROP-VIEW: data logging, device management, and visualization (graphical and tabular) of tensions and weights over time.
- HYPROP-FIT: parameter optimization and curve fitting; supports multiple models and integral fitting to minimize bias near saturation.
- WP4 data integration: instructions for adding WP4 data to HYPROP-FIT, including mass and pF data for enhanced fitting.

## Influences on measuring range and limitations

- Air entry point of tensio shafts is high (around 8.8 bars) and generally not limiting.
- Water vapor pressure and boiling point cap the upper measurement range; atmospheric pressure relative to sea level affects usable range, especially at higher elevations.
- Osmotic effects are negligible for typical ions due to pore size, but shown to be small; ensure degassed water to minimize errors.

## Typical curves and data interpretation

- Typical curves vary by soil type (clay, loam, sand, etc.); examples illustrate how retention and conductivity curves behave with pore size distribution and porosity.
- Evaluation can use single or multi-curve fitting; the topic includes guidance on model selection based on soil texture.

## Troubleshooting and maintenance

- Common issues include dry tensio shafts, bubbles, insufficient tension range, measurement data dropouts, misalignment of sensor units, and damaged sensor components.
- Solutions include re-degassing, checking for leaks, resealing O-rings, ensuring proper mounting, and verifying electrical connections.

## Cleaning, maintenance, and storage

- Sensor unit is IP65-rated and can be cleaned under running water; clean carefully with the unit upside down to prevent soil ingress.
- Replace O-rings if leakage is detected; follow careful handling when removing or re-installing tensio shafts.
- Store to prevent algae growth during long-term storage.

## Additional accessories and references

- Comprehensive list of HYPROP extensions, Refill Units, Beaker Mounts, tensio shafts, and sample rings; details include ordering numbers and configurations.
- Foundational references and notes for the HYPROP methodology, including historical development (Wind, Schindler), key papers (Peters & Durner, van Genuchten, Kosugi, etc.), and HYPROP-FIT manual links.

## Preliminary theory and terminology

- HYPROP measures the soil water tension/content relationship (retention curve) and the unsaturated hydraulic conductivity as a function of tension.
- Definitions of tension, matrix potential, and pF values; relation between pF, hPa, kPa, and water content for interpretation of results.
- Explanation of how two tensio shafts and mass change provide discrete data points for retention and conductivity curves via Darcy-based calculations.

## Addendum (WP4 data integration and typical curves)

- Guidelines for incorporating WP4 data into HYPROP-FIT evaluations to enhance curve fitting and data consistency.
- Examples and typical curve descriptions for various soil textures (sand, loam, clayey silt) with notes on measuring behavior and model applicability.

## Technical data and references

- Specifications for tensio shafts, sensors, and HYPROP balance; accuracy and operating ranges; protection, chemical resistance, and data formats.
- Key references for methodology, models, and software manuals.
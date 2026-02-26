# Operation Manual HYPROP

- HYPROP is a fully automated system to determine soil hydraulic properties by measuring water tension at two depths in a soil sample, using two tensio shafts.
- Based on Schindler’s evaporation method; outputs include water tension, water content (pF/WC), and hydraulic conductivity (Ku) as functions of tension.
- Evaluation is performed with HYPROP-FIT; data logging and management are handled by HYPROP-VIEW.

## Purpose, scope, and intended use

- Purpose: measure the water retention function and unsaturated hydraulic conductivity as functions of water tension or content during evaporation.
- Intended use: in laboratory settings for soil samples in rings; measures evaporation-driven changes in tension and mass.
- Data outputs: time series of tensions, masses, computed θ(h) and K(h) curves; supports fitting with standard models (e.g., van Genuchten, Brooks-Corey, Kosugi, PDI variants).

## System, components, and scope of delivery

- Sensor unit with two tensio shafts, degassing and filling components, saturation plate, and connection hardware.
- HYPROP-VIEW software (data logging; device management; displays graphs and tables).
- HYPROP-FIT software (data evaluation; model fitting; export).
- Additional accessories: Refill Unit, syringes, vacuum tubing, beakers, sample rings, silicone gaskets, extensible tensio shafts, adapters, and options for single or multi-balance setups.
- Device tree and safety documentation included.

## Software, data flow, and outputs

- HYPROP-VIEW: manages connected balances and sensor units; shows device status and measurement values (graphical and tabular).
- HYPROP-FIT: processes raw data to generate θ(h) and K(h) curves; supports multiple models and integral fitting; exports data for reporting.
- WP4 data integration: option to add WP4 measurements post HYPROP measurement; data points are weighted like HYPROP data.

## Getting started: initial operation

- Install HYPROP-VIEW and HYPROP-FIT from supplied CD or download; connect HYPROP balance via USB; software automatically detects devices.
- Ensure each sensor unit has a unique device ID to avoid communication collisions.
- The measurement workflow includes soil sampling, saturating the sample, preparing the apparatus, starting the measurement, and evaluating results with HYPROP-FIT.

## Preparing and saturating the soil sample

- Use UMS sample rings (250 ml typical) and prepare the soil surface to avoid loss.
- Saturation procedure: place soil in water to saturate, cap off air and evaporation; wait for capillary saturation until the surface shines.
- Saturation times vary by soil texture (e.g., coarse sands ~9–10 min; fine sands ~45 min–1 h; silts ~6 h–24 h; clays up to 2 weeks).

## Filling and degassing the tensio shafts

- Degassing methods:
  - HYPROP Refill Unit (vacuum pump; best results; follow color-coded connections; degas water for tensio shafts and sensor unit; ensure no air bubbles).
  - Syringes (basic scope; manual degassing; overnight pre-wetting of shafts improves time).
- Key safety: avoid touching ceramic tips; ensure no air enters via the tips; degas water in tensio shafts completely.

## Filling the sensor system and tensio shafts

- Degassed, bubble-free water fills the tensio shafts and sensor unit using the refilling attachment and syringes.
- Attach silicone caps to prevent evaporation; ensure air-free water reaches sensor unit seals.
- After degassing, ensure the vacuum reaches atmospheric pressure minus about 20 hPa (2 kPa) for sensor readiness.

## Implementing the tensio shafts and assembling the measurement

- Attach tensio shafts to the sensor unit with water-filled shafts; monitor pressure increase on the computer screen as shafts are threaded.
- Do not exceed about 2000 hPa (200 kPa) to avoid sensor damage; tighten gradually (roughly 9 full turns then an additional quarter-turn).
- Attach dirt protection and re-seal with silicone tubes; fill again with degassed water.

## Measurement setup: modes and weighing

- Multi balance mode: one balance per sensor unit; simpler for handling many units concurrently.
- Single balance mode: one balance for multiple sensor units (up to 20 samples); requires manual weighing of each sample twice daily.
- Weighing the samples: zero the balance, ensure correct device mapping, and follow on-screen prompts.
- Ensure the magneto cable is managed properly to avoid tangling; allow 5 minutes for cable tension to settle before weighing.

## Measuring procedure (step-by-step)

- Soil sampling and preparation; saturate; prepare the measuring system; place the sample in the system.
- Start the measuring campaign; the evaporation process drives tension changes and mass loss; tensions at two depths provide the basis for the pF/WC curve.
- Finishing a measurement: stop at cavitation phase or at air-entry points depending on evaluation strategy; HYPROP-FIT can interpolate across phases if needed.

## Dry weight and data evaluation

- After measurement, determine the dry weight by oven-drying the soil sample (105 C) and weigh to compute volumetric water contents.
- HYPROP-FIT performs curve fitting to θ(h) and K(h) using non-linear regression; supports integral fits and multiple models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, etc.).
- Input of dry mass is required for accurate θ(h). If not provided, HYPROP-FIT can estimate initial values; final fitting aligns data with the chosen model.

## Data interpretation and typical outputs

- Retention curve (pF/WC) and conductivity curve (Ku(h)) derived from tensions h1 and h2 and time-based mass changes.
- Medial water content and tension values derived from average tensions; mass changes yield flow rates and conductivities.
- Supports interpretation across soil types (sand, silt, clay) with model fits; operator can choose different models to match curve shapes.
- Add WP4 data points if WP4 measurements are performed; they are integrated into HYPROP-FIT with equivalent weighting.

## Maintenance, cleaning, and troubleshooting

- Cleaning: sensor unit IP65-rated; rinse with running water while keeping the unit upside down to prevent soil ingress.
- Changing O-rings: inspect if tension rise flattens; replace red O-rings using proper tools and procedures to avoid sensor damage.
- Storage: prevent algae growth; store in a clean environment.
- Troubleshooting highlights:
  - Dry tensio shaft: re-degas and refill.
  - Bubbles: re-fill and degas; check for leaks or worn O-rings.
  - Abnormal tensions or modes: verify wiring, USB connections, and device addressing; ensure proper operation of the balance and sensor unit.
  - Sensor failures: check or replace sensor units; send for service if readings exceed normal ranges.

## Safety, warranty, and support

- Electrical safety and EMC compliance required for the country of use; warranty excludes user-induced damages.
- Warranty: minimum 12 months; covers material/production defects; excludes shipping.
- Software: user support and Wizards guide through software features; administrator rights may be needed for installation.

## Additional notes, theory, and references

- Preliminary theory: HYPROP builds on Wind and Schindler’s evaporation method with two tensiometers at two depths to obtain pF/WC and Ku(h) curves through evaporation-driven mass loss and tension changes.
- Terms: matrix potential, tension, pF value all refer to soil water energy; negative values indicate suction.
- Typical curves and model selections are discussed; range limits are determined by air entry point, vapor pressure/boiling point, and boiling delay.
- The manual provides examples for various soil textures (sandy loam, clayey silt, loamy sand, sandy sand) and notes on curve interpretation and model fitting.
- References: foundational works by van Genuchten, Brooks-Corey, Kosugi, Peters & Durner, Schindler, and related HYPROP literature.
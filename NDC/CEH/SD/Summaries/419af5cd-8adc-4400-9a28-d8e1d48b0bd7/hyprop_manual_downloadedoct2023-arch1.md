# Operation Manual HYPROP

- HYPROP is an automated system to determine soil hydraulic properties by evaporation, measuring water tension at two depths with two tensio shafts while tracking sample mass on a balance.
- It yields the water retention function (pF/WC) and the unsaturated hydraulic conductivity function (Ku) as functions of tension/content.
- Core workflow: saturate soil in a sample ring, degas and fill tensio shafts, assemble the sensor unit on a balance, run evaporation, and evaluate results with HYPROP-FIT (and HYPROP-VIEW for logging).

## What is in the HYPROP system

- Sensor unit with two tensio shafts (50 mm and 25 mm) and associated wiring.
- Tensio shafts for measuring matrix potentials via porous ceramic tips.
- HYPROP balance(s) for mass measurement (multi balance mode or single balance mode).
- HYPROP-VIEW software (data logging, device management, configuration wizard).
- HYPROP-FIT software (data evaluation, curve fitting, export to models).
- Refill Unit (vacuum-based degassing) and/or syringes for degassing and filling.
- Saturation plate, beaker mounts, sample rings (e.g., 250 ml).
- Accessories for filling, cleaning, maintenance, and spare O-rings.

## Safety, intended use, and warranty

- Intended use: measure water retention and hydraulic conductivity of soil samples as a function of tension or water content.
- Safety: follow electrical safety/EMC requirements per country; sensor tips and surfaces must be handled with care (avoid touching ceramic tips; avoid damaging pressure sensors).
- IP65-rated sensor unit; warranty covers material/production defects per local laws (minimum 12 months).

## Key software functions

- HYPROP-VIEW
  - Displays connected devices and real-time measurement data (tensions, weights).
  - Filling assistant and measurement configuration wizard.
  - Manages device network and data logging; supports multiple sensor units and balances.
- HYPROP-FIT
  - Evaluates HYPROP data, fits θ(h) and K(h) curves using models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, including bimodal and PDI variants).
  - Applies linear interpolation via Hermitian splines to generate discrete data points (default ~100 time points).
  - Supports integral fit to reduce bias in retention curve fitting.

## Measuring concept and data generation

- Two tensiometers measure tensions h1 and h2 at different soil depths; the average tension corresponds to the medial pF value; mass loss of the sample yields volumetric water content changes.
- Data points per time: tensions h1, h2 and, in multi-balance mode, total mass; in single-balance mode, mass is weighed manually (twice daily) per sample.
- Data processing converts mass changes to θ (volumetric water content) and derives q (water flux) to compute Ku via Darcy-based relations.
- Typical outputs: time series of tensions and weights, plus derived θ(h) and K(h) curves.

## Measuring range and influencing factors

- Air entry point of tensio shafts is about 8.8 bar (highly hydrophilic and pore-structure dependent).
- Water vapor pressure at 20°C (~2.3 kPa) limits the practical range; as ambient pressure drops or as boiling delay occurs, the usable tension range extends beyond normal limits.
- Atmospheric pressure variations with altitude affect the absolute tension values; osmosis through ceramic pores is negligible due to pore size (~0.3 µm).
- Optimal measuring range can be extended by achieving an air-free fill and accounting for boiling delay; suboptimal curves can still be evaluated.

## General measuring procedure (high level)

- Soil sampling and preparation in a sample ring; saturate the sample via capillary action.
- Saturate and degas water in tensio shafts and sensor unit (two main methods: Refill Unit vacuum degassing or syringe-based degassing).
- Assemble tensio shafts into sensor unit and connect to computer for monitoring.
- Prepare and set up the measurement: fix sample, connect to the balance, and start the evaporation measurement.
- Weigh the dry mass of the soil after measurement for ε (volumetric calculations) and use HYPROP-FIT for evaluation.
- Use HYPROP-FIT to fit θ(h) and K(h); export results for further use.

## Saturating and degassing details

- Saturation: use a degassed water bath, avoid air entrapment; cap the sample ring appropriately to control evaporation while saturating.
- Degassing methods:
  - HYPROP Refill Unit: use vacuum pump to degas tensio shafts and sensor unit; ensure power timing, avoid air bubbles, and maintain vacuum below atmospheric pressure by about 8 hPa (0.8 kPa).
  - Syringes: fill and degas deionized water in reservoir syringe and vacuum syringe; create bubble-free connections to tensio shafts; monitor for residual air and repeat as needed.
- Filling the tensio shafts and sensor unit requires bubble-free water and careful connection to avoid pressure shocks to sensors.

## Assembly and operation

- Drilling holes and preparing the soil sample to ensure air gaps are minimized; assemble the sensor unit onto the soil sample without compressing the soil.
- Multi balance mode: one balance per sensor unit; single balance mode: one balance supports multiple sensor units; weighing workflow adjusted accordingly.
- Balance setup: ensure a vibration-free environment; zero/tare adjustments; ensure magneto cable loops do not create interference.

## Measuring curve and data interpretation

- Optimal measuring curve comprises four phases per tensio shaft:
  - Phase 1: regular rise in tension during evaporation.
  - Phase 2: boiling delay region (advantageous but not strictly required).
  - Phase 3: cavitation (vapor formation, tension drops).
  - Phase 4: air entry (tensions drop to near zero as air enters the ceramic).
- If curves are suboptimal, HYPROP-FIT can still fit using alternative models; refer to addendum for typical curves.
- Finishing a measurement can be done when appropriate phase conditions are reached or when both tensio shafts are in usable ranges; subsequent HYPROP-FIT evaluation is performed.

## Dry weight and evaluation

- After measurement, determine the dry weight by oven-drying the soil and weighing the dry mass; use this to compute true volumetric water content.
- HYPROP-FIT processes raw data: interpolation to fixed time points, computes θ(h) and K(h), and applies non-linear regression to fit models (e.g., van Genuchten-Mualem, Brooks-Corey, Kosugi, PDI).
- Integration with WP4 data is supported for gravimetric corrections and additional data points.

## Troubleshooting and maintenance

- Common issues: dry tensio shafts, air bubbles, insufficient sealing, leaks in O-rings.
- Solutions: re-fill degassed water, reseal O-rings, check sensor connections and vacuum integrity, ensure no air in syringes or tubes.
- Cleaning: sensor unit is IP65; wash under running water with sensor unit upside down; avoid removing tensio shafts; clean O-rings and replace if necessary.
- O-ring replacement: use service pack O-rings, follow procedure to snap into place; avoid damaging the sensor.
- Storage: keep equipment clean and dry; avoid algae growth during long-term storage.

## Additional notes and references

- The manual provides typical curves, WP4 data integration, and extensive theory on pF/WC curves, matrix potential, and model descriptions.
- References include foundational works by van Genuchten, Brooks-Corey, Kosugi, Peters & Durner, and Schindler et al. for evaporation-based soil hydraulic properties.
- For detailed procedures, software manuals and addenda are linked in the HYPROP documentation.
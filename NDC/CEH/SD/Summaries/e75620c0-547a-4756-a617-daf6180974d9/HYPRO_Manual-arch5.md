# Operation Manual HYPROP

## Overview
- HYPROP is a fully automated system to determine the hydraulic properties of soil samples by measuring water tension at two depths during evaporation.
- Produces the water retention curve (pF/WC) and the unsaturated hydraulic conductivity curve (Ku) as functions of tension/content.
- Based on Schindler's evaporation method; uses two tensio shafts to monitor tensions at two depths; mass change is recorded via a balance.
- Data can be processed with HYPROP-VIEW (data logging and storage) and HYPROP-FIT (data evaluation, fitting, and export).
- Measuring range and interpretation depend on soil type; typical measurement time ranges from 2 days (clays) to up to 10 days (peat, sand).

## What is Measured and Data Generated
- Tensions at two depths (h1, h2) over time; mass change of soil sample.
- Medial pF value derived from averaged tensions; medial WC from mass and soil volume.
- Hydraulic conductivity K(h) derived by inverting Darcy’s equation from measured water loss between time points.
- 100 time-point data points by default after interpolation; supports both retention and conductivity curves.
- Dry weight of the sample is needed for accurate volumetric water content calculation; WP4 data can be added post-measurement for extended data points.
- Data can be stored and logged in HYPROP-VIEW; evaluation with HYPROP-FIT follows, allowing model fits (van Genuchten, Brooks-Corey, Kosugi, PDI, etc.).

## Measuring Modes and Setup
- Multi balance mode: one balance per sensor unit (higher throughput; balance placed on a vibration-free surface).
- Single balance mode: one balance for multiple sensor units (up to 20 samples); manual weighing of samples twice daily.
- Two main hardware components: HYPROP sensor unit (with two tensio shafts) and HYPROP balance; HYPROP-VIEW and HYPROP-FIT software.
- Each sensor unit requires a unique device ID to avoid communication collisions.
- Degassing is essential (via Refill Unit or syringes) to remove dissolved air from water in tensio shafts and sensor unit.

## Preparing and Saturating Samples
- Saturation procedure: prepare soil in sample ring with cap, ensure air escapes, and capillary saturation occurs (varies by soil type; times range from minutes to weeks for different textures).
- Degassed water must fill tensio shafts and sensor unit; procedural steps differ for the Refill Unit vs. syringes.
- For the Refill Unit, use vacuum for degassing, monitor manometer for leaks, and ensure air is removed.
- For syringes, degas by pulling the plunger to generate vacuum, fill shafts, and connect via tubing with proper O-rings.
- After degassing, install the tensio shafts into the sensor unit while monitoring pressure to avoid sensor damage (avoid >2000–3000 hPa during insertion).

## Installing and Operating the System
- Connect sensor unit to computer via USB; HYPROP-VIEW automatically detects connected devices.
- Run HYPROP-VIEW to configure measuring mode, sample name, ring type, and balance type; use wizard or manual data entry.
- Weighing: in multi-balance mode, mass data are captured by the balance; in single-balance mode, weigh each sample twice daily (manual).
- Ensure the entire system is air-free to enable accurate tension readings and avoid bubbles.
- The measurement proceeds through four phases in ideal conditions: regular measurement range, boiling delay, cavitation, and air entry; air entry point is used for evaluation in some cases.

## Data Processing and Evaluation
- HYPROP-FIT processes raw data to produce θ(h) and K(h) curves, using non-linear regression to fit models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, Peters-Durner-Iden, etc.).
- For θ(h) and K(h), the method uses an integral fit to avoid bias when water content is not perfectly linear along the column.
- Input the soil dry mass and WP4 data if available; HYPROP-FIT converts gravimetric into volumetric water contents and assigns equal weighting to HYPROP and WP4 data during fitting.
- The evaluation workflow includes Information, Measuring, Evaluation, Fitting, and Export; detailed model options available in the HYPROP-FIT manual.
- If suboptimal curves occur, the data may still be evaluable using appropriate models; addendum contains example curves for various soils.

## Finishing a Measurement
- You can finish when the upper tensio shaft reaches cavitation ( Phase 3) or continue to use the air entry point (Phase 4) if both shafts are suitable for calculation.
- If using air entry, the medial value can be calculated when both shafts have advanced appropriately; otherwise wait until both reach compatible phases.
- After finishing, weigh the dry mass and proceed with HYPROP-FIT evaluation; follow steps for dry weight determination and sample preparation for post-measurement analyses.

## Data Quality, Troubleshooting, and Maintenance
- Common issues: dry tensio shaft, air bubbles, insufficient vacuum, leaks or worn O-rings, data not being recorded, misalignment of sensor units, or interchanged tensio shafts.
- Troubleshooting guidance covers correcting degassing, reseating shafts, detecting leaks, and replacing O-rings as needed.
- Cleaning: sensor unit is IP65; rinse under running water with the unit upside down to avoid soil intrusion; remove tensio shafts for thorough cleaning.
- O-ring replacement: use proper O-ring from service pack; ensure the shaft seats properly without damaging the sensor.
- Storage: avoid algae growth during long-term storage.
- Safety and warranty: follow electrical safety requirements; avoid touching ceramic tips; warranty covers material/production defects for at least 12 months as per local laws.

## Safety, Warranty, and Documentation
- Safety: electrical installations must meet local safety and EMC requirements; avoid contact with ceramic tensio shaft surfaces.
- Intended use: measuring water retention function and hydraulic conductivity of soil samples.
- Warranty: minimum 12 months; excludes damages due to misuse or external conditions; contact UMS or representative for service.
- Documentation: HYPROP manual references, HYPROP-FIT manual, and related literature and standards cited for methodology and model selection.

## Technical Data (Summary)
- Tensio shafts: two levels; capacities up to ~2000 hPa (200 kPa) typical during operation; bubble point > 200 kPa for the large shaft.
- Measuring range: pressure -3.0 to 3000 hPa (-0.3 to 300 kPa); temperature -30 to 70 °C; accuracy ~2.5 hPa, temperature accuracy ~0.01–0.2 K depending on range.
- Sensor unit: IP65 protection; 20 sensor units supported via tensioLINK; USB connection for HYPROP-Balance readout.
- Balance: weighing range up to 2200 g; readout resolution 0.01 g; reproducibility 0.01 g; linearity 0.01 g; built-in adjustment capabilities.

Note: For citation and detailed procedures, refer to the HYPROP manuals (HYPROP, HYPROP-VIEW, HYPROP-FIT) and the referenced literature within the document.
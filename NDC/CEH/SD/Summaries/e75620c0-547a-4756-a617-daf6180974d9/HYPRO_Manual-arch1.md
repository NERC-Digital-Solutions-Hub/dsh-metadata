# Operation Manual HYPROP

- HYPROP is a fully automated system to determine soil hydraulic properties by measuring water tension at two depths in a soil sample using two tensio shafts.
- The method detects differences between upper (dryer) and lower (wetter) horizons to infer water retention (pF/WC) and hydraulic conductivity as tension changes.
- Based on Schindler’s evaporation method; HYPROP-FIT software (separate manual) evaluates the data.

## System and scope of delivery

- Includes sensor unit, HYPROP device, tensio shafts (50 mm and 25 mm), saturation plate, reservoirs, vacuum syringe, droplet syringe, refilling attachment, cables, and sample rings (250 ml) with caps.
- Optional accessories and extensions listed (e.g., HYPROP Refill Unit, HYPROP Balance).

## Safety and intended use

- Intended for measuring water retention and unsaturated hydraulic conductivity as functions of tension or water content.
- Electrical safety and EMC requirements depend on country; damages from misuse not covered by warranty.
- Safety notes include avoiding contact with tensio shaft ceramics, and not inserting sharp objects into sensor holes.

## Software and setup

- HYPROP-VIEW for data logging; HYPROP-FIT for evaluation (separate manual).
- Install from CD or via download; connect HYPROP balance to USB; ensure unique device IDs to avoid collisions.
- Administrator rights may be required for software installation.

## General measuring procedure (overview)

- Steps: soil sampling and preparation → saturating the soil sample → preparing the measuring system → installing the sample and starting measurement → evaluating results with HYPROP-FIT.
- Saturation and preparation steps precede the actual evaporation measurement.

## Saturating the soil sample

- Prepare a sample ring with appropriate top/bottom protection to prevent soil loss.
- Capillary saturate by placing the sample in degassed water, ensuring air can escape; cover to limit evaporation.
- Saturation times vary by soil type (e.g., coarse sands ~9–10 min, fine sands ~45 min to 1 h, silts ~6 h, clays up to 2 weeks).

## Filling the device and degassing

- Tensio shafts must be degassed with degassed water to prevent air in the pores.
- Degassing methods:
  - Refill Unit (vacuum pump): connect, degas water, run in timer-based cycle, monitor for leaks.
  - Syringes: manual degassing, overnight soaking recommended for shafts.
- Steps cover filling sensor unit holes bubble-free, attaching refilling attachments, and ensuring vacuum levels reach near atmospheric minus ~20 hPa before measuring.

## Implementing the tensio shafts in the sensor unit

- Attach shafts with water-filled tips into the sensor unit; monitor pressure rise and seal with O-rings (~9 turns before rapid sealing).
- Do not exceed ~2000 hPa (200 kPa) when fully inserted; avoid air entrapment and damage to sensors.

## Attaching the dirt protection and final assembly

- Fit dirt protection O-rings, reassemble tubes, and fill tips with degassed water.
- Check for air bubbles and ensure no air entry during assembly.

## Balances and measurement setup

- Modes:
  - Multi balance mode: one balance per sensor unit.
  - Single balance mode: one balance for multiple sensor units (up to 20 samples; manual weighing required).
- Weighing steps: place sensor units on balance, zero before weighing, and reattach as needed.
- Data display includes tension curves and sample weights over time (graphical and tabular).

## Optimal measuring curve and phases

- Four phases if shafts and sensors are air-free:
  1) Regular measurement range (tensions rise toward boiling point).
  2) Boiling delay phase (if fully air-free; not always present).
  3) Cavitation phase (water vapor appears; tension drops).
  4) Air entry phase (air enters ceramic; tension drops to zero, usable as a point for evaluation).
- Air entry point of the ceramic tip is around 8.8 bars; vapor pressure and boiling limit the practical measuring range.
- Suboptimal curves may still be usable; HYPROP-FIT provides modeling options.

## Finishing a measurement

- End conditions:
  - Stop when the upper tensio shaft reaches cavitation (do not rely on air entry).
  - Or use air-entry point of one shaft if the other is in a valid phase; software can interpolate/average as appropriate.
- After finishing, transfer data to HYPROP-FIT for fitting and export.

## Determining the dry weight

- Weigh the dried soil after measurement (105°C oven recommended).
- Remove sample rings carefully to avoid damaging tensio shafts.
- Dry mass plus tare information are needed for accurate volumetric water content calculations.

## Evaluating the measurement (HYPROP-FIT)

- HYPROP-FIT performs step-by-step processing: Information → Measuring → Evaluation → Fitting → Export.
- Uses models for θ(h) and K(h) (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, Peters-Durner-Iden variants).
- Input includes dry mass, and optional WP4 data; employs Hermite spline interpolation to generate 100 time points by default.
- Integral fitting can be used to reduce bias in coarse/structured soils.
- Non-linear regression minimizes the distance between data and model forecasts.

## Parameter optimization and model fitting

- Simultaneous optimization of θ(h) and K(h) parameters (e.g., van Genuchten/Mualem parameters) is performed.
- Integral fit can be used to avoid bias when linear assumptions fail across the sample.

## Influences on measuring range

- Air entry point, water vapor pressure (boiling point), and boiling delay affect range.
- Atmospheric pressure variations with altitude affect maximum measurable tension.
- Osmosis effects are negligible due to pore size; ensure shafts are filled with degassed water.

## Typical measuring curves and example descriptions

- The manual includes descriptive examples for various soil textures (clay, clayey silt, sandy loam, loamy sand, pure sand) illustrating curve shapes, bubble points, and conductivities.
- These examples guide interpretation and model selection.

## Generating data points and units

- HYPROP provides h1, h2 tensions at defined times; mass changes are used to compute θ and q for conductivity.
- Water content is converted from gravimetric to volumetric using dry mass and sample volume.
- Units and conversions for pF, hPa, kPa, MPa, bars, psi, and percent relative to field capacity are provided.

## Troubleshooting

- Common issues include dry tensio shafts, air bubbles, insufficient tension (>500–700 hPa drop), leaks, and sensor unit communication problems.
- Solutions involve re-degassing, checking seals and O-rings, ensuring proper assembly, and verifying connections.

## Cleaning, maintenance, and O-rings

- Sensor unit is IP65; clean under running water with the unit upside down; don’t remove tensio shafts during cleaning.
- If tension rises flatten or drops before vacuum, O-rings may need replacement.
- Use fine tweezers to replace red O-rings; ensure proper seating.

## Storage and miscellaneous

- Store to prevent algae growth; keep equipment in good condition.
- List of additional HYPROP accessories and parts available.

## Preliminary note and theory (brief)

- HYPROP builds on evaporation-based methods (Wind; Schindler) to determine water retention and unsaturated hydraulic conductivity over a wide moisture range.
- The method relies on two tensiometers at different depths and mass-based calculation of water content, with data processed in HYPROP-FIT for parameterized hydraulic models.
- The document references extensive literature and methodological developments to extend measurement range and improve fitting accuracy.
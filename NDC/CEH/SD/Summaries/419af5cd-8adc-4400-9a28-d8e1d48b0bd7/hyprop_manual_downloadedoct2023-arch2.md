# Operation Manual HYPROP

## Overview
- HYPROP is an automated system to determine soil hydraulic properties from evaporation experiments.
- Measures water tension at two depths in a soil sample using two tensio shafts.
- Produces pF/WC (water retention) curves and unsaturated hydraulic conductivity (Ku) as functions of tension.
- Based on Schindler and Wind evaporation methods; data evaluated with HYPROP-FIT software (separate manual).
- Data are generated from two horizons; the upper vs lower tension differences indicate conductivity and drying patterns.

## System and components
- Sensor unit with two tensio shafts, saturation plate, beaker mounts, and wiring; connects to HYPROP balance.
- HYPROP balance (weighing up to ~2200 g, 0.01 g readout).
- HYPROP-VIEW software for data logging and device management; HYPROP-FIT for data evaluation and fitting.
- Degassing options: HYPROP Refill Unit (vacuum degassing) or syringes (manual).
- Accessories: sample rings (250 ml), saturating/ filling components, tubes, seals, lids, and related hardware.
- Data outputs include graphs and tables of tensions and masses over time; supports multiple measuring modes.

## Measuring principle and data workflow
- Two tensions (h1, h2) are measured during evaporation in two depths of the soil column.
- Medial pF value is derived from average tensions; medial WC from mass loss; vertical conductivity (Ku) from flow between the two levels.
- Data are logged over time; HYPROP-FIT interpolates to a standard set (e.g., 100 time points) to fit θ(h) and K(h) curves.
- Supported models for fitting include van Genuchten, Brooks-Corey, Kosugi, and Peters-Durner-Iden variants; integral fit may be used to reduce bias.
- Outputs include discrete data points, fitted curves, and various export options; WP4 data can be incorporated post-measurement.

## Preparation and general measuring procedure
- General steps:
  - Soil sampling and preparation; saturate soil in a controlled process.
  - Degas fill water via Refill Unit or syringes; degas tensio shafts and sensor unit thoroughly (air-free water required).
  - Install tensio shafts into sensor unit; connect to computer for monitoring during assembly.
  - Drill holes, assemble sample on the sensor unit, and attach to the balance (if in multi-balance mode, one sensor per balance).
  - Weigh the sample mass as required (especially in single-balance mode).
  - Begin measurement and subsequently evaluate with HYPROP-FIT.
- Saturation procedure varies by soil type with recommended times ranging from minutes (coarse sands) to hours/days (clays).
- Dry weight (for WC calculations) is determined after measurement by oven-drying the soil and weighing the dry mass.

## Degassing and filling the system
- Refill Unit method:
  - Create a bubble-free degassed water column; use silicone caps to prevent evaporation from the tensio shaft tips.
  - Use proper color-coded connections; ensure no air leaks; set timer for pump operation to optimize degassing and ballooning of air bubbles.
- Syringe method:
  - Degas water in reservoir and vacuum syringes; ensure no air remains in tensio shafts.
  - Connect syringes to tensio shafts; push water through to displace air and fill the shafts bubble-free.
- Sensor unit filling:
  - Fill holes bubble-free with degassed water; ensure zero air pockets to avoid sensor damage.

## Implementing tensio shafts and device setup
- Attach silicone tubing to tensio shaft tips; fill with degassed water until a meniscus forms.
- Screw tensio shafts into the sensor unit, monitoring pressure increase to avoid exceeding sensor limits (approx. 2000 hPa to 3000 hPa ceiling during initial engagement).
- After installation, attach dirt protection, ensure proper sealing, and verify zero-point and response speed via the on-screen checks.

## Measurement modes and weighing
- Multi balance mode: one balance per sensor unit (simplified workflow).
- Single balance mode: one balance for up to 20 sensor units (weighing required twice daily; separate weighing per sample).
- Weighing the sample mass is essential for accurate WC calculation; the system identifies which sensor unit is on the balance and enforces a proper weighing sequence.

## Data collection, curves, and interpretation
- Optimal measuring curve phases (for well-filled system):
  - Phase 1: regular rise of tension to near boiling range.
  - Phase 2: boiling delay; tension rises toward atmospheric pressure minus vapor effects.
  - Phase 3: cavitation; tension may drop as vapor forms.
  - Phase 4: air entry; tension drops toward zero as air enters the ceramic tip.
- Suboptimal curves may still be usable; HYPROP-FIT provides fitting options and model selection.
- The air-entry point, vapor pressure, and boiling delay influence the usable measurement range.
- Typical soil types produce characteristic curves (e.g., clays with broad porosity, sands with sharp bubble points).

## Finishing, dry weight, and evaluation
- Finishing criteria include reaching cavitation or permitting the use of the air-entry point for fitting depending on the data.
- After measurement, determine the dry mass to compute volumetric water content; weigh the dry soil after removing the sample ring carefully.
- HYPROP-FIT evaluates the data, fitting θ(h) and K(h) to models; the process is guided step-by-step through Information, Measuring, Evaluation, Fitting, and Export.
- WP4 data can be integrated into HYPROP-FIT with appropriate mass data.

## Safety, maintenance, and troubleshooting
- Electrical installations must meet local safety and EMC requirements; improper use voids warranty.
- Do not touch tensio shaft ceramics with bare fingers; avoid inserting sharp objects into sensor holes to prevent sensor damage.
- HYPROP is IP65-rated; can be cleaned under running water; remove tensio shafts before cleaning, and clean sensor unit upside down to avoid soil ingress.
- O-ring replacement in sensor unit recommended if leakage or poor sealing is observed.
- Warranty covers material/production defects for at least 12 months; excludes misuse and shipping costs.
- Storage guidance to prevent algae growth during disuse.

## Additional features and references
- Technical data: specifications for tensio shafts, sensors, temperature range, accuracy, and protection.
- Operational notes on models, data formats, and measurement ranges; details on sample treatment after WP4 measurements.
- Addendum includes typical curves for various soils, standard pF curves, and conversion tables for soil water units.
- Documentation and related manuals available from UMS (HYPROP-FIT manual, RH, and references cited within).

## Endnotes and references
- The manual references foundational literature (Brooks & Corey, van Genuchten, Kosugi, Peters & Durner, Schindler et al., Wind) and multiple HYPROP-specific methodological papers.
- Contact and licensing details for HYPROP software and hardware are provided by UMS GmbH.
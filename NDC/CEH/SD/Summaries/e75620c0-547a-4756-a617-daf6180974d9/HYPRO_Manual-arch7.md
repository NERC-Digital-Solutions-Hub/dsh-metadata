# Operation Manual HYPROP

## Overview of HYPROP
- Fully automated system to determine hydraulic soil properties using an evaporation-based method.
- Measures water tension at two depths with two tensio shafts; tracks mass change with a balance.
- Based on Schindler’s method; yields water retention (pF/WC) and unsaturated hydraulic conductivity (Ku) as functions of tension/content.
- HYPROP-VIEW for data logging; HYPROP-FIT for evaluation and fitting; supports exporting data and curves.

## What data/products HYPROP generates
- Time-series data: tensions at two depths (h1, h2) and mass of the sample during evaporation.
- Retention curve θ(h) and hydraulic conductivity curve K(h) via HYPROP-FIT.
- 100 interpolated time points by default; discrete data points and model fits (various soil models).
- Dry mass input (to convert mass loss to volumetric water content); WP4 data can be added post-measurement for integrated data points.
- Metadata to accompany GIS work: sample ring, soil sample name, measurement unit/mode, temperature, evaporation rate, etc.
- Units and ranges defined (pF, hPa, kPa, MPa, bar, psi) with guidance on standard measuring ranges.

## Intended use and theory
- Measures the soil water tension/water content relationship (retention curve) and how unsaturated conductivity depends on tension/content.
- Evaporation from a saturated soil column between two tensiometers; mass loss provides flow and conductivity estimates.
- Two measurement modes: multi balance (one balance per sensor unit) and single balance (one balance for several sensor units, up to 20 samples).
- Data interpretation relies on HYPROP-FIT using models (van Genuchten, Brooks-Corey, Kosugi, PDI, etc.) and both retention and conductivity data are fitted simultaneously.

## Measurement workflow (steps from start to finish)
- Soil sampling and preparation; saturate the soil sample in a ring.
- Saturation procedure with capillary saturation; ensure air escapes; follow recommended saturation times by soil type.
- Prepare the HYPROP device: degas water and tensio shafts (via Refill Unit or syringes); ensure air-free water in tensio shafts.
- Implement tensio shafts into the sensor unit and monitor pressure increase; attach dirt protection and complete assembly.
- Balance setup: choose multi-balance or single-balance mode; calibrate and zero with the balance.
- Weigh samples as required (two weighings per day in single-balance mode; or automatically in multi-balance mode).
- Start measurement: evaporation proceeds; tensions and mass logged over time.
- Finishing the measurement: stop at cavitation or use air-entry point depending on data; complete data capture for HYPROP-FIT.
- Determine dry weight after measurement by oven-drying and weighing; necessary for accurate water content determination.
- Evaluate data with HYPROP-FIT and export results; option to integrate WP4 data if available.

## Degassing, filling, and implementing the tensio shafts
- Degassing options: HYPROP Refill Unit (fast) or syringes (manual).
- Degas water in tensio shafts until bubbles cease; keep tensio shaft tips covered to minimize evaporation.
- Fill sensor unit and tensio shafts with bubble-free, degassed water; ensure airtight connections and avoid air pockets.
- Implement shafts into sensor unit, monitor pressure rise, and avoid over-tightening (risk of damage around 9 turns).
- After installation, perform a function check and zero-point verification before starting measurement.

## Optimal measuring curve and interpretation
- Four phases: regular rise, boiling delay (if fully air-free), cavitation, and air entry (end of useful data range).
- Air entry point and cavitation define limits of the measuring range; higher atmospheric pressure or humidity can shorten usable range.
- If curves are suboptimal, data can still be used with appropriate fitting; see addendum for examples.

## Data analysis and software
- HYPROP-VIEW: device management, data logging, and visualization of tensions and sample mass over time.
- HYPROP-FIT: fits θ(h) and K(h) to measured data; supports multiple soil models; includes integral fit to reduce bias near saturation.
- Data entry and workflow can be guided by built-in help and wizards; experienced users may bypass wizards.
- WP4 data integration: post-measurement inclusion of WP4 data points for enhanced data coverage.
- Export formats and modeling options are described in the HYPROP-FIT manual and related references.

## Units, ranges, and data interpretation for GIS
- pF, hPa, kPa, MPa, bar, psi as pressure/matrix potential units; pF relates to water potential via log-scale.
- Standard ranges: tensiometer ranges up to around 1000 hPa; vapor pressure and air-entry limits govern end points.
- Data outputs include discrete θ(h) and K(h) points across the measured tension range, with time stamp and sample metadata suitable for GIS attribute tables and soil hydraulic property mapping.

## Practical considerations for GIS specialists
- Each HYPROP measurement yields curves that describe soil hydraulic properties; use these as inputs for unsaturated flow and water balance models in GIS/soil-landscape analyses.
- Ensure consistent metadata: soil sample ID, soil type, sampling location (coordinates), date/time, temperature, sample ring type, dry weight, and measurement mode.
- When integrating with maps, link curve data to polygons or points representing soil horizons or sample sites; consider converting curves to tabular point data (θ at fixed h values and K at those values) for easier thematic mapping.
- Review recommended models (van Genuchten, Brooks-Corey, Kosugi, PDI) to select the most appropriate representation for regional soils.

## Safety, maintenance, and support
- Electrical installations must meet local safety/EMC requirements; warranty excludes user-made damages.
- Sensor tips must not be touched with bare fingers; do not damage sensor ceramic.
- Sensor unit is IP65; clean under running water; remove and inspect tensio shafts during maintenance.
- O-ring replacements if leaks occur; keep spare O-rings in service packs.
- Storage guidance to prevent algae growth; keep equipment clean and dry.

## Additional notes and references
- The manual provides extensive theory, measurement details, troubleshooting, and references to foundational literature (Wind, Schindler, Peters & Durner, etc.) and related HYPROP manuals for HYPROP-FIT.
- For deeper methodological and modeling details, consult HYPROP-FIT manual and the cited literature.
# Operation Manual HYPROP

## Overview
- HYPROP is an automated system to determine soil hydraulic properties by measuring water tension at two depths in a soil sample and tracking sample mass during evaporation.
- Outputs include the pF/WC retention curve and the unsaturated hydraulic conductivity function Ku as a function of tension, based on Schindler/Wind methods.
- Data are generated as time series of tensions h1 and h2, and mass; processed into discrete θ(h) and K(h) points via HYPROP-FIT, with HYPROP-VIEW handling logging and device management.

## System and data flow
- Key components: sensor unit with two tensio shafts, HYPROP balance, HYPROP-VIEW software, HYPROP-FIT evaluation; optional HYPROP Refill Unit or syringes for degassing.
- Operational modes: multi balance (one balance per sensor unit) or single balance (one balance for up to 20 sensor units).
- Data produced: tensions (h1, h2), sample mass over time, dry mass input, and derived water contents (θ) and pF; outputs are curves and fitted hydraulic functions.
- Data handling: input dry mass and optional WP4 data; export and interpretation via HYPROP-FIT (models such as van Genuchten, Brooks-Corey, Kosugi, PDI).

## Measuring method and procedure
- Measuring sequence: soil sampling and preparation → saturating the soil → preparing the measuring system → placing the sample and starting the campaign → evaluating results with HYPROP-FIT.
- Saturation timing depends on soil texture (e.g., coarse sands ~9–10 min; fine sands ~45–60 min; silts ~6 h; clays up to 2 weeks).
- Degassing and filling the tensio shafts water is essential to avoid air; two methods:
  - HYPROP Refill Unit (vacuum degassing, faster, includes beaker and attachment).
  - Syringes (manual, slower).
- Degassing/filling steps emphasize keeping water bubble-free, avoiding touching ceramic tips, and achieving a vacuum value near atmospheric pressure minus ~20 hPa (2 kPa) before measurement.
- Tensio shafts are installed into the sensor unit with degassed water, careful torque (avoid exceeding ~2000 hPa), and monitoring tensions during installation.
- Holes drilled into the soil sample, sample assembly checked to avoid air gaps and compression.
- Weighing and sample handling follow mode (multi vs single balance), with automatic identification of sensor units on the balance in multi-mode.

## Data quality and safety
- Data quality relies on fully air-free water and degassed components; check for leaks, bubbles, and proper seating of O-rings.
- Regular zero-point and response checks, vacuum checks, and end-vacuum checks are part of function checks.
- Safety: electrical safety/compliance, IP65 sensor housing, avoid contact with ceramic tips, do not puncture sensor holes.

## Data analysis and outputs
- HYPROP-FIT performs simultaneous optimization of θ(h) and K(h) using non-linear regression; supports standard soil models (van Genuchten, Brooks-Corey, Kosugi, Fayer-Simmons, bi-modal, and Peters-Durner-Iden variants).
- Interpolation via Hermite splines yields fixed time-point data for curve fitting; outputs 100 calculation points by default.
- Integration (integral fit) option reduces bias in the retention function, especially for uneven soil layers.
- WP4 data (if available) can be integrated post-measurement to extend data coverage; gravimetric to volumetric conversions are handled and weighted similarly to HYPROP data.
- Outputs include θ(h) and K(h) curves, plus fit parameters and export-ready data.

## Measuring range and considerations
- Air entry point, vapor pressure, and boiling delay limit/shape the measurement range.
- Air entry point for HYPROP tensio shafts is about 8.8 bars; vapor pressure at 20°C (~2.3 kPa) defines boil-point constraints relative to atmospheric pressure and elevation.
- Osmosis is negligible due to pore size (~0.3 μm) of the ceramic.
- Practical interpretation includes the possibility to measure beyond conventional ranges (boiling delay and cavitation phases), with appropriate modeling.

## Typical curves and interpretation
- The manual provides representative curves for sandy loam, clayey silt, slightly loamy sand, and pure sands, illustrating how tension and conductivity evolve during evaporation and how curves inform model selection (e.g., bimodal, Brooks-Corey, van Genuchten).

## Finishing and data interpretation
- Finishing a measurement can be done when upper tensio shaft reaches cavitation or when both shafts reach air-entry considerations; HYPROP-FIT then evaluates the measured data.
- Dry weight determination requires weighing the dry soil after measurement; careful handling to avoid soil loss or shaft damage.
- Final evaluation with HYPROP-FIT involves stepwise navigation (Information, Measuring, Evaluation, Fitting, Export) with extensive documentation in the HYPROP-FIT manual.

## Cleaning, maintenance, and storage
- Sensor unit with IP65 protection can be cleaned under running water; do not remove tensio shafts; clean upside-down to minimize soil ingress.
- O-rings in sensor unit can be replaced if leaks are detected.
- Storage guidance to prevent algae growth during long-term storage.

## Software and hardware details
- Hardware: two tensio shafts of different lengths, sensor unit, HYPROP balance; HYPROP Refill Unit, vacuum pump, beaker mounts, and other accessories.
- Software: HYPROP-VIEW (device management, logging, and measurement control) and HYPROP-FIT (data evaluation and curve fitting); wizard-assisted or direct data entry for measurement setup.
- Device management includes unique device IDs to avoid communication collisions.

## Addenda, theory, and references
- Explanations of terms (tension, matrix potential, pF, WC, etc.), units, and measurement concepts.
- Generating discrete data points for θ(h) and K(h) via dual tensiometers and mass data; underlying equations based on Schindler/Wind methodology.
- A comprehensive set of references supports the methodology, models, and evaluation approaches.

## Quick start highlights
- Degas and fill tensio shafts with degassed water; ensure air-free system throughout setup.
- Saturate soil per texture-specific timing, then assemble in the sensor unit on the balance.
- Start HYPROP-VIEW, connect devices, and begin measurement; monitor tensions and mass over time.
- After measurement, weigh dry soil, input dry mass, and evaluate with HYPROP-FIT to obtain retention and conductivity curves.
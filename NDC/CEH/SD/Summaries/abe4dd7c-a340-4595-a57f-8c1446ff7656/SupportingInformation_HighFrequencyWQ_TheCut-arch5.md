# Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012) - Supporting Information

## Overview
- Historical dataset of hourly water quality and nutrient measurements at The Cut, Bray Marina, Berkshire, UK (grid reference SU915786) from May 2010 to February 2012 (document title also references 2009-2012).
- Includes eight water quality parameters: total phosphorus (TP), total reactive phosphorus (TRP), ammonium (NH4 as N), conductivity, temperature, dissolved oxygen (DO), pH, and chlorophyll.
- Accompanying hourly flow data from the Environment Agency gauging station The Cut at Binfield (approximately 10 km upstream).

## Data content
- Measurements: TP and TRP (mg/L), NH4 (mg/L as N), turbidity (NTU), chlorophyll (μg/L; via fluorescence), DO, pH, conductivity, and temperature.
- Flow data: hourly averages derived from 15-minute flow measurements (m3/s) at Binfield station.
- Temporal format: date/time in day/month/year hour:minute; NaN indicates missing data points.
- Location references: Bray monitoring site (SU915786) and upstream Binfield station (SU853713).

## Monitoring methods and instrumentation
- In-situ high-frequency monitoring using:
  - Hach Lange Sigmatax and Phosphax Sigma for TP and TRP analyses (acid persulphate digestion for TP; phosphomolybdenum blue for TRP); detection limit 0.01 mg P/L; daily automated calibration; no filtration.
  - YSI 6600 sonde for in situ DO, pH, temperature, conductivity, turbidity, and chlorophyll; turbidity via light-scattering (830–890 nm) with NTU units; chlorophyll via fluorometry (470 nm).
- Setup: equipment housed in a trailer 5 m from riverbank; continuous water sampling from river center into a flow cell; sub-sample (10 mL) sent to Phosphax Sigma.
- Quality controls: YSI calibration every 2–3 weeks; turbidity and chlorophyll measurements account for sediment interference by comparison with turbidity data.
- Environmental controls: trailer heated to 20°C to maintain reaction temperatures and prevent instrument issues.

## Data format and units
- Time standard: day/month/year hour:minute.
- Flow: hourly average from 15-minute upstream measurements; units in cubic metres per second (m3/s).
- Concentrations: TP and TRP in mg/L; NH4 as N in mg/L.
- Turbidity: NTU.
- Chlorophyll: μg/L (total of chlorophyll a, b, c).

## Data quality and governance considerations
- High-frequency, instrument-driven data with explicit calibration and method references enhances traceability and reproducibility.
- No filtration step in chemical analyses; potential interference considerations noted for chlorophyll measurements due to sediment.
- Documentation includes instrument models, sampling workflow, and calibration routines.
- Supporting publications referenced for context and methodology:
  - Wade et al. (Hydrology and Earth System Sciences, 2012)
  - Halliday et al. (Hydrological Processes, 2015)

## Availability, usage, and stewardship notes
- The dataset is accompanied by methodological detail and literature references to facilitate reuse and integration with broader hydrochemical analyses.
- For stewardship:
  - Preserve raw and processed data with complete metadata (locations, time range, units, methods, calibration schedules).
  - Maintain provenance and any data transformations (e.g., 15-min to hourly aggregation).
  - Capture data gaps and reasons (NaN points) and document any updates or corrections.
  - Ensure clear data sharing terms and potential embargoes are respected for up-to-date datasets.
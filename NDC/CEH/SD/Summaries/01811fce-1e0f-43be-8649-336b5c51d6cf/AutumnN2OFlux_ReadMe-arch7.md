# ReadMe file for AutumnN2OFlux.csv

## Overview
- Describes N2O flux measurements from a field experiment in Snowdonia, Wales, UK.
- Treatments include: Control (no urine), Artificial sheep urine (applied in triplicate patches), and Nitrate + Glucose (C and N treatment).
- Data collected to 118 days post-treatment with both automated high-frequency measurements and later manual measurements.
- Data are quality-assured flux values (not raw concentrations) and require proper attribution when reused.

## Location and Timeframe
- Site: Humic gleysol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Treatments applied on 25/10/17.
- Monitoring period: 118 days following treatment.
- Ground measurements include high-frequency automated data and subsequent monthly manual measurements.

## Experimental Design
- Experimental setup uses a randomised block design with chamber-based flux measurements.
- Chamber details: base area 0.25 m2; chambers sized 50 cm x 50 cm x 15 cm (l x w x h).
- Each chamber records N2O fluxes over time, with multiple treatments assigned to plots.
- Treatment replication: n = 4 for the treatment groupings (as indicated in the description).

## Treatments
- Control: No urine application.
- Artificial sheep urine: Applied in triplicate discrete patches inside the chamber, delivering 1120 kg N ha-1 per patch (200 mL of artificial urine over 100 cm2 soil surface per patch).
- C and N (Nitrate + glucose): 106 kg N ha-1 and 213 kg C ha-1 applied; 1 L of nitrate + glucose solution applied within a 40 × 40 cm square inside the chamber.

## Data Collection and Instruments
- Automated high-frequency measurements:
  - System: Automated greenhouse gas monitoring system (Queensland University of Technology) with a SRI 8610 GC.
  - Flux measurements: Eight flux measurements per chamber per day (1-hour chamber closure, four gas samples per closure).
  - Calibration: Standard calibration after every fourth gas sample.
- Manual measurements:
  - After the automated period, monthly flux measurements were taken from the same chambers.
  - Instrument: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 autosampler; four calibration standards (BOC gases, Liverpool).
- Data quality and processing:
  - The included data are quality-assessed flux values, not raw gas concentrations.
  - QA involved inspecting raw data files and GC chromatograms for anomalies; problematic data were removed (e.g., gas peak interference).

## Data Structure and Content
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time relative to treatment (pre- or post-treatment)
  - Columns B to M: N2O fluxes (µg N2O-N m-2 h-1)
  - Column headers encode treatment and chamber/plot identifiers (e.g., Control, ArtUrine, CandN; corresponding chamber/plot numbers)
- Data scope:
  - Includes flux measurements from the high-frequency automated period and the subsequent monthly manual period.
  - Flux units are micrograms of N2O-N per square meter per hour.

## Usage Notes and Attribution
- Authors must be acknowledged if data are reused or reproduced.
- For GIS applications: data provide spatially explicit flux values by chamber (with associated treatment and time), suitable for map-based visualization and temporal analysis after linking chamber IDs to spatial locations.
- Location context and plot design details are provided to support spatial interpretation and reproducibility of analyses.
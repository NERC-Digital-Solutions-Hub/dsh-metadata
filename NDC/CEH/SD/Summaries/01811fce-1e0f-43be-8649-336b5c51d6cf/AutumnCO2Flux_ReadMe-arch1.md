# ReadMe file for AutumnCO2Flux.csv

## Overview
- Contains flux measurements (high-frequency) from an experiment on unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Data pertain to CO2/CH4 fluxes under three treatments plus a control, with measurements collected post-treatment.
- Note: The readme describes CO2 fluxes, but the data headers refer to CH4 fluxes expressed as mg CO2-C m-2 h-1.

## Study site and timeline
- Location: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Sheep were excluded from 15/05/17 to avoid recent excretal events confounding the data.
- Treatments applied on 25/10/17.
- Monitoring period: 45 days following treatment application.

## Treatments
- Control: no urine application.
- Artificial sheep urine (ArtUrine): artificial urine applied in triplicate discrete patches inside each chamber; each patch delivers 1120 kg N ha-1; 200 ml of artificial urine per patch over 100 cm² soil area.
- Nitrate and glucose (CandN): nitrate and glucose applied at 106 kg N ha-1 and 213 kg C ha-1; 1 L of the solution applied across a 40 × 40 cm square inside the chamber.
- Experimental design: randomized block with four treatments.

## Experimental design and field setup
- Chambers: each with a basal area of 0.25 m²; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
- Emissions monitored from plots using a randomized block design.
- Monitoring duration: 45 days post-treatment.

## Measurements and instrumentation
- Instrument: automated greenhouse gas monitoring system (operated by Queensland University of Technology) connected to a LI-COR LI-820 analyzer.
- Sampling cadence: eight flux measurements per chamber per day.
- Measurement protocol: 1-hour chamber closure periods; 4 gas samples analyzed per 1-hour closure.
- Calibration: calibration standard analyzed after every fourth gas sample.
- Output: high-frequency flux data (not raw gas concentration data).

## Data structure and content
- Data coverage: high-frequency flux data deemed quality-assessed; raw concentration data and some raw files may have been excluded.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment application
  - Columns B to M: CH4 fluxes (reported in mg CO2-C m-2 h-1)
  - Treatment identifiers: Control, ArtUrine (artificial urine), CandN (nitrate and glucose)
  - Chamber/plot numbers embedded in column headers

## Quality assurance and data provenance
- QA steps: inspection of raw data files and GC chromatograms for anomalies; removal of problematic data points as needed.
- Data were curated to represent quality-assessed flux measurements rather than raw gas concentrations.
- Authors must be acknowledged if data are reused or reproduced.

## Usage notes and potential analyses
- Suitable for comparing treatment effects on CH4/CO2 fluxes over time, including short-term responses and temporal trends within the 45-day post-treatment window.
- Data structure supports analyses by treatment, chamber, and time since treatment, enabling correlations, pattern identification, and predictive modeling related to land-management practices and excreta-derived inputs.
- Be mindful of potential scale limitations (plot/chamber level) when extrapolating to larger areas.
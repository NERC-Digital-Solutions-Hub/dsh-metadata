# ReadMe file for AutumnCH4Flux.csv

## Overview
- Methane (CH4) flux data collected from grazing land plots in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Treatments include control (no urine), artificial sheep urine, and nitrate plus glucose (CandN) applied to soil within chambers.
- Data represent high-frequency flux measurements gathered after treatment application, with quality-assured CH4 flux values (not raw gas concentrations).

## Location, site details, and timeline
- Location: unimproved grazing land with humic gleysol soil.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Sheep excluded from plots starting 15/05/2017 to avoid recent excretal events.
- Treatment application date: 25/10/2017.
- Experimental design: randomised block with four replicates per treatment (n = 4).
- Monitoring duration: 45 days following treatment.

## Treatments and experimental design
- Control: no urine application.
- Artificial sheep urine: applied in triplicate discrete patches inside the chamber; each patch corresponds to an N application rate of 1120 kg N ha-1 with 200 mL artificial urine per patch over 100 cm2 soil area.
- CandN (nitrate and glucose): nitrate and glucose solution applied at 106 kg N ha-1 and 213 kg C ha-1; 1 L applied across a 40 × 40 cm square inside the chamber.
- Treatments are labeled in the data headers as Control, ArtUrine (artificial urine), and CandN (nitrate and glucose). Data headers reference chambers/plots accordingly.

## Data collection and instrumentation
- Measurement system: automated greenhouse gas monitoring system (QUT) paired with a SRI 8610 GC (Torrance, USA).
- Sampling rate: eight flux measurements per chamber per day.
- Chamber operation: 1-hour chamber closure period; four gas samples analyzed per closure period.
- Calibration: a standard calibrator run after every fourth gas sample.
- Chamber specs: basal area 0.25 m2; chamber dimensions 50 cm × 50 cm × 15 cm (l × w × h).

## Data content and structure
- Data scope: high-frequency flux measurements post-treatment.
- Data type: quality-assessed CH4 flux data (not raw gas concentrations).
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B–M: CH4 flux values in µg CH4-C m-2 h-1
  - Column headers indicate treatment and chamber/plot numbers (Control, ArtUrine, CandN).

## Quality assurance and data processing
- QA procedures include inspecting raw data files and GC chromatograms for anomalies; data with anomalies (e.g., peak interference) are removed as needed.
- Emphasis on using quality-assessed flux data rather than raw concentrations.
- Data are prepared for analysis of treatment effects on CH4 fluxes over the 45-day post-treatment period.

## Metadata, attribution, and data use
- Data authors must be acknowledged if data are reused or reproduced.
- Metadata provided include treatment type, plot/chamber identifiers, measurement cadence, and timing relative to treatment.
- Data are suitable for evaluating how different treatments influence methane emissions and for integration into broader data systems focusing on greenhouse gas fluxes in grazing systems.

## Practical notes for data practitioners and data leaders
- The dataset supports end-to-end data governance: clear provenance, treatment specifications, sampling cadence, QA steps, and metadata for discoverability.
- Users should account for the potential variability across chambers and replicates due to environmental conditions and treatment effects.
- Consider linking this CH4 flux dataset with other site-level data (soil properties, moisture, temperature) to enhance interpretation and utility in data products.
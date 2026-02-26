# ReadMe file for SummerN2OFlux.csv

## Overview
- Data set of N2O fluxes measured from control (no urine), artificial sheep urine, and real sheep urine treatments.
- Field site: dystric histosol in an unimproved grazing area in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sheep excluded from plots from 15/05/17 to avoid confounding recent excretal events.
- Treatments applied on 24/07/17; randomized block design with four treatments and triplicate patches per treatment.
- 177 days of emissions monitoring post-treatment.

## Experimental design
- Treatments (n = 4): 
  - Control: no urine application.
  - Artificial sheep urine: patches with an N application rate of 920 kg N ha-1 (200 ml in 100 cm2 patches).
  - Real sheep urine: patches with an N application rate of 930 kg N ha-1 (200 ml in 100 cm2 patches).
- Each treatment implemented in triplicate discrete patches per plot.
- Chamber dimensions and area: 0.25 m2 per chamber; chambers sized 50 cm x 50 cm x 15 cm.
- Monitoring period: 177 days after treatment.

## Data collection and instruments
- High-frequency measurements:
  - Instrument: automated greenhouse gas monitoring system (Queensland University of Technology) with a SRI 8610 GC.
  - Protocol: eight flux measurements per chamber per day; 1-hour chamber closure; four gas samples per closure; calibration standard after every fourth sample.
- Manual measurements (post high-frequency period):
  - Instrument: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 autosampler.
  - Calibration: four gas standards spanning measured concentration ranges.
- Data scope:
  - Data include high-frequency flux measurements and monthly manual flux measurements from the same chambers.
  - Output represents quality-assessed flux data (not raw gas concentrations).

## Data content and structure
- Headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time relative to treatment (pre- or post-treatment)
  - Columns B–M: N2O fluxes (µg N2O-N m-2 h-1)
- Treatment and chamber/plot encoding in column headers:
  - Control, ArtUrine (artificial urine), Urine (real urine)
- Scope:
  - Combines high-frequency data with later monthly measurements; data provided as processed/quality-assessed flux values.

## Quality assurance
- Procedures include inspection of raw data files and GC chromatograms for anomalies; problematic data removed as necessary (e.g., peak interferences).
- Emission data reflect curated values rather than raw instrument outputs.

## Usage and attribution
- Authors must be acknowledged if data are reused or reproduced.
- Clear metadata on treatments, timings, and measurement methods facilitates data reuse and cross-study integration.
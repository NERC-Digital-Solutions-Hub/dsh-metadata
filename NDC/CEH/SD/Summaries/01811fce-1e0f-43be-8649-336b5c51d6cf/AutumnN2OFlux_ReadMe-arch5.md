# ReadMe file for AutumnN2OFlux.csv

## Overview
- Dataset of N2O fluxes measured from soil plots under three treatments: Control (no urine), Artificial sheep urine (applied as discrete patches inside the chamber), and C and N (nitrate and glucose).
- Location: humic gleysol in an unimproved grazing land area of the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level; approx 53°22'N, 3°95'W).
- Sheep excluded from plots from 15/05/17 to avoid confounding excretal events.
- Treatments applied on 25/10/17 (n = 4 replicates per treatment).
- Monitoring period: 118 days following treatment application.
- Data collected with both automated high-frequency measurements and later manual monthly measurements.

## Experimental design and treatments
- Experimental design: randomized block with four replicates per treatment.
- Treatments:
  - Control: no urine application.
  - ArtUrine: artificial urine applied in triplicate discrete patches inside the chamber (each patch ≈ 1120 kg N ha-1 rate; 200 ml artificial urine applied over 100 cm2 per patch).
  - CandN: nitrate and glucose treatment applied at 106 kg N ha-1 and 213 kg C ha-1; 1 L of nitrate+glucose solution applied over a 40 x 40 cm square inside the chamber.
- Treatment timing: applied on 25/10/17.
- Chamber setup: each chamber has a basal area of 0.25 m2 with dimensions 50 cm x 50 cm x 15 cm (L x W x H).

## Measurements and data collection
- Automated high-frequency measurements:
  - Instrument: greenhouse gas monitoring system (QUT) using a SRI 8610 GC.
  - Frequency: eight flux measurements per chamber per day; 1-hour chamber closure periods; four gas samples analyzed per closure.
  - Calibration: calibration standard analyzed after every fourth gas sample.
- Manual measurements:
  - Period: monthly flux measurements from the same chambers after the automated period.
  - Instrument: Perkin Elmer 580 GC with Turbo Matrix 110 auto sampler.
  - Calibration: four gas standards spanning measured concentration ranges (BOC gases, Liverpool).
- Data scope:
  - The dataset represents quality-assessed flux data (not raw gas concentration data).
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B to M: N2O fluxes (µg N2O-N m-2 h-1)
  - Column headers indicate treatment and chamber/plot numbers (Control, ArtUrine, CandN).

## Quality assurance and processing
- QA procedures: inspection of raw data files and GC chromatograms for anomalies; removal of data points as needed (e.g., interference in gas peaks).
- Data processing: flux values are supplied as quality-assessed measurements rather than raw gas concentrations.
- Calibration and standards: systematic calibration tied to GC measurements for both automated and manual datasets.

## Provenance and authorship
- Authorship must be acknowledged if data are reused or reproduced.

## Usage notes and considerations
- Data are specific to a particular field experiment and include four replicates per treatment.
- The dataset provides time-resolved N2O flux data over 118 days post-treatment, suitable for analyses of treatment effects on N2O emissions and temporal dynamics.
- Users should reference the treatment definitions, concentrations, and patch/plot configurations as described in the metadata to ensure proper interpretation and comparability.

## Metadata and attribution
- Location details (geographic coordinates and elevation) and experimental conditions (sheep exclusion period) are provided to support reproducibility and contextual interpretation.
- Data are accompanied by explicit notes on data quality, measurement methods, and data structure to facilitate proper data governance and reuse.
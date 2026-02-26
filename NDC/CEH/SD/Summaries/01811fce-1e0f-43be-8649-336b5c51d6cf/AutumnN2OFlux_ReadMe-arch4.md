# ReadMe file for AutumnN2OFlux.csv

## Overview
- Dataset of N2O flux measurements from an unimproved grazing land site in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Treatments: control (no urine), artificial sheep urine, and nitrate + glucose. Sheep were excluded from plots from 15/05/17 to avoid confounding by recent excretal events.
- Data collected from a randomised block design over 118 days post-treatment.
- High-frequency measurements from an automated system, plus subsequent monthly manual measurements.

## Experimental Setup
- Location: humic gleysol soil in an unimproved grazing area.
- Chambers: 0.25 m2 basal area; dimensions 50 cm x 50 cm x 15 cm (L x W x H).
- Treatment application date: 25/10/17.
- Treatments (n = 4, as described): 
  - Control: no urine application.
  - Artificial sheep urine: applied in triplicate discrete patches inside the chamber (1120 kg N ha-1 total N per patch; 200 ml artificial urine per patch over 100 cm2 soil).
  - C and N: nitrate and glucose at 106 kg N ha-1 and 213 kg C ha-1; 1 L applied across a 40 x 40 cm square inside the chamber.
- Emissions monitored for 118 days after treatment.

## Data Collection and Instruments
- High-frequency phase:
  - Instrument: automated greenhouse gas monitoring system (Queensland University of Technology) with a SRI 8610 GC (Torrance, USA).
  - Measurements: eight N2O flux measurements per chamber per day (1 h chamber closure; 4 gas samples per closure).
  - Calibration: standard calibration after every fourth gas sample.
- Post-high-frequency phase:
  - Manual measurements: monthly flux measurements from the same chambers.
  - Instrument: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 auto sampler (calibrated with four gas standards).
  - Calibration standards: four standards spanning measured concentration ranges (BOC gases, Liverpool).
- Data recorded reflect quality-assessed flux values (not raw gas concentrations); QA included checking raw data files and GC chromatograms for anomalies and removing problematic data (e.g., peak interference).

## Data Structure and Variables
- Timestamp: format dd/mm/yy hh:mm.
- Days: days pre- or post-treatment application.
- Flux data: Columns B to M contain N2O flux values (µg N2O-N m-2 h-1).
- Column headers: indicate treatment and chamber/plot numbers (Control, ArtUrine, CandN).

## Quality Assurance and Data Integrity
- Quality assurance procedures applied to raw data and chromatograms; anomalies removed as necessary.
- Data represent quality-assessed flux data, not raw concentration data.

## Usage and Provenance
- Authors must be acknowledged if data are reused or reproduced.
- The ReadMe provides detailed metadata to support data discoverability, interpretation, and potential integration with broader data communities examining soil-atmosphere N2O fluxes under different treatments and management.

## Key Considerations for Data Leaders
- Ensures end-to-end data governance: clear experimental design, treatment definitions, sampling schedules, and processing steps.
- Metadata richness supports reuse across networks and studies, enabling comparability of N2O flux measurements under varied treatments.
- Highlights data lifecycle: high-frequency data with subsequent monthly measurements, plus explicit QA steps and data quality notes.
- Potential data gaps: inconsistent treatment counts described (n = 4 treatments documented but only three treatments described); users should verify the intended experimental design with the data provider.
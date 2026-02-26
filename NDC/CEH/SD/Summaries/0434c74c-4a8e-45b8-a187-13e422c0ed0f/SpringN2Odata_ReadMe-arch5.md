# ReadMe file for SpringN2OData.csv

## Overview
- Data on N2O emissions from control (no urine), artificial urine, and real urine treatments.
- Experimental setting: orthic podzol within semi-improved upland grassland at Henfaes Research Station, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) in spring 2016.
- Experimental design: randomised block; emissions monitored using an automated gas monitoring system, with supplementary monthly manual measurements.

## Experimental setting and location
- Site: Henfaes Research Station, Abergwyngregyn, North Wales.
- Elevation: 270 m above sea level; coordinates 53°13'N, 4°0'W.
- Soil and vegetation: orthic podzol in semi-improved upland grassland.
- Timeframe: spring 2016.

## Data collection and instruments
- Automated measurements: high-frequency flux data using a system from Queensland University of Technology with a SRI 8610 GC (Torrance, USA).
  - cadence: eight flux measurements per chamber per day (1 h chamber closure; 4 gas samples analyzed per closure).
  - calibration: standard analyzed after every fourth gas sample.
- Manual measurements: monthly flux data from smaller chambers (40 cm × 20 cm × 20 cm).
- Chamber setup:
  - Automated chambers: 50 cm × 50 cm × 15 cm (l × w × h); base area 0.25 m2.
  - Manual chambers: 40 cm × 20 cm × 20 cm (l × w × h).
- Data handling: manual samples analyzed with a Perkin Elmer 580 GC with Turbo Matrix 110 auto sampler; calibration with four gas standards (BOC gases, Liverpool).
- Data type: emissions data representing quality-assessed fluxes (not raw gas concentrations).

## Experimental design and treatments
- Treatments: Control (no urine), ArtUrine (artificial urine), Urine (real urine).
- Design: randomised block; multiple plots/chambers.
- Data structure reflects two measurement regimes:
  - High-frequency automated data (continuous monitoring).
  - Monthly manual measurements from smaller chambers; these are indicated in the data structure.

## Data structure and headers
- Timestamp format: dd/mm/yy hh:mm.
- Flux columns: B to M represent N2O fluxes (μg N2O-N m^-2 h^-1).
- Column headers encode treatment and chamber/plot identifiers (e.g., Control, ArtUrine, Urine).

## Quality assurance and data processing
- QA steps: inspection of raw data files and GC chromatograms for anomalies; anomalies removed as appropriate (e.g., interference in gas peaks).
- Handling of detection limits: fluxes below detection limits from manual data replaced with zero.
- Data provenance: data quality assessed prior to sharing; non-raw concentration data provided.

## Usage, authorship, and attribution
- Authors must be acknowledged if the data are reused or reproduced.
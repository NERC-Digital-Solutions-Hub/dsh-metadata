# N2O emissions from control and urine-treated plots on orthic podzol within a semi-improved upland grassland at Henfaes Research Station, North Wales, autumn 2016

## Overview
- Dataset of N2O flux measurements from three treatments: Control (no urine), ArtUrine (artificial urine), and Urine (real sheep urine).
- Location: orthic podzol soil, semi-improved upland grassland, Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W); autumn 2016.
- Experimental design: randomised block.
- Emissions captured using both high-frequency automated measurements and later monthly manual measurements.

## Experimental setup
- Plot and chamber details:
  - Automated phase: chambers with a basal area of 0.25 m²; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
  - Manual phase: smaller chambers 40 cm × 20 cm × 20 cm.
- Treatments applied to plots within the randomised blocks to assess N2O emissions under differing urine inputs.

## Data collection and instrumentation
- Automated data collection:
  - System: automated greenhouse gas monitoring system (QLD University of Technology) with a SRI 8610 GC.
  - Measurements: eight flux measurements per chamber per day; 1-hour chamber closure; four gas samples analysed per closure.
  - Calibration: standard calibrations after every fourth gas sample.
- Manual data collection:
  - GC: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 auto sampler.
  - Standards: four gas standards spanning observed concentration ranges (BOC gases).
- Data type:
  - Automated high-frequency flux data and later manually collected monthly flux data.
  - The dataset represents quality-assessed flux values (not raw gas concentrations).

## Data structure and quality assurance
- Data headers:
  - Date_Time: format dd/mm/yy hh:mm.
  - Columns B–M: N2O fluxes (µg N2O-N m⁻² h⁻¹).
  - Labels in headers indicate treatment (Control, ArtUrine, Urine) and chamber/plot numbers.
- Quality assurance:
  - Raw data files and GC chromatograms inspected for anomalies; anomalies removed as needed (e.g., peak interference).
  - For manual data, fluxes below detection limits replaced with zero.

## Data notes and usage considerations
- High-frequency ( Automated ) data vs. monthly (Manual) data; alignment may be required for analyses.
- Units: N2O flux expressed as micrograms N2O-N per square meter per hour.
- Important when modeling treatment effects: ensure proper handling of missing data, detection-limit substitutions, and distinction between automated vs. manual measurement periods.
- Data provenance: authors must be acknowledged if data are reused or reproduced.
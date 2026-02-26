# ReadMe file for SummerN2OFlux.csv

## Overview
- A dataset of N2O fluxes measured from control (no urine), artificial sheep urine, and real sheep urine treatments.
- Study site: dystric histosol within unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sheep excluded from plots from 15/05/2017 to avoid recent excretal effects confounding results.
- Treatments (n = 4 per treatment): Control, Artificial urine, Real urine. Each treatment uses patch-based applications on soil.

## Treatments details
- Artificial sheep urine: 920 kg N ha-1 applied; 200 ml artificial urine over 100 cm2 per patch; triplicate patches per chamber.
- Real sheep urine: 930 kg N ha-1 applied; 200 ml real urine over 100 cm2 per patch; triplicate patches per chamber.
- All treatments applied on 24/07/2017 (dd/mm/yy).

## Experimental design and monitoring period
- Randomised block design.
- Emissions monitored for 177 days following treatment application.
- Data include both high-frequency automated measurements and subsequent manual monthly measurements.

## Measurements and instrumentation
- High-frequency data: automated greenhouse gas monitoring system (QUT) with a SRI 8610 GC.
  - Eight flux measurements per chamber per day.
  - 1-hour chamber closure period; four gas samples analyzed per closure.
  - Calibration standard analyzed after every fourth gas sample.
- Chamber specifications: basal area 0.25 m2; chambers 50 cm × 50 cm × 15 cm (L × W × H).
- Manual data: monthly gas flux measurements from the same chambers.
  - Analysed with Perkin Elmer 580 Gas Chromatograph and Turbo Matrix 110 autosampler.
  - Calibrated with four gas standards spanning measured concentration ranges.

## Data content and structure
- Data represent quality-assessed N2O flux data, not raw gas concentrations.
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time relative to treatment (pre- or post-treatment)
  - Columns B–M: N2O fluxes (µg N2O-N m-2 h-1)
- Column headers indicate treatment and chamber/plot identifiers:
  - Control = Control treatment
  - ArtUrine = artificial urine treatment
  - Urine = real urine treatment

## Quality assurance and data processing
- QA steps include inspecting raw data files and GC chromatograms for anomalies; affected data removed as necessary (e.g., chromatographic interferences).
- The dataset provides processed, quality-assessed flux values rather than raw concentration data.

## Data usage and attribution
- Authors must be acknowledged if data are reused or reproduced.

## Metadata and provenance
- Site location and altitude provided; exact coordinates given.
- Documentation includes treatment application dates, measurement cadence, and instrumentation specifics.
- Data managed with clear metadata about units (µg N2O-N m-2 h-1) and measurement methods to support reuse and interoperability.
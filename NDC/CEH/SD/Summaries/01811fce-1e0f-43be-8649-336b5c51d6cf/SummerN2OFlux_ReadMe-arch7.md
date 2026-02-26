# ReadMe file for SummerN2OFlux.csv

- This ReadMe documents a dataset of N2O flux measurements from control, artificial urine, and real sheep urine patches applied to soil in Snowdonia, UK. Emissions were monitored over 177 days after treatment using high-frequency automated measurements and later monthly manual measurements. Data are quality-assessed flux values (not raw concentrations). Authors should be acknowledged if data are reused.

## Study site and location
- Location: unimproved grazing land on a dystric histosol in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Exclusion period: sheep excluded from plots from 15/05/2017 to prevent recent excretal events confounding data.

## Treatments and experimental design
- Treatments (n = 4 described): Control (no urine), Artificial sheep urine, Real sheep urine. Note: description lists three treatment types; patches were applied in triplicate under each treatment.
- Patch design: discrete patches within each chamber; each patch corresponds to an N application rate of:
  - Artificial urine: 920 kg N ha-1, 200 ml urine over 100 cm2 soil surface per patch.
  - Real urine: 930 kg N ha-1, 200 ml urine over 100 cm2 soil surface per patch.
- Application date: 24/07/2017.
- Experimental setup: randomised block design with multiple chambers/plots.

## Data collection and instruments
- High-frequency data:
  - Instrument: automated greenhouse gas monitoring system (Queensland University of Technology) with a SRI 8610 GC (Torrance, USA).
  - Measurements: eight N2O flux measurements per chamber per day (1 hour chamber closure; four gas samples per closure; calibration after every fourth sample).
  - Chamber size: 0.25 m2 base area; chamber dimensions 50 cm x 50 cm x 15 cm.
- Post-high-frequency data:
  - Manual measurements: monthly flux measurements from the same chambers.
  - Instrument: Perkin Elmer 580 Gas Chromatograph with Turbo Matrix 110 auto sampler.
  - Calibration: four gas standards spanning measured concentration ranges (BOC gases, Liverpool).
- Data scope: includes quality-assessed flux data (not raw gas concentrations).

## Data structure and headers
- Timestamp: dd/mm/yy hh:mm.
- Days: days pre- or post-treatment application.
- Flux columns: Columns B–M represent N2O fluxes in µg N2O-N m-2 h-1.
- Treatment/plot identifiers: Column headers indicate treatment (Control, ArtUrine for artificial urine, Urine for real urine) and chamber/plot numbers.

## Quality assurance and data cleaning
- QA procedures: inspection of raw data files and GC chromatograms for anomalies; data removed if necessary (e.g., interference in gas peaks).

## Data usage, attribution, and provenance
- Usage note: Authors must be acknowledged if data are reused or reproduced.
- Data provenance: flux data derived from high-frequency automated measurements and subsequent manual measurements; data represent quality-assessed flux values rather than raw gas concentrations.

## Notes for GIS integration
- Spatial context: treatments applied as patches within chambers in a randomized block design; suitable for spatial mapping of N2O flux variation across treatments and plots.
- Geographic metadata: precise site location, elevation, and the relationship between patch treatments and chamber locations facilitate GIS-based analyses and visualization.
- Temporal context: explicit timing of treatments and measurement cadence supports time-series GIS analyses and Collaboration with other spatial datasets.
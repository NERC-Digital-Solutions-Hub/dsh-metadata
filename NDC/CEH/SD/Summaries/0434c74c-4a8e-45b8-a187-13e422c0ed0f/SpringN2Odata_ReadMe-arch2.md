# ReadMe file for SpringN2OData.csv

- Purpose
  - Document the N2O emissions dataset collected from control (no urine), artificial urine, and real urine treatments applied to an orthic podzol in semi-improved upland grassland, Henfaes Research Station, North Wales (spring 2016).
  - Data collected under a randomised block experimental design; includes high-frequency automated measurements and subsequent monthly manual measurements.

- Location and context
  - Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
  - Plot emissions monitored from randomized block plots during spring 2016.

- Experimental design and treatments
  - Randomised block design.
  - Treatments: Control (no urine), ArtUrine (artificial urine), Urine (real urine).

- Data collection methods and instruments
  - Automated high-frequency system:
    - Eight flux measurements per chamber per day; 1 h chamber closure; four gas samples analysed per closure.
    - Calibration standard analysed after every fourth sample.
    - Gas measurement system: SRI 8610 GC (Torrance, USA).
  - Chamber details (high-frequency measurements):
    - Base area: 0.25 m2; dimensions 50 cm x 50 cm x 15 cm (l x w x h).
  - Manual measurements (lower frequency, post-initial period):
    - Smaller chambers: 40 cm x 20 cm x 20 cm (l x w x h).
    - Gas analysis: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler (Perkin Elmer Inc, USA).
    - Calibration: four gas standards spanning measured concentration ranges (BOC gases, Liverpool).

- Data content and quality
  - Data represent quality-assessed fluxes, not raw gas concentrations.
  - Quality assurance: inspection of raw data files and GC chromatograms; anomalies removed as needed (e.g., gas peak interference).
  - Handling of detection limits: fluxes below detection limit replaced with zero in manual data.

- Data structure and headers
  - Timestamp format: dd/mm/yy hh:mm.
  - Flux columns: B to M (N2O fluxes, in micrograms N2O-N m-2 h-1).
  - Treatment/plot information embedded in column headers, e.g., Control, ArtUrine, Urine.

- Data usage notes
  - Authors must be acknowledged if data are reused or reproduced.
  - The dataset includes both high-frequency automated data and lower-frequency manual data; the structure reflects both data streams.
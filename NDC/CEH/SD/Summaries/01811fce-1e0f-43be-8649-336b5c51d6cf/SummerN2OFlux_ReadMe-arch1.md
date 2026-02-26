# ReadMe file for SummerN2OFlux.csv

- Purpose: Document the SummerN2OFlux.csv dataset, which records N2O fluxes from control (no urine), artificial sheep urine, and real sheep urine patches applied to a dystric histosol in grazing land within Snowdonia National Park, Wales.

- Study site and conditions:
  - Location: Carneddau mountains, Snowdonia National Park, Wales, UK
  - Elevation: 556 m above sea level
  - Coordinates: 53°22'N, 3°95'W
  - Environment: unimproved grazing land; dystric histosol
  - Timeline context: Sheep excluded from plots from 15/05/17 to avoid confounding excretal events

- Treatments and replication:
  - Treatments (n = 4 per treatment): 
    - Control: no urine application
    - Artificial urine patches: three replicate patches inside the chamber per treatment
    - Real urine patches: three replicate patches inside the chamber per treatment
  - N application rate per patch: artificial ~920 kg N ha-1; real ~930 kg N ha-1
  - Patch details: 200 ml urine applied over 100 cm2 soil surface per patch

- Experimental design:
  - Design type: randomized block
  - Measurement period: emissions monitored for 177 days following treatment
  - Chamber details: basal area 0.25 m2; chambers 50 cm x 50 cm x 15 cm

- Measurements and instrumentation:
  - Automated high-frequency measurements (post-treatment period):
    - Instrument: automated greenhouse gas monitoring system (QUT) with SRI 8610 GC
    - Sampling cadence: 8 flux measurements per chamber per day
    - Chamber closure: 1 hour
    - Gas samples per closure: 4 samples
    - Calibration: standard analyzed after every fourth sample
  - Manual measurements (after high-frequency period):
    - Instrument: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler
    - Calibration: four gas standards spanning measurement range (BOC gases)
  - Data scope: quality-assessed flux data (not raw gas concentration data)

- Data structure and content:
  - Timestamp format: dd/mm/yy hh:mm
  - Days column: time relative to treatment (pre- or post-treatment)
  - Flux data columns: columns B to M, representing N2O fluxes (µg N2O-N m-2 h-1)
  - Column labeling: reflect treatment and chamber/plot numbers
  - Treatment labels: Control (no urine), ArtUrine (artificial urine), Urine (real urine)

- Quality assurance and data processing:
  - QA steps: inspection of raw data files and GC chromatograms for anomalies; removal of anomalous data as needed
  - Data scope: flux data deemed quality-assured; not raw concentration data
  - Data provenance: high-frequency automated data complemented by later monthly manual measurements from the same chambers

- Usage notes and attribution:
  - Data provenance: authors should be acknowledged if data are reused or reproduced
  - Intended use: enables analysis of how urine patches (artificial vs. real) influence N2O emissions over time, comparisons with controls, and potential development of predictive models and correlations
  - Data format considerations: units are µg N2O-N m-2 h-1; timestamps and days relative to treatment are provided for temporal analyses

- Relevance for data analysts:
  - Suitable for exploring treatment effects, time-series patterns, and cross-method consistency (automated vs. manual measurements)
  - Supports analysis at plot/patch level within a randomized block framework
  - Highlights common data challenges such as ensuring data quality across high-frequency and low-frequency measurements and aligning patch-level treatments with chamber-level observations
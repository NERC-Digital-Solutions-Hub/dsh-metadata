# ReadMe file for SummerCH4Flux.csv

- Purpose: Documentation for a CH4 flux dataset collected after applying different urine treatments to soil in a field experiment; intended to support analysis of how artificial vs real sheep urine affects methane emissions.

- Location and site details:
  - Area: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK
  - Elevation: 556 m above sea level
  - Coordinates: 53°22'N, 3°95'W
  - Soil: dystric histosol
  - Sheep management: sheep excluded from plots from 15/05/17 to avoid recent excretal effects

- Treatments and experimental design:
  - Treatments (n = 4): Control (no urine), Artificial sheep urine, Real sheep urine
  - Application specifics:
    - Artificial urine: 920 kg N ha-1 per patch; 200 ml applied over 100 cm2 per patch; applied in triplicate discrete patches inside each chamber
    - Real urine: 930 kg N ha-1 per patch; 200 ml applied over 100 cm2 per patch; applied in triplicate discrete patches inside each chamber
  - Applied on: 24/07/17
  - Design: randomized block experimental design

- Data collection and monitoring:
  - Monitoring period: 80 days after treatment application
  - Instrumentation: automated greenhouse gas monitoring system with a SRI 8610 GC
  - Measurements: eight CH4 flux measurements per chamber per day
  - Chamber details: basal area 0.25 m2; chamber dimensions 50 cm x 50 cm x 15 cm (l x w x h)
  - Sampling: 1-hour chamber closure; 4 gas samples per closure period
  - Calibration: standard analyzed after every fourth gas sample
  - Data scope: emissions data from the high-frequency automated system only; not raw gas concentration data

- Data structure and variables:
  - Data includes a time series with the following headers:
    - Timestamp: dd/mm/yy hh:mm
    - Days: time relative to treatment (pre- or post-treatment)
    - Columns B–M: CH4 fluxes in µg CH4-C m-2 h-1
  - Treatment identifiers in headers: Control, ArtUrine (artificial urine), Urine (real urine)
  - Plot/chamber identifiers: included in headers to distinguish measurements

- Data quality and processing:
  - Quality assurance: inspection of raw data files and GC chromatograms for anomalies; anomalies removed if necessary (e.g., peak interference)
  - Data notes: data reflect quality-assessed flux measurements; not raw concentration data

- Metadata and usage considerations:
  - Publication and reuse: Authors must be acknowledged if data are reused or reproduced
  - Data accessibility: headers and metadata describe treatments, chamber/plot details, and timing to support analyses across patches and treatments
  - Scale and applicability: site-specific field measurements; potential extrapolation should consider local soil, vegetation, and management conditions

- Relevance for analysis:
  - Enables comparison of CH4 flux responses to artificial vs real urine versus control
  - Allows examination of short- to medium-term emission dynamics over 80 days post-application
  - Facilitates exploration of treatment effects across replicated patches within a controlled field setting
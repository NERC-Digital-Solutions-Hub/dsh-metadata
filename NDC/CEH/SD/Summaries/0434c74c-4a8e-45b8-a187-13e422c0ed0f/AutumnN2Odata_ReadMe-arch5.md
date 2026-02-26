# N2O emissions measured from control (no urine) artificial and real sheep urine applied to an orthic podzol within a semiimproved upland grassland at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) in autumn, 2016.

## Overview
- Study context: N2O emissions from different urine treatments (control, artificial urine, real sheep urine) on an orthic podzol in semi-improved upland grassland.
- Experimental design: randomised block design conducted at Henfaes Research Station, North Wales, during autumn 2016.
- Data aim: provide quality-assessed flux measurements suitable for reuse, with appropriate acknowledgement.

## Data collection and instrumentation
- Automated high-frequency measurements:
  - System: automated greenhouse gas monitoring (facility associated with Queensland University of Technology) using a SRI 8610 GC.
  - Frequency: eight flux measurements per chamber per day (1-hour chamber closure, four gas samples per closure).
  - Calibration: calibration standard analyzed after every fourth gas sample.
- Chamber specifications (high-frequency data):
  - Basal area: 0.25 m².
  - Dimensions: 50 cm × 50 cm × 15 cm (L × W × H).
- Manual measurements (monthly flux data):
  - Chambers: smaller chambers, 40 cm × 20 cm × 20 cm.
  - Analysis: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler.
  - Calibration: four gas standards spanning measured concentration ranges.
- Data scope:
  - The dataset includes high-frequency automated flux data and later monthly flux measurements from manual sampling.

## Data content and structure
- Data type: flux data for N2O (not raw gas concentrations).
- Units: micrograms N2O-N m^-2 h^-1.
- Time format: Date_Time header in dd/mm/yy hh:mm.
- Data columns:
  - Columns B to M contain N2O fluxes.
  - Headers encode treatment and chamber/plot identifiers.
  - Treatments labeled: Control (no urine), ArtUrine (artificial urine), Urine (real urine).

## Quality assurance and data processing
- QA procedures:
  - Inspection of raw data files and GC chromatograms to identify anomalies.
  - Anomalies removed as needed (e.g., peak interferences).
- Handling of detection limits:
  - Fluxes below detection limit from manual data replaced with zero.
- Data quality note:
  - The dataset represents quality-assessed flux data, not the raw gas concentration data.

## Metadata and data governance
- Data provenance:
  - Authors must be acknowledged if the data are re-used or reproduced.
- Documentation provided:
  - Explicit description of measurement methods, equipment, chamber sizes, data structure, and units to support proper interpretation and reuse.
- Site and temporal context:
  - Location: Henfaes Research Station, Abergwyngregyn, North Wales.
  - Elevation and coordinates provided.
  - Autumn 2016 timeline for the measurements.

## Practical considerations for data stewards
- Standards alignment:
  - Clear metadata on treatments, chamber configurations, and timing facilitates interoperability across systems and formats.
- Data maintenance:
  - Distinction between high-frequency automated data and monthly manual data should be preserved in the dataset structure.
  - Documentation of QA steps aids reproducibility and trust in the data.
- Usage considerations:
  - Ensure proper attribution to authors when re-using the data.
  - Be aware that data include processed flux values, not raw concentration data, which may affect re-analysis approaches.
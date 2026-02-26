# ReadMe file for SpringN2OData.csv

- Overview
  - Dataset of N2O emissions measured from three treatments: Control (no urine), artificial sheep urine (ArtUrine), and real urine (Urine) applied to an orthic podzol in semi-improved upland grassland, Henfaes Research Station, North Wales (270 m a.s.l.; 53°13'N, 4°0'W) during spring 2016.
  - Experimental design: randomised block.
  - Data collected to support analysis of urine application on N2O fluxes.

- Data collection and measurement methods
  - Automated greenhouse gas monitoring system (QUT) with a SRI 8610 GC; eight flux measurements per chamber per day (1-hour chamber closure; four gas samples per closure).
  - Calibration standard analyzed after every fourth gas sample.
  - Chamber basal area: 0.25 m2; chambers sized 50 cm x 50 cm x 15 cm (L x W x H).
  - After the automated period, monthly flux measurements were taken manually from smaller chambers (40 cm x 20 cm x 20 cm; L x W x H).
  - Manual samples analyzed with PerkinElmer 580 GC with Turbo Matrix 110 autosampler; four gas standards (BOC gases).
  - Data provided are quality-assessed flux data, not raw gas concentration data.

- Location details
  - Henfaes Research Station, Abergwyngregyn, North Wales.
  - Geographical coordinates and altitude as above.
  - Randomised block experimental design.

- Data structure and contents
  - Timestamp format: dd/mm/yy hh:mm.
  - Flux data columns B to M: N2O fluxes measured as micrograms N2O-N per m2 per hour (µg N2O-N m-2 h-1).
  - Column headers encode treatment and chamber/plot identifiers:
    - Treatments: Control, ArtUrine (artificial urine), Urine (real urine).
    - Chambers/plots linked to the respective treatments.

- Quality assurance and data processing
  - Raw data files and GC chromatograms inspected for anomalies; anomalies removed as needed.
  - Flux values below detection limit replaced with zero (based on manual data).
  - Emphasizes that data reflect processed flux values rather than raw concentrations.

- Data usage guidance
  - Note the combination of high-frequency automated data with later, lower-frequency manual measurements; structure in the dataset will reflect both data streams.
  - Suitable for analyses comparing N2O flux responses to urine treatments over time, and for creating data products (e.g., dashboards or time-series views) to support exploration of treatment effects.

- Attribution
  - Authors must be acknowledged if the data are reused or reproduced.
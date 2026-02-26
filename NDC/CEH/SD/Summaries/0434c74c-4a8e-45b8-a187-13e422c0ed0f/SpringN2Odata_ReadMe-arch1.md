# ReadMe file for SpringN2OData.csv

- This dataset records N2O emissions from a controlled experiment assessing the effects of no urine (Control), artificial sheep urine (ArtUrine), and real sheep urine (Urine) applied to an orthic podzol within a semi-improved upland grassland at Henfaes Research Station, North Wales.
- Location details: 270 m above sea level; coordinates 53°13'N, 4°0'W; spring, 2016; randomised block experimental design.

- Data collection and instrumentation
  - Automated greenhouse gas monitoring system (QUT) with a SRI 8610 GC.
  - Eight flux measurements per chamber per day (1-hour closure; 4 gas samples per closure).
  - Calibration after every fourth gas sample.
  - Chamber dimensions and area: 50 cm x 50 cm x 15 cm; base area 0.25 m2.
  - Two data collection regimes: high-frequency (automated) data and monthly manual flux measurements from smaller chambers (40 cm x 20 cm x 20 cm).

- Manual gas sampling and analysis
  - Manual samples analyzed with a Perkin Elmer 580 GC and Turbo Matrix 110 auto sampler.
  - Calibration with four gas standards spanning measured concentrations (BOC gases, Liverpool).
  - Manual data represent quality-assessed fluxes, not raw gas concentrations.

- Data quality and processing
  - Quality assurance includes inspecting raw data files and GC chromatograms for anomalies; questionable data removed as needed (e.g., gas peak interference).
  - Fluxes below detection limit were replaced with zero using manually sampled data.
  - Data headers indicate treatment, chamber/plot numbers; treatments labeled as Control, ArtUrine, Urine.

- Data structure and contents
  - Timestamp format: dd/mm/yy hh:mm.
  - Columns B to M contain N2O flux measurements (in micrograms N2O-N m-2 h-1).
  - The dataset includes both high-frequency flux data and the manually-measured flux data, with the respective chamber sizes and setups clearly indicated in the headers.
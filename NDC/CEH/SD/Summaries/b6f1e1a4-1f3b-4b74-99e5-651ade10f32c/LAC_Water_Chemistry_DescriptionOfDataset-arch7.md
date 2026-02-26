# LAC water chemistry_dataset.csv

- Overview
  - A CSV dataset of lake water chemistry analyses collected from the upper 1 m of the water column at the deepest point of each lake.
  - Regions include Norway, Greenland, Russia (ice-covered periods) and Alaska (ice-free periods); one sample per lake.

- Dataset context and purpose for GIS use
  - Created by Erika Whiteford, Loughborough University.
  - Designed to support map-based data visualisations of lake chemistry for analysis and communication to policy colleagues, clients, and the public.
  - Suitable for spatial comparisons of nutrient and related chemistry across lakes when joined to lake polygons or point locations.

- Sampling design and collection methods
  - Sampling target: upper 1 m of the water column at the deepest point of each lake.
  - Timing: during ice cover (Norway, Greenland, Russia) or ice-free periods (Alaska).
  - Field processing: selective filtration for most analytes; unfiltered water used for TP, TN, and total alkalinity.
  - Preservation and transport: samples kept cold, dark, typically analyzed within 8 hours (field to lab); some analyses preserved with H2SO4 and measured later.
  - Laboratory analyses followed established standard methods (references provided).

- Variables, units, and data structure
  - Key chemistry variables (with units):
    - TP, SRP, TN, NO3-N, NH4-N, Chlorophyll a: µg/L
    - SiO2, Sodium, Magnesium, Potassium, Calcium, Chloride, Sulphate: mg/L
    - DOC: ppm
    - Total Alkalinity: meq/L
  - Additional fields:
    - Region (country/area), Lake code (lake identifier), Date of collection (DD/MM/YY)
    - Abbreviations/terminology included for clarity (e.g., TP, SRP, NO3-N, NH4-N, Chl a)
    - BDL markers indicate below detectable level
  - Data structure is tabular with a single row per lake/lake sample.

- Data quality control and calibration
  - Calibration steps included checks for machine drift and standard curve validity.
  - Absorbance readings checked against the standard curve; standard curves adjusted if necessary.
  - Measurements checked for detection limits and cross-validated with previous lake data from the same locations.
  - Concentrations calculated using validated equations and quality checks to minimize errors.

- Data format and metadata
  - Stored as a .csv file.
  - Field definitions include region, lake code, date of collection, and concentration values for each parameter.
  - References for methods included (classic limnology and spectrophotometric methods) to support reproducibility.

- Geographic and temporal scope for GIS work
  - Spatial scope: lakes across Norway, Greenland, Russia, and Alaska; exact coordinates not provided in the metadata and would require joining to an external lake shapefile or point dataset using Region and Lake code.
  - Temporal scope: each lake has a single collection date; no explicit multi-year time series within this dataset.

- Potential GIS applications
  - Create lake-level chemistry maps (e.g., TP, TN, SRP, chlorophyll a) by joining to spatial lake data.
  - Multivariate choropleth or symbol maps showing nutrient status or pigment concentrations across lakes.
  - Temporal analyses if combined with other years or datasets (note: this dataset itself is a single sampling event per lake).
  - Data cleaning and harmonisation workflow to manage below-detection values (BDL) and unit consistency for mapping.
  - Quality assurance workflows comparing current values to historical lake data at the same sites.

- Limitations and considerations for mapping
  - Spatial coordinates are not included; requires join to external geospatial layers.
  - Only one sample per lake; limited ability to assess temporal trends without additional data.
  - Data spanning multiple regions with potential differences in collection timing and standards; ensure consistent unit handling and BDL treatment in GIS analyses.
  - Data standardisation and provenance rely on cited methods; ensure any integration with other datasets maintains traceability.

- References (methods and context)
  - Golterman et al. 1978; Jeffrey and Humphrey 1975; Koroleff 1983; Leavitt and Hodgson 2001; Mackereth et al. 1989; Qualls 1989; plus related methodological notes on spectrophotometric analyses and sample preservation.
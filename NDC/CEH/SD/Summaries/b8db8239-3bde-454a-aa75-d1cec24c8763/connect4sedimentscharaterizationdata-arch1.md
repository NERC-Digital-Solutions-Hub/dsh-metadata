# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

- The dataset compiles sedimentological and geochemical analyses from sediment cores collected across four countries (Botswana, South Africa, Zimbabwe, and Mozambique) as part of the Connect4 project.
- Overall structure: multiple country-specific folders containing numerous cores (Botswana: 7 cores; South Africa: 10 cores; Zimbabwe: 10 cores; Mozambique: 10 cores), each with standardized data on grain size, organic matter, and trace metal concentrations.
- Common analytical methods across cores: particle size distribution (Mastersizer 3000), organic matter content via Loss on Ignition (LOI), and geochemical analyses (ICP-OES or ICP-MS; XRF used in some Mozambican cores).
- Standard units across datasets: grain size in micrometres, organic matter in percent, trace elements in parts per million (ppm). Some datasets include additional statistics (averages, standard deviations, relative standard deviations, and replicates).
- Data structure: core-level files describe depth (cm), LOI calculations, organic matter, grain size distribution, and geochemical results. Several cores include raw data, some include only processed data, and a few have partial or missing sections of data (e.g., missing Fe data or incomplete grain-size records).
- Quality control notes: datasets include notes on potential measurement errors, large standard deviations, and detections below detection limits (negative values in some CSV entries); caution advised in interpretation, particularly for data points near detection limits.
- Data accessibility and metadata: cores are documented with collection sites, coordinates, depths, and sampling details; data structures specify column mappings (e.g., depth, LOI, organic matter, grain-size columns, and geochemical data by element).

Region-specific highlights

- Botswana
  - Cores: GC1 (146 cm), GC2 (81 cm), L11 (58 cm), S5 (33 cm), S6 (92 cm), S7 (113 cm), S8 (84 cm).
  - Analyses: most cores include grain size and organic matter; geochemical data present for several cores (notably S8 with extensive multi-element data); some cores lack full geochemical analyses.
  - Methods: Mastersizer 3000 for grain size, LOI, ICP-OES/MS for trace elements.

- South Africa
  - Cores: H1, H2, H3, H5 (Houtrivier); M4, M7, M8 (Mutshhedzi); N4, N5, N7 (Nwanedi); Z-related entries referenced in structure.
  - Analyses: ranging from LOI and grain size to full geochemical suites in several cores; several cores include arsenic, chromium, copper, iron, manganese, nickel, lead, zinc, with statistical summaries (averages, standard deviations, replicates) where available.
  - Notes: some cores have no geochemical data; others provide detailed distributions and replicates.

- Zimbabwe
  - Cores: Ripple Creek B1 (48 cm), B3 (12 cm), B5 (9 cm), B6 (12 cm); Zhovhe Z1 (13 cm), Z2 (25 cm), Z3 (75 cm), Z5 (19 cm), Z6 (24 cm); Ripple Creek B1 and Zhovhe cores include full geochemical data in several instances.
  - Analyses: combination of LOI, grain size, and multi-element geochemistry; some cores provide raw data for geochemical results; others limit to processed data.
  - Methods: Mastersizer 3000, LOI, ICP-OES/MS for trace elements; some datasets include replicates and summary statistics.

- Mozambique
  - Cores: MA1 (67 cm), MA2 (26 cm), MA3 (26 cm), MA4 (38 cm), MA5 (49 cm), MA5B (37 cm), MA7 (23 cm), MA10 (57 cm), OX1 (34 cm), OX2 (35 cm).
  - Analyses: most cores feature grain size and LOI; several cores include XRF data (MA10) or XRF-related raw data (MA10, MA5B); some cores lack geochemical analyses.
  - Methods: Mastersizer 3000, LOI, ICP-OES; XRF included in select cores.
  - Data notes: some missing data points (e.g., certain depth intervals not measured) and cleaning notes for MA5B (cleaned grain size data).

Key considerations for analysts

- Cross-country comparability: while units are harmonized (micrometres, % LOI, ppm metals), there are gaps in geochemical data for some cores and some datasets with partial measurements.
- Local-scale interpretation: cores vary in depth coverage and data completeness, which may affect regional comparisons or trend analyses at fine spatial scales.
- Data quality and uncertainties: presence of negative values (due to detection limits), large standard deviations, and missing raw data in several cores require careful QA/QC and possibly imputation or exclusion of uncertain points for certain analyses.
- Metadata and reproducibility: detailed core descriptions, coordinates, and sampling methods are provided, supporting reproducibility and dataset provenance; however, some tables include incomplete fields that may require verification from source files.

Potential uses

- Correlate grain size and organic matter with heavy metal concentrations to assess sediment deposition patterns and contaminant associations.
- Compare regional sediment characteristics (e.g., LOI vs. metal content) to infer geochemical weathering processes and dam sedimentation histories.
- Build regional or country-scale predictive models by integrating comparable cores and standardizing variables across datasets.
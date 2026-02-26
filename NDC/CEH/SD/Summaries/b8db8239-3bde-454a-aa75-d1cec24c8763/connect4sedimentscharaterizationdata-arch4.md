# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

## Overview
- Compilation of sedimentological and geochemical analyses across southern Africa (Botswana, South Africa, Zimbabwe, Mozambique).
- Botswana: 7 files covering 7 cores from dams; core identifiers include GC1, GC2, L11, S5, S6, S7, S8.
- South Africa: 10 files covering 10 cores (H1, H2, H3, H5, M4, M7, M8, N4, N5, N7).
- Zimbabwe: 10 files covering 10 cores (B1, B3, B5, B6, Z1–Z6).
- Mozambique: 10 files covering 10 cores (MA1–MA10, OX1–OX2).
- Data describe sediment particle size, organic matter content, and metal concentrations (various elements in ppm).

## Core Data and Analyses
- Sampling and cores
  - Cores collected by push corer from shore or small boat; 50 mm PVC cores; stored at 4 °C.
  - Cores split, photographed, sub-sampled for grain size and geochemical analysis.
  - Analyses typically include particle size distribution, organic matter content (LOI), and heavy metals (Cr, Fe, Ni, Cu, Zn, Pb); some cores include additional geochemical data or raw data.
- Core-specific content highlights
  - Botswana
    - GC1 and GC2: depth 146 cm and 81 cm; LOI and grain size; no geochemical analysis for GC1/GC2.
    - L11 (58 cm) and S5/S6/S7/S8: include LOI, grain size; S8 includes extensive geochemical data (As, Cr, Cu, Fe, Mn, Ni, Pb, Zn) and statistics.
  - South Africa
    - H1 (51 cm), H2 (50 cm), H3 (70 cm), H5 (78 cm): LOI and grain size; H2/H3/H5 include geochemical data (As, Cr, Cu, Mn, Ni, Pb, Zn; some Fe data absent in H3).
    - M4 (33 cm), M7 (58 cm), M8 (33 cm): LOI and grain size; M7/M8 include geochemical data; some rows show average/standard deviation and replicates.
    - N4 (40 cm), N5 (60 cm), N7 (27 cm): LOI, grain size; N5/N7 include raw geochemical data; detailed statistics for some elements.
  - Zimbabwe
    - Ripple Creek cores (B1, B3, B5, B6) and Z1–Z6: LOI and grain size; several with geochemical data (ppm) for multiple elements; some with full raw data or averages/replicates.
    - Structures vary by core; some files include detailed column layouts for LOI, grain size, and multiple geochemical columns.
  - Mozambique
    - MA1–MA10, OX1–OX2: mix of LOI/grain size data; several cores lack geochemical analyses; MA10 includes XRF data; some cores have missing depth ranges or missing data segments.
    - MA5B and MA5 variants show cleaned grain size data; MA7, MA1–MA4 show varying completeness.
    - OX1/OX2 include core description, LOI, grain size; no geochemical data in these cores.
- Data structure and metadata
  - Detailed core-level data structures described (often Columns A–L, with LOI calculations, organic matter, grain size, and then geochemical data columns).
  - Some cores provide:
    - Depth of samples (Column A)
    - LOI calculations (Columns B–H or equivalent)
    - Organic matter (%)
    - Grain size distributions (micrometres)
    - Geochemical data (ppm) for multiple elements, including averages, standard deviations, replicates, and in some cases raw data.
  - Zimbabwe and Mozambique datasets sometimes separate raw data from summarized statistics; several files note missing data segments or incomplete records.

## Data Quality, Gaps, and Notes
- Quality control
  - Most datasets note basic quality checks (identifying measurement errors and detection-limit issues); many entries mark quality control as N/A.
  - Occasional notes on large standard deviations or concentrations below detection limits.
- Data completeness
  - Several cores have missing geochemical data or incomplete grain size data (e.g., missing 12–13 cm intervals in MA10; some Mozambican cores lacking geochemical analyses).
  - Some cores provide extensive geochemical statistics (averages, SD, RSD, replicates), while others contain only LOI and grain size data.
- Metadata and discoverability
  - Location coordinates, collection dates, and core lengths are provided variably; some entries include precise lat/long, others provide approximate or missing values.
  - Cross-country consistency varies in core naming conventions and data column labeling, which may impact data discovery and integration.

## Implications for Data Leaders
- Data strategy and governance
  - There is a broad, multi-country dataset combining sedimentology and geochemistry with varying levels of completeness. Needs harmonization for cross-site comparability.
  - Key governance tasks: standardize core naming, unify column schemas, and ensure consistent metadata (depth, LOI method, grain size method, units, geochemical elements, detection limits).
- Data availability and accessibility
  - High-value data include LOI, grain size distributions, and multi-element geochemistry with replicates and statistics (not always consistently available across cores).
  - Address gaps by prioritizing data completion for cores with missing geochemical data or missing intervals.
- Usability and impact
  - The dataset supports cross-country analyses of sediment characteristics and contaminant burdens in dam sediments, useful for policy, environmental monitoring, and water-resource management.
  - Encourages co-ownership and collaboration across networks to improve data discovery, standards, and dissemination practices.

## Recommended Actions
- Harmonize data schema across all cores (standardize columns for depth, LOI, organic matter, grain size, and geochemical data, plus metadata fields).
- Develop a metadata catalogue with consistent coordinates, collection dates, core length, and methods (instruments and units) to improve discoverability.
- Create a data quality plan detailing detection limits, QA checks, and handling of missing data.
- Prioritize ingestion of missing geochemical data where feasible and clearly flag records with gaps or raw-data status.
- Establish cross-country data-sharing practices and communities of practice to align standards and improve reusability.
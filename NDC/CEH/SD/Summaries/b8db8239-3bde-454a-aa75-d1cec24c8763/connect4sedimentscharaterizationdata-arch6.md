# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

## Overview
- Datasets comprising sedimentological and geochemical analyses from sediment cores collected in four countries: Botswana, South Africa, Zimbabwe, and Mozambique.
- Each country folder contains multiple core files (total varies by country) with data on core depth, grain size distribution, organic matter content, and trace element concentrations (e.g., Cr, Fe, Ni, Cu, Zn, Pb; arsenic, manganese, nickel, chromium, iron, etc.).
- Sampling method: push corer with 50 mm PVC tubes from shore or small boat; cores stored at 4 °C, split, photographed, sub-sampled for grain size and geochemical analysis.
- Analytical methods referenced: Mastersizer 3000 (grain size), Loss on Ignition (organic matter), ICP-OES/MS/XRF for geochemistry.
- Data formats: raw data, processed LOI, organic matter, grain size, and geochemical results; some datasets include averages, standard deviations, and replicates; some cores lack certain analyses (e.g., no geochemical data for some cores).
- Quality notes: some datasets note missing values, detection-limit issues, and occasional negative values in CSVs to indicate below-detection results.

## Data contents by country

### Botswana
- Core count: 7 files (GC1, GC2, L11, S5, S6, S7, S8).
- Core specifics:
  - GC1: depth 146 cm; grain size, LOI, and organic matter analyzed; no geochemical data.
  - GC2: depth 81 cm; similar structure to GC1; no geochemical data.
  - L11: depth 58 cm; LOI, organic matter, grain size; geochemical data present.
  - S5: depth 33 cm; LOI and grain size; geochemical data present.
  - S6, S7: depths ~92 cm and ~113 cm; LOI, organic matter, grain size; some cores include raw data or replicates.
  - S8: depth 84 cm; comprehensive with LOI, organic matter, grain size, and multi-element geochemical results (Arsenic, Chromium, Copper, Iron, Manganese, Nickel, Lead, Zinc; with averages, SDs, and replicates).
- Data structure notes: core-specific column layouts; depths, LOI-derived calculations, and element-specific columns vary by core.

### South Africa
- Core count: 10 files (H1–H3, H5, M4, M7, M8, N4, N5, N7, etc.).
- Core specifics:
  - H1: depth 51 cm; LOI, organic matter, grain size; no geochemical data.
  - H2, H3: depths 50 cm and 70 cm; include LOI, OM, grain size, and extensive geochemical results (Arsenic, Chromium, Copper, Iron, Manganese, Nickel, Lead, Zinc) with regional structure variations.
  - H5, M4, M7, M8, N4, N5, N7: varying depths; mixture of LOI, organic matter, grain size, and geochemical data; several cores provide multi-element tables including averages and three-replicate data where applicable.
- Data structure notes: regionally consistent approach with per-core details; some files include detailed replicate and statistical summary columns for geochem data.

### Zimbabwe
- Core count: 10 files (B1–B6, Z1–Z6).
- Core specifics:
  - B1/B3/B5/B6 (Ripple Creek): depths 48 cm, 12 cm, 9 cm, 12 cm respectively; LOI, organic matter, grain size, and geochemical data (ppm) available in most cores.
  - Z1–Z6 (Zhovhe): depths 13 cm, 25 cm, 75 cm, 19 cm, 24 cm, etc.; data include LOI calculations, organic matter, grain size, and geochemical results; some cores with full raw data and replicates.
- Data structure notes: detailed per-core descriptions; variations exist in whether raw data or summarized statistics are provided for geochemical measurements.

### Mozambique
- Core count: 10 files (MA1–MA10, OX1, OX2).
- Core specifics:
  - MA cores: MA1 (67 cm) to MA10 (57 cm) with varying completeness; many show grain size and organic matter data, some with missing organic matter data (notably gaps in certain depth ranges); many lack geochemical data.
  - MA10 includes XRF data; other MA cores may lack geochemical analyses.
  - OX cores (OX1, OX2): 34 cm and 35 cm depths; described with core description, LOI, grain size, and trace elements; generally no geochemical data reported for these two cores.
- Data structure notes: emphasis on grain size and organic matter with occasional geochemical or XRF data; some cores have missing components (organic matter or geochemical data).

## Sampling techniques
- Common across all regions: push corer with extension rods; 50 mm diameter PVC tubes; samples stored at 4 °C; cores split, photographed, and sub-sampled for grain size and geochemical analyses.
- Analyzed properties: particle size distribution (grain size), organic matter content (LOI), and concentrations of heavy metals (Cr, Fe, Ni, Cu, Zn, Pb) with some datasets adding arsenic, chromium, manganese, nickel, and other elements; methods include Mastersizer 3000, Loss on Ignition, ICP-OES/MS, and XRF in select cores.

## Data structure and formats
- Core-specific data structures typically include:
  - Depth of sample (Column A or equivalent).
  - LOI calculations (Columns B–H or similar).
  - Organic matter percentage (Column I or corresponding).
  - Grain size distribution (Columns J–L or C–E; units micrometres).
  - Geochemical data (ppm) for various elements (structured in blocks per core; may include averages, standard deviations, and 3-replicate summaries in some cores).
  - Some cores provide raw data sections and detailed replicates (especially for multielement geochemistry).
- Variations exist by country and core, with some files lacking geochemical data or complete LOI/OM data.

## Quality control and caveats
- Botswana notes: potential large standard deviation values and values below detection limits; negative values in CSVs indicate measurements below detection limits.
- General caveats across datasets:
  - Missing data in several cores (no geochemical data or incomplete grain size/LOI data).
  - Some datasets include raw data, others include processed summaries or averages.
  - Formatting differences between cores and regional conventions may affect cross-core comparisons.

## How to use and potential data products
- Compare sediment properties across dams and regions:
  - Grain size distributions and organic matter content to assess sediment texture and organic-rich layers.
  - Geochemical signatures (trace metals) to identify contamination patterns or natural background levels.
- Build self-serve data products:
  - Core-level dashboards summarizing depth-wise changes in LOI, OM, grain size, and key element concentrations.
  - Tables and charts of average concentrations by core and region, with replication data where available.
- Data preparation needs:
  - Address missing values and units consistency across cores.
  - Interpret below-detection values appropriately (use detection limits where provided).
  - Harmonize depth references and column naming to enable cross-country comparisons.
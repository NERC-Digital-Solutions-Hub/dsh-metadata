# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

## Overview
- Datasets contain sedimentological and geochemical analyses of sediment cores from dams across Botswana, South Africa, Zimbabwe, and Mozambique.
- Botswana: 7 core files (GC1, GC2, L11, S5, S6, S7, S8).
- South Africa: 10 core files (H1, H2, H3, H5, M4, M7, M8, N4, N5, N7).
- Zimbabwe: 10 core files (B1, B3, B5, B6, Z1, Z2, Z3, Z5, Z6, plus others in table summaries).
- Mozambique: 10 core files (MA1–MA5, MA5B, MA7, MA10, OX1, OX2).
- Core data include depth, grain size distribution, organic matter content, loss on ignition (LOI), and various geochemical measurements (ppm for trace elements; some cores include raw data, averages, standard deviations, and replicates).
- Sampling: push corer from shore or small boat; cores stored at 4°C; split, photographed, and sub-sampled for grain size and geochemical analyses.
- Analytical methods mentioned: Mastersizer 3000 (grain size), Loss on Ignition (LOI), ICP-OES/ICP-MS/XRF for elemental concentrations.
- Data quality notes: acknowledgments of potential measurement errors, detection-limit issues, and occasional missing data; some CSVs show negative values for analyses below detection limits.

## Core-Level Data Structure and Metadata
- Common structure includes:
  - Depth of sample (cm) as a primary axis.
  - LOI calculations, organic matter percentages, and grain size distributions (in micrometres).
  - Geochemical data for multiple elements (ppm), with some datasets providing averages, standard deviations, relative standard deviations, and replicates.
  - Some cores provide raw data alongside summarized statistics; in others, only summarized or partial datasets are present.
- Country-specific detail highlights:
  - Botswana: Core GC1 and GC2 include LOI, organic matter, and grain size; GC1/GC2 show no geochemical data; other cores (e.g., S8) provide extensive geochemical results across multiple elements.
  - South Africa: H1–H3, H5, and others include both grain size/LOI and multi-element geochemical tables; some datasets include averages, standard deviations, and replicates for several elements.
  - Zimbabwe: Cores (e.g., B1, B3, Z1–Z6) mix LOI, organic matter, grain size, and geochemical results; data tables specify columns for elemental analyses and statistics where present.
  - Mozambique: MA cores contain grain size, LOI, and some have geochemical analyses or XRF data; MA10 additionally has XRF data; OX cores include core descriptions, LOI, grain size, and trace elements.
- Data documentation quality varies by core, with explicit method details and units typically listed, but with some missing sections (e.g., incomplete depth ranges or missing raw data) in a few cores.

## Sampling Techniques and Handling
- Uniform approach across regions: push corer with 50 mm PVC; from shore or small boat; cores stored at 4°C for water retention; halves photographed and sub-sampled.
- Samples analyzed for:
  - Particle size distribution (grain size) via Mastersizer 3000.
  - Organic matter content via LOI.
  - Trace metals via ICP-OES/ICP-MS or XRF (where available).
- Metadata captured typically includes:
  - Core ID, dam/collection site, depth, coordinates, date of collection, and length of core.
  - Collection method and units used for recorded measurements.

## Quality Control, Gaps, and Limitations
- Quality control statements present but vary by core; some datasets note no formal QC (N/A) while others flag potential human errors, laboratory instrument issues, or data points below detection limits.
- Data issues to be aware of:
  - Occasional missing data or incomplete depth ranges in certain cores.
  - Negative values in CSVs representing measurements below detection limits.
  - Some cores have no geochemical data; others provide only GR/LOI/organic matter data.
  - Some datasets include raw data, while others present only derived statistics (averages, standard deviations, replicates).
- These characteristics have implications for data harmonization, reproducibility, and cross-core comparisons.

## Regional Dataset Details (Key Points)
- Botswana
  - 7 cores (GC1, GC2, L11, S5, S6, S7, S8).
  - Mix of LOI, organic matter, grain size; geochemical data present for some cores (e.g., S8) across multiple elements.
  - Detailed per-core data structures describe depth, LOI, organic matter, grain size, and geochemical measurements with varying column mappings.
- South Africa
  - 10 cores (H1, H2, H3, H5, M4, M7, M8, N4, N5, N7).
  - Comprehensive core-level data including LOI, organic matter, grain size, and multi-element chemistry.
  - Detailed structural schemes for each core, including averages, standard deviations, and replicates for various elements.
- Zimbabwe
  - 10 cores (B1, B3, B5, B6, Z1, Z2, Z3, Z5, Z6, plus others implied by table).
  - Combines grain size, LOI, organic matter, and geochemical results; several cores include statistical summaries for As, Cr, Cu, Mn, Ni, Pb, Zn, Fe.
  - Core-specific data structures indicate varying column allocations and presence/absence of raw data.
- Mozambique
  - 10 cores (MA1–MA5, MA5B, MA7, MA10, OX1, OX2).
  - Some cores (MA1–MA5, MA5B) lack complete geochemical data; others (MA10) include XRF data; OX1/OX2 include grain size, LOI, and trace elements but vary in raw data availability.
  - Data structures emphasize depth, LOI, grain size, and sometimes XRF/ICP-derived elements.

## Governance and Stewardship Recommendations
- Metadata standardization:
  - Adopt a uniform schema across all cores (core_id, country, dam/site, collection_date, coordinates, core_length, depth, LOI, organic_matter, grain_size, elements measured, units, method/instrument, data_quality_flags, raw_vs_summary).
  - Clearly indicate which cores have raw data, which have summaries, and which have missing sections.
- Data quality and provenance:
  - Capture QA/QC notes per core (measurement errors, detection limits, negative-value flags).
  - Record instrument models, calibration dates, and measurement units consistently.
- Data interoperability:
  - Normalize units and column naming to enable cross-country comparisons.
  - Provide a data dictionary and a crosswalk table mapping core-specific columns to a common schema.
- Data availability and versioning:
  - Document data availability status (complete, partial, missing) and planned update cycles.
  - Implement version control for datasets and maintain changelog for corrections or additions (e.g., conversion of LOI values, corrected depths).
- Access, reuse, and governance:
  - Define data usage licenses and access terms; include contributor/institution contact points per dataset.
  - Archive provenance information (original filenames, data collection crews, processing steps) to ensure traceability.
- Documentation enhancements:
  - Provide consolidated, country-wide metadata files summarizing core IDs, locations, collection dates, and data coverage.
  - Include cross-region notes on methodological differences (e.g., instrument variants like ICP-OES vs ICP-MS vs XRF) to aid analysts in harmonization.
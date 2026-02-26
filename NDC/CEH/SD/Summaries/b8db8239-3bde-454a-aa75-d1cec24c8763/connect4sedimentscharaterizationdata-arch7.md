# SEDIMENTS CHARACTERISATION DATA FOR CONNECT4 PROJECT

- A multi-country sediment characterisation dataset comprising sedimentological and geochemical analyses from core samples collected in Botswana, South Africa, Zimbabwe, and Mozambique. Cores were obtained from various dams, processed via push corers, and analyzed for grain size distribution, organic matter (LOI), and trace element concentrations (ppm). Data are organized by country and core, with detailed descriptions of sampling methods, data structure, and quality control notes. Some cores include raw geochemical data or replicates; others have missing elements or incomplete data.

## Botswana

- Core set: GC1, GC2, L11, S5, S6, S7, S8 (7 cores)
- Sampling and processing:
  - Eight sediment cores collected from dams using a push corer (50 mm diameter), stored at 4 °C, halved, photographed, and sub-sampled for grain size and geochemical analysis.
- Data content per core:
  - Depth (cm), Organic matter (LOI, %), Grain size distribution (micrometres), and in many cores geochemical data (ppm) for trace elements (e.g., Cr, Fe, Ni, Cu, Zn, Pb). 
  - Core GC1 and GC2: depth up to 146 cm and 81 cm respectively; GC1 has no geochemical analysis, GC2 likewise; GC2 uses columns for depth, LOI, Organic matter, grain size.
  - Core L11: 58 cm; includes grain size, organic matter, and geochemical data (no raw data).
  - Cores S5, S6, S7: depths 33 cm, 92 cm, and 113 cm with grain size, LOI, Organic matter; S7 and S8 include broader geochemical data (S8 lists multiple element datasets).
  - Core S8 provides comprehensive geochemical breakdown (Arsenic, Chromium, Copper, Iron, Manganese, Nickel, Lead, Zinc) with averages, standard deviations, replicates.
- Data structure notes:
  - Column patterns described include: Depth, LOI calculations (A–H or B–H), Organic matter (%), Grain size distribution (micrometres), and Geochemical data (ppm) where available.
- Quality control:
  - Data checked for measurement errors, potential lab balance issues, and values below detection limits; negative values may appear in CSVs to indicate detections below detection limits.
- GIS considerations:
  - Data can be mapped as point features (cores) with attributes: country, dam, core ID, depth, LOI, organic matter, grain size statistics, and ppm concentrations for available elements. Some cores lack geochemical data; handle with nulls or separate layers.

## South Africa

- Core set: H1, H2, H3, H5, M4, M7, M8, N4, N5, N7 (10 cores)
- Sampling and processing:
  - Push corer (50 mm) collected from shore or boat; cores stored at 4 °C; split, photographed, and subsampled for grain size and geochemical analysis.
- Data content per core:
  - H1: depth 51 cm; particle size distribution and organic matter; no geochemical analyses.
  - H2: depth 0–50 cm; includes LOI, grain size, and geochemical results (As, Cr, Cu, Mn, Ni, Pb, Zn) but no raw data.
  - H3: depth 0–70 cm; grain size, LOI, organic matter, and geochemical data (As, Cr, Cu, Mn, Ni, Pb, Zn) with some Fe data omitted.
  - H5: depth 0–78 cm; grain size, LOI, organic matter, and geochemical results (with some missing particle-size intervals).
  - M4: depth 0–33 cm; grain size and organic matter (no geochemical data).
  - M7: depth 0–58 cm; grain size and organic matter; geochemical data averaged (no raw details).
  - M8: depth 0–33 cm; grain size, organic matter; geochemical data for several elements with statistics (averages, SDs, replicates).
  - N4: depth 0–40 cm; grain size, organic matter; geochemical results (As, Cr, Cu, Fe, Mn, Ni, Pb, Zn) with averages and 3 replicates.
  - N5: depth 0–60 cm; grain size and organic matter; raw geochemical data present.
  - N7: depth 0–27 cm; grain size, organic matter; geochemical data with averages and replicates.
- Data structure notes:
  - Core-specific layouts described include column designations for depth, LOI calculations, grain-size distributions, Organic matter (%), and multi-element geochemical tables (ppm) with averages/SDs and replicates where provided.
- Quality control:
  - Similar QC notes as Botswana; potential measurement errors and detection-limit considerations noted.
- GIS considerations:
  - Consistent core-point mapping with country-specific coordinates; plan for harmonizing unit presentation (ppm, % LOI, micrometres) across cores; incorporate replicate statistics where available.

## Zimbabwe

- Core set: B1, B3, B5, B6, Z1, Z2, Z3, Z5, Z6 (10 cores)
- Sampling and processing:
  - Push corer collection; cores stored at 4 °C; split, photographed, and sub-sampled for grain size and geochemical analysis.
- Data content per core:
  - B1 (Ripple Creek, 48 cm): grain size, LOI, Organic matter; geochemical data present in later columns.
  - B3 (Ripple Creek, 12 cm): grain size, LOI; geochemical data present.
  - B5 (Ripple Creek, 9 cm): grain size, LOI; geochemical data present.
  - B6 (Ripple Creek, 12 cm): grain size, LOI; geochemical data present.
  - Z1–Z6 (Zhovhe): depths 13–75 cm; grain size and LOI; geochemical data for multiple elements; some cores include raw geochemical data and replicates.
- Data structure notes:
  - Core descriptions detail depth, LOI calculations, grain size distributions, Organic matter (%), and geochemical data (ppm) with variations across cores (some lines specify averages, SDs, replicates; others indicate raw data).
- Quality control:
  - Standard QC notes apply; potential measurement and detection-limit considerations noted.
- GIS considerations:
  - Point features with core-level attributes; ensure consistent coordinate reference and handle missing data for certain elements or raw datasets.

## Mozambique

- Core set: MA1, MA2, MA3, MA4, MA5, MA5B, MA7, MA10, OX1, OX2 (10 cores)
- Sampling and processing:
  - Push corer from shore or boat; cores stored at 4 °C; split, photographed, and sub-sampled for grain size and organic content; some cores include geochemical data (XRF/XRF-like measurements) or raw data.
- Data content per core:
  - MA1: depth 67 cm; grain size and LOI present; organic matter missing in some intervals; no geochemical analysis.
  - MA2: depth 26 cm; grain size and organic matter; no geochemical analysis; cleaned particle-size data in some sections.
  - MA3: depth 26 cm; grain size and organic matter; no geochemical analysis.
  - MA4: depth 38 cm; grain size and organic matter; no geochemical analysis.
  - MA5: depth 49 cm; grain size and organic matter; no geochemical analysis (MA5B: 37 cm, cleaned grain size data).
  - MA7: depth 23 cm; grain size and organic matter; no geochemical analysis.
  - MA10: depth 57 cm; grain size, organic matter; XRF data present (raw data for XRF, some missing intervals).
  - OX1: depth 34 cm; grain size and organic matter; no geochemical analysis.
  - OX2: depth 35 cm; grain size and organic matter; no geochemical analysis; some lines indicate absence of raw data.
- Data structure notes:
  - Core data structures vary; patterns include depth, LOI calculations, grain size distribution, Organic matter (%), and geochemical data where available (ppm) with splits showing averages, replicates, and raw data for XRF in certain cores.
- Quality control:
  - Standard QC notes applied; some cores have missing data or incomplete geochemical records.
- GIS considerations:
  - Map-ready core points with attributes for country, dam, core ID, depth, LOI, organic matter, grain size, and any geochemical measurements; handle cores with no geochemical data as nulls; some XRF data may require special layers or a separate geochemical layer.

Overall GIS-focused notes and recommendations

- Spatial representation:
  - Create a point layer for all cores using coordinates provided per core (lat/long with appropriate hemisphere indicators). Attach core-level metadata (country, dam, core ID, depth range, sampling date).
- Attribute schema alignment:
  - Establish a common attribute schema across all cores: core_id, country, dam, depth_cm, LOI_percent, organic_matter_percent, grain_size_dist (summaries or separate fields per size class if available), and geochemical elements (ppm) with a standardized set of elements where data exist (e.g., As, Cr, Cu, Fe, Mn, Ni, Pb, Zn).
  - For cores with partial data, use nulls or separate flags to indicate missing geochemical data or raw data presence.
- Data quality and harmonisation:
  - Note and document detection limits, non-detect values (e.g., negative entries in CSVs as indicators), and any missing intervals in depth records.
  - Harmonise units across cores (e.g., grain size in micrometres, LOI in %, ppm for metals) to enable cross-core comparisons.
- Visualization ideas for GIS specialists:
  - Layer 1: core locations with basic metadata (country, dam, core ID, depth range).
  - Layer 2: thematic maps of organic matter content by core (color scale by LOI %).
  - Layer 3: geochemical intensity maps for selected elements where data exist (ppm color ramp), with separate layers per element or aggregated heatmaps.
  - Layer 4: uncertainty/replicate layer where QC indicates variability (e.g., SDs, replicates for M8, S8, N7, etc.).
  - Layer 5: data availability indicators to show which cores have full geochemical datasets vs. partial datasets.
- Data integration considerations:
  - When combining across countries, include a country field to enable regional analyses and cross-border comparisons.
  - Consider creating a metadata layer or data dictionary summarizing data structure per country and per core to facilitate use by non-domain GIS users.

Endnote

- The dataset offers rich core-based sediment characterisation suitable for map-based exploration of particle size, organic content, and trace element distributions across four countries. Some cores include comprehensive geochemical datasets, while others have partial data; plan for handling missing values and standardizing units for consistent GIS analysis and visualization.
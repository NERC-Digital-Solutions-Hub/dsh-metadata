# SOIL PROFILE OF RIGG Foot, Sourhope : BLOCK 4

## Overview
- Multi-component soil and vegetation data for Rigg Foot, Sourhope, focusing on BLOCK 4 with horizon-level descriptions, lab analyses, auger samples, and vegetation surveys.
- Includes related BLOCK 5 details and ECOTRON plot data presented in the same dataset.
- Captures both soil profiles and associated plant community information, along with site metadata.

## Data types and structure
- Soil profile descriptions
  - Horizon sequence and depths: LF (0–1 cm), FH (1–4 cm), H (4–8 cm), Ah (8–29 cm), Abg (29–40 cm), B sg (40–61 cm), C gx (61–95 cm).
  - Detailed soil descriptions per horizon (texture, colour, structure, moisture, roots, boundary).
- Soil analyses (BLOCK 4, horizon-based)
  - Measured variables per horizon: %N, %C, C:N, Ca (meq/100 g), Na (meq/100 g), K (meq/100 g), Mg (meq/100 g), %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
  - Heights/weights (Wt, mg) for each horizon sample (FH, H, Ah, AB, Bs, Cx).
- Auger samples (BLOCK 4 AUGER SAMPLES)
  - Sub-sample measurements for horizons 4A–4F: %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
- Vegetation surveys (BLOCK 4)
  - Plot-level species counts across subplots (Ac, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs Hm, Je, Lm, Lzm, Pe, Pp, Pt, Ra, Rr, Rs, Tr, Vc).
  - Totals per plot and per subplot, with species abbreviations mapped (e.g., Ac, Ao, Fr, Ns, Pp, Tr, etc.).
- ECOTRON PLOT data
  - Soil analysis (Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2)).
  - Vegetation survey with plot-level species counts similar to non-ECOTRON plots.
- Site metadata (BLOCK 5 and ECOTRON references)
  - GRID reference, altitude, slope, soil drainage, soil series, parent material, rock type, and major soil subgroup (Brown forest soil with gleying).

## Provenance and metadata
- Unique identifiers (MLURI Barcodes) label horizon samples (e.g., FH 603951, H 603952, Ah 603953, AB 603954, Bs 603955, Cx 603956).
- Auger samples labeled 4A–4F with corresponding barcodes (e.g., 603918–603923).
- ECOTRON horizon sample: barcode 603930.
- Site details include precise grid references and soil-subgroup classifications for BLOCK 5 (NT8544019520; Brown forest soil with gleying).

## Data management, storage, and sharing
- Horizon-level and auger data are catalogued with explicit sample weights, chemical properties, and pH measurements, enabling traceability.
- Data are organized by block and plot, with horizon-specific data tables and per-plot vegetation tallies.
- Vegetation and soil datasets are aligned to common subplot/plot schemes and horizon coding to support integration and cross-site comparisons.
- Data include explicit documentation of boundary locations, root presence, and horizon differentiation to aid reproducibility.

## Data quality, limitations, and considerations
- Missing or incomplete data in several plots and horizons (e.g., blanks for Na, incomplete canopy/root data, or gaps in plot subsamples).
- Complex horizon nomenclature (e.g., LF, FH, H, Ah, AB, Bg, BCg, Cg) requires careful standardization for interoperability.
- Vegetation tallies show some plots with sparse or zero counts, indicating variable sampling intensity across blocks and plots.
- Inter-block differences in soil colour, structure, and mottling indicate spatial heterogeneity requiring careful interpretation when aggregating data.

## Practical guidance for Data Stewards
- Metadata and standardization
  - Maintain a consistent ontology for horizon labels and depth intervals; map to standard soil classification schemes where possible (e.g., NVC associations for vegetation where relevant).
  - Use a controlled set of species codes and include a legend or dictionary for abbreviations to ensure reproducibility across users and sites.
- Provenance and traceability
  - Preserve MLURI Barcodes and ensure links between horizon data, auger samples, and vegetation records for each plot.
  - Document sample collection dates, methods, and any deviations from standard procedures.
- Data quality and completeness
  - Capture and flag missing data clearly; implement a data quality checklist to record sampling coverage, horizon completeness, and measurement reliability.
  - Where possible, fill gaps with metadata describing why data are unavailable (e.g., access issues, damage).
- archiving, sharing, and governance
  - Store datasets with versioned metadata and maintain a data dictionary detailing variable definitions and units.
  - Prepare data packages for sharing through standard portals or repositories, including crosswalks to allow cross-site meta-analyses.
- Reuse and interoperability
  - Provide linkage between soil profile data and vegetation data, including plot geometry and boundary definitions, to enable integrative analyses.
  - Include site-level context (grid refs, altitude, drainage, parent material) to support regional comparisons and long-term monitoring initiatives.

## Key takeaways
- The dataset offers rich, horizon-level soil chemistry, texture, moisture, structure, and pH data, alongside detailed vegetation surveys across BLOCK 4 and BLOCK 5, plus ECOTRON references.
- Provenance is strong through explicit horizon and auger barcodes, enabling traceability from field collection to laboratory analysis.
- While data are comprehensive, some gaps and heterogeneity exist; consistent metadata, standardized nomenclature, and thorough data dictionaries are essential for robust reuse and cross-site comparability.
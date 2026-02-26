# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview
- Compiles baseline soil, vegetation, and experimental design data for Sourhope field sites (Sourhope and Rigg Foot) to support GIS- and map-based analyses.
- Documents site context, climate, geology, soils, vegetation, land use, and the Soil Biodiversity experiments; emphasizes data quality, cross-project data integration, and repeatable GIS workflows.

## Data structure, scope, and organization
- Data are organized at multiple geographic scales: site-wide, block-level (Blocks 4 and 5 highlighted in the provided extract), and plot/subplot levels; includes detailed horizons and depth-interval schemas.
- Core data collections include:
  - Soil analyses (chemical and physical properties) across auger samples and soil horizons; horizon-specific measurements for FH, H, Ah, AB, Bg, BCg, Cg, etc.
  - Vegetation surveys using standardized plots and subplots; presence/absence data with notes on dominant and indicator taxa.
  - Profiling data (depth-based) for soil horizons, including horizon descriptions and archiving details (e.g., -80°C storage for sub-samples).
- Data are linked to MLURI barcodes, grid references, and site coordinates to support GIS georeferencing and replication.

## Block 4 and Block 5: soil and vegetation data (highlights)
- Block 4 (AUger samples) — key soil properties across six sub-samples (4A–4F):
  - %N, %C, C:N ratio, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH (H2O and CaCl2).
  - Weight data (for sample normalization) and horizon-level notes are provided in tabular form.
  - Vegetation surveys per plot (4A, 4B, 4C, 4D, 4E, 4F) document species totals and presence/absence cues; data are organized by plot and subplots with species tallies.
- Block 5 (soil profiles) — detailed soil profile described by horizon:
  - Horizons described: FH, H, Ah, AB, Bg, BCg, Cg with depth intervals (0–100 cm in excerpt) and narrative soil descriptions.
  - Associated analyses per horizon: %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O) and pH(CaCl2).
  - Profile-level data include depth-specific chemistry and pH trends across horizons, plus archiving and catalogue references (MLURI barcodes).
- Block 5 auger samples (5A–5F) — per-sample suite mirroring Block 4 variables with detailed depth- and horizon-analog measurements, enabling cross-block comparisons.

## ECOTRON and site-wide components
- ECOTRON PLOT:
  - Soil analysis includes Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
- Vegetation surveys for ECOTRON plots provide presence/absence tallies by subplot and plot, complementing the main Block 4/5 vegetation datasets.

## GIS-ready data products and opportunities
- Spatial layout maps:
  - Blocks (e.g., Blocks 4 and 5), plots (A–F within blocks), subplots (A–Q), and Ecotron subdivisions; color-code by treatment, block, or community type.
- Vegetation and indicator taxa layers:
  - Map dominant communities (e.g., U4d, U5b) and indicator species distributions; create richness heatmaps for focal taxa (e.g., Deschampsia flexuosa, Agrostis capillaris, Nardus stricta).
  - Presence/absence data by subplot enable fine-scale distribution mapping.
- Species distribution and community maps:
  - Point or raster layers for key species (e.g., Agrostis capillaris, Festuca rubra, Nardus stricta, Poa pratensis) with plot-level abundance cues where available.
- Soil property surfaces and horizon-aware layers:
  - Interpolated or gridded surfaces for pH, %N, %C, C:N, Ca, Na, K, Mg, %LOI, and moisture loss by plot or depth interval; horizon-specific layers (FH, H, Ah, AB, Bg, BCg, Cg) to enable depth-aware analyses.
- Horizon and depth schemas in GIS:
  - Attribute layers capturing horizon codes and their associated chemical/physical properties for depth-resolved visualization and modeling.
- Time-series and baseline comparison layers:
  - If repeat surveys exist, create temporal GIS layers showing changes in vegetation, soil chemistry, LOI, and other properties over time.
- Data quality and metadata guidance:
  - Document sampling schemes (50 x 50 cm vegetation quadrats, 25-point subsamples per quadrat, W-pattern auger cores) to support spatial weighting and uncertainty estimates.
  - Note coverage limitations (e.g., one-third subplot sampling for vegetation) to inform map confidence and bias assessments.
  - Ensure georeferencing through site grid, block labels, and plot identifiers for accurate map alignment.

## Data notes, limitations, and provenance
- Data are produced by MLURI and collaborators; linked with ECN and related programs; includes detailed figure/table legends to support GIS replication and integration.
- Coverage limitations:
  - Some vegetation surveys cover only a fraction of subplots within certain plots; results are indicative of broader site patterns rather than exhaustive plot-level conclusions.
- Horizon and soil data:
  - Rich horizon descriptions and depth-specific chemistry allow depth-aware GIS analyses but require careful handling of boundary definitions and horizon coding.

## Appendix, data availability, and GIS integration
- Appendix A and linked tables/figures provide block-level soil and vegetation data, grid references, horizons, and a wide array of chemical and physical properties.
- Data are catalogued with MLURI barcodes and horizon-level identifiers to facilitate archival storage and GIS workflows.
- Guidance is provided for integrating the data into GIS, including coordinate references, grid references, and depth-schema transcription.

## Endnotes and practical takeaway for GIS specialists
- The handbook provides a comprehensive foundation for map-based data products of the Sourhope field site, enabling policy, client-facing, or public GIS visualizations of soil biodiversity, vegetation communities, and land-use treatments across the Rigg Foot/Sourhope landscape.
- For GIS workflows, prioritize organizing data into horizon-aware soil layers, block/plot/subplot spatial schemas, and vegetation/community layers, then integrate with time-series analyses if repeat measurements are available.
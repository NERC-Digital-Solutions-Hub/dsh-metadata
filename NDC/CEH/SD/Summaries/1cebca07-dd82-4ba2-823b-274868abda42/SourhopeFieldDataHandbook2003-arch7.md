# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE : BLOCK 4 AUGER SAMPLES

- A detailed multi-block dataset from Sourhope, focusing on Block 4 auger samples, with accompanying Block 5 soil/vegetation data and ECOTRON plots to support GIS-based analyses of soil chemistry, horizon development, vegetation patterns, and their spatial relationships.

## Overview of contents and purpose for GIS work

- Provides block-level and plot-level spatial framework (blocks, plots, subplots, Ecotron area) with associated soil chemistry and vegetation data.
- Includes horizon-by-horizon soil profiles (0–100 cm and deeper in some sections) and a range of soil attributes (N, C, C:N, pH, base cations, moisture loss, LOI).
- Contains vegetation surveys at plot/subplot scales, species counts, and NVC classifications, suitable for habitat and biodiversity mapping.
- Data linked to precise grid references, elevations, slope, drainage descriptors, and time context (baseline 1998, ECN/SERAD contexts, Ecotron data).

## Spatial and sampling framework (GIS-relevant structure)

- Blocks and plots:
  - Block 4: Auger sample data for subplots A–F across multiple plots (e.g., 4A–4F) with per-sample measurements.
  - Block 5: Site details, soil profiles (LF, FH, H, Ah, AB, Bg, BCg, Cg) and associated auger analyses; grid references and elevation data provided.
- Ecotron site:
  - Separate soil analyses and vegetation survey for Ecotron plot, with coordinates and horizon-specific data.
- Vegetation sampling:
  - Block 4 and Block 5 vegetation surveys at plot and subplot levels; presence/absence and totals for species, plus notes on dominant taxa and indicator species.
  - NVC classifications (e.g., U4d Festuca ovina-Agrostis capillaris-Galium saxatile grassland, with occasional U5b).
- Data points and areas:
  - Plot polygons (12 m x 20 m) and subplots (4 m x 4 m); soil cores (0–30 cm) and horizon data per block/plot.
  - Vegetation quadrats (50 x 50 cm) within selected subplots, with 25 sampling points per quadrat.

## Soil data structure and key attributes (Block 4 and Block 5)

- Block 4 auger samples:
  - Variables per sample: Weight (mg), %N, %C, C:N, Ca (meq/100 g), Na (meq/100 g), K (meq/100 g), Mg (meq/100 g), %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
  - Sample IDs: 4A–4F with associated barcodes and values across all measured attributes.
- Block 5 soil profiles:
  - Profiles for FH, H, Ah, AB, Bg, BCg, Cg horizons with depth ranges (e.g., 0–1 cm, 1–5 cm, 5–7 cm, 7–25 cm, etc.).
  - Attributes by horizon: %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
  - Soil descriptions include horizon color and structure details and depth intervals, reflecting pedogenic development.
- Block 5 auger samples (analyses):
  - Similar chemical suite as Block 4 with per-sample values for %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH H2O, pH CaCl2, and weight.
- ECOTRON plots:
  - Soil analysis (Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH H2O, pH CaCl2).
- Data relationships:
  - Horizon data tied to blocks/plots; horizon-level chemistry linked to plot and Ecotron identifiers; depth-resolved data enable depth-specific GIS overlays.

## Vegetation data and classification (GIS-ready context)

- Block 4 and Block 5 vegetation surveys:
  - Plot-level totals for species presence across subplots; counts of dominant and indicator species.
  - Subplot-level species totals and community associations; notes on edge effects and habitat preferences.
- Vegetation classification:
  - NVC-based groupings with dominant grasses and forbs; indicator species identified (e.g., D. flexuosa at edges; G. saxatile, H. mollis, P. pratensis as subplot indicators).
- ECOTRON vegetation:
  - Separate vegetation data for ECOTRON plots, aligned to Ecotron coordinates and plot designations.

## Data structure, formats, and GIS usage

- Spatial layers:
  - Block polygons with coordinates and elevation; slope and drainage descriptors per block.
  - Plot polygons (12 x 20 m) and subplot polygons (4 x 4 m) with treatment and vegetation data.
  - Ecotron plot boundary and associated data.
  - Soil layers by horizon (0–30 cm cores and horizon boundaries) and horizon-specific attributes.
  - Soil chemical layers by horizon and by plot, including N, C, C:N, Ca, Na, K, Mg, moisture loss, LOI, and pH values.
  - NVC classification layer with U4d and occasional U5b subcommunities.
  - Vegetation sampling points (50 x 50 cm quadrats) with presence/absence data and abundance where available.
- Temporal context:
  - Baseline data (1998) linked to ongoing ECN/SERAD Micronet contexts and Ecotron time-series potential.
- Likely GIS outputs:
  - Habitat maps by block/plot, soil property rasters or layered polygons by horizon, vegetation community maps, and time-series overlays for soil–vegetation interactions.

## Practical implications for GIS specialists

- Enables multi-scale mapping of soil properties (horizon-specific) and vegetation communities across a sloped landscape with defined blocks and plots.
- Supports analysis of relationships between soil chemistry (pH, C, N, base cations) and vegetation communities (NVC types, indicator species).
- Allows depth-resolved GIS overlays, integrating soil data with slope, drainage, and microtopography.
- Facilitates time-series analyses by linking baseline 1998 data with ongoing survey and Ecotron contexts, enabling landscape-scale ecological modelling and habitat assessment.

## Appendix and data context notes

- Appendix-style blocks provide block-wise baseline data, horizon descriptions, and sampling records to support re-analysis and integration with other long-term environmental datasets.
- Data are organized to support GIS-enabled re-analysis and integration with broader environmental-change datasets, with clear block/plot/horizon associations and detailed soil and vegetation attributes.
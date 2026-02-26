# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview of this chunk
- Presents soil and vegetation data for Sourhope: Block 4 auger samples, Block 5 site details, soil profiles, auger analyses, vegetation surveys, and an Ecotron plot.
- Data are designed for GIS-ready mapping and spatial analyses of soil properties, vegetation patterns, and their relationships to management treatments and site features.

## Data components

- Block 4 Auger Samples (Block 4A–4F)
  - Measurements per sample: weight (mg), %N, %C, C:N ratio, Ca, Na, K, Mg (meq/100g), %Moisture loss, %Loss on Ignition, pH H2O, pH CaCl2.
  - Provides horizon- or plot-scale soil chemistry and basic physical indicators for the block.

- Block 4 Vegetation Survey (Plot 4A, 4B, 4C, 4D, 4E, 4F)
  - Subplots and species presence/absence counts (with totals per subplot/plot).
  - Indicates dominant species and species richness patterns across plots and slope positions.
  - Data include per-plot totals for species totals and key indicator species.

- Block 5 Site Details and Soil Profile
  - Site details: grid reference NT8544019520, altitude ~315 m, slope ~5°, imperfect drainage; soil series Sourhope Bellshill with brown forest soil and gleying.
  - Soil profile (Block 5): depths and horizon descriptions from 0–100 cm across horizons LF, FH, H, Ah, AB, Bg, BCg, Cg, including color, structure, roots, and boundary characteristics.

- Block 5 Auger Samples (Auger 5A–5F)
  - Analyses per auger sample: weight, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH H2O, pH CaCl2.
  - Horizon- and sample-specific data enabling horizon-wise mapping and plot-level summaries.

- Block 5 Vegetation Survey (Plot 5A, 5B, 5C, 5D, 5E, 5F)
  - Subplot-level species counts (Ac, Ao, At, Br, Cp, etc.) with species totals per subplot.
  - Includes per-plot totals for species richness and indicator species, enabling per-plot habitat classification.

- ECOTRON PLOT
  - Soil analysis: weight, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH H2O, pH CaCl2.
  - Vegetation survey: subplot-level counts and totals, indicating species presence and community structure within ecotron conditions.

## GIS-ready data layers and attributes

- Spatial boundaries and footprints
  - Block footprints, plot footprints (Block 4 and Block 5), plus Ecotron plot boundaries.
  - Grid references and site coordinates to anchor GIS layers.

- Horizon- and plot-scale soil attributes
  - Block 5 horizon layers (LF, FH, H, Ah, AB, Bg, BCg, Cg) with pH, %N, %C, C:N, LOI, Ca, Mg, Na, K, moisture loss, and other exchangeable cations.
  - 0–100 cm depth profiles for horizon-based rasterized or polygonal mapping.

- Auger sampling points and attributes
  - Point features for samples 4A–4F and 5A–5F, carrying all measured soil chemistry and physical properties.

- Vegetation layers
  - Plot and subplot vegetation classifications with dominant species, indicator species, and total species counts per plot/subplot.
  - ECOTRON plot vegetation data for comparison with natural blocks.

- Lab provenance and metadata
  - MLURI barcodes for each sample and horizon, enabling traceability to laboratory analyses and ramps of data provenance.

## Data quality, gaps, and considerations

- Missing values indicated by dots (.) in several fields, especially in Block 4 vegetation detail and some horizon measurements.
- Block 5 horizons show rich depth- and horizon-specific data, but variability exists across horizons (e.g., Ca, Mg, pH values vary by depth and zone).
- Data granularity supports both horizon-level mapping and plot-level synthesis, but care needed to aggregate across subplots to avoid over-interpretation of localized anomalies.
- An Ecotron plot provides controlled-environment context, useful for comparing with field plots.

## GIS-driven use cases and recommendations

- Map products to create:
  - Block and plot boundary layers with associated soil and vegetation attributes.
  - Horizon-based soil layers (pH, %N, %C, C:N, LOI, Ca, Mg, K, Na, moisture loss) by horizon (LF, FH, H, Ah, AB, Bg, BCg, Cg) for Block 5, enabling detailed soil-landscape analyses.
  - Auger-sample point maps linked to horizon data and plot IDs for site-wide spatial modeling.
  - Vegetation habitat maps: dominant communities, indicator species, and richness by plot, overlaying with soil layers to explore soil-vegetation relationships.
  - Ecotron context: compare ecotron soil/vegetation profiles with adjacent field plots.

- Analytical approaches facilitated by GIS
  - Spatial comparison of soil chemistry and texture with vegetation patterns across blocks and slope positions.
  - Integration with other environmental layers (climate, SERAD Micronet) for multi-criteria habitat assessment.
  - Use block-level and horizon-level data to assess treatment effects and spatial heterogeneity within and between blocks.

## Conclusion

- This chunk enriches the Sourhope dataset with Block 4 auger chemistry, Block 5 detailed site, horizon-level soil properties, and vegetation compositions, plus Ecotron context.
- When mapped, these data enable robust spatial analyses of soil properties, vegetation communities, and their interactions across the Sourhope field site, supporting GIS-based data products for visualization and policy/research communication.
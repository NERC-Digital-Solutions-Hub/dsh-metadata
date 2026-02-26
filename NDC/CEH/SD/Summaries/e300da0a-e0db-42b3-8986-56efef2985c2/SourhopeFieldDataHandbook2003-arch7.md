# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview (GIS-focused)

- Presents Block 4 and Block 5 soil analysis and vegetation survey data from Rigg Foot, Sourhope, including auger samples and horizon descriptions, plus ECOTRON plot data.
- Data are organized for GIS-based mapping and long-term biodiversity analysis, with block/plot structures, horizon-level chemistry, and subplot vegetation records.
- Includes site-context details (grid references, altitude, slope, drainage) and soil-series classifications to support spatial interpretation.

## Data Structure and Variables (for GIS layering)

- Blocks and plots
  - Block 4: Plots A–F with subplots; ECOTRON subplot exists.
  - Block 5: Site details and plots 5A–5F with multiple subplots (Ac, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs, Hm, Je, Lm, Lzm, Mc, Ns, Pe, Pp, Pt, Ra, Rr, Rs, Tr, Vc, etc.).
- Horizons and profiling (per auger/core)
  - Horizons labeled FH, H, Ah, AB, Bg, BCg, Cg, etc. with depth ranges.
  - For each horizon: weight (mg), %N, %C, C:N ratio, Ca (meq/100g), Na (meq/100g), K (meq/100g), Mg (meq/100g), %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
- Vegetation surveys (per plot/subplot)
  - Species presence/absence indicators and species totals per subplot.
  - Per-plot tallies of species counts and indicator species where present.
- Site context and coordinates
  - Block 5 includes grid reference (NT8544019520), altitude (315 m), slope (~5°), drainage (Imperfect), soil series (Brown forest soil with gleying), parent material, rock types.
- ECOTRON data
  - Separate soil analysis and vegetation survey for ECOTRON PLOT, enabling comparisons with field plots.

## Sampling Methods and Data Scope

- Soil sampling
  - Auger cores collected per horizon within each main plot; horizons sampled and analyzed for nutrient and physical-chemical properties.
  - Depth ranges and horizon definitions documented; some horizons described with color/structure notes (e.g., Ah, Bg, BCg, Cg).
- Vegetation sampling
  - 50 x 50 cm quadrats or subplot-specific surveys across selected plots; presence/absence used to derive species abundance by frequency and richness indicators.
- Data integration
  - Includes ECN/Micronet context and is designed to be GIS-ready, with block-level and horizon-level measurements enabling layered spatial interpretation.

## Key Pattern Highlights (Block 4 and Block 5)

- Soil chemistry and horizon trends
  - Surface horizons tend to be more acidic with higher organic content and LOI; deeper horizons show varying Ca/Mg with depth.
  - Ca, Mg, K, Na values exhibit block-to-block and horizon-to-horizon variability; some horizons show anomalous values requiring special treatment in analyses.
- Moisture and organic content
  - %Moisture loss and LOI are typically higher in upper horizons (FH, H, Ah) and decrease with depth, reflecting organic matter distribution.
- pH and exchangeable cations
  - pH in water generally acidic (roughly in the mid- to low-4 range across horizons); CaCl2 pH values are slightly lower, reflecting base saturation differences across horizons.
- Vegetation composition (block-level richness)
  - Vegetation surveys indicate diverse communities across plots with varying species totals per subplot; some plots show higher richness on moister or slope-affected microsites.
  - Indicator or key species are recorded per plot/subplot, facilitating association analyses and GIS-driven habitat classification.

## Data Quality and Considerations for GIS Use

- Data completeness
  - Some cells/entries are blank or partially transcribed in the provided chunk; expect similar gaps in other sections and plan for imputation or exclusion where appropriate.
- Horizon labeling consistency
  - Horizon nomenclature includes FH, H, Ah, AB, Bg, BCg, Cg, etc.; ensure uniform horizon coding when integrating with other soil datasets or national classifications.
- Anomalies and block-level variation
  - Certain horizons or blocks show atypical values; separate them in analyses to avoid biasing generalized models.
- Units and scaling
  - Measurements in meq/100g for cations, %N, %C, LOI, moisture loss, pH values, and mg weights; confirm unit consistency during GIS attribute setup.

## GIS Integration Recommendations

- Create multi-layer schema
  - Soil horizon layer: attributes per horizon (name, depth, %N, %C, C:N, Ca, Mg, K, Na, LOI, moisture loss, pH H2O, pH CaCl2).
  - Plot-level vegetation layer: subplots with species totals and presence/absence indicators; link to horizon layer via plot/plotID.
  - Block-level context layer: block IDs with site context (grid ref, altitude, slope, drainage, soil series, rock type).
  - ECOTRON comparison layer: ECOTRON PLOT data as a separate time-series or snapshot layer.
- Data quality flags
  - Include flags for missing values, horizon labeling inconsistencies, and blocks with anomalous measurements to guide QA/QC workflows.
- Visualization targets
  - Spatial maps of soil pH, organic content (LOI), and exchangeable Ca/Mg across horizons.
  - Habitat/vegetation maps showing species richness and indicator species per subplot.
  - Temporal analyses by ECOTRON vs field plots to assess long-term biodiversity and soil changes.

## Appendices and References (context for GIS work)

- Data are intended for integration into GIS products, supporting long-term biodiversity studies and analyses under ECN/Micronet objectives.
- Barcodes and cataloging (MLURI) accompany each sample to aid data provenance and traceability in GIS databases.
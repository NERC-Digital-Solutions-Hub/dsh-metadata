# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

## Overview
- Compilation of soil and vegetation data from Rigg Foot, Sourhope, focusing on Block 4 auger samples, Block 5 site details, and ECOTRON plot data.
- Includes horizon descriptions, chemical properties, moisture indicators, pH measurements, and vegetation surveys by plot/subplot.
- Data are part of the Sourhope field data programs and linked to MLURI and CEH Merlewood archives; sample identifiers include MLURI barcodes (e.g., 603930–603963).

## Spatial structure and data organization
- Spatial components:
  - Blocks: Block 4 (auger samples) and Block 5 (site details, profiles, and vegetation data).
  - Plots and subplots: Data are organized by Plot and Subplot within each Block, with various configurations (e.g., A, B, C, D, E, F subplots; Ecotron plots in ECOTRON SITE).
  - ECOTRON PLOT: A dedicated experimental subplot within Block 4/ECOTRON context.
- Data organization:
  - Horizon-focused soil data for each horizon within a profile (e.g., FH, H, Ah, AB, Bg, BCg, Cg in Block 5).
  - Auger sample data per sub-sample (e.g., 4A–4F for Block 4; 5A–5F for Block 5).
  - Vegetation surveys aligned to plots/subplots with species totals and presence-absence indicators.
- Temporal scope: Cross-sectional snapshot tied to 1990s–early 2000s field campaigns; data intended for integration with broader ECN/Micronet time-series where applicable.

## Data columns and variables

- Block 4 AUGER SAMPLES (4A–4F)
  - Wt (mg)
  - %N
  - %C
  - C:N Ratio
  - Ca (meq/100g)
  - Na (meq/100g)
  - K (meq/100g)
  - Mg (meq/100g)
  - %Moisture loss
  - %Loss on Ignition
  - pH(H2O)
  - pH(CaCl2)

- BLOCK 5 SITE DETAILS
  - Site grid reference (NT8544019520)
  - Altitude, slope, drainage, soil series, parent material, base of profile pit
  - Major soil subgroup: Brown forest soil with gleying
  - Rock type information

- BLOCK 5 SOIL PROFILE
  - Depths and horizon designations (FH, H, Ah, AB, Bg, BCg, Cg)
  - Horizon descriptions (e.g., color, structure, roots, stones)
  - Depth interval data (0–1 cm through 100 cm, etc.)

- BLOCK 5 AUGER SAMPLES (5A–5F)
  - Wt (mg)
  - %N
  - %C
  - C:N Ratio
  - Ca (meq/100g)
  - Na (meq/100g)
  - K (meq/100g)
  - Mg (meq/100g)
  - %Moisture loss
  - %Loss on Ignition
  - pH(H2O)
  - pH(CaCl2)

- BLOCK 5 VEGETATION SURVEY
  - Subplots and species totals per subplot
  - Presence/absence and counts of dominant species per plot/subplot (e.g., Ac, Ao, At, Br, etc.)
  - Totals across plots (e.g., species totals per subplot)

- ECOTRON SOIL SITE
  - ECOTRON PLOT: Wt (mg), %N, %C, C:N Ratio, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2)

- ECOTRON VEGETATION SURVEY
  - Subplots with species presence/absence and counts by plot
  - Totals across subplots for indicator species and overall richness

## GIS-ready data products and layers

- Spatial layers to consider:
  - Block polygons (Block 4, Block 5) and plot polygons within blocks
  - Subplot polygons (A–F and other designations) within each main plot
  - Ecotron and ECOTRON subplot delineations
  - Horizon-based soil property maps or point layers (per horizon depth intervals: FH, H, Ah, AB, Bg, BCg, Cg)
  - Soil type classification layer (Brown forest soil with gleying)
  - Vegetation layers by plot/subplot (dominant species, presence/absence, species richness)
- Attribute fields to capture:
  - Sample/plot identifiers (e.g., 4A–4F, 5A–5F, PLOT IDs, BLOCK IDs)
  - Horizon labels and depth ranges
  - Chemical properties (N, C, C:N, Ca, Mg, K, Na, LOI, moisture loss, pH)
  - Physical properties (depths, horizon descriptions, root presence)
  - Vegetation metrics (dominant species, counts, total species per plot/subplot)
  - Experimental design flags (Block, Plot, Subplot, Ecotron status)
- Analytical outputs to map:
  - Twinspan/NVC associations (for vegetation) linked to plot polygons
  - Horizon-specific nutrient distributions and pH gradients
  - Spatial patterns of moisture loss and LOI across blocks and depths
  - Linkages to ECN/Micronet time-series where relevant

## Data management, access, and context

- Data provenance:
  - Collected by MLURI; archived at CEH Merlewood
  - Associated with Sourhope Soil Biodiversity datasets and ECN Micronet programs
  - MLURI barcodes provide sample traceability (e.g., 603930–603963)
- Context for GIS integration:
  - Rich, multi-resolution spatial data suitable for habitat classification, soil-vegetation modeling, and landscape-scale biodiversity analyses
  - Horizon-level chemistry enables 3D soil characterization when integrated with plot topology
  - Temporal context supports change-detection studies when time-series data are linked

## Considerations for GIS Specialists

- Data integration:
  - Align blocks, plots, and subplots with consistent geometry and IDs to enable seamless joins to horizon and vegetation attributes
  - Integrate horizon-depth data with 2D map layers (for mapping) and consider 3D representations if depth interpolation is pursued
- Data quality and gaps:
  - Expect partial data across horizons and samples; account for missing values in analyses and mapping
  - Verify barcodes and sample IDs against archival records for accuracy
- Applications:
  - Baseline mapping of soil properties and vegetation across Sourhope site
  - Habitat classification and biodiversity assessments by NVC associations
  - Spatially explicit soil-plant interaction studies within the ECN/Micronet framework

## Endnotes and resources

- Data references include block/plot/subplot inventories, horizon-by-horizon analyses, and soil-vegetation survey tables
- Primary data sources archived under Sourhope Field Data programmes; linked to Soil Biodiversity Programme documentation and ECN/Micronet time-series where applicable
# SOURHOPE FIELD DATA HANDBOOK 2003

## Executive summary for GIS specialists
- Provides a comprehensive, multi-layered field dataset from Sourhope, focused on upland grassland soils and vegetation, laid out across a block-plot-subplot grid with an Ecotron component.
- Data are structured for map-based analysis: site boundaries, block delineations, plot and subplot geometry, treatments, topography, soils (horizons and chemistry), vegetation communities, and long-term environmental context.
- Data sources include soil cores, profile pits, and vegetation surveys, with detailed metadata, archival samples, and multiple data formats referenced for multivariate analyses.

## Geographic and project context
- Sourhope field site comprises multiple blocks (1–5) with defined boundaries and elevations around 300–315 m.
- Blocks are arranged north–south with main plots (12 × 20 m) subdivided into 4 × 4 m subplots; an Ecotron plot (8 × 24 m) hosts controlled environment experiments.
- Topography includes varying slopes (approximately 4°–8°) and drainage characteristics described per block.
- Site is used for long-term soil-plant research, including ECN/Micronet programs; data are intended for integration into GIS workflows.

## Data structure and organization
- Plot/network layout:
  - 5 blocks, each containing 5 main plots, subdivided into multiple subplots (A–Q) and Ecotron subplots (A–M).
  - Treatments applied at the main-plot level: Control (C1), Lime, N, NL, Biocide, Fallow (reallocated in practice).
- Data types:
  - Soils: horizon-wise, depth-based data with chemical (Ca, Mg, Na, K, %N, %C, C:N, LOI), physical (moisture loss), and pH (H2O and CaCl2) measurements; profile descriptions and horizon nomenclature (FH, H, Ah, AB, Bg, BCg, Cg, etc.).
  - Vegetation: species presence/absence data from 50 × 50 cm quadrats within randomly selected subplots; dominant grasses listed; NVC classification alignment (U4d primarily, with possible U5b in moister blocks); indicator species identified via multivariate analyses.
  - Sampling design: baseline year 1998 for many measurements; subplots sampled represent roughly one-third of subplots per main plot; data documented per plot and per subplot with site-wide summaries.
- Data management:
  - Appendices and files referenced for detailed analyses (Appendix A; Twinspan.doc; Association.xls); MLURI barcodes linked to samples for traceability.
  - Archive samples stored at -80°C; data intended for GIS-enabled integration with environmental datasets.

## Block 4 and Block 5: key GIS-relevant data descriptions
- Block 4 (Soil and vegetation):
  - Auger samples (4A–4F) with detailed measurements:Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2).
  - Vegetation data per plot (4A–4F) includes subplot-level species totals and presence/absence by species; dominant vegetation markers and indicator species noted.
  - Data tables indicate plot-by-plot species composition and sampling coverage.
- Block 5 (Site details, soils, profiles, and vegetation):
  - Site details include grid reference NT8544019520, altitude 315 m, slope 5°, soil drainage and major soil subgroups (Brown forest soils with gleying); profile descriptions include FH, H, Ah, AB, Bg, BCg, Cg with depth ranges.
  - Soil profiles (5A–5F) with comprehensive analyticals: %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2).
  - Auger sample analyses (5A–5F): comparable chemical/physical metrics across six auger samples, enabling block-level comparisons.
  - Vegetation surveys for Block 5 plots (5A–5F) capturing subplot-level species totals and plant community data; total species counts and indicator species patterns documented.
  - ECOTRON PLOT data: soil analysis (Wt, %N, %C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH) and vegetation survey across Ecotron plots, with consistent plotting of species and abundances.

## ECOTRON data integration
- ECOTRON PLOT data provide controlled-environment context within Sourhope, offering parallel soil chemistry (pH, cation content, carbon/nitrogen metrics) and vegetation structure to contrast with ambient plots.
- GIS opportunities include comparing Ecotron versus field plots to model environmental drivers of vegetation composition and soil processes.

## GIS-ready data layers and attributes (opportunities)
- Site boundary and block delineations (blocks 1–5) with precise plot boundaries and Ecotron geometry.
- Treatments and block-level assignments: main-plot treatment codes (C1, Lime, N, NL, Biocide, Fallow) linked to spatial features.
- Topography and drainage: elevation, slope, and drainage descriptors integrated at block/plot scales.
- Soils:
  - Horizon-level classifications (FH, H, Ah, AB, Bg, BCg, Cg) with depth ranges and color/structure notes.
  - Chemical attributes: %N, %C, C:N, Ca, Mg, K, Na, LOI, %Moisture loss, pH (H2O and CaCl2).
- Vegetation:
  - Dominant species per plot, NVC classification (U4d; potential U5b in moister zones), indicator species from Twinspan and association analyses.
  - Species richness per plot, and presence/absence data per 50 × 50 cm quadrat (five subplots per main plot sampled).
- Sampling design metadata:
  - Plot and subplot indices (A–Q; Ecotron A–M), grid references, and MLURI barcodes for traceability.
- Environmental context:
  - ECN weather/climate data linkage, long-term environmental measurements for correlative GIS analyses.
- Data provenance and documentation:
  - Appendices and metadata references (Appendix A; Twinspan.doc; Association.xls) to support reproducibility and advanced GIS modelling.

## Limitations and considerations for GIS analyses
- Subplot coverage: sampling covers approximately one-third of subplots per main plot; results should be treated as site-wide guides rather than exhaustive inventories.
- Temporal scope: baseline year is 1998 for many analyses; longitudinal GIS studies should incorporate temporal depth and potential data gaps.
- Block variability: block- and horizon-specific differences observed; careful normalization or stratified analyses recommended when comparing across blocks.

## Endnotes: practical takeaways for GIS workflows
- The Sourhope dataset enables robust GIS-based exploration of soil-plant relationships in upland grasslands, with well-documented blocks, plots, subplots, and Ecotron contexts, plus rich soil chemistry and vegetation data.
- The combination of NVC classifications, indicator species, horizon-level soil chemistry, and treatment regimes supports diverse spatial analyses, from habitat mapping to multivariate ecological modelling.
- When integrating into GIS, leverage the block/plot/subplot hierarchy, horizon-based soil attributes, and vegetation community classifications to build multi-layer maps and perform spatially explicit analyses.
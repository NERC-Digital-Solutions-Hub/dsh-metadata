# SOURHOPE FIELD DATA HANDBOOK 2003

## Purpose and scope
- Describes Sourhope Field Site within the Soil Biodiversity Programme, focusing on long-term soil, vegetation, and ecosystem data to support spatial analyses and GIS-driven investigations.
- Provides baseline datasets, methodological details, and a structure suitable for data integration, visualization, and longitudinal GIS work.

## Spatial structure and sampling design (GIS-relevant units)
- Five blocks (1–5) located on Sourhope Rigg Foot with defined slope gradients and micro-topography.
- Each block contains six main plots (A–F) totaling 30 plots, with each main plot subdivided into 15 subplots (A–Q) for fine-grained sampling.
- Ecotron plots (8 × 24 m) subdivided into 12 sections (A–M) for controlled-environment studies.
- Spatial layout supports gradient analyses (upslope/downslope, edge vs interior) and block-level comparisons.
- Block 5 includes detailed soil profiles and augmented block-level horizon data; Block 4 provides extensive auger datasets and vegetation mappings.

## Data collection domains

### Vegetation data
- Methods: 50 cm × 50 cm vegetation quadrats within five of the fifteen 50 × 50 subplots per main plot; 25 sampling points per quadrat.
- Data captured: presence/absence of species, with some abundance context; species lists and relative dominance.
- Key outcomes: Dominant grasses (e.g., Festuca ovina, Agrostis capillaris); overall species richness increases downslope; close alignment with National Vegetation Classification (NVC) grassland types; indicator species identified (e.g., Deschampsia flexuosa linked to edges; Rhytidiadelphus squarrosus bryophyte patterns with moisture gradients).

### Soil data
- Auger sampling (0–30 cm) per main plot: 30 cores in a W-pattern to characterize surface soils; samples archived and analyzed; detailed horizon sampling in profile pits.
- Horizon descriptions (examples from Block 5): FH, H, Ah, AB, Bg, BCg, Cg with depth ranges (0–100 cm typical) and horizon-specific chemistry and texture notes.
- Chemistry and physical properties (per horizon; across blocks and plots): %N, %C, C:N, Ca, Na, K, Mg (meq/100 g); moisture loss (%), loss on ignition (%LOI); pH (H2O) and pH CaCl2.
- Block-level variability: notable differences in Ca, Na, Mg, K, pH and horizon composition across blocks and along slope; near-surface horizons generally more acidic and organic-rich with higher LOI.
- Data formats: horizon-level chemistry per block/plot, along with aggregate plot data; tables designed for GIS integration (per-horizon attributes and plot-level summaries).

### ECOTRON data
- ECOTRON soil analysis: Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %Loss on Ignition, pH(H2O), pH(CaCl2).
- ECOTRON vegetation survey sections provide a controlled-context counterpart to main plots, enabling comparisons under standardized conditions.

## Data types and GIS-ready attributes

- Spatial units
  - Blocks (1–5), main plots (A–F), subplots (A–Q), and ECOTRON subdivisions (A–M).
- Attributes
  - Treatment/experimental design: e.g., lime, nitrogen, lime+N, biocide, control (for main plots); enables mapping of treatment effects.
  - Topographic context: slope gradient, edge vs interior, block position.
  - Vegetation: presence/absence of species, dominance indicators, community classifications (NVC matches).
  - Soils: horizon-level chemistry (N, C, C:N, Ca, Na, K, Mg), moisture loss, LOI, pH values (H2O and CaCl2), horizon depths and descriptions.
  - Data provenance: block, plot, horizon, sample type (aug­er vs profile), year/base dataset (e.g., baseline 2001 data).
- Temporal dimension
  - Baseline year(s) data with potential for longitudinal GIS analyses as additional data are collected.

## GIS-relevant workflows and integration ideas

- Data organization
  - Create a geodatabase or shapefiles for blocks, plots, subplots, and ECOTRON sections; attach attributes for treatment, slope position, and dominant vegetation.
  - Store horizon-level soil chemistry as related tables linked to plot records, enabling horizon-based gradient mapping.
- Visualization and mapping
  - Map vegetation community types and indicator species distribution across plots and along slope gradients.
  - Create soil property rasters by interpolating plot-level horizon data (pH, %C, %N, LOI, exchangeable Ca/Mg/K/Na) to visualize spatial gradients.
  - Overlay soil gradients with vegetation classifications to explore spatial covariation between soil chemistry and plant communities.
- Analyses and workflows
  - Gradient analyses comparing upslope vs downslope and edge effects using block positions.
  - Multivariate analyses (e.g., Twinspan) linked to spatial layers to identify spatially structured community patterns.
  - Integrate ECOTRON data with baseline Sourhope data for environmental change assessments and cross-site comparisons.
- Data integration and sharing
  - Appendices A and baseline 2001 data support longitudinal GIS analyses; ECN (Environmental Change Network) data provide cross-site comparability.
  - Ensure traceability of samples via MLURI/barcodes and connect to GIS attributes for reproducibility.

## Findings at a glance (GIS context)

- Vegetation
  - Dominant grassland communities with increasing species richness downslope; NVC alignment with Festuca ovina-Agrostis capillaris-Galium saxatile grassland.
  - Moisture gradients strongly influence bryophyte and indicator species distributions.
- Soils
  - Overall acidic, humic upland soils with horizon-depth variability and block-specific anomalies in base cations and pH.
  - Strong relationships among %N, %C, LOI, moisture loss, and pH; horizon and depth drive nutrient and carbon dynamics impacting vegetation patterns.

## Appendices and data availability

- Appendix A and related tables provide block-, plot-, and horizon-level data for soil and vegetation surveys.
- Baseline site characterization data (2001) support longitudinal GIS analyses and data integration.
- ECOTRON and block-specific datasets (Block 4 and Block 5 exemplars) illustrate horizon-level and sub-plot data structures for GIS workflows.
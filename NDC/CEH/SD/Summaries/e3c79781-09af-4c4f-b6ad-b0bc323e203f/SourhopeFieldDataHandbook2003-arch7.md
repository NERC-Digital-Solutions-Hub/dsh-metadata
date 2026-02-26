# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

- This document presents detailed soil and vegetation data for Rigg Foot, focusing on Block 4 auger samples, Block 5 site details and profiles, ecotron soil site, and associated vegetation surveys.
- Data are organized by block, plot, and horizon, with accompanying archive information and GIS-relevant attributes.

## Key Data Layers and Structures for GIS

- Block and plot boundaries
  - Block 5 site details with grid reference NT8544019520, altitude 315 m, slope 5 degrees, Imperfect drainage.
  - Major soil subgroups and rock types described for site context (Brown forest soil with gleying; andesite/igneous rock).
- Auger sampling geometry and points
  - Block 4 auger samples 4A–4F with corresponding weights, %N, %C, C:N, base cations (Ca, Na, K, Mg), moisture loss, loss on ignition, pH values (H2O and CaCl2).
  - Block 5 auger samples 5A–5F with the same suite of measurements.
  - ECOTRON plot has its own soil sample with key chemistries and pH values.
- Horizon and profile geometries for Block 5
  - Depths and horizons: LF (0–1 cm), FH (1–5 cm), H (5–7 cm), Ah (7–25 cm), AB (25–35 cm), Bg (35–49 cm), BCg (49–70 cm), Cg (70–100 cm).
  - Horizon-level descriptions (moisture, structure, root presence, stones) and color/mottling notes.
- Horizon-level chemical and physical data (Block 5)
  - Percent N, percent C, C:N ratio per horizon.
  - Cation chemistry: Ca, Na, K, Mg (meq/100 g).
  - %Moisture loss, % LOI, pH (H2O and CaCl2) per horizon.
- ECOTRON soil site data
  - Weights, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH H2O, pH CaCl2.
- Vegetation survey data
  - ECOTRON PLOT and Block 5 plots show vegetation presence/absence and species totals across subplots.
  - Block 4 and Block 5 vegetation data include per-plot and per-subplot species totals and presence of indicator/dominant taxa where recorded.
- Data provenance and archiving
  - MLURI barcodes associated with each sample (e.g., Block 4 samples 4A–4F; Block 5 samples 5A–5F; ECOTRON 1; ECOTRON vegetation entries).
  - Soil samples and analyses are archived with associated depth horizons and horizon-level metadata.

## Data Schema and Attributes (GIS applicability)

- Site and context
  - Block/Plot identifiers, grid references, altitude, slope, drainage, soil series, rock type.
  - Profile horizon set names, depth intervals, and boundary descriptions.
- Soil data by horizon
  - Horizon name, depth (cm), %N, %C, C:N, Ca (meq/100 g), Na (meq/100 g), K (meq/100 g), Mg (meq/100 g), %Moisture loss, %LOI, pH H2O, pH CaCl2.
- Physical/chemical patterns
  - Depth-related trends in nutrient content and acidity; cation balance (Ca/Mg/K/Na) across horizons; moisture and LOI correlations.
- Vegetation data
  - Plot-level and subplot-level presence/absence of species, total species counts, and notes on indicator/dominant taxa.
- Temporal and archival context
  - Barcode-linked samples; depth- and horizon-specific time-stamped data; archival storage details.

## Data Access, Quality, and Archiving

- Primary documentation references Block 4 auger samples, Block 5 site details and profiles, and ECOTRON soil/vegetation data.
- Archive identifiers and barcodes enable retrospective GIS analyses and cross-site comparisons.
- Descriptions include qualitative horizon notes and quantitative chemistry across horizons, with some horizon-level data gaps typical of field-sampling variability.

## GIS Opportunities and Recommended Products

- Depth-resolved soil maps
  - Create horizon-specific maps (0–100 cm) showing pH (H2O and CaCl2), %N, %C, C:N, and exchangeable Ca/Mg/K/Na by horizon across Blocks 4 and 5.
- Block and plot dashboards
  - Boundary polygons for Blocks 4 and 5 with attribute tables detailing site context (altitude, slope, drainage, soil series) and plot-level treatments where recorded.
- Auger sampling points and profile data
  - Point layers for 4A–4F, 5A–5F, and ECOTRON samples with attributes: horizon, depth, chemical properties, pH, LOI, moisture loss, and weight.
- Horizon-level layers
  - Polygons or line-based representations for each horizon per block, enabling depth-stratified overlays and modeling.
- Vegetation and ecological context
  - Map vegetation presence/absence and totals by plot/subplot; link to soil properties to explore soil-vegetation relationships.
- Ecotron integration
  - Separate ECOTRON layers for soil chemistry and vegetation surveys, with links to the main site layers.
- Data integration and time series
  - Combine Block 4, Block 5, and ECOTRON data to visualize spatial patterns and potential temporal changes (where time stamps exist or can be inferred).

## Notable Points for GIS Specialists

- The dataset provides multi-layer geospatial data: blocks, plots, Ecotron, nested subplots, and horizon-specific soil chemistry, enabling depth-resolved mapping and modeling.
- Vegetation data accompany soil profiles, supporting analyses of soil-vegetation relationships and NVC-like classifications where applicable.
- Horizon-level chemistry and physical properties support depth-stratified analyses and visualization (e.g., soil acidity and nutrient distribution with depth).
- Archive-ready data with MLURI barcodes and standardized horizon descriptors facilitate re-analysis and cross-site GIS comparisons.
- The combination of site context, detailed horizon data, and vegetation information allows comprehensive map-based data products for policy, client, or public-facing outputs.
# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE : BLOCK 4 AUGER SAMPLES

- Purpose and scope
  - Provides detailed chemical analyses for Block 4 auger samples (4A–4F) at Rigg Foot, Sourhope, including accompanying vegetation data where applicable.
  - Part of a broader dataset covering Block 5 and ECOTRON plots, facilitating soil-vegetation analyses and GIS-oriented mapping.

- Spatial context and data structure
  - Block 4 auger data linked to a larger Sourhope field site dataset with blocks, plots, and subplots.
  - Each auger sample has a unique MLURI barcode (4A–4F) and a set of soil chemistry and physical property measurements.
  - Data types include soil chemical properties, moisture-related metrics, pH, and texture indicators described per sample.

- Data types and key attributes (Block 4 Auger Samples)
  - Measurements per sample (4A–4F)
    - Weight (Wt in mg)
    - %N, %C, C:N ratio
    - Ca, Na, K, Mg (meq/100 g)
    - %Moisture loss, %Loss on ignition (LOI)
    - pH(H2O), pH(CaCl2)
  - Data pattern
    - N, C, C:N show modest variation across samples.
    - Major cations (Ca, Mg) and minor cations (Na, K) reported with sample-level variability.
    - Moisture-related metrics and LOI indicate organic-rich, acidic conditions typical of the site.
    - pH values reflect acidic surface conditions (approximate pH 4.5–4.8 in H2O; slightly lower in CaCl2).

- GIS-ready data products and outputs
  - Point-level soil chemistry layer
    - Each sample point (4A–4F) with attributes: Wt, %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2)
  - Horizon-agnostic summaries (for Block 4 context)
    - Use sample-level values to interpolate or summarize across plots/blocks as needed.
  - Supporting vegetation data (Block 4) for spatial context
    - Presence/absence tallies per subplot and plot, enabling GIS-based association analyses with soil chemistry.

- Practical notes on data quality and limitations
  - Data are sample-level measurements with no explicit horizon stratification in Block 4 augment data; interpretation should consider potential micro-site variability.
  - Missing or anomalous values are not indicated in the Block 4 auger table; ensure data validation before integration with broader GIS datasets.

- Related data sections (for broader GIS integration)
  - Vegetation surveys (Block 4) show species presence/absence by plot/subplot and totals, valuable for overlay with soil chemistry layers.
  - ECOTRON PLOT data provide comparable soil chemistry and vegetation observations for a controlled subplot context.
  - Block 5 data (profiles and augers) offer horizon-level attributes and deeper soil information that can be joined to Block 4 data via block/plot identifiers for regional analyses.

- GIS workflow recommendations
  - Establish a master spatial schema with blocks, plots, and subplots as polygon features; attach Block 4 auger points using MLURI barcodes as join keys.
  - Create a dedicated soil chemistry point layer from Block 4 samples (4A–4F) with the six chemical/physical attributes plus pH metrics.
  - If horizon-level data are desired, compile Block 5 and ECOTRON horizon layers and join to corresponding plots via block/plot identifiers; create horizon-specific attribute tables (Ah, AB, Bg, BCg, Cg, FH, H, etc.).
  - Build thematic maps for:
    - %N and %C distributions
    - C:N ratios
    - Ca/Mg/K/Na gradients
    - LOI and moisture loss
    - pH contrasts between H2O and CaCl2
  - Integrate vegetation data as overlay layers to analyze soil-vegetation relationships (e.g., correlation of soil chemistry with species richness or presence/absence).
  - Prepare data exports in common GIS formats (shapefiles, GeoJSON) and tabular formats for database ingestion; ensure join keys (MLURI barcode, block/plot IDs) are preserved.

- Provisional interpretation guidance for GIS analysts
  - Expect acidic, organic-rich soil conditions with notable LOI and moisture variability across Block 4 samples.
  - Use Ca and Mg values in conjunction with pH to assess soil fertility constraints and potential liming needs at specific sampling points.
  - Combine with vegetation data to explore spatial associations between soil chemistry and community composition, noting that Block 4 is part of a larger mosaic including Block 5 and Ecotron contexts.

- References and data keys
  - MLURI Barcodes: 4A–4F for Block 4 auger samples
  - Related sections for broader context: Block 5 profiles and augers, ECOTRON plots, and SV data
  - Horizon descriptors and depth context available in Block 5 profile data for cross-block horizon alignment (FH, H, Ah, AB, Bg, BCg, Cg)

- Appendices and data provenance
  - Block 4 auger data tied to sample barcodes for traceability
  - Cross-linking potential with Block 5 and ECOTRON datasets via block/plot identifiers for integrated GIS analyses
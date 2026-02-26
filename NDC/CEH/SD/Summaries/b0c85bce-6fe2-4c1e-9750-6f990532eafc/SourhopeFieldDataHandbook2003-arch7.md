# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE : BLOCK 4 AUGER SAMPLES

- Document scope
  - Presents soil composition data for Block 4 auger cores (labeled 4A–4F) and accompanying vegetation data for Block 4 in the Sourhope site.
  - Includes additional blocks and ecotron site data for context (Block 5 soil profiles, auger samples, vegetation, and ecotron plot).

- Block 4 auger samples: key variables
  - Identifiers: MLURI Barcodes for samples 4A–4F
  - Mass: Wt (mg) per sample
  - Nutrients and chemistry: %N, %C, C:N Ratio
  - Cations (meq/100 g): Ca, Na, K, Mg
  - Soil properties: %Moisture loss, %Loss on Ignition
  - Acidity/alkalinity: pH(H2O), pH(CaCl2)

- Block 4 vegetation survey: approach and outputs
  - Plot-level sampling per main plot (e.g., PLOT 4A, 4B, 4C, 4D) with species tallies
  - Dominant/indicator taxa observed (e.g., various grasses/herbs, bryophytes)
  - Species totals provided per subplot; presence/absence and abundance indications summarized per plot reference

- GIS-relevant data cues for Block 4
  - Sample points tied to auger cores (4A–4F) with horizon-context attributes
  - Link between soil chemistry (Ca, Mg, K, etc.) and vegetation components for spatial analysis

- Data quality notes
  - Values are provided per sample; some fields show sparse or partial data in tabular extracts
  - Sampling scale is at the auger-sample level; extrapolations to whole plots require careful aggregation

- Provisional GIS integration concepts
  - Create per-sample point layer: attributes include Wt, %N, %C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH(H2O), pH(CaCl2)
  - Build plot-level aggregation: mean/median soil metrics per Block 4 main plot and per subplot
  - Connect to vegetation layer: align plot/ subplot codes with species counts for ecosystem mapping

- Data provenance
  - Source: MLURI (Macaulay Institute) soil analyses; integrated with vegetation survey outputs
  - Context: Part of Sourhope Field Data Handbook 2003 dataset; GIS-ready potential for site-wide analyses

---

# SOIL PROFILE AND AUGER DATA: BLOCK 5

- Block 5 site details
  - Locational markers: Grid reference NT8544019520; Altitude ~315 m; slope ~5 degrees
  - Soils: Brown forest soil with gleying; imperfect drainage; parent material and rock context described
  - Horizon scheme in profiles: FH, F H, H, Ah, AB, Bg, BCg, Cg with depth ranges

- Block 5 soil profile (selected horizons)
  - Depths and descriptive notes per horizon (e.g., FH 0–1 cm, H 1–5 cm, Ah 7–25 cm, AB 25–35 cm, Bg 35–49 cm, BCg 49–70 cm, Cg 70–100 cm)
  - Soil descriptions include colour, texture (sandy silt loam to clay loam), structure, moisture, roots, and presence of stones

- Block 5 soil chemistry and properties (horizons)
  - Per horizon: %N, %C, C:N Ratio, Ca, Na, K, Mg (meq/100 g)
  - Moisture metrics: %Moisture loss, %Loss on Ignition
  - pH: pH(H2O) and pH(CaCl2)
  - Weight data: Wt (mg) associated with horizon samples (FH, H, Ah, AB, Bg, BCg, Cg)

- Block 5 auger samples: key variables (A–F)
  - Identifiers: MLURI Barcodes for samples 5A–5F
  - Mass and chemistry: Wt (mg), %N, %C, C:N Ratio
  - Cations (meq/100 g): Ca, Na, K, Mg
  - Moisture/ignition: %Moisture loss, %Loss on Ignition
  - Acidity: pH(H2O), pH(CaCl2)
  - Notable: horizon-type diversity and depth context implied in sample set

- Block 5 vegetation data (plots 5A–5F)
  - Species counts/totals per subplot within each main plot
  - Counts cover a range of taxa; presence/absence and relative abundance indicated
  - Subplot-level summaries used for cross-plot comparisons

- GIS-ready implications for Block 5
  - Horizon-level soil attribute layers (per horizon within blocks)
  - Auger-sample attribute table aligned to block/plot/subplot geometry
  - Vegetation tally data per subplot enabling habitat-vegetation correlations

---

# ECOTRON SITE DATA SUMMARY

- Soil site: ECOTRON PLOT
  - Soil analysis (ECOTRON PLOT 1)
    - Weight (mg), %N, %C, C:N, Ca, Na, K, Mg
    - Moisture loss, LOI, pH(H2O), pH(CaCl2)
  - Vegetation survey (ECOTRON PLOT)
    - Subplot tallies forAc, Ao, At, Br, Cp, Cxp, Dc, Df, Fo, Fr, Gs, Hm, Je, Lm, Lzm, Mc, Ns, Pe, P, etc.
    - Species totals per subplot summarized in an aggregated fashion
- GIS relevance
  - ECOTRON plots provide a baselined longitudinal context for site-wide comparisons
  - Enables temporal GIS analyses by tying ECOTRON data to baseline year and subsequent layers

---

# DATA SOURCES, ACCESS, AND ARCHIVING (GIS CONTEXT)

- Primary sources
  - MLURI soil descriptions and analyses; ECN long-term monitoring context
  - CEH Merlewood for archival storage of soil samples
- Data products and formats
  - Tabular soil chemistry, horizon data, and vegetation tallies
  - Potential for GIS layers: block/plot/subplot geometries, auger sample points, horizon attribute polygons/points, vegetation class mappings
- GIS workflow potential
  - Multi-layer integration: plot geometry with horizon-specific soil attributes and vegetation classifications
  - Spatial-temporal analyses: baseline (1998) and subsequent ECN/MLURI data overlays
  - Correlation analyses: link soil chemistry with vegetation composition across horizons and blocks

---

# Key Considerations for GIS Specialists

- Data scope and completeness
  - Some blocks/plots show partial Vegetation and Soil data in the extract; treat as indicative where gaps exist
  - Horizon descriptions and depth data vary by horizon; ensure consistent schema when integrating
- Resolution and alignment
  - Align auger-sample points with horizon layers to maintain depth-context in attribute tables
  - Maintain clear mapping between sample IDs (4A–4F, 5A–5F) and their corresponding plots/subplots
- Suggested data schema (GIS-ready)
  - Point/polygon layers: Block, Plot, Subplot geometry; ECOTRON area
  - Horizon layer: horizon_id, horizon_name, depth_start, depth_end, soil_attributes (N, C, C:N, Ca, Na, K, Mg, LOI, moisture_loss, pH_H2O, pH_CaCl2)
  - Sample layer: sample_id (4A–4F, 5A–5F, ECOTRON 1), weight, %N, %C, C:N, Ca, Na, K, Mg, moisture_loss, LOI, pH_H2O, pH_CaCl2
  - Vegetation layer: plot_id, subplot_id, species_code, count_totals
  - Metadata: data_source, year, method notes, units

Overall, the document presents a rich, multi-block, multi-layer soil and vegetation dataset with explicit soil chemistry, horizon descriptions, and vegetation tallies that are suitable for GIS-based integration and spatial-temporal analyses, including horizon-specific soil properties, auger-sample points, and plot-level vegetation classifications across Block 4, Block 5, and ECOTRON sites.
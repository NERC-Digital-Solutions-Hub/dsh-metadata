# SOIL ANALYSIS OF RIGG FOOT, SOURHOPE

- The document presents detailed soil chemistry and vegetation data for Rigg Foot, Sourhope, focusing on Block 4 auger samples and Block 5 data, including site details and an Ecotron plot.
- Includes soil profile descriptions (horizons), horizon-by-horizon chemical/physical measurements, and vegetation survey data linked to plots/subplots.
- Each auger sample is identified by MLURI barcode and labeled (e.g., 4A–4F); measurements include weight, %N, %C, C:N ratio, Ca/Na/K/Mg (meq/100g), %Moisture loss, %Loss on Ignition, pH(H2O), and pH(CaCl2).
- Block 5 provides a full soil profile (horizons LF, FH, H, Ah, AB, Bg, BCg, Cg) with detailed soil descriptions and horizon-specific chemical data.
- An Ecotron plot is included with its own soil analyses and vegetation survey data, illustrating multi-layer integration across an experimental subplot.
- Vegetation surveys accompany soil data, listing species occurrences and totals by plot/subplot, across several plots (e.g., 4A–4F, 5A–5F) with presence/absence indicators and species totals.
- Block 5 site details:
  - Grid reference: NT8544019520
  - Altitude: 315 m; slope about 5 degrees; imperfect drainage
  - Major soil subgroup: Brown forest soil with gleying; parent material: undifferentiated intermediate igneous and andesite
  - Soil profile base: lowest horizon continues
- The data are organized for GIS use with identifiers (blocks, plots, subplots, horizons) and multifaceted soil properties enabling spatial analysis of soil-vegetation relationships.

## Data structure and identifiers

- Blocks: Block 4 (auger samples) and Block 5 (soil/vegetation data); Ecotron PLOT as a separate dataset
- Sampling units:
  - Auger samples Block 4: labeled 4A–4F with corresponding MLURI barcodes
  - Block 5 soil profile: horizons FH, H, Ah, AB, Bg, BCg, Cg with depth ranges
  - Block 5 auger samples: FH, H, Ah, AB, Bg, BCg, Cg (multiple barcodes)
- Vegetation data: plots and subplots labeled (e.g., PLOT 4A, 4B, 4C, 4D, 4E, 4F; PLOT 5A, 5B, 5C, 5D, 5E, 5F; ECOTRON PLOT)
- Measurements per sample/horizon:
  - Weight (mg)
  - %N, %C, C:N ratio
  - Ca, Na, K, Mg (meq/100g)
  - %Moisture loss, %Loss on Ignition
  - pH(H2O), pH(CaCl2)

## Soil analysis highlights by block

- Block 4 auger samples (4A–4F): recorded across multiple chemical/physical metrics; data indicate horizon-level variation and mineral interactions
- Block 5 profiles:
  - Horizon sequence includes LF, FH, H, Ah, AB, Bg, BCg, Cg with horizon-specific descriptive text
  - Horizon data include %N, %C, C:N, Ca, Na, K, Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2)
  - Depths captured for each horizon (0–100 cm) and profile-wide characteristics
- Auger samples for Block 5 (5A–5F) provide horizon-anchored chemical data (N, C, C:N, Ca, Na, K, Mg) and pH values, enabling horizon-based comparisons across sub-sites
- ECOTRON PLOT:
  - Soil analysis provides weight, %N, %C, C:N, Ca, Na, K, Mg, moisture loss, LOI, pH(H2O), pH(CaCl2)
- Overall, the datasets enable linking soil chemistry and physical properties to specific plot locations and horizons for GIS analyses

## Vegetation data overview

- Vegetation surveys accompany soil data for blocks 4 and 5, including species presence/absence and totals per plot/subplot
- Example plots include:
  - PLOT 4A–4F (Block 4) with per-subplot species totals and counts
  - PLOT 5A–5F (Block 5) with species totals across several subplots
- ECOTRON PLOT vegetation data provide per-subplot species presence totals and summaries
- Vegetation data are structured to support spatial analyses of community composition in relation to soil properties and horizon depth

## GIS relevance and data layers

- Geospatial structure to map:
  - Blocks (Block 4, Block 5) and Ecotron plots with plot/subplot identifiers
  - Soil horizons per profile (depth-based layers: LF, FH, H, Ah, AB, Bg, BCg, Cg)
  - Auger sample locations linked to their block/plot/subplot
  - Site-level metadata (grid reference, altitude, slope, drainage, soil series)
  - Vegetation distributions by plot/subplot with species totals
- Data layers enable:
  - Multi-resolution mapping of soil properties by horizon across hillside transects
  - Spatial correlation analyses between soil chemistry (e.g., Ca, Mg, pH) and vegetation composition
  - Temporal analyses if repeated measurements are available (ECN-like long-term context)
- Data modeling notes:
  - Hierarchical relationships: site -> block -> plot/subplot -> horizon or sample
  - Use MLURI barcodes as unique identifiers for soil samples
  - Treat horizon depth as a vertical dimension layer in GIS/3D environments
  - Ensure units are consistent (percent nitrogen and carbon; meq/100g for cations; pH values; LOI)

## Data quality and limitations

- Some data entries are transcription-heavy and may contain gaps or formatting inconsistencies
- Block 5 provides comprehensive horizon descriptions and measurements, while Block 4 data are more sparse and horizon-specific
- Temporal context is limited in this extract; long-term trends would require repeated sampling and consistent methodologies
- The hierarchical, multi-resolution structure requires careful data modeling to preserve relationships among blocks, plots, subplots, horizons, and vegetation data

## GIS-driven workflows and recommendations

- Data ingestion:
  - Import barcoded samples (4A–4F; 5A–5F; ECOTRON 1) and link to corresponding plots, subplots, and horizons
  - Create horizon-specific layers with depth attributes for 3D visualization
- Data schema:
  - Entities: Site, Block, Plot, Subplot, Horizon, Sample, VegetationCategory
  - Attributes: depth, horizon name, %N, %C, C:N, Ca/Na/K/Mg, %Moisture loss, %LOI, pH(H2O), pH(CaCl2), species counts
- GIS analyses:
  - Spatial interpolation of soil properties across plots
  - Correlation/association analyses between soil chemistry and vegetation indicators
  - Habitat classification by soil type and horizon characteristics
  - Time-series visualization if additional blocks/years are added
- Visualization:
  - Choropleth maps of horizon-level pH, Ca, Mg, or LOI by plot/subplot
  - 3D cross-sections along the hillside showing horizon depth and soil properties
  - Overlay of vegetation totals with soil gradients to identify habitat associations

## Key takeaways for GIS Specialists

- The dataset offers a rich, multi-layered, horizon-resolved soil and vegetation dataset for Rigg Foot, Sourhope, suitable for advanced GIS analyses of spatial patterns and soil-vegetation interactions along a hillside transect.
- Clear geospatial linkage is possible through blocks, plots/subplots, horizons, and MLURI barcodes, enabling detailed mapping of soil chemistry and vegetation distributions.
- The inclusion of site-level metadata (grid reference, altitude, slope, drainage) enhances contextual mapping and supports integration with climate or environmental change datasets.
- Proper GIS implementation requires careful handling of hierarchical relationships, consistent units, and attention to data quality issues and potential gaps in the transcription.
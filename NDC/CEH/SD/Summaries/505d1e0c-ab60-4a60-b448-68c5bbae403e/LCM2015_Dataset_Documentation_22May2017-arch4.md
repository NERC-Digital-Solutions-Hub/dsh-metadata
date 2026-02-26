# Dataset documentation

- Overview
  - Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map classifying satellite imagery into 21 Broad Habitat classes (based on UK Biodiversity Action Plan definitions).
  - Built from two-date Landsat-8 (30 m) composites, with AWIFS data (60 m) as required; updates the 2007 map (LCM2007) within the same spatial framework, reflecting a move toward change mapping readiness.
  - Data are delivered as multiple products: a core vector dataset, a 25 m raster, and 1 km percentage/dominant cover products (GB and Northern Ireland separated due to different projections).

- Data products and structure
  - Core vector dataset: polygons with rich attributes for each parcel (gid, dominant class, pixel counts per class, uncertainty, modal class, etc.). Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 25 m raster: two-band image per area; band 1 = dominant LCM2015 class per polygon, band 2 = mean per-polygon classification probability.
  - 1 km raster products: aggregated from the 25 m raster to provide dominant cover and percentage cover for both 21 classes and 10 aggregate classes (GB and NI separate).
  - Class mapping: 21 LCM2015 target classes aligned with Broad Habitats; some broad habitat groups are subdivided in the raster products (e.g., Urban/Suburban, Heather/Heather grassland, Littoral subdivisions).
  - Metadata and uncertainty: polygon-level metadata includes dominant class, counts of pixels per class, mean probability (uncertainty), and a per-polygon gid for unambiguous communication; 25 m raster band 2 provides per-polygon mean probability.

- Data access and citation
  - GB 1 km raster data are available via the CEH Environmental Information Platform (EIP).
  - The full vector and 25 m raster products are available on request under licence from CEH; some users may incur licence fees.
  - All LCM2015 products have DOIs for citation; guidance provided on how to cite (authors, date, and DOI) in publications.
  - Coordinate systems: GB products in British National Grid; NI products in TM75 Irish Grid.

- Methodology and key differences from earlier maps
  - Classification algorithm: new Random Forest classifier (replaces maximum likelihood); handles multi-model training data and reduces need for spectral sub-classes.
  - Training data: uses a stable core set of training areas (areas classified the same in 2000 and 2007) plus additional coastal and difficult classes; ancillary data (when needed) is integrated into input data rather than applied post-classification.
  - Ancillary data integration: in LCM2015, ancillary data are used as input features, making knowledge-based adjustments objective and integral to the process.
  - Spatial framework and segmentation: no segmentation-based polygons in LCM2015; per-pixel classification with a fixed per-polygon aggregation later; segmentation used in LCM2007 to break up large upland polygons was removed to simplify change mapping.
  - Output data changes: montane class removed (reclassified as Inland Rock or other upland habitats); rough grassland removed (aligns grassland types with JNCC Broad Habitats); 25 m raster becomes a two-band image; probability data simplified (mean probability per polygon in vector and in band 2 of 25 m raster); mixed woodland training uses pixel-based classification with modal class applied at polygon level.
  - Classification scope: LCM2015 maps land cover (not land use); includes 21 target classes plus several aggregations for 1 km products.

- Classification and data quality notes
  - LCM2015 cautions: differences between LCM products over time arise from real change, classification error, and evolving data standards; differences across years should be interpreted carefully; LCM2015 is not recommended for current-state change mapping without careful validation.
  - Uncertainty information: Random Forest provides per-pixel probability estimates; these are included as per-polygon uncertainty values and in the 25 m raster band 2.

- Class definitions and mapping framework (highlights)
  - 21 LCM2015 target classes include Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grasslands, Bracken, Dwarf Shrub Heath (Heather/Heather grassland), Fen/Marsh/Swamp, Bog, Standing Open Water, Rivers/Streams, Montane, Inland Rock, Built-Up Areas and Gardens (split into Urban and Suburban), Supra-littoral/Littoral rock and sediment, Saltmarsh, Urban/Suburban distinctions, and related coastal/shoreline classes.
  - Appendix-style notes in the documentation provide definitions aligned with JNCC Broad Habitat classifications and discuss spectral interpretation limits, especially for mixed habitats and transitional vegetation.

- Documentation and supplementary information
  - Extensive appendix material covers class mapping specifics, colour mappings, composite image usage, and citation details.
  - The dataset is archived with stable identifiers (DOIs) to support reproducibility and reuse in scientific and policy contexts.
  - Related resources and contact points are provided for further information and access.

- Practical implications for data leadership
  - LCM2015 offers a robust, well-documented, multi-resolution set of land cover products suitable for wide-ranging analyses, modelling, and reporting, with clear data lineage and uncertainty measures.
  - The dataset supports co-ownership and user-centered product evaluation through rich metadata and explicit guidance on product choices (vector vs raster vs aggregated 1 km outputs).
  - Governance considerations include managing licensing, citing DOIs, aligning with UK Broad Habitat classifications, and planning for data integration across GB and NI given projection differences.
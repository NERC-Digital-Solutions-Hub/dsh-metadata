# Dataset documentation

- Land Cover Map 1990 (LCM1990) dataset documentation describing the 1990 UK land cover data products, their generation, structure, metadata, quality assurance, access, and usage considerations.

## Purpose and scope
- Provides a parcel-based land cover map for the UK classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from two-date Landsat-5 composite imagery (30 m resolution) to enable analysis of land cover and change in a consistent framework.
- Reuses and aligns with the LCM2007/LCM2015 spatial framework to maximize compatibility and enable potential long-term change products (e.g., 1990–2015 change analyses).
- Clarifies that LCM1990 maps land cover (not always directly interpretable as land use).

## Data products and structure
- Core data products:
  - Vector data set: parcels (polygons) with rich per-polygon attributes; 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 25 m raster: derived from the vector data; three bands (dominant class per polygon, mean per-polygon classification confidence, and percentage cover of the modal class).
  - 1 km raster products: derived by aggregating 25 m data to provide dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
- Class structure:
  - 21 target LCM1990 classes aligned to Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - 1 km products include both target-class and aggregate-class representations; areas mapped as >0.5 ha minimum; smaller parcels dissolved into surrounding landscape.
- Attributes and metadata:
  - Vector attributes include gid (unique parcel ID), hist (list of classes with pixel counts within each polygon), mode (recommended dominant class), purity, conf (per-polygon mean classifier confidence), stdev, n (number of pixels), and cmp (composite image index).
  - Rich polygon metadata and per-polygon probability from the Random Forest classifier.
- Output formats and coordinate systems:
  - Vector data with detailed attributes; 25 m and 1 km raster products provided as uncompressed GeoTIFFs.
  - GB projections: British National Grid; NI projections: Irish Grid (TM75).

## Data quality, uncertainty, and validation
- Uncertainty information:
  - Random Forest classifier provides per-pixel probability; included as mean per-polygon value (vector) and in the 25 m raster band 2.
- Quality assurance:
  - QA checks for projections, spatial completeness, modal class presence, attribute consistency, value ranges (0–100 for rasters), and pixel size accuracy.
- Validation:
  - Full validation performed against other datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.
- Classification caveats:
  - LCM1990 is complex; some land cover types (e.g., certain grassland classifications, swamp/fen mixes) may be misclassified spectrally or due to patch size and spectral similarity.
  - LCM1990 captures land cover, not always reliable land-use distinctions.

## Data access, licensing, and citation
- Data access:
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (EIP).
  - Full vector product available on request from CEH; licences may apply.
- Data governance and reuse:
  - All LCM1990 products have individual DOIs for citation; recommended to cite DOIs to ensure reproducibility and track usage.
  - Example citation formats are provided for Great Britain and Northern Ireland products; include author/date and DOI in references.
- Licences and fees:
  - Licence fees may apply for some users and applications.

## Data governance and use in monitoring contexts
- Suitability for monitoring frameworks:
  - Provides a stable, archived land cover baseline for the UK at high spatial detail (25 m) with complementary 1 km products for regional modelling.
  - Facilitates cross-product comparability with LCM2007 and LCM2015, enabling historical trend analyses and integration into monitoring dashboards and policy evaluations.
  - The vector product’s rich metadata and per-polygon uncertainty support transparent data quality assessment and governance.
- Temporal and spatial considerations:
  - Baseline dataset for 1990; designed to support integration with later LCM products and potential 1990–2015 change analyses.
  - Spatial framework ensures alignment with other CEH land cover products and compatibility with additional environmental datasets (e.g., meteorological or species distribution data).

## Usage guidance and interpretation
- Land cover vs. land use:
  - Users should treat LCM1990 as land cover. Some land-use inferences (e.g., recreation grasslands) may be ambiguous and require auxiliary data.
- Minimum mapping unit and aggregation:
  - Minimum mappable area >0.5 ha; very small parcels and narrow features are dissolved or generalized.
  - 1 km rasters represent percentage or dominant cover at coarse scale, useful for regional modelling and integration with other coarse-resolution datasets.
- Data handling tips for monitoring:
  - Retain the gid field in vector products to preserve unique parcel identities for reproducibility and linkage to ancillary data.
  - Use per-polygon uncertainty (conf) to weight or filter analyses where confidence is low.
  - When aggregating to 1 km, be aware of rounding effects that may cause sums to deviate slightly from 100% and coastal area underestimation.

## Appendices and additional information
- Appendices provide:
  - Detailed Broad Habitat (JNCC) definitions and mapping considerations to aid class interpretation.
  - Color mapping recipes for LCM1990 classes.
  - Composite image information used in the classification process.
- Citing and further information:
  - DOIs and example data citations are provided; contact CEH for access details and licensing.
  - Data may be complemented by related LCM change products (e.g., 1990–2015 datasets) for broader monitoring applications.
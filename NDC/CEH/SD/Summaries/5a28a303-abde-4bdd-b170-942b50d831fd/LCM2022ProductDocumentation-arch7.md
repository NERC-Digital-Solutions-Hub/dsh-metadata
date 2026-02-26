# The UKCEH Land Cover Map for 2022

- UKCEH produces LCM2022, the tenth UK land cover map, classified at 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP) definitions.
- Product suite includes seven datasets: three per region (Great Britain and Northern Ireland) consisting of 10 m classified pixels, land parcels, and 25 m rasterised land parcels, plus a 1 km summary raster across GB and NI.
- Data production combines Sentinel-2 Seasonal Composite Images with Context Rasters and uses Bootstrap Training with a Random Forest classifier; annual production supports change detection and temporal consistency.
- Formal validation reports an overall accuracy of 86.1% at full thematic detail.

## Data products and structure

- 10 m Classified Pixel datasets (GB and NI)
  - Output: two-band rasters per location
    - Band 1: most likely UKCEH Land Cover Class (integer)
    - Band 2: class membership probability/confidence
  - Not generalised by Land Parcel Spatial Framework to preserve fine landscape detail; validation aligned to 25 m parcel dataset.
- Land Parcel datasets (GB and NI)
  - Generate land parcel attributes by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised from the Land Parcel datasets; three-band rasters:
    - Band 1: dominant land cover class (_mode)
    - Band 2: mean probability/confidence (_conf)
    - Band 3: parcel purity (_purity)
- 1 km Summary rasters (GB and NI)
  - Summary products: dominant class at 1 km; dominant aggregate class; and percentage cover per class and per aggregate class (integer values; sums may deviate from 100 due to rounding and coastal omissions).
- Seasonal Composite Images
  - Derived from Google Earth Engine; Sentinel-2 reflectance resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Some gaps due to cloud, but classification tolerates partial spectral information.
- Context Rasters (10 m)
  - Resolve spectral confusion with features such as terrain, proximity to roads/buildings, water, foreshore, woodlands, etc.
  - GB: height, aspect, slope; distance to nearest building, road, tidal water, freshwater; foreshore, woodland, and saltmarsh masks.
  - NI: height, aspect, slope; urban mask; distances to coast, freshwater, road; foreshore and tidal water masks.
- Classification Scenes
  - GB: 32 GB Classification Scenes (tiles ~100 x 100 km) for full GB coverage; each scene trained and classified independently.
  - NI: single 49-band Classification Scene (40-band Sentinel-2 Seasonal Composite plus NI Context Rasters).
- The UKCEH Land Parcel Spatial Framework
  - A fixed 0.5 ha minimum mapping unit; parcels derived from generalised national cartography to reduce noise and support change detection.
  - Parcel identifiers (gid) are not the same as LCM2015; useful for time-series comparisons may be limited by identifier changes.
- Bootstrap Training
  - Automated training using historical LCM products (2019–2021) with >80% probability and consistent class across years.
  - Large bootstrap training set improves learning; some crops with rotations (arable vs. improved grassland) may require alternative training data.
- Random Forest classification
  - Balanced sampling: 10,000 samples per class per training bag.
  - Custom, in-house software integrating Weka, PostGIS, and GDAL; uses Bootstrap Training to drive RF classification.
- Validation and accuracy
  - 33,107 validation points, covering all 21 classes, compiled from GB countryside survey, open data inventories, and bespoke validation points.
  - Overall accuracy: 86.1%; Producer’s and User’s accuracies vary by class (detailed matrices provided in Appendix 4).
- Known issues
  - A small number of polygons missing from vector land parcel products; 25 m rasterised parcels and 1 km rasters may be affected, but 10 m classified pixels are unaffected.

## Dataset specifications and access

- Coordinate systems
  - Great Britain: British National Grid, EPSG 27700
  - Northern Ireland: TM75 Irish Grid, EPSG 29903
- Extents and parcels
  - GB Land Parcel extents and counts provided; NI extents scoped to the Northern Ireland grid with parcel counts listed.
- Dataset naming and DOIs
  - Each LCM2022 dataset has a DOI; citations include Marston et al. (2024) for the production methods and the individual dataset DOIs for 10 m classified pixels (GB and NI), 25 m rasterised land parcels (GB and NI), land parcels (GB and NI), and 1 km summary rasters.
- Citing guidance
  - Users should cite the corresponding DOIs for the data products; see Table 5 in the document for exact references.

## Data interpretation and use

- UKCEH Land Cover Classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes are related to, but not identical with, UK BAP Broad Habitats; some mappings require italicising BAP terms to avoid ambiguity.
  - Appendix 1 and Appendix 2 provide detailed notes on class definitions, potential spectral confusion, and the relationship to BAP Broad Habitats.
- Common interpretation considerations
  - Spectral confusion between similar vegetation and non-vegetated surfaces; context rasters and training data mitigate some confusion but some overlap remains (e.g., Bog vs. Acid grassland, Ferns vs. Bracken).
  - Coastal zones, tidal waters, and water bodies have complexities; Saltwater is less prioritized and may show lower accuracy in some coastal zones.
- Data presentation
  - Appendix 5 and Appendix 6 provide color recipes (including color-blind friendly options) for displaying the 21 UKCEH Land Cover Classes and related legends.
  - A QGIS symbology file is provided alongside data products to facilitate ready map creation.

## Practical notes for GIS work

- Data handling
  - 10 m Classified Pixels preserve fine landscape features but require careful interpretation due to no cross-zone generalisation; suitable for detailed mapping and feature-level analysis.
  - 25 m Rasterised Land Parcels provide a balanced, noise-reduced representation suitable for time-series comparisons and change detection.
  - Land Parcel Spatial Framework enables parcel-based analysis and aggregation; be mindful of MMU and identifier changes since LCM2015.
- Validation and quality
  - Expect some class-level variability due to spectral similarity; refer to Appendix 4 for per-class producer’s and user’s accuracies and confusion notes.
- Change detection and time series
  - Annual production supports distinguishing persistent land cover changes from annual classification noise; Bootstrap Training uses recent maps to train new classifications.

## References and further reading

- Marston et al. (2024) – Land Cover Map 2022 data product papers (10 m classified pixels, 25 m rasterised land parcels, land parcels, vector land parcels, 1 km summary rasters).
- Supporting appendices with UKCEH Land Cover Classes, BAP Broad Habitats definitions, dataset lists, correspondence matrices, and color schemes.
- Key methodological references: Breiman (Random Forest), Carrasco et al. (seasonal composites in GEE), Morton et al. (LCM2007 framework), Jackson (BAP habitat guidance).
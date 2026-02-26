# The UKCEH Land Cover Map for 2021

## Overview and purpose
- UKCEH LCM2021 is the ninth UK land cover map, produced annually to improve temporal consistency and change detection.
- Product comprises six geospatial datasets (three for Great Britain and three for Northern Ireland):
  - 10 m Classified Pixel dataset
  - Land Parcel Spatial Framework (land parcel dataset)
  - 25 m Rasterised Land Parcel dataset
  - (For NI, the same three dataset types; in addition there are 1 km summary products derived from 25 m data)
- The guide explains data production, validation, and data accuracy to enable informed use and future updates.
- Aims align with governance of large-scale datasets: maintain standards, metadata, and mechanisms for updates and discovery.

## Data governance, standards, and access
- Datasets follow defined coordinate systems:
  - Great Britain: British National Grid, EPSG 27700
  - Northern Ireland: Irish Grid, EPSG 29903
- Data extents:
  - GB: full extent within 0–700000 East, 0–1300000 North (metres)
  - NI: truncated Irish Grid extent
- Land Parcel Spatial Framework:
  - minimum parcel area ~0.5 ha (MMU)
  - designed for discrete real-world units (fields, parks, urban areas, etc.)
  - unique parcel identifiers (gid) may not match LCM2015 identifiers; not always directly cross-comparable by id
- Data portals and dissemination:
  - datasets are uploaded to appropriate portals; metadata documented
  - 10 m pixel data preserve fine details (not generalized by the Land Parcel Framework)
- Documentation and governance artifacts:
  - Glossaries, appendices (UKCEH vs BAP Broad Habitats mappings), dataset lists, and color recipes are provided to aid consistent use and interpretation
- Data stewardship implications:
  - annual production supports change detection and temporal comparability
  - if new methods yield significant improvements, UKCEH may re-apply across the entire catalogue

## Data production and processing workflow
- Classification approach:
  - Bootstrap Training: automatic training data generation from historic maps (LCM2018–LCM2020) to seed classifier training
  - Random Forest classifier used to assign land cover classes
  - Training data are filtered for high purity (>80%) and cross-year consistency
  - Balancing across classes achieved by sampling with replacement (10,000 samples per bag)
- Seasonal information and context:
  - Seasonal Composite Images derived from Sentinel-2 (4 seasons) with 10-band spectral information
  - Context Rasters (GB: 10 layers; NI: 9 layers) provide terrain, proximity to features (buildings, roads, coast, water), and other contextual cues to reduce spectral confusions
- Classification Scenes and tile structure:
  - GB used a grid of ~100 km tiles (Classification Scenes) to classify 32 scenes across GB
  - NI used a single 49-band Classification Scene due to smaller area
- Data products by type:
  - 10 m Classified Pixel datasets: mosaic of Classification Scenes; first band = most likely UKCEH Land Cover Class; second band = associated class probability (confidence)
  - Land Parcel datasets: intersect 10 m pixels with the UKCEH Land Parcel Spatial Framework to generate land parcel attributes
  - 25 m Pixel Rasterised Land Parcels: rasterised version of land parcels; 3-band raster carrying per-parcel dominant class, mean confidence, and purity
  - 1 km raster products: summarised 25 m data to compute dominant class and percentage cover per 1 km pixel (with rounding)
- Validation and quality checks:
  - Validation dataset: 35,182 reference points spanning all 21 classes
  - Overall accuracy: 82.6% (95% CI: 82.19%–82.99%)
  - Validation data for 25 m rasterised parcels; the 10 m classified pixels are not independently validated against the parcel framework
- Software and tooling:
  - Custom UKCEH pipeline integrating Weka, PostGIS, and GDAL; open-source components used for reproducibility

## Dataset descriptions and structure
- 10 m Classified Pixel datasets (GB and NI):
  - Pixel-level classifications with two bands: class identifier (UKCEH Land Cover Class) and associated probability/confidence
  - Not generalized by the Land Parcel Spatial Framework to preserve fine landscape features
- Land Parcel datasets (GB and NI):
  - Attributes include hist (history of class occurrence within parcel), mode (dominant class), conf (mean confidence), stdev (confidence variability), agg (aggregate class), and n (number of 10 m pixels per parcel)
- 25 m Rasterised Land Parcel datasets (GB and NI):
  - 3-band rasters per parcel: dominant land cover class (mode), mean confidence (conf), and purity
- 1 km rasters:
  - Dominant class per 1 km pixel (21-class and 10-class aggregations)
  - Percentage cover per 1 km pixel for 21-class and 10-class aggregations; values rounded to integers
- Seasonal Composite Images and Context Rasters:
  - 10-band context rasters and 40-band Sentinel-2 seasonal composites (GB) or 49-band scene for NI
  - Bands cover coastal, vegetation, and atmospheric/solar geometry features
- Dataset naming and identifiers:
  - Official dataset names and documentation provided in Appendix 3
  - Some cross-version identification changes noted for parcel identifiers (gid)

## Classification specifics and semantic mappings
- UKCEH Land Cover Classes (21 classes) map to Biodiversity Action Plan (BAP) Broad Habitats (where applicable)
  - Class naming uses UKCEH convention; BAP terms italicised when explicitly referenced
  - Appendix 1/2 provide the crosswalk and notes on areas of potential spectral confusion (e.g., Bracken vs Acid Grassland; Heather vs Heather Grassland; Bog vs other upland vegetation)
- Note on uncertainties and spectral confusion:
  - Saltwater vs Freshwater distinctions are weaker and often rely on coastal context rasters
  - Small water bodies under MMU may be omitted unless aligned with criteria
  - Linear features (hedgerows, walls, etc.) are not classified by shape; limited to narrow features visible in 10 m data
- Complementary content:
  - Appendix 5/6 provide color recipes for display and color-blind friendly palettes to support map interpretation

## Validation, accuracy, and limitations
- Validation details provide an overall accuracy figure with confidence interval
- The main validation outcome applies to the 25 m Land Parcel raster dataset; 10 m classified pixels are not independently cross-validated against parcel-level outcomes
- Users should consider potential spectral confusions and the MMU when interpreting fine-scale patterns, especially around:
  - Bracken vs Acid Grassland
  - Heather vs Heather Grassland
  - Fen, Marsh and Swamp vs Bog
- The guide emphasizes that while annual updates improve temporal consistency, random classification errors will flicker over time, whereas real land-cover changes persist

## Change management, updates, and data stewardship considerations
- LCM2021 is designed to support annual updates; improvements may be rolled out across the full catalogue
- The time-series nature helps separate true changes from random errors
- Cross-version comparisons should account for changes in parcel identifiers and the Land Parcel Spatial Framework
- Data stewards should document any methodological changes, dataset scope shifts, and validation updates to preserve traceability

## Practical use and caveats for Data Stewards
- The 10 m Classified Pixel dataset provides high-detail representation suitable for specialist analysis; analysts should understand that its validation is not tied to parcel-level classifications
- The Land Parcel Spatial Framework adds a robust, consistent basis for change detection, but parcel IDs may differ from earlier releases
- When disseminating, ensure the appropriate color schemes are used (Appendix 5) and consider color-blind palettes (Appendix 6)
- For cross-temporal studies, prefer the 25 m parcel-based products and 1 km summary products for robust change detection and aggregation

## Appendices and documentation (summary)
- Appendix 1: Notes on UKCEH Land Cover Classes with BAP Broad Habitats relationships and detailed class notes
- Appendix 2: Summary of BAP Broad Habitats and their remote-sensing considerations
- Appendix 3: Full list of LCM2021 datasets by region and product type
- Appendix 4: Correspondence matrices (cross-tabulation) between UKCEH classes and BAP broad habitats, including accuracy metrics
- Appendix 5: Recommended color recipes for displaying UKCEH Land Cover Classes
- Appendix 6: Color-blind friendly color recipes for displaying UKCEH Land Cover Classes

## Key takeaways for data governance and use
- LCM2021 offers a robust, annually updated set of six geospatial datasets (GB and NI) with multiple representations (10 m pixels, land parcels, 25 m rasters, and 1 km summaries)
- The workflow combines Bootstrap Training and Random Forest classification, enhanced by Seasonal Composite Images and Context Rasters to address spectral confusion
- Validation yields an overall accuracy of 82.6%, with detailed appendix material documenting cross-walks to BAP habitats and class-specific considerations
- Data stewardship should maintain metadata integrity, document methodological updates, and provide guidance on the appropriate use cases for each data type (high-detail 10 m vs parcel-based products and 1 km summaries)
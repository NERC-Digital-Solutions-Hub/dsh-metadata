# The UKCEH Land Cover Map for 2023

## Purpose and scope
- User guide for UKCEH Land Cover Map 2023 (LCM2023), detailing data production, validation, accuracy, and guidance for informed use.
- LCM2023 comprises seven datasets: three for Great Britain (GB) and three for Northern Ireland (NI) plus a 1 km summary raster product.
  - For each region: a 10 m classified pixels dataset, a land parcel dataset, and a 25 m pixel rasterised land parcels dataset.
- Aim: enable informed decisions about current applications and future updates of UKCEH LCM data; provide insight into data structure, metadata, and quality.

## Key outputs and data products
- 10 m Classified Pixel datasets ( GB and NI )
  - Derived from Classification Scenes using Bootstrap Training and Random Forest.
  - Band 1: dominant UKCEH Land Cover Class; Band 2: associated class probability (confidence).
- Land Parcel datasets (GB and NI)
  - Result of intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised version of land parcels carrying per-parcel attributes: dominant land cover (mode), conf, and purity.
- 1 km raster products (GB and NI)
  - Summary rasters: dominant class at 1 km; percentage cover per class (and per aggregate class); note rounding may cause sums to deviate from 100%.
- Spatial framework and metadata
  - UKCEH Land Parcel Spatial Framework; parcels have a minimum area of ~0.5 ha (MMU) and are designed to represent discrete real-world units.

## Classification methodology and data sources
- Seasonal Composite Images
  - Derived from Sentinel-2 data (10 m), with four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec; spectral bands listed in the guide.
  - Contextual information (Context Rasters) reduces spectral confusion.
- Classification Scenes and tiling
  - GB: 32 Classification Scenes (tiles ~100 x 100 km) trained and classified independently; some edges/overlaps exist.
  - NI: single Classification Scene (44-band) due to smaller area.
- Bootstrap Training
  - Automated training using historic LCM maps (LCM2020–LCM2022) with >80% probability and consistent class across three years; used to sample training observations for classifier.
  - Addressed data gaps and limited fresh field data; some crops (e.g., arable vs improved grassland) may rely on Crops dataset when Bootstrap Training is less effective.
- Random Forest classifier
  - Balances class representation by sampling with replacement to ensure even learning across classes.
  - Software stack includes bespoke UKCEH tools, WEKA, PostGIS, and GDAL (open source).

## Data structure and land cover classification
- 21 UKCEH Land Cover Classes
  - Based on Biodiversity Action Plan (BAP) Broad Habitats; mappings provided with notes on relationships and occasional deviations.
  - Tables and appendices explain correspondences between UKCEH classes, BAP Broad Habitats, and Aggregate Classes.
- Context and auxiliary layers
  - 10 m Context Rasters (terrain, proximity to buildings/roads/water, foreshore, woodland, etc.) supplement spectral data to improve classification.
- Classification and output format
  - 10 m Classified Pixels: first band is class identifier; second band is class membership probability/confidence.
  - 25 m Rasterised Land Parcels: three bands per parcel (dominant land cover mode, conf, purity).
  - 1 km rasters: dominant class and percentage cover per class; breakdowns for both class and aggregate class schemes.

## Validation, accuracy, and quality
- Independent validation
  - 33,107 validation points covering all 21 classes from GB and NI; data sources include countryside surveys, National Forest Inventory, Rural Payments data, and expert points.
- Overall accuracy
  - 83% accuracy at full thematic detail (LCM2023).
- Class-level performance
  - Detailed confusion/producer’s/user’s accuracy matrices provided in Appendix 4 (maps of misclassification by class).
- Known issues related to validation
  - Some discrepancies between 25 m parcel predictions and 10 m pixel classifications due to different aggregation scales.
  - Some spectral/habitat confusion remains (e.g., certain grassland types, bog, heath, and peat-related classes).

## Data governance, accessibility, and citations
- Data citation and DOIs
  - Each LCM2023 dataset has its own DOI; recommended to cite Marston et al. (2023–2024) and related dataset records when using products.
- Documentation and dissemination
  - Outputs are accompanied by descriptive metadata, documentation of production methods, and a user guide to support appropriate use and interpretation.
- Updates and versioning
  - UKCEH emphasizes continuous development; method changes can lead to genuine changes in land cover as well as changes due to classification methods.

## Practical use for monitoring policy, management, and decision-making
- Monitoring change and state of the countryside
  - Annual LCMs enable distinction between real land-cover change and random mapping errors (errors tend to flicker over time).
  - 1 km summary rasters enable large-area summaries; 10 m data capture fine-scale patterns and small patches (below 0.5 ha MMU).
- Indicators and decision-support
  - Use percentages or dominant classes to track temporal trends in land cover types aligned with policy objectives (e.g., woodland, arable land, grassland types, urban expansion, wetlands).
  - Combine with context rasters to improve detection of habitat types that are spectrally similar.
- Data integration and governance for monitoring frameworks
  - Metadata, data provenance, and data-sharing considerations are highlighted; data can be linked with governance processes to ensure datasets meet standards and are openly accessible where appropriate.
  - The dataset suite supports dashboards, reports, and change-detection analyses across GB and NI.

## Limitations and known issues
- Data completeness and accessibility
  - Occasional missing polygons in vector Land Parcel products; minimal impact on 1 km rasters but could affect parcel-level analyses.
- Classification uncertainties
  - Some habitat types (e.g., bog, fen, heather, neutral grassland) exhibit interclass confusion; reliance on Context Rasters and Bootstrap Training helps but does not eliminate confusion.
- Temporal and methodological changes
  - Method variations across years mean some apparent differences may reflect changes in methodology rather than real land-cover change.
- Cross-version comparability
  - In LCM2023, gid identifiers in the Land Parcel Spatial Framework may not align with LCM2015/earlier datasets, affecting direct cross-map parcel comparisons.

## Appendices and supplementary information (highlights)
- Appendix 1 and 2
  - Notes on UKCEH Land Cover Classes and detailed BAP Broad Habitat definitions; guidance on how classes relate to BAP concepts and potential ambiguities.
- Appendix 3
  - Full list of LCM2023 datasets with DOIs and citation guidance per region and product type.
- Appendix 4
  - Correspondence (confusion) matrices detailing agreement between observed validation classes and predicted classes, plus accuracy statistics.
- Appendix 5 and 6
  - Recommended colour schemes for displaying UKCEH Land Cover Classes, including color-blind-friendly options; accompanying QGIS symbology files.
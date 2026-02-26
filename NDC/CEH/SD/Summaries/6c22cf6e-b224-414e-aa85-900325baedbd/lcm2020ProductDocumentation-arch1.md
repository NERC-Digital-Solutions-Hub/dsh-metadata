# The UKCEH Land Cover Map for 2020

## Overview
- The document is a user guide for LCM2020, the UKCEH land cover map for 2020.
- LCM2020 consists of six datasets: three for Great Britain and Northern Ireland each (a 10m Classified Pixel dataset, a Classified Land Parcel dataset, and a 25m Rasterised Land Parcel dataset; NI uses a 20m Classified Pixel dataset in place of the 10m for GB in some parts).
- Purpose: describe data production, validation, and accuracy to help users apply LCM data effectively and understand limitations.

## Product Components and Datasets
- GB datasets (three per region):
  - 10m Classified Pixel dataset: pixels classified into UKCEH Land Cover Classes; includes a confidence/probability band. Not generalised by the Land Parcel Spatial Framework to preserve fine landscape detail.
  - Land Parcel dataset: results from intersecting 10m pixels with UKCEH Land Parcel Spatial Framework; includes parcel-level attributes.
  - 25m Rasterised Land Parcel dataset: per-parcel raster with three bands (dominant class, mean confidence, and purity).
- NI datasets (three per region):
  - 20m Classified Pixel dataset (instead of GB’s 10m in some areas).
  - Land Parcel dataset (parcel-level attributes).
  - 25m Rasterised Land Parcel dataset.
- Full dataset list and naming are provided in Appendix 5.

## The Data and Land Cover Classes
- LCM2020 uses 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Classes are mapped against BAP Broad Habitats with defined relationships; some cross-class distinctions exist (e.g., Urban vs Suburban; Saltwater vs Freshwater), and italicisation is used to distinguish BAP terms when referenced.
- The product enables detailed land cover mapping with both full thematic classes and aggregated forms (as described in the appendices).

## Methods and Data Production
- Sentinel-2 Seasonal Composite Images: four seasons (winter, spring, summer, autumn) derived from Sentinel-2 surface reflectance data, resampled to 10 m or pixel-equivalent, using nine spectral bands.
- Context Rasters: 10m GB context rasters (terrain, proximity to buildings/roads/coast/freshwater, foreshore, tidal water, woodland) to reduce spectral confusion. NI context rasters include urban mask and proximity layers.
- Classification Scenes: GB uses 100x100 km overlapping tiles (36-band Seasonal Composite Images plus 10 Context Rasters, total ~46 bands) to generate Classification Scenes; 74 overlapping scenes classified independently and merged with manual precedence in overlaps. NI uses a single 43-band scene per year (36-band Sentinel-2 plus NI context rasters).
- Bootstrap Training: automatic, self-starting training using historic LCM data (LCM2017–2019) with high purity (>99%) to generate training data; used to bootstrap the RF classifier for 2020. This leverages long-term wall-to-wall coverage to balance learning and reduce the need for fresh field data.
- Random Forest Classification: supervised learning using balanced training data; 10,000 samples per class per bag; implemented with bespoke UKCEH software integrating Weka, PostGIS, and GDAL (open source).
- Land Parcel Spatial Framework: parcels are fixed units (~0.5 ha MMU) derived from generalised national cartography to support change detection and parcel-based analysis; identifiers (gid) differ from LCM2015 to reflect framework updates.

## Validation and Accuracy
- Validation approach: compared LCM2020 outputs with GB Countryside Survey (2019–2020), National Forest Inventory, IACS data, and bespoke validation points (34,715 points total) intersected with Land Parcel datasets.
- Overall accuracy: 79.2% at full thematic detail (Appendix 4). Validation details include producer’s and user’s accuracy by class and confusion matrices.

## Practical Use and Interpretation
- Pixel vs Parcel data: 
  - 10m Classified Pixel data preserves fine detail but is not generalised to Land Parcel Framework; best for specialists who understand the implications.
  - Land Parcel datasets provide parcel-level attributes and facilitate change detection and aggregation, with validated accuracy reported at the parcel level.
  - 25m Rasterized Parcel datasets provide per-parcel rasters and per-parcel statistics (mean probability, purity).
- Time-series and change detection: annual production enables differentiation between random classification errors and real land cover change; persistent changes indicate real dynamics.
- Data provenance and metadata: multiple metadata fields accompany Land Parcel data (e.g., _hist, _mode, _conf, _stdev, _agg, _n) to support analysis and interpretation.

## Data Access, Structure, and Technical Details
- Spatial references:
  - GB Land Parcel products: British National Grid (EPSG: 27700).
  - NI Land Parcel products: Irish Grid (EPSG: 29903).
- Extents and parcel counts:
  - GB: approximately 6.7 million parcels; NI: ~0.9 million parcels (numbers given in Table 2).
- Dataset specifics:
  - 10m Classified Pixels: 2-band (class ID, confidence) per GB and 3-band for NI variants.
  - 25m Rasterized Parcels: three-band rasters (mode, conf, purity) per parcel.
  - Land Parcel datasets include a detailed attribute schema and example fields to support analysis.

## Methods, Quality Assurance, and Limitations
- Validation and quality:
  - Validation relies on multiple independent data sources and bespoke validation points to quantify accuracy and class-level performance.
  - Acknowledges that errors are inherent in all land cover products; annual updates help separate random errors from real change.
- Limitations and challenges:
  - Spectral confusion remains for several habitat types; context rasters mitigate some confusion but challenges persist (e.g., differentiating certain grassland types, peatland vegetation).
  - Saltwater vs Freshwater differentiation can be tricky in coastal and tidal contexts.
  - Small patches and mosaics (below the 0.5 ha MMU) may be underrepresented in parcel frameworks.
  - Some classes show lower producer’s accuracy (e.g., Heather grassland) due to spectral similarity with other classes.
- Appendices provide detailed notes on UK BAP Broad Habitats, mapping nuances, and recommended color recipes for display.

## Appendix Highlights (for Analysts)
- Appendix 1 and 2: detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; guidance on interpretation and potential misclassifications.
- Appendix 3: color coding scheme for displaying classes.
- Appendix 4: full correspondence matrices and class-level accuracy metrics (producer’s and user’s accuracy) by class.
- Appendix 5: full list of LCM2020 datasets and their official names.

## Key Takeaways for Data-Driven Analysis
- LCM2020 provides a robust, annually updated, remotely sensed land cover map with 21 classes aligned to biodiversity habitats, enabling change detection and temporal analysis.
- The combination of hierarchical data (10m pixels, 25m parcels, and land parcel framework) supports both detailed, pixel-level studies and parcel-based change assessment.
- Bootstrap Training and Random Forest offer a scalable, automatic training regime that leverages recent wall-to-wall data to maintain accuracy with minimal new field data.
- Validation indicates strong overall accuracy (~79%), with explicit class-level metrics and confusion information to guide interpretation.
- Users should be aware of scale-related limitations, spectral confusion, and the differences between GB and NI dataset configurations when designing analyses.
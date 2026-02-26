# The UKCEH Land Cover Map for 2020

- Purpose of the document: This user guide explains the UKCEH Land Cover Map for 2020 (LCM2020), detailing its six geospatial datasets (three for GB and Northern Ireland), how the data were produced, validated, and how accuracy is assessed. It aims to help users apply LCM2020 appropriately and understand its limitations.

## What LCM2020 consists of

- Six datasets (GB and Northern Ireland combined):
  - 10m Classified Pixels (GB)
  - 10m Classified Pixels (Northern Ireland)
  - Land Parcel Dataset (GB)
  - Land Parcel Dataset (Northern Ireland)
  - 25m Rasterised Land Parcel (GB)
  - 25m Rasterised Land Parcel (Northern Ireland)
- Classification outputs include a first band with the most likely UKCEH Land Cover Class and a second band indicating classification confidence.
- Three general data products per region are produced to capture both detailed pixel-level information and parcel-based summaries.

## Data production workflow

- Seasonal data and context layers:
  - Seasonal Composite Images derived from Sentinel-2 via Google Earth Engine, with four seasons (winter, spring, summer, autumn) using 9 Sentinel-2 bands (spectral information at multiple resolutions).
  - Context Rasters (10 for GB; 7 for Northern Ireland) to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, water, coast, and vegetation masks).
- Classification Scenes:
  - GB used 100x100 km tiling to create 36-band Seasonal Composite Images, resulting in 46-band Classification Scenes (spectral plus contextual data).
  - NI used a single 36-band seasonal scene per year based on minimum bounding rectangle of NI land mass.
- Land Parcel Spatial Framework:
  - A fixed framework with a minimum mapping unit of ~0.5 ha (MMU) used to derive land parcel attributes by intersecting with the 10m Classified Pixels.
  - Parcel identifiers (gid) differ from LCM2015; cross-year parcelID comparisons require spatial overlap rather than ID matching.
- Bootstrap Training and Random Forest:
  - Bootstrap Training automatically uses historic LCM data (2017–2019) to train the classifier, reducing the need for new field data.
  - Training data: GB ~941,027 objects; Northern Ireland ~214,833 objects (filtered to >99% purity across three years).
  - Random Forest classifier trained with 10,000 samples per class (balanced learning) to produce the 10m Classified Pixels.

## Data formats, attributes, and governance

- Class labels and metadata:
  - 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with careful notes on relationships and differences between UKCEH classes and BAP Broad Habitats.
  - Appendix materials provide class notes, color scales, and correspondence matrices to relate UKCEH classes to BAP Broad Habitats.
- Dataset details and formats:
  - Pixel and parcel datasets are provided with clear EPSG codes (GB: EPSG 27700; NI: EPSG 29903).
  - 10m pixel data preserve fine landscape features (not generalized to the Land Parcel Spatial Framework), suitable for specialist use.
  - 25m rasterised parcels carry per-parcel attributes: mode (dominant class), conf (mean class probability), purity (percentage of modal class within parcel).
  - Land Parcel dataset includes per-pixel and per-parcel attributes such as _hist, _mode, _purity, _conf, _stdev, and _agg (linking to the UKCEH Land Cover Classes and broader aggregates).
- Validation and accuracy:
  - Validation used countryside survey data (2019, 2020), open-source National Forest Inventory data, IACS data, and bespoke validation points (34715 locations).
  - Overall accuracy reported as 79.2% (Appendix 4), with class-by-class accuracies shown in the validation matrices.
  - Accuracy varies by class (e.g., Urban/Suburban, Heather, Heather grassland, Bog, etc.), with detailed producer’s and user’s accuracies provided in the appendix.
- Continuous improvement and annual production:
  - LCM2020 is produced annually to improve temporal consistency, comparability, and change detection.
  - Manual post-editing for regional corrections has been reduced to maintain annual production pace; problems are noted for future methodological improvements.

## Practical implications for data leaders

- System-wide data view:
  - The approach emphasizes a holistic data system, including data discovery, metadata, quality, and updates to support decision-making across data products and partners.
- User needs and co-ownership:
  - The datasets are designed to support end-users across networks, with attention to ensuring metadata, context, and class definitions are clear for effective reuse.
- Data quality and standards:
  - Clear documentation of validation results, confidence metrics, and per-class accuracies supports assessment of data fitness for purpose.
  If cross-year analyses are planned, practitioners should use the Land Parcel Spatial Framework and be aware of changes in parcel identifiers since LCM2015.
- Change detection and monitoring:
  - Annual maps enable differentiation of random errors (flicker) from real-world change, supporting monitoring of UK countryside states and environmental objectives.

## Appendices – key references for detailed understanding

- Appendix 1: Notes on UKCEH Land Cover Classes (class definitions, distinctions, and training considerations).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – mapping between BAP categories and UKCEH classes.
- Appendix 3: Colour recipes for displaying UKCEH Land Cover Classes (for map visualisation).
- Appendix 4: Validation matrices – detailed class-level user’s and producer’s accuracies, plus confusion matrices.
- Appendix 5: Full list of datasets for UKCEH LCM2020 (dataset names and metadata).

## Summary of the main outcomes

- LCM2020 provides six GB/NI geospatial datasets (10m classified pixels for GB and NI; land parcel datasets for GB and NI; 25m rasterised land parcels for GB and NI).
- The maps are produced automatically via Bootstrap Training and Random Forest, using Sentinel-2 Seasonal Composite Images plus 10 context rasters, with annual re-generation to enable change detection.
- Validation shows an overall accuracy of 79.2%, with detailed per-class accuracies documented.
- The product supports both detailed pixel-level analysis and parcel-based summaries, with clear guidance on interpretation, limitations, and compatibility with historical classifications.
- Data leaders can leverage the comprehensive metadata, lineage, and validation information to govern data quality, support cross-network collaboration, and plan for ongoing methodological improvements.
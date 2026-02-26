# The UKCEH Land Cover Map for 2022

- UKCEH LCM2022 comprises seven geospatial data products: three datasets for Great Britain and three for Northern Ireland (10 m classified pixels, land parcel data, and 25 m rasterised land parcels) plus a 1 km summary raster product covering GB and NI.
- Land cover is represented as 21 UKCEH Land Cover Classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats, created via automatic classification of Classification Scenes built from Sentinel-2 Seasonal Composite Images plus Context Rasters.
- Overall validation accuracy is 86.1% at full thematic detail; annual production aims to improve temporal consistency and support change detection.
- The methodology uses Bootstrap Training to generate training data from historic LCMs (2019–2021), combined with a Random Forest classifier. The approach supports rapid, automated map updates while enabling change detection across years.
- Data products come with DOIs for citation and metadata, ensuring discoverability and reuse.

## Overview of Data Products and Outputs

- 10 m Classified Pixel datasets
  - GB and NI each provide a national mosaic of classified pixels.
  - Each pixel encodes the most likely UKCEH Land Cover Class (band 1) and the associated classification confidence (band 2).
  - No land parcel framework generalisation is applied to preserve fine-scale detail (e.g., narrow features, small patches).

- 25 m Rasterised Land Parcel datasets
  - GB and NI land parcels are produced by rasterising the 10 m classified pixels over the UKCEH Land Parcel Spatial Framework.
  - Each parcel dataset includes per-parcel attributes such as dominant class, confidence, and purity.

- 1 km Summary raster products
  - Summary rasters for GB and NI created by aggregating the 25 m data to 1 km cells.
  - Products include: dominant class (1 band), dominant class (aggregate), and percentage cover per class (21 bands) plus aggregate percentage (10 bands).
  - Percentage values are integer-rounded; totals may not exactly sum to 100 due to rounding, and coastal pixels may sum to less than 100.

## Data Production and Methodology

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 reflectance resampled to 10 m with four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Ten Sentinel-2 bands used; occasional cloud-related gaps are handled by the classifier.

- Context Rasters
  - 10 m context rasters reduce spectral confusion (e.g., terrain, proximity to features, coastal masks).
  - GB: terrain height, aspect, slope; distances to buildings, roads, tidal water, freshwater; foreshore, woodland, and saltmarsh masks.
  - NI: similar context with additional urban mask and distance to coast/roads.

- Classification Scenes and Tiling
  - GB is partitioned into 32 Classification Scenes (tiles ~100 x 100 km) to manage regional phenology and data volume.
  - NI uses a single Classification Scene tailored to its extent (49-band scene: Sentinel-2 seasonal bands plus NI context rasters).

- The UK Land Parcel Spatial Framework
  - Land parcels are designed to represent discrete real-world units (minimum area ~0.5 ha, MMU).
  - Spatial framework re-ordered for efficiency; parcel identifiers (gid) differ from LCM2015 for most users.

- Bootstrap Training
  - Automatic, field-data-light training using historic LCM observations with >80% probability and consistent class across 3 years.
  - Large bootstrap training sets enable robust Random Forest learning and reduce noise from minor yearly changes.
  - Some classes affected by rotation or short-term change may rely on auxiliary training data (e.g., Crops dataset for arable/improved grassland).

- Random Forest Classification
  - 10 m classified pixels produced from labeled bootstrap bags; 10,000 samples per bag with replacement to balance class representation.
  - Model combines Bootstrap Training observations with spectral and contextual features to yield pixel class membership probabilities.

- Validation and Quality Assurance
  - Validation against 33,107 reference points spanning all 21 classes.
  - Overall accuracy: 86.1% at full thematic detail.
  - Detailed class-level producer’s and user’s accuracies are provided in the accompanying validation documentation.

## Land Cover Classes and BAP Relationship

- LCM2022 uses 21 UKCEH Land Cover Classes derived from, but not identical to, UK BAP Broad Habitats.
- Appendices clarify relationships and note where differences occur (e.g., splits in some BAP classes, coastal vs. freshwater distinctions).
- The mapping is designed for consistency with earlier LCM products while acknowledging spectral limitations and training data constraints.

## Access, Citation, and Documentation

- Each LCM2022 dataset has a Digital Object Identifier (DOI) and accompanying citation. Examples include:
  - 10 m Classified Pixels (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - Land Parcels (GB and NI)
  - 1 km Summary Rasters (GB and NI)
- References include Marston et al. and related production method papers; users are encouraged to cite the DOIs when using the data.

## Known Issues and Limitations

- A small number of land parcel polygons are missing from vector products, causing nodata areas in 25 m rasterised land parcels; impact on 1 km products is negligible.
- 10 m Classified Pixels are not affected by these parcel gaps, but users should be aware of alignment nuances when linking 10 m and parcel-based products.
- Annual methodological changes mean some inter-annual differences may reflect production changes in addition to real land-cover change.

## Appendices and Additional Resources

- Appendix 1–2: Notes on UKCEH Land Cover Classes and detailed notes on BAP Broad Habitats, including guidance on interpretation and potential spectral confusions.
- Appendix 3: Full list of LCM2022 datasets with DOIs and citations.
- Appendix 4: Correspondence matrices (confusion matrices) for class-level accuracy validation.
- Appendix 5–6: Recommended colour recipes for displaying land cover classes (standard and colour-blind friendly) plus accompanying QGIS symbology files.

- Disclaimer: While annual production enables timely monitoring, methodological changes between maps can produce differences beyond actual land-cover change.
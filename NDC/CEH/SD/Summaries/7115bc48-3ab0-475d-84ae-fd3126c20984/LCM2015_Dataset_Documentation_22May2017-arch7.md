# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classifying satellite data into 21 Broad Habitat classes, primarily using Landsat-8 (30 m) and AWIFS (60 m) data.
- Provides a range of data products to support map-based data visualisation and analysis for GIS applications, including a core vector dataset, a 25 m raster, and 1 km percentage/dominant cover products.
- LCM2015 is a stable, archived dataset with rich metadata and uncertainty information; DOIs are provided for all products to support citation and reproducibility.

## Data scope and purpose
- Purpose-built for GIS users requiring map-based representations of land cover across Great Britain and Northern Ireland.
- Vector and raster formats are designed to support diverse workflows, from detailed site-level analysis to national-scale modelling (e.g., species distribution, meteorology).

## Key differences from LCM2007 (implications for workflow)
- Montane class removed; upland areas reclassified as Inland Rock or other upland habitats based on spectral data.
- Rough grassland class removed; grassland types now align with JNCC Broad Habitat definitions; no soil data used as input in LCM2015.
- 25 m raster is a two-band image: band 1 = dominant class, band 2 = mean per-polygon probability.
- Probability information simplified: vector stores mean polygon probability; 25 m raster band 2 stores the same; 1 km products do not include probability.
- Sub-class spectral divisions removed; Random Forest classification replaces Maximum Likelihood, simplifying training data requirements.
- Spatial framework: no segmentation in LCM2015; per-pixel classification without segmentation; segmentation changes primarily affect upland areas and GB vector/25 m products.
- Mixed woodland training uses pure stands for training, with modal_class assigned at polygon level; users can inspect pix_dist for detailed composition.

## Data products and formats
- Core vector dataset for Great Britain and Northern Ireland; 21 target classes (with some aggregated forms for raster products).
- 25 m raster product derived from the vector dataset (two bands as described above).
- 1 km raster products:
  - Dominant cover at 1 km (for 21 classes and for 10 aggregate classes)
  - Percentage cover at 1 km (21 class bands and 10 aggregate class bands)
- Spatial detail:
  - GB vector: 6.7 million polygons; NI vector: 0.9 million polygons.
  - 25 m raster and 1 km rasters provided separately for GB and NI to reflect different projections.
- Composite concept:
  - Each polygon has a gid (Geometry ID) and a composite image number indicating the data source combination.

## Vector data specifics
- Attributes (nine core fields in Table 2):
  - gid: unique parcel identifier
  - BHAB: dominant land cover at Broad Habitat level (text)
  - Pix_dist: counts of pixels per class within the polygon (length 23)
  - unc: mean per-polygon probability (0–255 scale)
  - unc_stdev: standard deviation of the uncertainty
  - npix: number of pixels in the polygon
  - Modal_class: LCM2015 target class (1–21)
  - Modal_prop: proportion of polygon classified as dominant class
  - Composite: composite image number used for classification
- Coverage: GB vector = 6.7M polygons; NI vector = 0.9M polygons.
- Metadata-rich: includes dominant class, per-class pixel breakdown, and mean probability for each polygon.

## Raster data specifics
- 25 m raster: two bands
  - Band 1: dominant LCM2015 class per polygon
  - Band 2: mean per-polygon probability from Random Forest
- 1 km rasters: aggregate and detailed percentage products
  - 1 km dominant and percentage cover products (both 21-class and 10-aggregate-class schemes)
  - Rounding may cause sums to deviate slightly from 100%; coastal areas may sum to less than 100
- Spatial details:
  - Great Britain and Northern Ireland provided separately with appropriate projections
  - 1 km pixel is equivalent to 1,600 x 25 m cells

## Data quality, uncertainty, and metadata
- LCM2015 includes per-polygon uncertainty (mean probability) derived from the Random Forest classifier.
- Rich metadata accompanying vector polygons, including the breakdown of pixel counts by class and the mean polygon probability.
- The 25 m raster’s second band provides per-polygon probability; 1 km products do not include probability data.

## Data access, licensing, and citations
- Data access:
  - 1 km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector and 25 m raster products: available on request under licence from CEH
- Licensing: some users may incur licence fees; contact spatialdata@ceh.ac.uk for details.
- Citing LCM2015:
  - Each product has its own DOI; cite in-text and in references (examples provided in the dataset documentation).
- Map projections:
  - GB data: British National Grid
  - NI data: TM75 Irish Grid

## Version and updates
- Dataset documentation: Version 1.2, 22 May 2017
- Prior updates: 1.0 (April 2017), 1.1 (May 2017)
- Notes: The document highlights that LCM2015 is complex and not recommended for current change mapping; differences across LCM products reflect both real change and classification changes.

## Practical considerations for GIS workflows
- Use the vector gid to link polygon data with detailed attributes and pixel breakdowns; retain the gid for unambiguous communication.
- When analysing change over time, account for methodological differences between LCM series; LCM2015 is optimized for per-polygon classification and change-mapping readiness, but direct change detection between LCM2007 and LCM2015 requires careful interpretation.
- Choose data product resolution based on workflow:
  - Vector: rich attributes and per-polygon summaries (larger file sizes)
  - 25 m raster: consistent with per-polygon classification and useful when metadata is less critical
  - 1 km rasters: suitable for national-scale modelling and integration with other coarse-resolution datasets
- Ensure appropriate handling of aggregation effects and coastal area limitations when using 1 km percentage data.
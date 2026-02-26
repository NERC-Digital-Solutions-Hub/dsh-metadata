# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map created by classifying satellite data into 21 land cover classes, aligned with UK Broad Habitat definitions.
- Uses two-date composite imagery, mainly Landsat-8 (30 m) with AWIFS (60 m) as needed.
- Produces multiple data products (vector, 25 m raster, and 1 km rasters) to support diverse user needs; GB and Northern Ireland (NI) data are provided separately in their respective projections.
- LCM2015 updates the 2007 Land Cover Map, built on an updated spatial framework, and emphasizes per-pixel classifications suitable for change mapping in future work.

## Purpose and cautions
- LCM2015 is complex; users should review accompanying documentation to avoid inappropriate use.
- Do not rely on the LCM series for current change mapping in its present state, since differences between maps reflect real change and classification error, compounded by methodological and data differences over time.

## Data content and formats
- Core products:
  - Vector data set: polygons with attached attributes; used for detailed per-polygon analysis.
  - 25 m raster: two-band image (band 1 = dominant class per polygon; band 2 = mean per-polygon probability from classification).
  - 1 km rasters: aggregate products providing dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
- Class structure:
  - LCM2015 has 21 target classes (based on Broad Habitats); some habitats are subdivided to reflect spectral signatures.
  - Spatially, vector and 25 m rasters are per-polygon classifications; 1 km rasters summarize 25 m data.
- Minimum mapping unit:
  - >0.5 ha; parcels smaller than 0.5 ha or lines <20 m are dissolved into surrounding landscape.

## Classification methodology and output differences (LCM2007 vs LCM2015)
- New classifier:
  - Random Forest replaces Maximum Likelihood, handling multi-modal training data and avoiding sub-class grouping.
- Training data:
  - Initial stable training areas (areas classified the same in 2000 and 2007) augmented with coastal areas and underrepresented classes.
  - Ancillary data (e.g., slope, distance to water) are integrated into input data rather than applied post-classification.
- No spectral sub-classes:
  - Spectral sub-classes used in earlier maps are now redundant with Random Forest; per-polygon outputs use the dominant class.
- Spatial framework:
  - No segmentation-based polygons in LCM2015; per-pixel classifications feed into polygon labels, reducing segmentation-related inconsistencies and facilitating change mapping.
- Output data changes:
  - Montane class removed (reclassified as Inland Rock or upland habitats for change mapping eligibility); Montane distribution from LCM2007 remains available only in LCM2007 datasets.
  - Rough grassland removed; grassland types align with JNCC Broad Habitats; no soil data used in LCM2015.
  - 25 m raster is two-band; probability data recorded as mean polygon probability (vector) and in band 2 of the 25 m raster.
  - Mixed woodland handled by per-pixel classification with polygon-level modal class; potential misclassification for mixed stands is documented (users can inspect pix_dist for details).

## Data products in detail
- Vector data set:
  - ~6.7 million GB polygons and ~0.9 million NI polygons.
  - 9 attributes per polygon, including land cover class (text and integer), source image, uncertainty (mean per-polygon probability), number of class pixels per polygon, dominant class proportion, and a unique gid (geometry identifier).
  - Composite image reference indicates which composite was used (99 = infill from LCM2007).
- 25 m raster:
  - 2-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability.
  - Metadata specifies relationships to the 21 target classes and data extent.
- 1 km rasters:
  - Dominant cover (21 target classes) and dominant aggregate (10 aggregates) at 1 km.
  - Percentage cover (21 bands for 1 km; 10 aggregates for aggregated products).
  - Values are integers; sums may deviate from 100 due to rounding and coastal area considerations.
- Labels and metadata:
  - Each polygon includes a gid; vector products include extensive metadata and uncertainty metrics.
  - DOIs exist for all LCM2015 products to support citation and reproducibility.

## Access, licensing, and referencing
- Data access:
  - 1 km raster data available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product and 25 m raster available on request under licence from CEH (licensing may apply).
- Projections:
  - Great Britain: British National Grid; Northern Ireland: TM75 Irish Grid.
- Citations:
  - Each LCM2015 product has its own DOI for formal citation; users are encouraged to cite DOIs in publications.
- Identity and provenance:
  - LCM2015 is a stable, archived dataset with rich metadata and per-polygon uncertainty information.

## Practical notes for analysts
- The dataset supports robust environmental monitoring and policy evaluation, but plan for data differences across versions when assessing change.
- Use the vector’s gid and pix_dist attributes to understand per-polygon composition and to investigate potential misclassifications, especially in mixed habitats.
- When combining with other datasets, leverage the stable training areas and the integrated ancillary data to improve classification reliability.
- For coastal and upland areas, consider the methodological changes (e.g., removal of segmentation) that affect interpretation and cross-version comparisons.

## Projections, formats, and documentation
- Data are provided in GB and NI formats with corresponding coordinate systems; detailed tables and appendices document class definitions, color mappings, and composite usage.
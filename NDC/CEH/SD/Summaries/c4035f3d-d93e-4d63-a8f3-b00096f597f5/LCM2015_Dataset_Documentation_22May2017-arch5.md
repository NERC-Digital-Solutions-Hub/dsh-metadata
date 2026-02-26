# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map with 21 classes, created from two-date Landsat-8 (30 m) and AWIFS (60 m) imagery, reflecting real-world boundaries to support diverse user needs.
- LCM2015 updates the 2007 map and uses an updated spatial framework; it is designed for a publishing-like workflow to support discovery, reuse, and change mapping over time.
- The document emphasizes that LCM2015 should not be used for current-state change mapping in its present form due to differences from earlier products and inherent classification/accuracy limitations.

## Data and methodology highlights
- Classifier and inputs
  - Uses a Random Forest classifier that handles multi-modal training data and does not require spectral sub-classes.
  - Ancillary data (e.g., slope, distance to rivers) are integrated as required by the classifier, making knowledge-based enhancements part of the input data rather than a post-classification step.
  - Stable training areas, built from areas consistently classified the same in 2000 and 2007, were supplemented with coastal and difficult classes to improve robustness.
- Differences from LCM2007 (highlights)
  - Montane class removed; upland areas reclassified as Inland Rock or other upland habitats based on spectral data.
  - Rough grassland removed; grassland types re-aligned with JNCC Broad Habitat definitions without relying on soil data.
  - 25 m raster becomes a 2-band image (classification in band 1; mean per-polygon probability in band 2).
  - Probability data presentation simplified: vector contains mean polygon probability; 25 m raster band 2 contains the same value; 1 km products do not include per-pixel probabilities.
  - No spectral sub-classes; segmentation-based spatial framework from LCM2007 is removed to avoid misalignment with the per-pixel classification and simplify change mapping.
  - Mixed woodland training moved from object-based training to per-pixel training with polygon-level summarisation.
- Outputs and data structure
  - Final outputs include: core vector dataset, 25 m raster dataset, and 1 km percentage/dominant cover products (21 target classes and 10 aggregate classes for 1 km).
  - LCM2015 maps land cover (not strictly land use); classification reflects spectral signatures with some context-based interpretation.
  - Minimum mappable area set at >0.5 ha; polygons smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding areas.

## Data products and formats
- Vector data set
  - Polygons with attributes: land cover class (text and integer), source image, uncertainty measures, counts of pixels per class (pix_dist), dominant class proportion (modal_prop), number of pixels (npix), and a unique geometry identifier (gid).
  - Approximately 6.7 million polygons in Great Britain and 0.9 million in Northern Ireland.
- Raster data sets
  - 25 m raster: two bands; Band 1 = dominant LCM2015 class, Band 2 = mean per-polygon probability from Random Forest.
  - 1 km raster products: dominant class (1-band) and percentage cover for both 21 target classes and 10 aggregate classes (integer values; sums may not equal exactly 100 due to rounding and coastal extents).
  - Great Britain and Northern Ireland provided separately with appropriate projections (Great Britain: British National Grid; Northern Ireland: TM75 Irish Grid).
- Class mapping and metadata
  - 21 LCM2015 classes based on UK Broad Habitats (JNCC Jackson definitions); several Broad Habitats are further subdivided for certain products (e.g., Built-up Areas and Gardens into Suburban and Urban).
  - Appendix and Table mappings describe how 21 classes relate to 10 aggregates used in 1 km products.
  - Each polygon’s gid enables unambiguous communication of features across datasets.

## Metadata, uncertainty, and quality information
- Each polygon includes rich metadata: dominant class, breakdown of pixel counts per class within the polygon, and mean probability from the classifier.
- Uncertainty is quantified as mean per-polygon probability (with standard deviation available in Unc_stdev).
- The Random Forest output provides per-pixel probability estimates, summarized per polygon (and available in the 25 m raster’s Band 2).
- Documentation notes that differences between LCM series can arise from both real change and classification/processing differences, especially relevant for change mapping use.

## Data access and licensing
- Data access
  - 1 km raster data for Great Britain and Northern Ireland are available via the CEH Environmental Information Platform (EIP).
  - The full vector product and the 25 m raster product are available under licence on request from CEH.
- Licensing and fees
  - Licences may apply for some users; fees may be charged depending on use case.
- Data citation and DOIs
  - Each LCM2015 product has a DOI. Citing DOIs is encouraged to ensure reproducibility and traceability.
  - GB products include DOIs for vector, 25 m raster, 1 km percentage target class, 1 km dominant target class, and 1 km aggregate classes.
  - NI products have corresponding DOIs for vector, 25 m raster, 1 km percentage target class, 1 km dominant target class, and 1 km aggregate classes.
- Projections and data layout
  - GB data in British National Grid; NI data in TM75 Irish Grid.
  - Separate GB and NI datasets reflect differing coordinate systems and extents.

## Usage notes and cautions for Data Stewards
- LCM2015 is a stable, archived dataset with a DOI and rich metadata, suitable for long-term governance and reuse.
- The dataset is not recommended for current-state change mapping in its present form; changes in outputs across versions may reflect methodological shifts rather than pure surface change.
- Users should review methodological differences (e.g., removal of segmentation, Montane/Rough grassland changes, use of Random Forest, inclusion of ancillary data) when performing time-series analyses or data integration with earlier LCM products.
- The gid attribute in the vector product supports unambiguous cross-dataset communication but may require careful handling in large-scale processing due to data volume.

## References and support
- Contact: CEH Spatial Data (spatialdata@ceh.ac.uk; +44 (0)1491 838800); CEH website for LCM2015 information and data access.
- Further information and data papers available through CEH:
  - Land Cover Map 2015 information pages and EIP access
  - Citing data: CEH/EIDC guidelines and DOIs
- Appendices provide detailed definitions of Broad Habitats, class mappings, standard colour mapping, and composite image information for LCM2015.
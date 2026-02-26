# Dataset documentation

- LCM2015 is a UK land cover map dataset in 21 Broad Habitat classes, produced from two-date Landsat-8 (30m) and AWIFS (60m) imagery, mapped as real-world boundary polygons and built to update the LCM2007 framework.
- The dataset emphasizes data provenance, processing methods, and metadata to support data governance, reuse, and change analysis.

## Data products and formats

- Core vector data set: polygons with attached attributes describing dominant class and detailed per-polygon information.
- 25m raster: two-band product where band 1 = dominant LCM2015 class, band 2 = mean per-polygon classification probability.
- 1km raster products: 
  - Dominant cover by class (21-band and 10-band aggregates)
  - Percentage cover by class (21 bands) and by aggregates (10 bands)
- Coverage and scale:
  - Great Britain (GB) and Northern Ireland (NI) provided separately with appropriate projections.
  - GB vector: 6.7 million polygons; NI vector: 0.9 million polygons.
  - 25m raster and 1km products aligned to GB and NI projections.
- Spatial resolution and minimum mapping unit:
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and linear features < 20 m dissolved into surrounding landscape.

## Class structure and labeling

- 21 target classes based on UK Broad Habitats (JNCC Jackson 2000).
- Some classes are subdivided within products (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral subtypes) and aggregated in 1km products where appropriate.
- Each polygon has a unique identifier (gid) and rich attribute set, including a per-polygon breakdown of pixel counts and a modal (dominant) class.

## How LCM2015 was produced (methodology)

- Classification approach: Random Forest classifier (instead of previous Maximum Likelihood).
- Training data:
  - Initial stable set defined from 2000 and 2007 classifications, then extended (coastal areas, grassland types, etc.).
- Use of ancillary data:
  - Ancillary layers (e.g., slope, distance to water) are integrated as inputs to the classifier rather than post-classification refinements.
- Spatial framework:
  - Per-pixel classification without segmentation; no segmentation polygons in LCM2015 spatial framework to improve change-mapping consistency.
- Output considerations:
  - No spectral sub-classes required; no per-subclass probabilities in vector product (band 2 of 25m raster provides mean polygon probability).
  - Mixed woodland training uses pixel-level labeling with polygon-level summarization (modal class assigned to polygon).

## Differences from earlier LCM versions (notable changes)

- Montane class removed; upland areas reclassified as Inland Rock or other upland habitats based on spectral data.
- Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitat definitions; no soil data used in LCM2015.
- 25m raster format changed to two-band product (classification band + probability band).
- Probability data: simplified in vector, with mean polygon probability; 25m raster band 2 provides this value; 1km products do not include per-pixel probabilities.
- Sub-classing and spectral sub-classes eliminated due to Random Forest approach.
- Spatial segmentation removed from the GB framework; segmentation-based adjustments in upland areas were not carried forward.
- Training data evolution: reliance on stable data across prior maps supplemented with targeted coastal and poorly mapped classes.

## Uncertainty and data quality

- Per-pixel probability provided by the Random Forest classifier; represented as mean polygon probability (vector) and as band 2 in the 25m raster.
- Cautions on change mapping: differences in method and output between LCM2007 and LCM2015 can affect interpretation of changes.

## Metadata, provenance, and identifiers

- Each polygon (gid) has a unique label; rich polygon metadata and a pixel-level breakdown of class composition (Pix_dist) and majority class (modal_class).
- LCM2015 provides extensive provenance metadata for traceability and reproducibility.
- Uncertainty (unc) and standard deviation (unc_stdev) attributes accompany polygons.

## Data access, licensing, and citation

- Data access:
  - 1km raster products available via the CEH Environmental Information Platform.
  - Full vector and 25m raster products available on request under license; fees may apply.
- Data citation:
  - Each LCM2015 product has its own Digital Object Identifier (DOI) for formal citation.
  - Guidance provided for citing DOIs in publications (author list, date, full DOI in references).
- Projections:
  - GB data in British National Grid; NI data in TM75 Irish Grid.
- Further information and contact:
  - Primary contact: CEH spatialdata@ceh.ac.uk
  - More information at CEH LCM2015 pages and the CEH EIDP platform.
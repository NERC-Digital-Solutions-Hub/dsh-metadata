# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classifying two-date satellite composites into 21 classes based on JNCC Broad Habitat definitions.
- Primary data sources: Landsat-8 (30 m) and supplementary AWIFS (60 m) data.
- Uses a Random Forest classifier incorporating ancillary data; outputs include per-polygon metadata and uncertainty estimates.
- Products available: vector (core), 25 m raster, and 1 km percentage/dominant cover products.
- LCM2015 is a stable, archived data set with DOIs for citation; not recommended for change mapping in its current state.

## Data and methods
- Classification approach
  - Per-pixel spectral classification using a Random Forest algorithm.
  - Two-date composites underpin the classification; ancillary data are integrated as inputs rather than post-classification rules.
  - No spectral sub-classes are used; training areas built from stable data and coastal/enhancement considerations.
- Dataset scope and scale
  - UK-wide dataset reflecting real-world boundaries with a minimum mapping unit of greater than 0.5 ha.
  - Parcels smaller than 0.5 ha and very short linear features are dissolved into surrounding areas.
- Data products
  - Core vector dataset: polygons with 9 attributes per polygon, including dominant class, pixel counts per class, and uncertainty metrics.
  - 25 m raster: 2-band product (band 1 = dominant class, band 2 = mean per-polygon probability).
  - 1 km raster: aggregate products (dominant, and percentage cover for 21 target classes or 10 aggregates).
- Spatial detail and class structure
  - 21 LCM2015 target classes mapped from 21 Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral categories).
  - Vector and 25 m raster closely aligned; 1 km products derived from 25 m data.
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon dominant class (Modal_class) with breakdown of pixel counts by class (Pix_dist) and mean probability (uncertainty).
  - Uncertainty information encoded as per-polygon probability (0–255 scale) and standard deviation (unc_stdev).
- Data accessibility and formats
  - Great Britain and Northern Ireland provided in separate datasets with different projections.
  - GB vector: ~6.7 million polygons; NI vector: ~0.9 million polygons.
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk) for 1 km products; full vector and 25 m products available on request; licensing may apply.
- Projections and DOIs
  - GB products: British National Grid; NI products: TM75 Irish Grid.
  - Each product has a DOI for citation (vector, 25 m, and 1 km products for GB and NI).

## Differences from LCM2007 (highlights)
- Output data and class structure
  - Montane class removed; replaced by inland rock or other upland habitats based on spectral data.
  - Rough grassland class removed; aligns grassland types with JNCC Broad Habitats; no soil data used in 2015.
  - 25 m raster becomes two-band (classification band + probability mean).
  - Probability data reporting simplified: per-polygon mean probability; vector stores modal probability; 1 km products do not include per-pixel probabilities.
  - No spectral sub-classes; Random Forest handles multi-model data, removing need for sub-class grouping.
  - Spatial framework no longer uses segmentation; polygons are per-pixel-defined without Segmentation-derived splits.
  - Mixed woodland training uses pure canopy classes; polygon labels reflect modal per-pixel classification.
- Methodological changes
  - Transition from Maximum Likelihood to Random Forest classifier.
  - Stable training areas used as a base, with added coastal and poorly mapped classes for supplementary training.
  - Ancillary datasets (altitude, soil, etc.) are now integrated into the input data rather than post-classification rules.

## Data products and structure (in detail)
- Vector data set
  - Core product: polygons with attributes including gid, BHAB (dominant Broad Habitat), Modal_class, Pix_dist (detailed pixel counts per class), unc (uncertainty), npix (pixels in polygon), Modal_prop (dominant class proportion), composite (source image).
  - Coverage: GB ~6.7 million polygons; NI ~0.9 million polygons.
- 25 m raster
  - 2-band format: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability.
- 1 km raster
  - Derived products: dominant class at 1 km; percentage cover for 21 target classes; and percentage cover for 10 aggregate classes.
  - Rounding can lead to sums slightly above or below 100%; coastal areas may sum to less than 100%.

## Class definitions and mapping
- 21 LCM2015 target classes anchored to Broad Habitat definitions; includes subdivisions where reliably separable spectrally.
- Examples of mapped broad habitat groups and subdivisions (e.g., Built-up Areas and Gardens with Urban and Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral categories into Littoral Rock, Littoral Sediment, Saltmarsh, etc.).
- Appendix-like guidance provides interpretation nuances for specific habitats, including woodland types and grassland distinctions.

## Practical guidance for analysts
- Use cases
  - The vector dataset is richly attributed and suitable for detailed spatial analyses, while the 25 m raster is a leaner alternative when metadata overhead is prohibitive.
  - The 1 km products support regional or national-scale modelling with aggregate class information.
- Cautions
  - Do not rely on LCM2015 for precise change mapping without dedicated change detection workflows.
  - Differences from LCM2007 can affect time-series analyses; cross-walking between versions and DOIs is advised.
- Citation and reproducibility
  - Each product has its own DOI; cite according to standard data citation practices.
  - Data provenance is documented (composite images, training data origins, and uncertainty metrics) to support reproducibility.

## Access and further information
- Access
  - CEH Environmental Information Platform for 1 km data.
  - Full vector and 25 m data available on request via CEH; licensing may apply.
- References and further reading
  - Primary background on Broad Habitat definitions and LCM2007 comparison reports.
  - LCM2015 product pages and data citation guidelines.
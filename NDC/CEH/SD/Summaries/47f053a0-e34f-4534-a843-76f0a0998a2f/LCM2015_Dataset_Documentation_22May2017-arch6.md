# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map, classifying satellite data into 21 Broad Habitat-based classes.
- Created mainly from Landsat-8 (30 m) two-date composites, with AWIFS (60 m) as needed.
- Updates and refines the LCM2007 framework; polygons reflect real-world boundaries for easier interpretation and compatibility with other datasets.
- Aimed at diverse user needs, including change mapping and cross-domain analyses.

## Data products and formats
- Core products:
  - Vector data set: polygons with rich attributes (9 attributes per polygon) and a gid label for unique identification.
  - 25 m raster: two-band image (band 1 = dominant class; band 2 = mean per-polygon probability from Random Forest).
  - 1 km rasters: aggregate products providing dominant class and percentage cover for both 21 classes and 10 aggregates.
- Spatial coverage and resolutions:
  - Great Britain and Northern Ireland provided separately, using British National Grid (GB) and TM75 Irish Grid (NI) projections.
  - Minimum mappable area > 0.5 ha; polygons < 0.5 ha dissolved into surrounding area.
- Metadata and uncertainty:
  - Rich polygon metadata, including dominant class, per-polygon pixel counts for each class, and mean probability.
  - Uncertainty estimates derived from the Random Forest classifier, available in vector (unc) and in 25 m raster (band 2).

## Key methodological highlights
- Classification approach:
  - Uses Random Forest classifier (instead of Maximum Likelihood) to handle multi-modal training data and simplify training data preparation.
  - Ancillary data (e.g., slope, proximity to rivers) are integrated as input features rather than applied post-classification, enabling objective knowledge-based enhancements.
- Training and framework:
  - Stable training areas approach builds on 2000 and 2007 classifications, then expanded for coastal and difficult classes.
  - No image-based segmentation in the 2015 spatial framework (unlike LCM2007); aims for per-pixel classification to support change detection.
- Output and interpretation:
  - No spectral sub-classes are used; sub-classes were found redundant for practical use.
  - Mixed woodland handling updated: training uses pure stands; polygon labels reflect modal class from per-pixel decisions, with pix_dist and gid aiding interpretation.
- Output changes vs LCM2007:
  - Montane class removed; inland upland areas reclassified as Inland Rock or other upland habitats.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats without soil data usage.
  - 25 m raster now two-band; probability data recorded as mean per-polygon probability in vector and in band 2 of the 25 m raster.
  - Segmentation-based spatial framework removed; no segmentation in spatial framework.
  - Differences in methodology include a shift to stable training areas and inclusion of ancillary data as inputs.

## The 21 LCM2015 classes and aggregation
- LCM2015 maps 21 classes based on JNCC Broad Habitats (with some refinements and splits, e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral categories).
- Some classes are split into subcategories (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories).
- Aggregates: 21 classes can be grouped into 10 aggregates for the 1 km products.

## Data access and citation
- Access:
  - 1 km raster data available via the CEH Environmental Information Platform (eIP).
  - Full vector and 25 m raster products available on request under licence from CEH.
- Licensing:
  - Licence fees may apply for some users/applications.
- Citing LCM2015:
  - Each product has its own DOI; researchers should cite the relevant DOI(s) in publications.
  - Example citation format provided in the documentation.
- Contact and further information:
  - Data and queries: spatialdata@ceh.ac.uk; more info at CEH websites.

## Data structure and attributes
- Vector dataset (GB and NI):
  - gid: Unique parcel identifier for each polygon.
  - BHAB: Dominant land cover at Broad Habitat level (text).
  - Pix_dist: Vector with counts of pixels per class within the polygon (plus npix and modal_class).
  - unc: Mean per-polygon probability from Random Forest (0–255 scale).
  - unc_stdev: Standard deviation of the uncertainty.
  - npix: Number of pixels in the polygon.
  - Modal_class: LCM2015 target class (1–21).
  - Modal_prop: Proportion of polygon classified as dominant class.
  - Composite: Indicates the composite image source (99 = infill from LCM2007).
- Raster datasets:
  - 25 m raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability.
  - 1 km rasters: dominant class and percentage cover products (both 21-class and 10-aggregate schemes).

## Projection, extent and data quality
- Projections:
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: TM75 Irish Grid (EPSG 29903).
- Spatial extents and cell sizes:
  - 25 m GB and NI rasters; 1 km GB and NI rasters; detailed metadata tables specify pixel counts and grid extents.
- Data quality and cautions:
  - LCM2015 is a stable, archived dataset with DOIs; caution advised when using LCM2015 directly for change mapping in its current state.
  - Differences between LCM products over time reflect real change and classification error; users should verify compatibility with prior mappings and scripts.

## Appendix and additional information
- Appendix sections provide detailed Broad Habitat definitions (JNCC) and class mapping guidance, color mapping recipes, and composite image usage.
- The document references prior reports (LCM2007, related datasets) for context and methodological evolution.
# Dataset documentation

- LCM2015 is a complex UK land cover dataset produced from satellite imagery (Landsat-8 and AWIFS) to map 21 Broad Habitat classes across Great Britain and Northern Ireland.
- It provides multiple data products (vector, 25m raster, 1km percentage/dominant products) designed for map-based data exploration and analysis.
- The dataset uses a per-polygon (parcel) basis for classification, with accompanying uncertainty information and detailed metadata.

## Key purpose and scope

- Supports diverse GIS applications with map-based visuals and analyses for policy, planning, biodiversity, and public information.
- Not intended for change mapping in its current state; differences between timepoints reflect real change plus classification and data differences.

## Data sources and framework

- Primary inputs: two-date composite satellite imagery, mainly Landsat-8 (30 m), supplemented by AWIFS (60 m).
- Spatial framework built on generalised cartography (OSMM GB, LPS Northern Ireland) and refined using rural boundaries; polygons reflect real-world boundaries for interpretability and compatibility with other data.
- LCM2015 maps land cover (not land use) across 21 classes derived from spectral data and ancillary information.

## Differences from LCM2007 (highlights)

- Montane class removed; areas reclassified as Inland Rock or other upland habitats to enable change mapping.
- Rough grassland removed; grassland types aligned with JNCC Broad Habitats; no soil data used in 2015 classification.
- 25m raster becomes a two-band product (band 1 = classification, band 2 = mean per-polygon probability).
- Probability data: vector includes mean polygon probability; 25m raster band 2 contains the same concept; 1km products do not include probability.
- Sub-class spectral detail removed: Random Forest replaces ML classifier, eliminating spectral sub-classes.
- Spatial framework segmentation removed; per-pixel classification used without segmentation for most areas (uplands affected more).
- Training approaches for mixed woodland updated; pixels classified then summarized to polygons; potential misassignment documented (pix_dist available).

## Data products and structures

- Core products and relationships:
  - Vector data: polygon geometries with 9 attributes including dominant class, pixel counts per class (Pix_dist), uncertainty, and gid (unique parcel label).
  - 25m raster: 2 bands (band 1 = dominant class per polygon, band 2 = mean per-polygon probability).
  - 1km raster: aggregate products (dominant/percentage) for both 21 classes and 10 aggregate classes.
- Class and labeling details:
  - LCM2015 uses 21 target classes; some Broad Habitats are subdivided for specific products.
  - Each polygon has a gid and a rich metadata set, including a breakdown of pixel counts per class and a modal_class for display.
- Spatial resolution and extents:
  - Minimum mappable unit: >0.5 ha (parcels smaller than 0.5 ha and very small linear features are dissolved).
  - GB and NI data are provided separately due to different projections (Great Britain in British National Grid; Northern Ireland in TM75 Irish Grid).
- Data formats and access:
  - Vector: polygon features with extensive attributes (6.7 million GB polygons, 0.9 million NI polygons).
  - 25m raster: per-polygon classification with a secondary probability band.
  - 1km raster: dominant class and percentage covers (21-class and 10-aggregate schemes).

## Attributes and data details

- Vector attributes (illustrative): gid, BHAB (dominant Broad Habitat class), Pix_dist (23-number array of pixel counts per class plus totals and modal_class), unc (mean per-polygon probability), unc_stdev, npix (pixels in polygon), Modal_class (LCM2015 target class ID), Modal_prop (dominant class proportion), Composite (composite image source).
- Raster details: 25m and 1km rasters with per-pixel/area representations of class and percentage cover; 25m band 2 provides per-polygon probability; 1km products summarize 25m data into 1km squares.

## Metadata, uncertainty, and curation

- Rich polygon-level metadata retained during production to support reproducibility and interpretation.
- Uncertainty is quantified via per-polygon probability from the Random Forest classifier (also stored in 25m band 2 and as vector attributes).
- LCM2015 is an archived dataset with Digital Object Identifiers (DOIs) for each product, enabling proper citation and traceability.

## Access, licensing, and citation

- Data access:
  - 1km raster data: available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25m raster products: available under license on request from CEH (licensing fees may apply).
- Data citation:
  - Each LCM2015 product has a DOI (GB vector, GB 25m, GB 1km targets, NI vector, NI 25m, NI 1km targets, etc.).
  - Users should cite the respective DOIs in publications and include authorship and date as per the provided guidance.

## Map projections and coordinate systems

- Great Britain: British National Grid (EPSG 27700) for vector, 25m, and 1km rasters.
- Northern Ireland: TM75 Irish Grid (EPSG 29903) for vector, 25m, and 1km rasters.

## Class definitions and supplementary material

- Appendix materials provide:
  - Definitions of the 21 Broad Habitat classes (per JNCC Broad Habitat framework and Jackson 2000).
  - Recipe for standard LCM2015 colour mapping (RGB mappings for each class).
  - Details on composite image usage and data provenance.
- The appendix materials aid interpretation, visualization, and cross-walking with other habitat classifications.

## Practical guidance and cautions for GIS users

- Use LCM2015 products in their intended context (land cover mapping) and be cautious about applying these outputs to change mapping without accounting for the methodological differences.
- Consider the differences in output data (e.g., removal of montane/rough grassland, probability handling) when migrating scripts from LCM2007.
- For large-area or model-ready analyses, the 1km percentage and dominant products may be most convenient; for detailed mapping and feature-level analyses, the vector and 25m raster offer richer detail and uncertainty information.
- Retain the gid and Pix_dist attributes in vector data to preserve traceability of polygon-level classifications and to support detailed analyses of mixed/class uncertainty.
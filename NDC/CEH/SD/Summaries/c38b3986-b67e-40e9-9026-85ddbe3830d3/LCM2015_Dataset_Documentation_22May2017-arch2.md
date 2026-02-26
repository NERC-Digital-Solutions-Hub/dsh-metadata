# Dataset documentation

## Overview
- CEH (NERC) dataset documenting Land Cover Map 2015 (LCM2015).
- Purpose: provide a consistent, long-term view of environmental condition for monitoring policy and health over time.
- LCM2015: UK parcel-based land cover map produced from satellite data (primarily Landsat-8 at 30 m, supplemented by AWIFS at 60 m) classified into 21 Broad Habitat classes.
- Produces multiple data products (vector, 25 m raster, 1 km raster) to support diverse user needs and applications.
- Important caveat: LCM2015 is complex; not recommended for change mapping in its current state due to real change vs classification error and cross-time differences.

## Data products and formats
- Vector data (core product)
  - Great Britain and Northern Ireland polygons with rich attributes.
  - 6.7 million GB polygons; 0.9 million NI polygons.
  - Key attributes include: gid (unique parcel id), BHAB (dominant Broad Habitat class text), Pix_dist (counts per class within polygon), unc (mean per-polygon probability), Unc_stdev, npix (pixels in polygon), Modal_class (LCM2015 class code), Modal_prop (dominant class proportion), Composite (composite image used).
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest.
- 1 km raster
  - Summary products derived from 25 m: dominant class at 1 km; dominant aggregate class; 21-band percentage cover for classes; 10-band percentage cover for aggregate classes.
- Data projections and extents
  - Great Britain: British National Grid (OSGB 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)
  - Resolution details and table metadata provided (e.g., number of columns/rows, pixel sizes, extents).
- DOIs and citation
  - Each product has a DOI for formal citation (GB vector, GB 25 m, GB 1 km target and aggregate classes, NI vector, NI 25 m, NI 1 km target and aggregate classes).
- Access
  - 1 km raster accessible via CEH Environmental Information Platform.
  - Full vector and 25 m raster available on request under licence (fees may apply).
- Metadata and uncertainty
  - Rich metadata per polygon; per-polygon probability provided by Random Forest; uncertainty values scaled to 0–255.
  - Composite images and historical lineage are documented to aid reproducibility.

## Background and design
- Classification basis: 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Data sources: primarily Landsat-8 imagery (30 m) with AWIFS supplement as needed.
- Output format aims for ease of interpretation and compatibility with other geospatial datasets.
- Spatial framework: designed to reflect real-world boundaries; output is per-pixel (no segmentation in LCM2015).

## Differences from LCM2007 and methodological changes
- Output data differences
  - Montane class removed (replaced by Inland Rock or other upland habitats based on spectral data).
  - Rough grassland class removed; grassland types now align with Broad Habitat definitions and lack soil data reliance.
  - 25 m raster now 2-band (classification + mean probability).
  - Probability data presentation simplified (vector uses major class probability; 25 m raster band 2 stores mean polygon probability).
  - No spectral sub-classes; Random Forest classifier eliminates need for sub-class groupings.
  - Spatial framework: segmentation removed (no per-image segmentation in 2015); per-pixel, to ease change mapping across time.
  - Mixed woodland training now uses pure stands with pixel-level classification and polygon-level modal class; training is based on higher-accuracy stand-level data.
- Methodology differences
  - Classifier: Random Forest replaces Maximum Likelihood Classifier.
  - Training data: stable training areas from 2000 and 2007 supplemented with coastal areas and difficult classes; inter-tidal areas excluded.
  - Ancillary data: now part of input data and used by the classifier rather than post-classification rules.
- Data products and usage implications
  - LCM2015 maps land cover (not strictly land use); some land cover types do not map directly to land use categories.
  - Stable training areas concept supports repeatability and comparability across time.

## Class definitions and interpretation
- 21 Broad Habitat classes, mapped with a detailed crosswalk to JNCC Broad Habitat definitions.
- Appendix 1 and Appendix 2 provide class descriptions, mapping nuances, and notes on potential field verification needs.
- Some classes (e.g., Mixed Woodland, Bracken) are treated with specific rules for training and labeling to reflect spectral realities.
- Appendix 3 provides a standard colour mapping for map display; Appendix 4 lists composite imagery used during production.

## Data usage and cautions
- LC2015 is a stable, archived dataset with DOIs; appropriate citation required for publications.
- For change detection and mapping across time, users should be aware of methodological and data differences between LCM series; direct change mapping is cautioned due to real-change vs classification-error signals and cross-time differences.
- Guidance and notes emphasize caution when interpreting certain grassland, woodland, and wetland classes due to spectral similarities and training data limitations.

## Access, references, and further information
- Contact: spatialdata@ceh.ac.uk; CEH website for LCM2015 details.
- Full dataset documentation and data pages:
  - CEH LCM2015 pages and data access portals.
- References for background and methodology
  - Jackson (2000) Broad Habitat classification definitions.
  - Morton et al. (2011) LCM2007 technical report.
- Data citation practice
  - Each product has a dedicated DOI; use author list and date when citing in publications.

## Quick summary for monitoring analysts
- LCM2015 provides a rich, multi-resolution view of UK land cover (21 Broad Habitat classes) derived from consistent, modern methodologies (Random Forest, integrated ancillary data).
- Outputs include: detailed vector polygons with per-polygon metadata, a 25 m classification raster with probability band, and 1 km aggregated/percentage products.
- Designed for broad comparability with past maps, but with important methodological differences that affect change detection and cross-temporal analyses.
- Access pathways exist for both broad distribution (1 km raster) and full, licensed vector/25 m data; DOIs enable robust data citation.
- Users should consult the detailed appendices for class definitions, color mappings, and production history to ensure correct interpretation and application in monitoring workflows.
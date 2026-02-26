# Dataset documentation

## Overview
- LCM2015 is a parcel-based UK land cover map classifying satellite data into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Data sources: two-date Landsat-8 (30 m) with AWIFS (60 m) as needed.
- Built to update LCM2007; designed as a stable, per-pixel classification framework compatible with other geospatial data.
- Outputs include vector polygons, 25 m rasters, and 1 km percentage/dominant cover products; minimum mappable unit is >0.5 ha.

## Data products and formats
- Core vector data set: polygons with attached attributes; ~6.7 million polygons in Great Britain and ~0.9 million in Northern Ireland.
- 25 m raster: two-band product (band 1 = dominant class per polygon; band 2 = mean per-polygon probability).
- 1 km raster: dominant cover and percentage cover for both 21 classes and 10 aggregate classes.
- Separate GB and NI data sets and projections (GB: British National Grid; NI: TM75 Irish Grid).

## Vector and raster attributes
- Vector attributes include: gid (unique parcel ID), BHAB (dominant Broad Habitat), pix_dist (counts per class), unc (mean per-polygon probability), npix, modal_class, modal_prop, composite (source image set).
- 25 m raster band 2 provides classification probability; 1 km products include percentage and dominant class values (rounded integers).
- Clear metadata and uncertainty information accompany outputs; GIDs recommended to be retained for traceability.

## Methodology and differences from previous maps
- Classification method: Random Forest (RF) instead of Maximum Likelihood; RF handles multi-model training data and often matches/outperforms ML.
- Training areas: use a stable core set (areas classified the same in 2000 and 2007) with manual augmentation for coastal areas and poorly mapped classes.
- Ancillary data: incorporated as input features within RF rather than post-classification rules; enhances objectivity and integration.
- Spatial framework: no segmentation-based polygons in LCM2015; outputs are per-pixel classifications, aiding consistent change mapping and future analyses.
- Output and class changes: several updates to class definitions and mapping rules (e.g., Montane and Rough Grassland removed; mixed woodland labeled via pixel-level classification; 25 m raster structure expanded to two bands; probability handling streamlined).

## Land Cover classes and labeling
- 21 target classes aligned with Broad Habitats; some groups subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories subdivided).
- Labelling emphasizes per-polygon dominant class with detailed per-polygon composition (Pix_dist) and uncertainty metrics.

## Data quality, uncertainty, and guidance
- RF provides per-pixel probability; uncertainty conveyed at polygon level (and in band 2 of the 25 m raster for the GB product).
- Users should treat LCM2015 as a stable archive; recommended for use as land cover (not always directly equating to land use) and be cautious with change mapping due to classification and spectral differences over time.

## Data access and citation
- Data formats and access:
  - 1 km raster data accessible via the CEH Environmental Information Platform.
  - Full vector and 25 m raster products available on license on request from CEH.
  - Projections: GB (British National Grid); NI (TM75 Irish Grid).
- DOIs are provided for all LCM2015 products (GB vector, GB 25 m, GB 1 km, NI vector, NI 25 m, NI 1 km); use DOIs for citation to ensure reproducibility.
- Data use notes: license fees may apply; some applications restricted; follow CEH licensing process.

## Practical notes for analysts
- LCM2015 is designed for broad ecosystem monitoring, trend analysis, and integration with other UK environmental data.
- When comparing with earlier maps, account for changes in methodology (RF vs ML), spatial framework, and class definitions.
- The 25 m raster’s second band provides per-polygon classification confidence, useful for downstream modeling and uncertainty assessment.
- For UK-wide modeling, 1 km products offer efficient aggregation; for detailed site-level work, the 25 m and vector products provide richer class detail and metadata.

## Appendices and references
- Appendices provide Broad Habitat definitions and color-mapping guidance; supplementary details on composite images and class labelling rules.
- References include foundational works on Broad Habitats and the LCM2007/Countryside Survey lineage.
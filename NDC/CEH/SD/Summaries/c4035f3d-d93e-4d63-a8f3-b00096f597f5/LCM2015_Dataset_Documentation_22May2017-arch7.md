# Dataset documentation

- LCM2015 provides a range of land cover data products for the UK, designed for map-based data use and GIS analysis. It is a stable, archived dataset with individual DOIs for each product.

## Key purpose and cautions
- Designed to support a diverse user community with per-polygon vector data, 25m raster, and 1km products.
- Important caution: LCM2015 in its current state should not be used for change mapping; differences over time reflect real change, classification differences, and varying inputs/methods between products.

## Data products and formats
- Vector data (core product)
  - Great Britain and Northern Ireland provided as separate vector datasets.
  - ~6.7 million polygons (GB) and ~0.9 million polygons (NI).
  - Rich metadata attached to polygons; per-polygon attributes including dominant class and detailed breakdowns.
- 25m raster
  - 2-band raster: Band 1 = dominant LCM2015 class per polygon; Band 2 = mean per-polygon classification probability (from Random Forest).
- 1km raster products
  - Aggregate products for 1km squares based on 25m raster summaries.
  - Dominant class (1 band) and dominant aggregate class (1 band).
  - Percentage cover products (21 bands for classes; 10 bands for aggregate classes).

## Spatial coverage and projection
- Separate data sets for Great Britain and Northern Ireland.
- Projections:
  - GB: British National Grid (EPSG 27700).
  - NI: Irish National Grid (TM75 Irish Grid, EPSG 29903).

## Data access and citation
- 1km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25m raster: available under licence on request from CEH.
- Data citations: Each product has a DOI (GB vector, GB 25m, GB 1km percentage/dominant classes, GB 1km aggregates, NI equivalents) to ensure reproducibility.

## LCM2015 classes and aggregation
- Maps 21 target land cover classes based on UK Broad Habitats (JNCC Jackson 2000).
- Some classes are subdivided or aggregated for specific products:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral Sediment Broad Habitat split into Littoral sediment and Saltmarsh.
- 1km products provide both 21-class and 10-aggregate-class options.

## Data structure and attributes (highlights)
- Vector product attributes (example set)
  - gid: Unique polygon identifier.
  - BHAB: Dominant land cover at Broad Habitat level (text).
  - Pix_dist: List of 23 numbers giving pixel counts for each class plus total and modal_class.
  - unc: Per-polygon mean probability (0–255) from Random Forest.
  - unc_stdev: Standard deviation of the uncertainty.
  - npix: Number of pixels in the polygon.
  - Modal_class: LCM2015 target class as an integer (1–21).
  - Modal_prop: Proportion of polygon classified as the dominant class.
  - Composite: Identifier for the composite image used (99 = infill from LCM2007).
- 25m raster
  - Band 1: Dominant class per polygon (same 21-class scheme).
  - Band 2: Mean per-polygon probability (RF output).
- 1km raster
  - Dominant class (21-class and 10-aggregate options) and percentage cover per class (21 bands for 1km, plus aggregates).

## Methodology and differences from earlier maps (LCM2007)
- Classification algorithm
  - New: Random Forest classifier (handles multi-modal training data; no need for spectral sub-classes).
  - Previous: Maximum Likelihood Classifier.
- Training data and stability
  - Use of stable training areas (areas classified the same in 2000 and 2007) as a base, supplemented for coastal areas and historically poorly mapped classes.
  - Ancillary data (e.g., slope, distance to rivers) are now input data and integral to classification rather than post-classification corrections.
- Data and outputs
  - No spectral sub-classes; spectral sub-classes deemed redundant.
  - Montane class removed for change-mapping suitability; inland rock and other upland habitats used instead.
  - Rough Grassland class removed to align with JNCC Broad Habitat types; grassland types mapped spectrally without soil data.
  - 25m raster is two-band (classification and mean probability).
  - Segmentation-based spatial framework removed; per-pixel, per-polygon approach used to improve consistency and change-mapping potential.
- Mixed woodland handling
  - Training uses pure stands for Coniferous or Broadleaf woodland; polygon labels derived from per-pixel classifications and summarized to polygons (modal_class), with pix_dist available for detailed exploration.

## Spatial framework details
- LCM2015 maps land cover (not strictly land use); some land cover may resemble land use but is not always directly equivalent (e.g., arable crops vs arable land use).
- Minimum mappable area and MMU
  - Minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha or linear features < 20 m are dissolved into surrounding landscape.

## Uncertainty and quality information
- Uncertainty is quantified via per-pixel probability from the Random Forest classifier.
- Uncertainty is provided in vector (mean per polygon probability) and in the 25m raster (band 2).
- 1km products do not include per-pixel probability data, but are derived from 25m summaries.

## Documentation, metadata, and appendices
- Rich metadata for vector polygons, including dominant class and pixel-level breakdowns.
- Appendix and color-mapping guidance available for standard LCM2015 color mapping.
- DOIs and data-citation guidance provided to support reproducibility.

## Summary for GIS workflows
- Choose data product by need:
  - Vector: rich attributes, suitable for detailed queries and attribution; larger file sizes.
  - 25m raster: efficient for map display and analysis without polygon-level metadata.
  - 1km rasters: suitable for regional modeling and integration with other 1km data.
- Retain gid/addressing for unambiguous cross-referencing across products.
- Use aggregated 1km products if needing standardized, country-scale summaries.
- Be aware of differences from LCM2007 when comparing across time or scripts; ensure compatibility of data formats and spatial frameworks.
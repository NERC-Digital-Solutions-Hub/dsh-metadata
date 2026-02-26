# Dataset documentation

- LCM1990 is a parcel-based UK land cover map produced from Landsat-5 30m imagery, classifying into 21 Broad Habitat-based land cover classes. It supports compatibility with later LCM products (e.g., 2015) and enables 25-year change analyses.
- The dataset is provided in multiple data formats and resolutions (vector and raster) to support a range of applications, from detailed mapping to national-scale modelling.

## Data products and structure

- Core products
  - Vector dataset: polygon features for Great Britain and Northern Ireland with rich per-polygon attributes and metadata.
  - 25m raster: rasterized representation derived from the vector data, including per-polygon confidence and dominance information.
  - 1km raster products: aggregate percentage covers and dominant class per 1km pixel for both target (21 classes) and aggregate (10 classes) schemes.
- Classification and classes
  - 21 LCM1990 target classes mapped from the Broad Habitat framework (JNCC Jackson 2000).
  - Some Broad Habitats can be subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral/Saline coastal classes).
  - LCM1990 maps land cover (not always land use); some land-use inferences may be uncertain (e.g., recreation grass vs grazed grass).
- Attributes and metadata
  - Vector: gid (unique parcel ID), hist (class composition per polygon), mode (dominant LCM1990 class), purity, conf (per-polygon classifier confidence), stdev, n (pixels), cmp (composite image), among other attributes.
  - Raster: band 1 (dominant class), band 2 (mean per-polygon confidence), band 3 (percentage of polygon covered by modal class).
- Extent and samples
  - GB vector: ~6.7 million polygons; NI vector: ~0.9 million polygons.
  - 25m raster and 1km raster products supplied separately for GB and NI, with coordinate systems: British National Grid (GB) and Irish Grid (NI).

## Technical details

- Data formats and resolutions
  - Vector: polygon features with detailed attributes; suitable for precise communication through the gid and hist fields.
  - 25m raster: three-band GeoTIFF (dominant class, confidence, coverage) for GB and NI.
  - 1km raster: dominant cover (1-band) and percentage cover (21 bands for target; 10 bands for aggregate) for GB and NI.
- Spatial frameworks and comparability
  - LCM1990 is built on a refined spatial framework aligned with LCM2015 methods to enable long-term change products (1990–2015).
  - Projections: GB data in British National Grid; NI data in Irish Grid.
- Minimum mapping unit
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and linear features < 20 m are dissolved into surrounding landscape.
- Data access points
  - 25m and 1km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available under licence on request from CEH.
- DOIs and citation
  - All LCM1990 products have individual DOIs (GB vector, GB 25m raster, 1km target/aggregate classes, NI vector, NI 25m raster, NI 1km products). See Tables 5–6 in the document for details and citation examples.
- Data quality and validation
  - QA checks cover projections, spatial completeness, polygon modal class presence, value ranges (0–100 for rasters), and pixel size accuracy.
  - A full validation against other datasets (e.g., Countryside Survey, National Forest Inventory) has been performed; results published separately.

## Access, licensing, and usage notes

- Access and licensing
  - 25m and 1km rasters: available via the CEH EIP.
  - Full vector product: available on request; license fees may apply for some users/applications.
- Data citation guidance
  - Use the DOIs and cite authors and date in-text (e.g., Rowland et al., 2020) with full DOI references in the bibliography.
- Important usage considerations
  - LCM1990 maps land cover, not always land use; users should be cautious when inferring land use from land cover (e.g., recreation grass vs grazed grass).
  - Coasts: coastal mapping extent is constrained by the data boundaries; some coastal features may be mapped with limited extent.
  - 1km products: percentages are rounded; sums may not equal 100 exactly due to rounding and coastal area effects.
  - The dataset is a stable, archived resource with DOIs for reproducibility and traceability.

## Appendices and supporting information

- Appendix 1: Detailed notes on LCM1990 class definitions and interpretation (mapping nuances, training data, and caveats for specific Broad Habitats).
- Appendix 2: Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000) used to inform class labels.
- Appendix 3: Standard LCM colour mapping recipes for visualization of each class.
- Appendix 4: Composite image metadata used in LCM1990 production.

## Summary of key takeaways for data use and support

- LCM1990 provides a comprehensive, multi-format representation of UK land cover circa 1990, with detailed metadata and uncertainty information to aid data integration, analysis, and product development.
- The dataset is designed for broad applicability—from detailed GIS analyses using the vector data to national-scale modelling with 1km rasters—while offering interoperability with later LCM products for change detection.
- Practically, users should: leverage gid and hist for communicating and reconciling mixed parcels; use 25m rasters for detailed mapping and confidence estimates; utilize 1km products for large-scale analyses; cite DOIs for reproducibility; and consult the appendices for nuanced class interpretation and color mappings.
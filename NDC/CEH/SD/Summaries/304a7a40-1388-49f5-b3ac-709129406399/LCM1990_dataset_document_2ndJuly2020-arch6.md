# Dataset documentation

- LCM1990 is a parcel-based UK land cover map produced to support diverse user needs, classifying satellite data into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats. It uses Landsat-5 (30 m) two-date composites and aligns with the LCM2015 framework for cross-compatibility and to enable long-term change products.

- Data structure and formats
  - Vector data set: polygons with metadata attached; 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland. Core attributes include gid (unique polygon identifier), hist (class breakdown within the polygon), mode (recommended display class; 1–21), purity, conf (mean per-polygon RF confidence, 0–100), stdev, n (pixel count), and cmp (composite image source).
  - Raster data sets: derived from the vector; 25 m raster (three bands) and 1 km raster products. Great Britain and Northern Ireland have separate rasters due to different projections.
    - 25 m raster: band 1 = dominant class per polygon, band 2 = mean per-polygon RF confidence, band 3 = percent of polygon area covered by the modal class.
    - 1 km raster: dominant cover (21 target classes and 10 aggregate classes) and percentage cover (for both target and aggregate classes). Percentage values are integers and may not sum exactly to 100 due to rounding and coastal partial coverage.
  - Core workflow: vector → 25 m raster → 1 km percent/dominant products; 1 km products are used for large-scale modelling with other datasets.

- Classes and aggregation
  - 21 LCM1990 target classes mapped from the 21 Broad Habitat definitions; some broad habitats are split (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Aggregates: 10 aggregate classes used for 1 km raster products, enabling coarser analyses when full 21-class resolution is unnecessary.

- Spatial framework and geography
  - Vector and raster products are provided for Great Britain (GB) and Northern Ireland (NI) with respective projections: GB uses British National Grid; NI uses Irish Grid (TM75). Minimum mappable area is >0.5 ha; polygons smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding areas.

- Data quality, uncertainty, and validation
  - Uncertainty information included: per-pixel RF probability is summarized per polygon as mean probability (conf and stdev accompany the per-polygon statistics).
  - QA checks cover projections, spatial completeness, modal class presence in polygons (vector), value ranges (0–100 for raster percent products), and pixel sizes.
  - Validation has been conducted against other datasets (e.g., Countryside Survey, National Forest Inventory) and will be described in a separate publication.
  - Limitations and caveats: some grassland classes (Neutral, Calcareous) may be misclassified as Improved Grassland; fine distinctions among certain habitat types can be challenging due to spectral similarity and the MMU constraints. Small/mosaic patches (e.g., Fen, Marsh and Swamp) are frequently underestimated.

- Metadata, identification, and citation
  - LCM1990 is a stable, archived data set with Digital Object Identifiers (DOIs) for all products. DOIs should be cited in publications to support reproducibility.
  - Provisions include rich metadata per polygon (dominant class, per-class pixel counts, and classification probabilities) and documentation on how to interpret and map classes to the underlying Broad Habitats.

- Data access and licensing
  - 25 m and 1 km raster data are available via the CEH Environmental Information Platform (eip.ceh.ac.uk). The full vector product is available under licence on request from CEH; fees may apply.
  - Contact spatialdata@ceh.ac.uk for access details. More information is available at the LCM1990 data page.

- Projections and geographic details
  - GB data: British National Grid; NI data: TM75 Irish Grid. Details for coordinate referencing and pixel geometry are provided in the data documentation.

- Practical guidance for use
  - For detailed, localized analysis with rich polygon metadata, use the vector data and/or the 25 m raster; for large-scale modelling or across the UK, use the 1 km raster products.
  - When sharing results, consider masking or removing gid identifiers to avoid exposing internal identifiers; retain gid for development and communication among specialists if appropriate.
  - Use the DOIs when citing the data to ensure clear attribution and reproducibility.

- References and appendices
  - Appendices include detailed Biodiversity Action Plan Broad Habitat definitions, standard color mappings for LCM1990 classes, and notes on class interpretation and training considerations.
  - Acknowledgement: supported by NERC and part of UK-SCAPE National Capability.
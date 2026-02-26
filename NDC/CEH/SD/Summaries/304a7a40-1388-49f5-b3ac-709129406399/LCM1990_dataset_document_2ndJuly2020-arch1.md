# Dataset documentation

- Land Cover Map 1990 (LCM1990) dataset documentation provides an introduction to the 21-class, parcel-based UK land cover map created from Landsat-5 two-date composites at 30m resolution, aligned with the LCM2015 framework to enable long-term change products.
- The data are structured to support a range of users, from researchers to policy and management bodies, with emphasis on robust metadata, uncertainty information, and clear data provenance.

## What LCM1990 is and how it’s built

- Classifies satellite imagery into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats definitions.
- Built as polygons that reflect real-world boundaries (vector) and also produced derived 25m rasters and 1km products for broad-scale analyses.
- The spatial framework is designed to be compatible with LCM2007 and LCM2015, enabling the creation of long-term change products (1990–2015 and beyond).
- Data framework uses OS MasterMap for GB and Land & Property Services large-scale vector data for Northern Ireland; tabled methods ensure consistency with later LCM products.
- Minimum mapping unit is 0.5 ha; parcels smaller than 0.5 ha or linear features under 20 m are dissolved into surrounding landscape.

## Data products and formats

- Vector dataset
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each parcel has a unique geometry identifier (gid) and a rich attribute set, including dominant class, per-polygon pixel breakdown, mean probability, and classification confidence.
  - Key attributes include: gid, hist (class composition per polygon), mode (recommended dominant LCM1990 class), purity, conf (confidence 0–100), stdev, n (pixel count), and cmp (source composite image).
- Raster datasets
  - 25m raster (GB and NI): three bands per pixel (dominant class, per-polygon confidence, and percentage of polygon covered by the modal class).
  - 1km raster products: dominant cover for 21 target classes and 10 aggregate classes; percentage cover for each class (21 target and 10 aggregate). Rounding may cause sums to deviate from exactly 100%.
  - Spatial references: GB uses British National Grid; NI uses TM75 Irish Grid.
  - Data extents and pixel sizes: GB 25m and 1km rasters; NI 25m and 1km rasters; detailed dimensions provided in the data documentation.
- DOI-cited products
  - Each LCM1990 product (vector, GB 25m raster, 1km products, NI counterparts) has a DOI to enable formal citation and reproducibility.

## Class structure and mapping

- 21 LCM1990 classes mapped from Broad Habitats (JNCC Jackson 2000). Some classes are subdivided for spectral distinctions:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather Grassland.
  - Littoral Sediment split into Littoral Sediment and Saltmarsh (Priority Habitat).
- Aggregate classes provide a simplified, higher-level schema for some analyses (especially at 1km).
- Tables and appendices provide the mapping between LCM1990 classes and aggregate classes, and the color mapping used for standard visualization.

## Uncertainty, quality, and validation

- Uncertainty information is embedded: Random Forest per-pixel probability is summarized as mean per polygon for vector data and raster bands.
- QA checks cover projections, spatial completeness, modal class presence, data range validation (0–100 for rasters), and pixel size accuracy.
- Validation has been conducted against external datasets (e.g., Countryside Survey, National Forest Inventory) with results reported in separate publications; field boundary updates between maps are considered limited in impact.

## Data access and usage notes

- Access points
  - 25m and 1km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available on request from CEH (licensing may apply).
  - Licensing and access details are provided on CEH’s LCM1990 pages; contact: spatialdata@ceh.ac.uk.
- Citation and DOIs
  - All LCM1990 products have individual DOIs; guidance is provided on how to cite (author, year, title, DOI) in publications.
  - Example citation format is specified (e.g., Rowland et al., 2020) with full DOI references for each product.
- Map projections and coordinate reference
  - GB vector/raster use British National Grid; NI uses Irish Grid (TM75) or equivalent for its datasets.
- Documentation and further information
  - Additional details on data access, product specifications, and technical tables are provided in the main document, with appendices covering class definitions, color mappings, and composite image information.

## Quality assurance and provenance

- Documentation highlights robust processing pipelines and versioning (LCM1990 and its alignment with LCM2015 methods).
- Provenance traces from source imagery through classification to polygon-level outputs, with metadata preserved for reproducibility.
- Ongoing and future validation efforts are noted, with results to be published separately.

## Appendices and supplemental material

- Appendix 1: Class interpretations and caveats for LCM1990 Broad Habitat mappings.
- Appendix 2: Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000).
- Appendix 3: Colour mapping recipe for standard LCM1990 class visualization.
- Appendix 4: Details on composite images used in the classification process.

## Acknowledgement and references

- Funded by the Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- References to foundational habitat classifications and prior LCM reports (e.g., Jackson 2000; Morton et al. 2011; Rowland et al. 2020) are provided for context and methodological grounding.

## Summary of end-user guidance

- For analysts: LCM1990 offers a rich, well-documented land cover dataset with both detailed vector polygons and scalable raster products, enabling robust local to national-scale analyses, change detection, and habitat-based modelling, while emphasizing data provenance, uncertainty, and reproducible citation.
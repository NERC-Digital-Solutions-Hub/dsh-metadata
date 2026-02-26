# Dataset documentation

- Provides Land Cover Map 1990 (LCM1990) data products to support diverse user requirements.
- UK parcel-based land cover map created from Landsat-5 (30 m) imagery, classified into 21 Broad Habitat classes.
- Built to be compatible with LCM2015/LCM2007 frameworks to enable long-term change studies (25-year change product).

## What LCM1990 is and how it’s structured

- Scope: Land cover mapping (not land use) for the UK, with 21 classes based on UK Biodiversity Action Plan Broad Habitats.
- Data products:
  - Vector data set: parcels/polygons with rich metadata and 21-class labeling.
  - 25 m raster: derived from vector with three bands (dominant class, mean per-polygon confidence, percentage coverage of modal class).
  - 1 km raster products: dominant cover and percentage cover for both 21 target classes and 10 aggregated classes.
- Spatial framework and comparability:
  - Uses an updated LCM2007 framework; designed to align with LCM2015 for cross-product compatibility.
  - GB vector/raster in British National Grid; Northern Ireland in TM75 Irish Grid.
- Minimum mapping unit:
  - Parcels must be >0.5 ha; lines <20 m dissolved into surrounding landscape.

## Classes and mapping details

- 21 LCM1990 target classes mapped; some refinements:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather Grassland.
  - Littoral Sediment split into Littoral Sediment and Saltmarsh (Priority Habitat).
- Class definitions anchored in Broad Habitat concepts (Appendix 2 provides JNCC Broad Habitat definitions).
- Vector attributes (key ones):
  - gid: unique parcel identifier.
  - _hist: list of classes present in polygon with pixel counts.
  - _mode: recommended dominant LCM1990 class (1–21).
  - _purity: percentage of polygon covered by modal class.
  - _conf: mean confidence (0–100) from Random Forest per polygon.
  - _stdev: standard deviation of uncertainty.
  - _n: number of pixels in polygon.
  - _cmp: composite image index used for classification.

## Data formats and products

- Vector data
  - 6.7 million polygons (Great Britain) and 0.9 million (Northern Ireland).
  - Rich polygon-level metadata per feature.
- Raster data
  - 25 m raster: 3-band GeoTIFF (dominant class, confidence, modal coverage percentage).
  - 1 km rasters: dominant cover (21-target and 10-aggregate classes) and percentage cover (21-band and 10-band sets).
- Data volumes and organization:
  - Spatial detailing ranges from vector polygons to 1 km summary products for UK-wide modelling and integration with other data (e.g., meteorology, species distributions).

## Data access, formats, and citation

- Access
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence; licence fees may apply.
- DOIs and citation
  - Each LCM1990 product has a DOI to facilitate repeatable citation (GB vector, GB 25 m raster, GB 1 km target/dominant/percentage products; NI equivalents also provided).
  - Example citation format includes author(s) and year, with full DOI in references.
- Examples of usage
  - DOIs enable reproducible methods and usage tracking; recommended for scientific publications.

## Quality assurance and validation

- QA checks ensure:
  - Correct projections and spatial completeness.
  - Modal class presence in all polygons (vector).
  - Metadata headings match documentation.
  - Raster values fall within 0–100 for percentage products.
  - Pixel sizes and coordinate systems are correct.
- Validation
  - Cross-validated against other datasets (e.g., Countryside Survey, National Forest Inventory).
  - Full validation reported in a separate publication.

## Metadata, uncertainty, and provenance

- Rich metadata per polygon, including:
  - Dominant class, per-polygon pixel breakdown, processing lineage, and classification probabilities.
- Uncertainty
  - Random Forest per-pixel probability reproduced as per-polygon mean probability (and included in raster bands).
- Processing lineage
  - Based on the 2007 OS MasterMap-derived parcel framework; field boundary changes are infrequent, with methodology designed for consistency across LCM generations.

## Citing and further information

- Documentation and access details
  - Data access: CEH Environmental Information Platform; licensing inquiries via spatialdata@ceh.ac.uk.
  - CEH project information: Land Cover Map 1990 data pages.
- Acknowledgement and funding
  - Supported by Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme.

## Appendices overview (supporting interpretation and usage)

- Appendix 1: Class interpretation notes and mapping nuances (e.g., mixture in woodland, grassland distinctions, floodplain considerations).
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats (JNCC definitions for the 22 Broad Habitats, aligned with LCM1990 classes).
- Appendix 3: Standard color mapping recipe for LCM1990 classes (for map visuals).
- Appendix 4: Composite images used in LCM1990 production (image metadata and dates).
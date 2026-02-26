# Dataset documentation

- UK Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map, classifying Landsat-5 imagery (30 m) into 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Built to be compatible with LCM2015/LCM2007 frameworks to enable long-term land cover change analyses (25-year change product).

## Data products and formats

- Vector data set
  - Polygons with rich attributes per parcel, including dominant class, per-polygon pixel breakdown, and classification confidence.
  - gid: unique parcel identifier; hist: list of present classes with pixel counts; mode: recommended display class; conf: mean per-polygon classification confidence; n: number of pixels in polygon; cmp: source composite image.
  - Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons.
- Raster data sets
  - 25 m raster: 3-band (band1: dominant class per polygon; band2: mean confidence; band3: percent coverage of modal class).
  - 1 km raster: dominant class per 1 km cell (for target and aggregate classes) and percentage cover per class (21 target, 10 aggregate bands). Rounding may cause sums to deviate from 100; coastal areas may sum to less than 100.
  - Separate GB and NI rasters due to different projections.
- Spatial framework and classes
  - 21 LCM1990 target classes aligned with Broad Habitats; subset aggregation available for 1 km products.
  - Some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Resolution and sampling
  - Minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha or linear features < 20 m dissolved into surrounding landscape.

## Data access and identifiers

- Data access
  - 25 m and 1 km rasters available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH (licensing may apply).
- Documentation of DOIs
  - Each LCM1990 product has a DOI for citation (GB vector, GB 25 m raster, GB 1 km target/dominant/aggregate, NI equivalents).
  - Example citation format provided; facilitates reproducibility and usage tracking.

## Metadata, uncertainty, and quality assurance

- Rich metadata
  - For each polygon: dominant class, per-class pixel counts, mean classification confidence, and processing details.
- Uncertainty information
  - Random Forest classifier yields per-pixel probability; reported per-polygon mean confidence and associated statistics.
- Quality Assurance (QA)
  - Comprehensive checks (projections, spatial completeness, modal class presence for vector, value ranges for rasters, pixel sizes).
  - Validation against external datasets (Countryside Survey, National Forest Inventory, validation points) with results to be published separately.
- Provenance and framework
  - Built on LCM2007/2015 methods; uses OS MasterMap-based framework; designed to facilitate cross-LCM comparisons and 25-year change analyses.

## Class definitions and mapping

- 21 LCM1990 classes rooted in JNCC Broad Habitat definitions (Appendix 2).
- Notable mappings
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral/Supralittoral categories distinguished (Rock and Sediment), with Saltmarsh included in Littoral Sediment.
- Appendix 3 provides a standard color mapping for mapping outputs.
- Appendix 1 and 2 give detailed class interpretation guidance and biodiversity habitat context.

## Usage considerations and caveats

- LCM1990 maps land cover (not always directly deducible land use).
- Minimum mapping unit and tender boundaries may affect boundary precision; fragmentation at small scales is dissolved to surrounding landscape.
- 1 km products are summarized from 25 m rasters; rounding can lead to minor sum discrepancies.
- Coarse-resolution products (1 km) are suitable for national-scale modelling alongside other data (meteorology, species distributions).

## Citations and further information

- DOIs provided for all products; citation recommended in publications (e.g., Rowland et al., 2020).
- Access details and contact information: CEH Spatial Data team; spatialdata@ceh.ac.uk; https://eip.ceh.ac.uk/lcm/lcmdata
- Acknowledgement: NERC Environmental Information Centre support; UK-SCAPE programme.

## Appendices (overview)

- Appendix 1: Class-specific notes and interpretation guidance for mapping in LCM1990.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions.
- Appendix 3: Standard LCM color mapping recipes.
- Appendix 4: Composite images used in LCM1990 (metadata for imagery used in classification).
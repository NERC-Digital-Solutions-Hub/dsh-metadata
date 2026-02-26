# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classifying Landsat-5 imagery into 21 Broad Habitat-based classes. It provides both vector and raster data products designed for a range of applications and user needs.
- The dataset is archived with stable DOIs for citation and is available through CEH’s Environmental Information Platform, with access to the full vector product on request and potential licensing fees.

## Data products and structure

- Vector data set
  - Contains 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each parcel (polygon) has key attributes including:
    - gid: unique geometry identifier
    - hist: list of present classes with pixel counts per class within the polygon
    - mode: recommended dominant LCM1990 target class (1–21)
    - purity: percent coverage by the modal class
    - conf: mean per-polygon confidence (0–100) from Random Forest
    - stdev: uncertainty standard deviation
    - n: number of pixels in the polygon
    - cmp: composite image index used for the classification
- Raster data sets (derived from the vector)
  - 25 m raster (GB and NI separately)
    - 3-band GeoTIFF: band 1 = dominant class per polygon, band 2 = mean per-polygon confidence, band 3 = percent polygon covered by modal class
    - Spatial reference systems: Great Britain uses British National Grid; Northern Ireland uses TM75 Irish Grid
  - 1 km raster products (GB and NI)
    - Dominant cover at 1 km for target and aggregate classes (1-band)
    - Percentage cover at 1 km for target (21 bands) and aggregate (10 bands) classes
    - Rounding may cause sums to differ from 100; coastal values may sum to less than 100 due to mapping extent and MMU considerations
- Class structure and mapping
  - 21 LCM1990 target classes aligned to UK Broad Habitat definitions
  - Table 2 provides the relationship between Broad Habitats, aggregate classes, and LCM1990 target classes
  - Some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland)
- Metadata and color mapping
  - Appendix 3 provides standard colour mappings for each LCM1990 class
  - Appendix 1/2 explain class definitions and Broad Habitat interpretations
- Data formats and documentation
  - Core product is the 1990 vector; 25 m raster derived from it; 1 km products built from 25 m data
  - DOIs are provided for each product (vector, 25 m raster, 1 km target/aggregate classes, etc.)

## Quality assurance, validation, and provenance

- QA checks include:
  - Projection accuracy and spatial completeness
  - Presence of a modal class in all polygons (vector) and value ranges (0–100 for rasters)
  - Correct pixel sizes and alignment with metadata
- Validation
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) and a core validation point set
  - Results of validation published separately
- Processing lineage
  - Based on a consistent parcel framework derived from 2007 Ordnance Survey MasterMap data
  - Vector polygons are summarized to polygons with associated metadata; 25 m rasters are generated from vector data; 1 km rasters aggregate 25 m data

## Data access, licensing, and citation

- Access points
  - 25 m and 1 km raster data sets: available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product: available under licence on request from CEH
- Licensing and fees
  - Some users/applications may incur licence fees; contact spatialdata@ceh.ac.uk for details
- Citing LCM1990
  - Each product has its own DOI and should be cited in publications
  - Example citation format provided in the dataset documentation (Rowland et al., 2020 and related DOIs)
  - See Tables 5 and 6 for GB and NI DOIs and product titles
- Projections and geographic scope
  - GB data: British National Grid (OSGB36)
  - NI data: Irish Grid (TM75)

## Usage notes and considerations

- Minimum mapping unit
  - Parcels smaller than 0.5 ha and linear features under 20 m are dissolved into the surrounding landscape
- Classification nuance and interpretation
  - LCM1990 maps land cover (not strictly land use); some land-use inferences may be ambiguous from remote sensing alone
  - Some Broad Habitat classes can be spectrally similar; metadata and hist/consensus attributes help in interpretation
- Data scale and aggregation
  - Vector provides rich polygon-level metadata; raster products offer a simpler per-pixel view for modelling at national scales
  - 1 km products are suitable for UK-scale modelling with other datasets (e.g., meteorology, species distribution)

## Appendices and supplementary information (highlights)

- Appendix 1: Detailed class interpretations and mapping notes for LCM1990 classes
- Appendix 2: Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000)
- Appendix 3: Recipe for standard LCM colour mapping for visualization
- Appendix 4: Composite images used in LCM1990 classification (metadata for image sources and dates)

## Contact and further information

- Data access and inquiries: spatialdata@ceh.ac.uk; https://eip.ceh.ac.uk/lcm/lcmdata
- CEH contact and licensing details: https://www.ceh.ac.uk/services/land-cover-map-1990
- References and further documentation available through CEH Environmental Information Platform and the cited DOIs
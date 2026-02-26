# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map produced from two-date Landsat-5 composites (30m) and classified into 21 Broad Habitat-based classes. It replaces the previous LCMGB and aligns with the LCM2007/LCM2015 spatial framework to support long-term land cover change analyses (25-year progression). DOIs are provided for citation.

## Data products and structure

- Vector data set
  - ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon contains rich metadata and eight key attributes, including dominant class (mode), history of class composition (_hist), certainty (_conf), and the per-polygon sample size (_n).
  - Unique geometry identifier (gid) preserved for unambiguous communication.
- Raster data sets
  - 25m raster derived from the vector data (three-band: dominant class, mean confidence, and modal coverage).
  - 1km raster products: dominant cover (1-band) for target and aggregate classes; and percentage cover (21 target bands and 10 aggregate bands). Values are integer-rounded; coastal areas may sum to less than 100 due to mapping extents.
  - GB and Northern Ireland datasets provided separately to reflect distinct projections (British National Grid for GB; Irish Grid for NI).

## Class definitions and aggregation

- LCM1990 uses 21 classes derived from UK Broad Habitats (JNCC Jackson 2000). Some classes are subdivided for detail:
  - Built-up Areas and Gardens split into Suburban and Urban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral Sediment split into Littoral sediment and Saltmarsh (Priority Habitat).
- The dataset offers both detailed 21-class products and aggregated 10-class (Broad Habitat-based) products for 1km rasters.

## Spatial framework and comparability

- Built on a refined OS MasterMap-based spatial framework to ensure polygons reflect real-world boundaries and facilitate compatibility with LCM2015.
- Aimed to enable a 25-year land cover change product (1990–2015) by using a consistent framework across LCM generations.

## Metadata and uncertainty

- Rich per-polygon attributes include dominant class, per-class pixel counts, mean probability from the classifier, and confidence metrics (Random Forest probability) for per-pixel and per-polygon uncertainty.
- Uncertainty is quantified as mean per-polygon probability; 25m rasters include a mean confidence band.
- Minimum mappable unit is >0.5 ha; polygons smaller than 0.5 ha or linears <20 m are dissolved into surrounding landscape.

## Data access and formats

- Access via the CEH Environmental Information Platform (eip.ceh.ac.uk). Full vector product available on request; license fees may apply for some users/applications.
- Data formats:
  - Vector: polygon shapefile/Geopackage-like structure with gid and metadata.
  - Raster: uncompressed GeoTIFFs (GB and NI) at 25m and 1km with specified coordinate systems.
- Projections:
  - Great Britain: British National Grid (OSGB 27700).
  - Northern Ireland: Irish Grid (TM75), with corresponding 1km and 25m extents.

## Data citation and DOIs

- All LCM1990 products have individual DOIs to support repeatable citation:
  - GB vector; GB 25m raster; GB 1km percentage/dominant target classes; GB 1km percentage/dominant aggregate classes.
  - NI vector; NI 25m raster; NI 1km percentage/dominant target classes; NI 1km dominant/aggregate classes.
- Example citation format: Rowland et al. (year). Land Cover Map 1990 (vector, GB) etc., with the corresponding DOI.

## Quality Assurance

- QA measures include: projection correctness, spatial completeness checks, modal class existence in polygons (vector), header consistency, raster value ranges (0–100 for 1km rasters), and pixel size verification.
- Validation performed against independent datasets (e.g., Countryside Survey, National Forest Inventory) with results to be reported in a separate publication.
- Dataset creation follows a documented, reproducible workflow; field boundary changes are infrequent and mapped within the established parcel framework.

## Appendices and supporting information (highlights)

- Appendix 1: Notes on LCM1990 classes with habitat-specific interpretations and common misclassifications (e.g., grassland types, bracken, bog, fen, littoral types) and guidance on aggregating classes where appropriate.
- Appendix 2: Biodiversity Action Plan Broad Habitats (JNCC definitions) corresponding to the LCM1990 classes.
- Appendix 3: Standard color mapping recipe for LCM1990 classes (RGB values per class).
- Appendix 4: Composite images used during classification (metadata of images, dates, and paths).

## Further information and contact

- Data access portal: https://eip.ceh.ac.uk/lcm/lcmdata
- Licensing and access inquiries: spatialdata@ceh.ac.uk
- Related journal publication and data citations forthcoming; references include Jackson (2000), Morton et al. (2011), Rowland et al. (2020a,b).

## References and acknowledgements

- Key references for methodology and classification framework (JNCC Broad Habitats; LCM2007/LCM2015 lineage).
- Acknowledgement: Support from NERC and UK-SCAPE programme.
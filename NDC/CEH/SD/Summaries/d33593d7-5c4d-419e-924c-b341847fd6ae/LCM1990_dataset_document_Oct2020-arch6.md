# Dataset documentation

- LCM1990 is a parcel-based land cover map for the UK produced from two-date Landsat-5 imagery (30 m resolution) and classified into 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- It replaces the previous LCMGB and is produced using the same methods as LCM2007/LCM2015 to ensure compatibility for long-term change analysis (up to 25 years).

## Data products and formats

- Core products:
  - Vector data set (polygons with rich attributes)
  - 25 m raster derived from the vector data
  - 1 km raster products (aggregate and dominant cover)
- Class structure:
  - 21 target LCM1990 classes (based on Broad Habitats)
  - 10 aggregate classes used for 1 km raster products
- Data relationships:
  - 1 km products provide both dominant cover and percentage cover per class
  - 25 m raster and vector products carry per-polygon confidence and distribution of classes within each polygon
- Spatial detail and use:
  - Vector: detailed polygon boundaries with metadata; larger file size
  - 25 m raster: detailed per-polygon dominance with confidence and area share
  - 1 km rasters: suitable for UK-wide modelling with other data (e.g., climate, species distributions)

## Classes and labeling

- 21 LCM1990 target classes (e.g., Broadleaf woodland, Coniferous woodland, Arable and Horticulture, Various grassland types, Water bodies, Built-up areas, Coastal and Littoral habitats, etc.)
- Some classes are subdivided for spectral clarity (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral/Supra-littoral distinctions).
- LCM1990 maps land cover (not always directly equating to land use). For example, arable crop cover indicates arable land use, but some land uses may be visually similar to other covers.
- Minimum mapping unit and dissolution:
  - Minimum mappable area > 0.5 ha
  - Parcels < 0.5 ha and linear features < 20 m dissolved into surrounding landscape

## Data access and citation

- Access:
  - 25 m and 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product available on request from CEH (licensing may apply)
- Projections:
  - Great Britain: British National Grid
  - Northern Ireland: Irish Grid (TM75)
- DOIs and citing:
  - All LCM1990 products have individual DOIs; cite using author, date, and full DOI
  - Example formats provided in the documentation (tables for GB and NI products)
- Example data access and citations:
  - GB vector, GB 25 m raster, GB 1 km percentage/dominant target classes, GB 1 km aggregate classes (and NI equivalents) with their DOIs
- Acknowledgement:
  - Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability

## Technical specifics

- Data structure:
  - Vector: six.7 million polygons (GB) and 0.9 million polygons (NI)
  - 25 m raster: three-band raster (band 1: dominant class per polygon; band 2: mean per-polygon confidence; band 3: percentage of polygon covered by modal class)
  - 1 km rasters: dominant class and percentage cover for both target and aggregate classes
- Coordinates and pixel details:
  - Pixel size: 25 m for 25 m rasters; 1000 m for 1 km rasters
  - South-west corner references used for pixel geometry
- Quality assurance:
  - QA checks for projections, spatial completeness, polygon modal class, value ranges (0–100 for rasters), and pixel sizes
  - Comprehensive validation against reference datasets (e.g., Countryside Survey, National Forest Inventory); formal validation published separately
- Metadata and provenance:
  - Rich metadata per polygon (dominant class, per-class pixel counts, mean classification probability)
  - Uncertainty information included (Random Forest per-pixel probability, mean per polygon)
  - Data are archived with DOIs and stable identifiers to support reproducibility

## Appendices and additional information

- Appendix 1: Class definitions and mapping notes (how Broad Habitat definitions map to LCM1990 classes; guidance on common mapping ambiguities)
- Appendix 2: Biodiversity Action Plan Broad Habitats (definitions of each broad habitat class)
- Appendix 3: Standard LCM color mapping (RGB mappings for classes)
- Appendix 4: Composite images used in LCM1990 (image metadata for reproducibility)
- Data citation and usage guidance: how to reference DOIs in publications and recommendations for attributing authors and date

## Contact and further information

- Data access: CEH Environmental Information Platform and spatialdata@ceh.ac.uk for vector data
- More information: https://eip.ceh.ac.uk/lcm/lcmdata
- Journal and related publications: LCM1990-related journal paper in preparation; related Rowland et al. (2020a, 2020b) papers for land cover change products
- Acknowledgement and project context: NERC award NE/R016429/1, UK-SCAPE programme
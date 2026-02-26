# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- Purpose and scope
  - Countryside Survey 1984 estimates of Broad Habitat areas in Great Britain.
  - National stock estimates (Habitats 1-17) for 1984, derived using the 1998 ITE Land Classification.
  - Results presented as total areas (000s ha) per Broad Habitat within each Land Class, including 95% confidence intervals (lower and upper estimates).

- Data files and structure
  - CS1984_Broad_Habitat_Stock.csv
    - Columns:
      - YEAR: Survey year
      - LAND_CLASS: ITE Land Class
      - BROAD_HABITAT: Broad Habitat code
      - BROAD_HABITAT_NAME: Broad Habitat description
      - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
      - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
      - LOWER_ESTIMATE: Lower 95% CI for Broad Habitat area (000s ha)
      - UPPER_ESTIMATE: Upper 95% CI for Broad Habitat area (000s ha)
  - cs1984_stock.tif
    - Raster file with 1 km pixel resolution; each band corresponds to a Broad Habitat class.
    - Band-to-Habitat mapping indicates which habitat corresponds to each band (e.g., Band 2: Coniferous Woodland; Band 3: Boundary/Linear Features; etc., with variations for Broad Habitat 1 vs Broad Habitat 2 as described).
    - Pixel size: 1 km (1000 m)
    - Spatial reference: British National Grid (OSGB36), Transverse Mercator
    - Extent: Great Britain

- Spatial, temporal, and provenance details
  - Spatial reference and extent designed for Great Britain.
  - Data are drawn from Countryside Survey 1984 and aligned with ITE Land Classification frameworks (Bunce et al. 1996; 1998) and related Habitat guidance (Jackson 2000).
  - Acknowledgement and copyright requirements:
    - Data owned by NERC - Centre for Ecology & Hydrology.
    - All use must be acknowledged; Countryside Survey data © NERC CEH.

- Data quality, metadata, and accessibility considerations
  - Metadata specifics include classification sources, confidence intervals, and pixel-level habitat percentages for raster bands.
  - Potential barriers for monitoring use:
    - Public sharing of underlying datasets and metadata quality considerations.
    - Need for data provenance and consistent metadata to verify suitability for new analyses.
  - The 1984 baseline nature of the data may limit comparability with newer datasets without careful harmonisation of classifications.

- Relevance for monitoring frameworks
  - Provides a baseline of Broad Habitat stock by Land Class across Great Britain for 1984, enabling trend analysis when integrated with subsequent surveys.
  - Offers both area estimates (CSV) and spatially explicit habitat distributions (1 km raster), supporting aggregated reporting and map-based monitoring dashboards.
  - The dual presentation (means with confidence intervals and spatial rasters) supports uncertainty-aware monitoring and policy evaluation.

- References and further information
  - Core sources: Countryside Survey 1984 methodologies; ITE Land Classification (Bunce et al., 1996; 1998); Jackson (2000) habitat guidance.
  - Related publications and technical context available through Countryside Survey materials and accompanying technical reports.
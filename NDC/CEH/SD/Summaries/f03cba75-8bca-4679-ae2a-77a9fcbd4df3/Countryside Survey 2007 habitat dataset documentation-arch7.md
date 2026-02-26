# Broad Habitat Area Estimates by Land Class for Great Britain

- Overview
  - National estimates of Broad Habitat stock (Habitats 1-17) for 2007, calculated using the 2007 ITE Land Classification.
  - Units are total area in thousands of hectares (000s ha); includes lower and upper 95% confidence limits.
  - Freshwater habitats were analyzed with a different statistical model from other habitats.
  - Data produced by Countryside Survey, CEH; data and publications available through Countryside Survey resources.

- Data products
  - CS007_Broad_Habitat_Stock.csv
    - Columns:
      - YEAR: Year of Survey
      - LAND_CLASS: ITE Land Class
      - BROAD_HABITAT: Broad Habitat code
      - BROAD_HABITAT_NAME: Broad Habitat description
      - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
      - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha) (may include negative values due to model; treat as 0)
      - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
      - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
  - CS2007_Stock.tif
    - A 1 km resolution raster where each band represents a Broad Habitat class.
    - Each 1 km pixel contains a mean percentage estimate of that habitat within the square.
    - Band-to-habitat mapping is provided (i.e., which Broad Habitat class each band corresponds to; includes cross-walk with Land Class strata such as Coniferous Woodland, Broadleaved Mixed and Yew Woodland, etc.).
    - Spatial resolution: 1 km (1000 m); Coordinate system: British National Grid; Projection: Transverse Mercator Great Britain.

- Spatial and technical details
  - Spatial reference: OSGB1936 (British National Grid)
  - Pixel size: 1 km (1000 m)
  - Extent: Great Britain
  - Data are suitable for map-based visualizations and GIS analyses of habitat distribution by Land Class, with per-class and per-area estimates.

- Data usage and standards
  - All Countryside Survey data must be acknowledged in copies, publications, and presentations.
  - Acknowledgement text (to be used on all copies and outputs):
    - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
    - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
  - Note: The dataset includes negative MEAN_ESTIMATE values due to modelling; these should be treated as 0 in analyses or presentations.

- Data provenance and references
  - Primary sources include:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007
    - Scott (2007) CS Technical Report No.4/07: Statistical methods for deriving national estimates from 1 km squares
    - Bunce et al. (1996, 1981) ITE Merlewood Land Classification
    - Jackson (2000) Guidance on the interpretation of Biodiversity Broad Habitat Classification
    - Countryside Survey field mapping methodologies and related documentation
  - Useful links and reports are listed in the data documentation and cited references.
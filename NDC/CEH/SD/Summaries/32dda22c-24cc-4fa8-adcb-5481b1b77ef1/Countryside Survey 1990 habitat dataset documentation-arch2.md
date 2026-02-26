# Broad Habitat Area Estimates by Land Class for Great Britain 1990

- Purpose and scope
  - National estimates of Broad Habitat stock (Habitats 1–17) for 1990, calculated using the 2007 ITE Land Classification.
  - Provides total area in 000s hectares for each Broad Habitat per Land Class, with lower and upper 95% confidence limits.
  - Note: Freshwater habitats were analyzed with a different statistical model; there was no separate Montane (BH15) class in 1990.

- Data files and content
  - CS1990_Broad_Habitat_Stock.csv
    - Year of survey (YEAR)
    - ITE Land Class (LAND_CLASS)
    - Broad Habitat code (BROAD_HABITAT)
    - Broad Habitat description (BROAD_HABITAT_NAME)
    - Total area of relevant Land Class (LAND_CLASS_AREA) in 000s ha
    - MEAN_ESTIMATE (000s ha) with potential negative values (treat as 0)
    - LOWER_ESTIMATE and UPPER_ESTIMATE (95% confidence interval, 000s ha)
  - cs1990_stock.tif
    - 1 km pixel raster; each pixel band represents a Broad Habitat class as mapped to Land Class strata
    - Pixel value indicates mean percentage of habitat in that square for that Broad Habitat
    - Notes: 1 km pixels; there was no Montane class in 1990; mapping adjustments: Band 15 corresponds to BH16, Band 16 to BH17

- Key fields and units
  - YEAR: survey year (1990)
  - LAND_CLASS: ITE Land Class (from Bunce et al. classifications)
  - BROAD_HABITAT / BROAD_HABITAT_NAME: habitat code and description (Habitats 1–17)
  - LAND_CLASS_AREA: total area of relevant Land Class (000s ha)
  - MEAN_ESTIMATE / LOWER_ESTIMATE / UPPER_ESTIMATE: area estimates for each Broad Habitat within each Land Class (000s ha)
  - Units: 000s hectares; mean may be negative due to the statistical model (treat as 0)

- Important notes for interpretation
  - Negative MEAN_ESTIMATE values should be treated as zero
  - 1990 estimates are derived using the 2007 ITE Land Classification framework
  - No Montane (BH15) class exists in 1990 data

- Spatial reference and coverage
  - Raster: 1 km grid (pixel size 1000 m)
  - Coordinate system: British National Grid (OSGB36)
  - Projection: Transverse Mercator
  - Extent: Great Britain

- Data usage, acknowledgement and accessibility
  - All Countryside Survey data must be acknowledged
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; rights reserved
  - Data are intended to support monitoring environmental health and policy performance; outputs can be shared via standard formats (CSV, TIFF) and published in reports or maps

- How this data supports monitoring and analysis
  - Provides standardized, comparable national estimates of Broad Habitat areas by Land Class for 1990
  - Enables historical comparisons and trend analyses when combined with later datasets (e.g., 2007 results), with awareness of classification framework changes
  - Facilitates integration with other environmental data sources for broader monitoring (e.g., habitat–land-use relationships, landscape change)

- Related references and context
  - Countryside Survey methodology and outputs (overview and technical reports)
  - ITE Land Classification of Great Britain (Merlewood classifications)
  - Guidance documents on interpreting Broad Habitat classifications (JNCC) and related public biodiversity classifications
  - Links and citations provided in the dataset documentation for further methodological details and historical context
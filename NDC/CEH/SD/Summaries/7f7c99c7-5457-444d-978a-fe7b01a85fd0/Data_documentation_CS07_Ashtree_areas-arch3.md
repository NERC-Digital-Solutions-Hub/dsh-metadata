# Countryside Survey: Ash tree distribution in areas <5ha,  2007

- Purpose and scope
  - Provides estimates of ash trees for Great Britain within broadleaved woodland areas less than 5 hectares, derived from Countryside Survey 2007 data.
  - Aimed at monitoring environmental health indicators and informing policy decisions, with a focus on small-scale woodland areas to complement broader datasets.

- Data sources and context
  - Primary dataset: CS07_ashtree_areas (ash presence in 2007 within <5ha broadleaved woodlands).
  - Associated data sources:
    - ITE Land Classification (1990) with 32 land classes.
    - Land Cover Map 2007 (1 km raster).
    - Countryside Survey outputs and documentation.
  - Coverage and limitations:
    - Represents ash presence in 2007 for GB, restricted to areas where ash is present.
    - For internal analyses, the CS also limits representation to woodlands under 0.5 ha to avoid duplication with Forestry Commission data.

- Data structure and metadata
  - Columns:
    - Gridcode: code for band interval (1-7) corresponding to Ha_per_km bands.
    - Ha_per_km: estimated hectares of ash per km^2, provided in 7 bands:
      0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5 (text values).
  - Spatial resolution: 1 km.
  - Coordinate system / projection: British National Grid (OSGB36), Transverse Mercator.
  - Extent: Great Britain.

- Methods and calculation approach
  - Sampling framework: Countryside Survey uses 1 km squares across GB with stratified random sampling based on major ecological gradients (land classes).
  - Within each 1 km square:
    - Habitats mapped and assigned to Broad or Priority Habitat.
    - Dominant species recorded by percentage cover categories (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).
  - Ash data handling:
    - The dataset reflects areas where ash is present in 2007, focusing on woodlands <0.5 ha to avoid duplication with other datasets.
    - Mean area of ash woodland within each 1 km square is calculated by land class.
    - The per-square mean is multiplied by the area of each land class and summed across land classes to produce a national estimate (in hectares) for the areal extent of ash in GB.
  - Land classification and scaling:
    - Base land classification: 1990 ITE Land Classification with 32 classes.
    - Means per land class are scaled to a percentage of 1 km by weighting according to the proportion of Broadleaved Woodland in each 1 km square, using Land Cover Map 2007 data.

- Outputs and usage
  - Delivers a national (GB) estimate of ash extent within broadleaved woodlands, derived from 1 km square data and land-class weighting.
  - Facilitates monitoring of ash distribution patterns and trends over time, and supports policy analysis related to woodland composition and biodiversity.
  - More information and methods documentation available at Countryside Survey outputs site and related references.

- Accessibility and governance
  - Data are linked to broader Countryside Survey datasets (Land Classification, Land Cover Map 2007) and associated literature.
  - Metadata and transformation details are essential for reuse; the dataset relies on standard, transparent methodologies to enable verification and replication.
  - Barriers highlighted in general monitoring contexts (e.g., data access, data sharing, metadata quality) may apply, underscoring the need for clear data governance and open sharing of underlying data where possible.

- References and further reading
  - Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013), Maskell et al.
  - CS_Sampling_Strategy_Revised (2007/2011)
  - Barr et al. (1998) and related CEH/Land Classification publications
  - LCM2007 Final Report and UK results from 2007
  - Countryside Survey outputs and project documentation available at the official Countryside Survey site
# Tree Distribution (2007) Dataset Documentation

- Overview
  - Documentation for CS07_Ash_Ind_Trees: estimates of individual ash trees outside woodland across Great Britain, derived from Countryside Survey 2007 data.
  - Purpose: provide national-scale estimates of the areal extent of ash (Fraxinus excelsior) in GB by land class, using a stratified sampling framework.

- Dataset Details
  - File: CS07_Ash_Ind_Trees
  - Coverage: Great Britain
  - Content: records of individual ash trees in the landscape (outside woodland or hedgerows); includes up to 10 veteran trees per 1km square (maximum 2 per species).
  - Measurement: Mn_tree_km — mean number of individual ash trees per 1km square for each land class.
  - Spatial units: 1km squares; point features for trees (field or hedgerow); small clumps included if below the minimum mappable unit (mmu) of 20m x 20m; trees above mmu would be captured in area data.
  - Resolution: 1km
  - Extent: Great Britain
  - Coordinate system / Projection: British National Grid, OSGB36; Projection specified as Transverse Mercator

- Sampling & Land Classification
  - Sampling design: stratified random sampling of 1km squares across GB, based on land classes representing major ecological gradients (soil, geology, climate).
  - Land classification: 2007 ITE Land Classification with 45 land classes.
  - Variables: LC2007 (numeric land class), LandClass (text description)

- Data Columns
  - LC2007: Land Class numeric code
  - LandClass: Land Class textual description
  - Mn_tree_km: Mean number of individual ash trees per 1km square within the land class

- Calculating National Estimates
  - Method: national estimate = sum over land classes of (mean ash trees per 1km square in the land class) × (area of that land class)
  - Rationale: uses a stratified sampling framework to scale from sample squares to country-wide areal estimates
  - Notes: ash trees recorded as point features; national areal extent derived by aggregating across land classes

- Spatial & Reference Information
  - Extent: Great Britain
  - Resolution: 1km
  - Projection: OSGB36 / British National Grid; coordinate system described as Transverse Mercator

- Associated Datasets & References
  - ITE Land Classification (2007)
  - Countryside Survey (UK results 2007) and associated CEH reports
  - Related methods and technical reports:
    - Distribution of Ash trees in Countryside Survey data (2013)
    - CS Sampling Strategy and its revisions
    - LCM2007: Final Report for the new UK land cover map

- Use for Analysis and Considerations
  - Suitable for analyzing national-scale distribution of ash outside woodland and exploring relationships with land-class gradients
  - Useful as a basis for correlations with environmental variables, or for modeling spatial patterns at 1km resolution
  - Cautions:
    - Scale limitation: 1km squares; local accuracy may be limited
    - Includes small clumps below mmu; larger clumps captured in area data
    - Data are tied to the 2007 Countryside Survey framework and land classification; applicability to other years requires careful harmonization
  - Access & Provenance: dataset is documented with methodological references; main methods information available at www.countrysidesurvey.org.uk

- Documentation & Further Reading
  - Primary dataset documentation and file details
  - Supporting literature and methodological reports listed under "Further reading" in the dataset documentation
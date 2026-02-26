# Countryside Survey: Individual Ash tree distribution 2007

- Overview
  - Dataset contains estimates of individual ash trees in Great Britain, outside woodland or hedgerows, based on Countryside Survey 2007 data.

- Data content
  - Records individual ash trees observed within 1km squares (landscape trees, not in woodland).
  - Includes up to 10 veteran trees within each 1km square (maximum 2 per species).
  - National estimates created by: mean number of ash trees per 1km square by land class (Mn_tree_km) multiplied by the area of each land class and summed across all land classes to yield GB areal extent (in hectares) of ash.
  - Land classification used: 2007 ITE Land Classification with 45 land classes.
  - Extent: Great Britain; Resolution: 1km.

- Data structure and fields
  - Columns include:
    - LC2007 (Land Class numeric)
    - LandClass (Land Class text)
    - Mn_tree_km (Mean number of ash trees per 1km square by land class)
  - Additional metadata:
    - Resolution: 1km
    - Coordinate system: British National Grid
    - Projection: Transverse Mercator
    - Extent: Great Britain
    - Projection detail: OSGB1936

- Methods and derivation
  - Countryside Survey uses stratified random sampling of 1km squares across GB based on major ecological gradients (soil, geology, climate).
  - Within each 1km square, all individual trees outside woodland are recorded with an estimated modal DBH.
  - National GB estimates derived by summing (mean trees per 1km square by land class × land class area) across all land classes.
  - Data reflect 2007 land classification (45 classes). Small clumps are included if above the minimum mappable unit (mmu 20m × 20m); otherwise they would be included in area data.

- Associated datasets and access
  - ITE Land Classification (2007)
  - Countryside Survey (official site)
  - More information and methods are described in related publications and technical reports (listed in the document).

- Usage notes for data support
  - Useful for regional-to-national-scale analysis of ash distribution outside woodlands.
  - Enables integration with land-class and habitat data; suitable for trend analysis or environmental risk assessments.
  - As a survey-derived estimate, users should account for sampling design and potential uncertainties in extrapolation across land classes.
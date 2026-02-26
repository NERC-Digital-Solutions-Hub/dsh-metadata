# Countryside Survey: Individual Ash tree distribution 2007

## Overview
- Dataset of estimates for individual ash trees in Great Britain, outside woodland and hedgerows, based on Countryside Survey 2007.
- File: CS07_Ash_Ind_Trees; 1km (resolution) spatial units; data stored in British National Grid.

## Data content and structure
- Columns:
  - LC2007: Land Class (numeric)
  - LandClass: Land Class (text)
  - Mn_tree_km: Mean number of individual ash trees per 1km square per land class
- Spatial characteristics:
  - Resolution: 1km
  - Extent: Great Britain
  - Coordinate system/Projection: OSGB36 (British National Grid, Transverse Mercator)

## Spatial, resolution and technical details
- Trees recorded are those in the landscape (outside woodland or hedgerows).
- Data are derived from 1km square samples across GB using stratified random sampling by land class (based on major ecological gradients).
- Up to 10 veteran trees per 1km square recorded (maximum 2 per species).

## Methodology and estimation approach
- Within each 1km square, every individual ash tree in the landscape is recorded, with modal DBH estimated.
- National estimates produced by:
  - Calculating mean ash trees per 1km square by land class.
  - Multiplying by the area of each land class.
  - Summing across all land classes to yield GB-wide areal extent estimates for ash.

## Data sources, classifications and associations
- Land classification: 2007 ITE Land Classification, 45 land classes.
- Methodological context and related outputs described in Countryside Survey documentation (2007 results, sampling strategy, and related technical reports).

## Data quality, limitations and governance
- Sample-based estimates; precision depends on stratified sampling design.
- Limitations include 1km resolution; mmu considerations (20m x 20m) for inclusion of small clumps; excludes trees within woodland.
- Focused on ash trees; limited to Great Britain and to landscape trees outside woodland/hedgerows.

## How to use in GIS and best practices
- Suitable for map-based visualization of ash distribution across GB by land class.
- Can be used with the 2007 ITE Land Classification map to allocate 1km counts by region and to estimate national ash extent.
- Ensure alignment to OSGB36 / British National Grid when integrating with other GB spatial datasets.

## References and further reading
- Associated datasets: ITE Land Classification (2007); Countryside Survey outputs (UK Results 2007) and related technical reports.
- Key sources for methods and context:
  - Distribution of Ash trees in Countryside Survey data (2013) and supporting CS Technical Reports on sampling and land classification.
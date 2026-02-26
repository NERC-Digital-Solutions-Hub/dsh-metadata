# Tree Distribution (2007) Dataset Documentation

## Overview
- Documentation for Countryside Survey: Individual Ash tree distribution 2007 (GB)
- File: CS07_Ash_Ind_Trees
- Purpose: provide estimates of individual ash trees outside woodland across Great Britain, based on Countryside Survey 2007 data
- Data copyright: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Document version: 1:19-8-2013
- Prepared by: C.M. Wood, L.C. Maskell, P.A. Henrys, CEH Lancaster

## Dataset details
- Content: estimates of individual ash trees in Great Britain (trees in the landscape, outside woodland or hedgerows)
- Associated datasets:
  - ITE Land Classification (2007)
  - Countryside Survey (www.countrysidesurvey.org.uk)
- Columns:
  - LC2007: Land Class (numeric)
  - LandClass: Land Class (text)
  - Mn_tree_km: Mean number of individual ash trees per 1km per land class
- Resolution: 1km
- Spatial reference: British National Grid
- Projection: Transverse Mercator
- Extent: Great Britain
- Notes: OSGB36 projection referenced; used for national-scale estimation

## Methods and data collection
- Survey design: Countryside Survey samples 1km squares across GB using a stratified random sampling scheme based on land classes that reflect major ecological gradients
- In each 1km square:
  - Record every individual ash tree in the landscape (outside woodland)
  - Record modal DBH
  - Include small clumps (if above minimum mappable unit of 20m x 20m); clumps below mmu excluded from area data
  - Record up to 10 veteran trees per square (maximum 2 per species)
- National estimates: sum of trees within each 1km square by land class, multiplied by the land class area, then aggregated across land classes to produce GB-wide areal extent of ash
- Land classification used: 2007 ITE Land Classification with 45 land classes
- Methods references and further reading provided for detailed methodology

## Data quality, governance and reuse considerations
- Metadata and provenance are documented (file details, coordinate system, projection, extent)
- Methodology emphasizes reproducibility across squares and land classes, with explicit mmu and veteran-tree considerations
- Documentation links to additional sources and technical reports for transparency and potential updates
- Suitable for data discovery and reuse within governance frameworks that require structured 1km-resolution, landscape-scale tree distribution data

## References and further reading
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013)
- CS Sampling Strategy and related technical reports (various authors, 1998–2011)
- Related outputs:
  - ITE Merlewood Land Classification of Great Britain (1996)
  - Countryside Survey UK Results from 2007 (Carey et al. 2008)
  - Final Report for LCM2007 (Morton et al. 2011)
- External links:
  - ITE Land Classification (2007): DOI provided
  - Countryside Survey outputs: www.countrysidesurvey.org.uk
  - CS Technical Reports and PDFs referenced in the documentation
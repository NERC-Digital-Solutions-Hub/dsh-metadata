# Countryside Survey: Individual Ash tree distribution 2007

## Overview
- Dataset documentation for estimates of individual ash trees in Great Britain, outside woodland or hedgerows, based on Countryside Survey 2007 data.
- File details pertain to the CS07_Ash_Ind_Trees dataset and related metadata.
- Data credited to NERC - Centre for Ecology & Hydrology; prepared by CEH authors.

## Data Content and Structure
- Columns:
  - LC2007 (Land Class numeric)
  - LandClass (Land Class text)
  - Mn_tree_km (Mean number of individual ash trees per 1km per land class)
- Resolution: 1 km
- Coordinate system/Projection: British National Grid (OSGB36), Transverse Mercator
- Extent: Great Britain
- Purpose: Estimates of individual ash trees in the landscape (outside woodland) derived from Countryside Survey 2007 data
- The dataset uses a stratified random sample of 1 km squares across GB based on land classes formed from major ecological gradients (so that national estimates can be scaled from samples)

## Methods and how national estimates are produced
- In each 1 km square, all individual trees in the landscape are recorded with an estimate of modal DBH; small clumps below mmu (minimum mappable unit) 20 m x 20 m are treated specially (if below mmu, included in area data; if above, included in tree counts).
- Up to 10 veteran trees are recorded per 1 km square (maximum 2 per species).
- National estimates are computed by:
  - Calculating mean ash trees per 1 km square by land class
  - Multiplying by the area of each land class
  - Summing across all land classes to obtain the national areal extent of ash for GB
- Land classification used: 2007 ITE Land Classification with 45 land classes
- Methods sources and further methodological details are available at www.countrysidesurvey.org.uk

## Data Access, Metadata, and Provenance
- Data are © NERC - Centre for Ecology & Hydrology; Countryside Survey data are cited as the basis for estimates
- The document provides associated datasets and references, including:
  - ITE Land Classification (2007)
  - Countryside Survey outputs and UK results from 2007
- Related references for methodological context and historical sampling strategies are listed (e.g., CS Sampling Strategy, land classification literature, and CEH technical reports)
- File details and version: Document Version 1:19-8-2013
- Metadata considerations mentioned include data sharing, data governance, and the potential need to fill metadata gaps by consulting data originators

## Related Resources and Further Reading
- ITE Land Classification (2007) dataset
- Countryside Survey: UK Results from 2007
- CS Sampling Strategy (revisions and methodologies)
- Final Report for LCM2007 and related CEH outputs
- Additional references listed in the dataset documentation for context on sampling and land classification

## Implications for Monitoring Frameworks
- Demonstrates a framework for deriving national-scale biodiversity measures from stratified 1 km square sampling and land-class weighting.
- Shows how to translate landscape-level observations (individual trees outside woodland) into national estimates of species distribution (ash) via area-weighted aggregation by land class.
- Highlights data governance and metadata considerations critical for monitoring frameworks:
  - Need for accessible, well-documented metadata and provenance
  - Importance of sharing underlying data while respecting rights and governance
  - Potential barriers from data format transformation, timeliness, and data silos
- Useful for policy monitoring of tree species distribution, disease impact assessments (e.g., ash decline), and landscape-scale monitoring programs.
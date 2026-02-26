# Tree Distribution (2007) Dataset Documentation

## Overview
- Documents the Countryside Survey: Individual Ash tree distribution 2007 dataset (CS07_Ash_Ind_Trees).
- Provides estimates of individual ash trees in Great Britain outside woodland or hedgerows, derived from Countryside Survey 2007 data.
- Data are prepared and credited to NERC – Centre for Ecology & Hydrology (CEH).

## Dataset Details
- File: CS07_Ash_Ind_Trees
- Content: Estimates of individual ash trees in GB landscapes outside woodland/hedgerows.
- Associated datasets: ITE Land Classification (2007); Countryside Survey (website).
- Columns:
  - LC2007 (Land Class numeric)
  - LandClass (Land Class text)
  - Mn_tree_km (Mean number of individual ash trees per 1km square per land class)
- Resolution: 1 km
- Extent: Great Britain
- Coordinate system / Projection: British National Grid (OSGB36), Transverse Mercator

## Methods and Sampling
- Countryside Survey uses a stratified random sample of 1 km squares across GB based on land classes representing major ecological gradients.
- In each 1 km square, all individual trees in the landscape (outside woodland) are recorded, with an estimate of modal DBH.
- Small clumps are included if below the minimum mapping unit (mmu) of 20 m × 20 m; larger clumps are captured in area data.
- Up to 10 veteran trees per 1 km square are recorded (maximum 2 per species).

## Estimation and Calculations
- National estimates are produced by:
  - Calculating the mean number of ash trees within each 1 km square by land class.
  - Multiplying by the area of each land class.
  - Summing across all land classes to obtain the national areal extent of ash for GB.
- Land classification used: 2007 ITE Land Classification, consisting of 45 land classes.

## Data Quality, Provenance, and Access
- Data originate from Countryside Survey 2007; document version 1:19-8-2013.
- Data rights: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Metadata supports discoverability: extent, coordinate system, projection, resolution, and data lineage.
- Further information and related literature are available at the Countryside Survey website and in referenced methodological documents.

## References and Further Reading
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (Maskell et al., 2013)
- Barr (1998) Sampling Strategy for Countryside Survey; revised by Wood (2011)
- Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Morton et al. (2011) CS Technical Report No 11/07: Final Report for LCM2007
- Links to Countryside Survey outputs and LCM2007 final reports included in references
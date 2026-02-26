# Countryside Survey: Ash tree distribution in areas <5ha, 2007

## Overview
- Dataset provides estimates of ash trees for Great Britain specifically in broadleaved woodland areas less than 5 hectares.
- Based on Countryside Survey 2007 data.
- Aims to support national-scale assessment of ash distribution within targeted woodland areas.

## Data Content and Structure
- Columns:
  - Gridcode: Code for the 1km square band interval relating to ash per km square (values 1-7; numeric).
  - Ha_per_km: Estimate of the number of hectares of ash per 1km square, defined in seven bands: 0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5 (text representing band intervals).
- Resolution: 1 km.
- Coordinate system: British National Grid (OSGB36), projection Transverse Mercator.
- Extent: Great Britain.

## Data Geography and Coverage
- Based on 1km squares across GB, using a stratified random sampling system tied to land classes.
- Represents areas where ash is present in 2007 within broadleaved woodland <5ha; excludes larger woodlands to avoid duplication with Forestry Commission data.

## Methodology and Calculations
- In each 1km square, habitats are mapped and dominant species recorded by percentage cover (e.g., categories such as <10%, 10-25%, 25-50%, etc.).
- Mean ash woodland area within a 1km square by land class is calculated from percentage cover data (mid-point of ranges).
- National GB ash area estimate derived by:
  - Multiplying mean ash area per land class by the area of each land class.
  - Summing across land classes.
  - Land classification used: 1990 ITE Land Classification with 32 classes.
  Scaling by the proportion of Broadleaved Woodland in each 1km square (per Land Cover Map 2007).
- More detailed methodological context available in accompanying Countryside Survey documentation and related readings.

## Related Data
- ITE Land Classification (1990)
- Land Cover Map 2007 (1km raster)
- Countryside Survey (general outputs and datasets)

## Notes and Limitations
- Focuses on ash distribution within broadleaved woodland areas <5ha; not a complete national ash-density map.
- Assembly relies on 2007 field observations and the 1990 land classification framework, scaled to 2007 land cover context.
- Data intended to enable self-serve analyses and integration with other CS outputs.

## Further Reading and References
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (Maskell et al., 2013)
- The Sampling Strategy for Countryside Survey (Barr; revised by Wood, 2011)
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996)
- Countryside Survey: UK Results from 2007 (Carey et al., 2008)
- LCM2007 Final Report: Final Report for the new UK land cover map (Morton et al., 2011)
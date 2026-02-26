# Countryside Survey: Ash tree distribution in areas <5ha, 2007

## Overview
- Dataset CS07_ashtree_areas provides estimates of ash trees for Great Britain in broadleaved woodland areas less than 5 hectares.
- Based on Countryside Survey 2007 data.

## Data file details
- Columns:
  - Gridcode: Code for the band interval relating to the hectares of ash per km^2 (1–7, numeric).
  - Ha_per_km: Estimated hectares of ash per km^2, based on Countryside Survey measurements, presented in 7 bands: 0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5 (text).
- Resolution: 1 km.
- Coordinate system / Projection: British National Grid (OSGB1936), Transverse Mercator.
- Extent: Great Britain.

## Methods and context
- Countryside Survey sampling:
  - 1 km squares across GB, using stratified random sampling by land classes derived from major ecological gradients.
  - In each 1 km square, habitats are mapped and dominant species recorded by percent cover categories.
- Ash distribution estimation:
  - Mean area of ash woodland within a 1 km square by land class is calculated.
  - This mean is multiplied by the land class area and summed across land classes to yield national estimates (areal extent of ash for GB).
- Land classification and weighting:
  - Uses 1990 ITE Land Classification (32 land classes).
  - Means per land class are scaled to a percentage of 1 km squares by weighting according to the proportion of Broadleaved Woodland in each 1 km square, based on Land Cover Map 2007 (LCM2007).
- Additional information:
  - More methodological details available at www.countrysidesurvey.org.uk.

## Scope and limitations
- The dataset focuses on ash distribution in woodlands within small areas, specifically less than 5 ha.
- To avoid duplication with Forestry Commission analyses, the CS approach emphasizes smaller woodland units (noted as <0.5 ha in some contexts within CS outputs).

## Associated datasets and sources
- ITE Land Classification (1990) — 32 land classes.
- Land Cover Map 2007 (1 km raster).
- Countryside Survey project outputs (www.countrysidesurvey.org.uk).

## Practical notes for GIS work
- Suitable for map-based products showing spatial distribution of ash in small broadleaved woodland patches across GB.
- Data are aligned to GB national grid and 1 km resolution, enabling aggregation or overlay with LCML and other landClassification data.
- Interpret Ha_per_km values as categorical bands representing ash presence intensity within each 1 km grid cell.
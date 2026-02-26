# This dataset provides a 1km resolution raster (gridded) coverage of wooded areas in riparian zones across Great Britain.

## Overview
- Provides a 1km resolution raster (GeoTIFF) showing the proportion of woodland within riparian zones across Great Britain.
- Riparian areas are defined by buffering the CEH 1:50,000 watercourse network by 50 metres.
- Wooded areas are identified from Land Cover Map 2007 (LCM2007) as coniferous or deciduous woodland.

## Data Processing
- Buffer the CEH 1:50,000 watercourse network by 50 metres.
- Dissolve the buffered network into a single polygon feature.
- Clip the LCM2007 25m raster to the dissolved polygon extent.
- Extract raster cells corresponding to woodland classes: LCM2007 class 1 (Coniferous) and class 2 (Deciduous).
- Calculate total woodland areas from LCM2007 within each clip and express as the percentage of riparian area per 1km square.

## Data Inputs
- CEH 1:50,000 watercourse network.
- Sub-set of UK digital 1:50,000 river centreline network (Moore, Morris & Flavin, 1994).
- Land Cover Map 2007 (LCM2007) for GB (25m raster), derived from satellite imagery and digital cartography; related to UK Biodiversity Action Plan Broad Habitats.
- Sources referenced: ESRI ArcGIS Desktop (10.3); Moore et al. 1994; Morton et al. 2014.

## Data Structure
- Format: 1km resolution GeoTIFF (.tif).
- Spatial reference: OSGB 1936 / British National Grid.
- Each cell contains the proportion (as a percentage) of wooded riparian areas within that 1km square.

## Usage and Applications
- Enables end users to self-serve analyses of riparian woodland coverage by 1km cells.
- Suitable for landscape planning, environmental assessments, policy development, and monitoring changes in riparian woodland within Great Britain.
- Can be used to compare across regions, support reporting, or feed dashboards and charts that visualize riparian woodland distribution.

## Considerations
- Temporal context: based on LCM2007 data; woodland classifications reflect 2007 land cover, not current conditions.
- Spatial scale: results are aggregated to 1km cells, which may smooth finer-grained patterns.
- Methodology relies on buffering and clipping steps, which may influence edge-cells near boundaries.

## References
- ESRI (2016) ArcGIS Desktop: Release 10.3.
- Moore, R.V., Morris, D.G. and Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network. NERC, Institute of Hydrology.
- Morton, R.D., Rowland, C.S., Wood, C.M., Meek, L., Marston, C.G., Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.
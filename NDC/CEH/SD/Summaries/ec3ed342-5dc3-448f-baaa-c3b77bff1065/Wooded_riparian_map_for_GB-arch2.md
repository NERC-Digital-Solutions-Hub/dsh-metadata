# Wooded riparian areas in Great Britain (1km raster)

## Aim
- Provide a standardised, 1km resolution raster that quantifies the proportion of woodland within riparian zones across Great Britain, enabling consistent monitoring of environmental health and policy performance over time.

## Description
- 1km resolution raster coverage of wooded areas in riparian zones across Great Britain.
- Riparian areas defined by a 50 metre buffer around the CEH 1:50,000 watercourse network.
- Wooded areas within the buffer identified using Land Cover Map 2007 woodland classes (Coniferous or Deciduous).
- Data aggregated to 1km cells and expressed as a percentage of riparian area that is woodland.

## Data Processing
- Buffer the CEH 1:50,000 watercourse network by 50 metres.
- Dissolve the buffered network into a single polygon.
- Clip the corresponding areas from the LCM2007 25m raster using the polygon.
- Extract woodland values (LCM07 classes 1 and 2) from the clipped raster.
- Calculate total woodland area per 1km cell and express as the percentage of riparian area within that cell.

## Data Inputs
- CEH 1:50,000 watercourse network (and related river centreline dataset; UK origin).
- Land Cover Map 2007 (LCM2007) 25m raster for GB.
- Ordnance Survey-derived river network data forming the base layer.

## Data Structure
- Output format: 1km resolution GeoTIFF (.tif).
- Spatial Reference: OSGB 1936 / British National Grid.
- Each cell value: proportion of the riparian area within that 1km square that is woodland, expressed as a percentage.

## Use and Applications for Analysts
- Enables time-series monitoring of riparian woodland cover in a standard, comparable format.
- Suited for producing maps and charts to support environmental health assessments and policy evaluation.
- Designed for storage and sharing on appropriate data portals to facilitate access and reuse.

## Data Quality, Limitations and Considerations
- Based on a 50m riparian buffer and 25m LCM2007 data, aggregated to 1km, which may smooth fine-scale patterns.
- Woodland classification limited to LCM2007 woodland classes (coniferous and deciduous).
- Temporal context tied to LCM2007 data (2011 release) and related inputs; may not reflect the most recent land-cover changes.

## References
- ESRI (2016) ArcGIS Desktop: Release 10.3.
- Moore, R.V., Morris, D.G. and Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network. NERC, Institute of Hydrology.
- Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.
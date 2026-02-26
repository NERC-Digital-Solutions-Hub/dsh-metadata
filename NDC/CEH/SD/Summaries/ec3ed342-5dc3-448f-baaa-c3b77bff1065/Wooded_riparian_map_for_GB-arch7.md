# 1km resolution raster coverage of wooded areas in riparian zones across Great Britain

- Purpose: A map-based data product for GIS specialists to visualise and analyse the extent of woodland within riparian zones across Great Britain at a uniform 1km resolution.

## What the dataset represents

- 1km resolution raster (GeoTIFF) where each cell shows the percentage of riparian woodland within that 1km square.
- Riparian areas defined by a 50 metre buffer around the CEH 1:50,000 watercourse network.
- Wooded areas identified from Land Cover Map of Great Britain 2007 (LCM2007) as coniferous or deciduous woodland.

## Data processing workflow

1. Buffer the CEH 1:50,000 watercourse network by 50 metres.
2. Dissolve the buffered network into a single polygon (ArcMap 10.3).
3. Clip corresponding areas from the LCM2007 (25m) raster using the dissolved polygon.
4. Extract raster cells belonging to woodland classes (LCM2007 classes 1 = Coniferous, 2 = Deciduous).
5. Calculate total woodland areas per 1km cell and express as the percentage of riparian area in that cell.

## Data inputs

- CEH 1:50,000 watercourse network (baseline line data).
- Sub-set of UK digital 1:50,000 river centreline network (Moore, Morris, Flavin, 1994; NERC CEH).
- Land Cover Map 2007 (25m raster, GB) v1.2 (LCM2007) linked to UK Biodiversity Action Plan habitats.

## Data structure and metadata

- File type: 1km resolution GeoTIFF (.tif).
- Spatial reference: OSGB 1936 / British National Grid.
- Value meaning: proportion of the wooded riparian area within each 1km square, expressed as a percentage.

## Applications and notes for GIS work

- Suitable for map-based visualisations of riparian woodland coverage and for spatial analyses of woodland-riparian interactions.
- Useful in planning, policy briefing, and public-facing map products to illustrate woodland extent in riparian zones.

## References

- ESRI (2016) ArcGIS Desktop: Release 10.3.
- Moore, R.V., Morris, D.G., Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network. NERC, Institute of Hydrology.
- Morton, R.D. et al. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.
# Summary

- This dataset provides a 1km resolution raster (gridded) coverage of wooded areas in riparian zones across Great Britain.

## Riparian definition and woodland classification

- Riparian areas are defined by applying a 50 metre buffer to the CEH 1:50000 watercourse network.
- Wooded areas within this buffer are those classified in Land Cover Map 2007 (LCM2007) as either coniferous (class 1) or deciduous (class 2) woodland.
- The data are aggregated to a 1km resolution.

## Data processing workflow

1. Buffer the CEH 1:50,000 watercourse linear network by 50 metres.
2. Dissolve the buffered network into a single polygon feature.
3. Clip corresponding areas from the LCM2007 25m raster dataset using the dissolved polygon.
4. Extract woodland (LCM07 classes 1 and 2) values from the clipped raster.
5. Calculate total woody areas for these classes within each 1km cell and express as the percentage of riparian area per 1km grid square.

## Data inputs

- CEH 1:50,000 watercourse network (Moore, Morris, Flavin, 1994). Based on OS 1:50,000 maps.
- Land Cover Map 2007 (LCM2007) 25m raster (GB). Morton et al., 2014. Datasets hosted by NERC Environmental Information Data Centre.

## Data structure and format

- File type: 1km resolution GeoTIFF (.tif).
- Spatial reference: OSGB 1936 / British National Grid.
- Each cell value: proportion of wooded riparian area within that 1km cell expressed as a percentage.

## References

- ESRI (2016) ArcGIS Desktop 10.3.
- Moore et al. (1994) CEH river network subset (UK 1:50k).
- Morton et al. (2014) LCM2007 (25m raster, GB) v1.2.
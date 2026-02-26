# Land Cover Map 2007 (LCM2007) is available in different formats, to suit the requirements of various users.

## Overview for GIS Specialists
- Provides both vector and raster data products of land cover for the UK to support map-based visualisations and spatial analyses.

## Data formats and specifications

- Vector data
  - Each polygon represents a land parcel with attributes describing land cover.
  - Metadata describes how the information was derived.
  - Minimum Mapable Unit: 0.5 hectare.
  - Coverage: UK.
  - Supply format: ESRI Shapefile.

- Raster data
  - Five raster products in total.
  - 25 x 25 m raster: assigns the most likely Broad Habitat to each pixel.
  - Four freely available 1 x 1 km rasters: summarize the 25 m raster data.
  - Pixel sizes: 25 m and 1 km.
  - Coverage: UK.
  - Supply format: GeoTiff.

## Documentation and metadata
- Further information available in the Land Cover Map 2007 Dataset Documentation.
  - Table 1: Attributes of the LCM2007 vector dataset.
  - Table 2: Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Table 3: Metadata information for the raster datasets.

## Practical notes for use
- Choose vector (Shapefile) for detailed parcel-level analysis and attribute queries.
- Choose raster (GeoTiff) for wall-to-wall coverage analyses and broad habitat mapping at 25 m and aggregated 1 km scales.
- Refer to the Dataset Documentation for schema, class mappings, and raster metadata to inform data joins, symbolisation, and quality checks.
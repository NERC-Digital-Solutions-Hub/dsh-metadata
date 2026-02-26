# Land Cover Map 2007 (LCM2007)

## Overview
- Provides UK land cover data in both vector and raster formats to meet diverse user needs.
- Includes detailed metadata and derivation information to support reuse and understanding.

## Data formats and specs

- Vector data
  - Most detailed product: polygons representing land cover parcels with attributes and metadata on how derived (see Dataset Documentation)
  - Minimum mapable unit: 0.5 ha
  - Supply format: ESRI Shapefile
  - Coverage: UK

- Raster data
  - Five raster products in total
  - 25 x 25 m raster: most likely Broad Habitat per pixel
  - Four freely available 1 x 1 km rasters: summarise the 25 m raster
  - Scales: 25 m and 1 km pixel sizes
  - Supply format: GeoTiff
  - Coverage: UK

## Documentation and metadata
- Detailed metadata and class information are available in the Land Cover Map 2007 Dataset Documentation, including:
  - Table 1: Attributes of the LCM2007 vector dataset
  - Table 2: Habitats, LCM2007 classes and Broad Habitat sub-classes
  - Table 3: Metadata information for the LCM2007 raster datasets

## Practical considerations for Data Stewards
- Formats (Shapefile and GeoTIFF) support interoperability and sharing via standard data portals.
- Metadata and class descriptions are centralized in the Dataset Documentation, aiding data governance, discovery, and reuse.
- Ensure alignment of data creation with the specified minimum mapping unit and class definitions when curating or integrating LCM2007 data.
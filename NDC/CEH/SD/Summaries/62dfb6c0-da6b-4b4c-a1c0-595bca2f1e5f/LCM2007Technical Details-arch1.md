# Land Cover Map 2007 (LCM2007)

## Overview
- LCM2007 provides land cover information for the UK in multiple formats to suit different user needs (vector and raster).

## Data formats and content

- Vector data
  - Most detailed product: polygons representing land cover parcels
  - Each polygon includes attributes describing land cover and metadata on derivation
  - Minimum mapable unit: 0.5 hectares
  - Supply format: ESRI Shapefile

- Raster data
  - Five raster products in total
  - A 25 x 25 m raster gives the most likely Broad Habitat for each pixel
  - Four freely available 1 x 1 km rasters summarise the 25 x 25 m raster
  - Detailed metadata available in the Land Cover Map 2007 Dataset Documentation

## Scales, resolution, and coverage

- Scales/resolutions
  - Vector: 0.5 ha minimum mapping unit
  - Raster: 25 m pixel size (primary), plus four 1 km pixel size rasters
- Coverage: United Kingdom (UK)

## Access and documentation

- Further information is available in the Land Cover Map 2007 Dataset Documentation
  - Table 1: Attributes of the LCM2007 vector dataset
  - Table 2: Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Table 3: Metadata information for the raster datasets

## Analyst considerations

- Choose data format based on analysis scale and need:
  - Use vector data for detailed parcel-level analysis (0.5 ha units and rich attribute metadata)
  - Use 25 m raster for pixel-level Broad Habitat classification
  - Use 1 km rasters for larger-scale analyses or when computational resources are limited
- Leverage accompanying metadata and tables to understand class definitions and data provenance
- Ensure alignment of land cover classifications with other datasets by consulting the dataset documentation
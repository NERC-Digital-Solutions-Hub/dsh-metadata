# Land Cover Map 2007 (LCM2007) is available in different formats, to suit the requirements of various users.

## Overview
- LCM2007 is provided in two main formats: vector data and raster data, designed to suit different GIS needs.
- Coverage: United Kingdom (UK).

## Vector data (most detailed)
- Product: polygons representing land parcels with land cover attributes and metadata about derivation.
- Minimum mapped unit: 0.5 hectares.
- Supply format: ESRI Shapefile.

## Raster data
- Five raster products available.
- 25 x 25 m raster: provides the most likely Broad Habitat for each pixel.
- Four freely available 1 x 1 km rasters: summarize the 25 m raster.
- Supply format: GeoTIFF.

## Documentation and data attributes
- Detailed metadata and class descriptions are in the Land Cover Map 2007 Dataset Documentation.
- Key tables in the documentation:
  - Table 1: Attributes of the LCM2007 vector dataset
  - Table 2: Habitats, LCM2007 classes, and Broad Habitat sub-classes
  - Table 3: Metadata information for the raster datasets

## GIS workflow considerations
- Choose data resolution based on analysis scale and performance (vector 0.5 ha units vs. rasters 25 m or 1 km).
- Ensure compatible coordinate reference systems when overlaying vector and raster layers.
- Data quality and transformation needs may include cleaning, harmonizing classes, and integrating multiple datasets.
- Use vector data for precise, parcel-level mapping; use raster data for broad habitat mapping and large-area assessments.

## Practical guidance for users
- Refer to the Dataset Documentation for class definitions and metadata details.
- Use 25 m rasters for detailed habitat classification; use 1 km rasters for general, large-scale summaries.
- Be mindful of potential file size and resolution considerations when handling vector shapefiles and multiple rasters.
# Land Cover Map 2007 (LCM2007)

- LCM2007 provides land cover information in both vector and raster formats to suit different user needs, with UK coverage.
- Purpose is to support environmental monitoring by delivering data that can be used to assess environmental health and policy performance over time.

## Data formats and structure

- Vector data
  - Most detailed product: polygons represent land parcels with land cover attributes and metadata on derivation.
  - Minimum mapable unit: 0.5 hectares.
  - Supply format: ESRI Shapefile.
- Raster data
  - Five raster products in total.
  - 25 x 25 m raster: assigns the most likely Broad Habitat for each pixel.
  - Four freely available 1 x 1 km rasters: summarize the 25 x 25 m raster data.
  - Supply format: GeoTiff.
  - Scales: 25 m and 1 km pixel sizes.
- Coverage: United Kingdom (UK).

## Documentation and metadata

- Detailed metadata and descriptions are provided in the Land Cover Map 2007 Dataset Documentation.
  - Table 1: Attributes of the LCM2007 vector dataset.
  - Table 2: Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Table 3: Metadata information for the raster datasets.

## Relevance to monitoring and data sharing

- Enables standardized, comparable land cover data for environmental monitoring and policy assessment.
- Supports data quality assurance, cleaning, and transformation processes consistent with monitoring workflows.
- Datasets should be stored and uploaded to appropriate data portals, with underlying data accessible to others to maximize reuse and value.

## Practical considerations for analysts

- The vector format provides detailed parcel-level land cover with derivation metadata; suitable for precise analysis.
- The raster formats offer scalable summaries (25 m detail with broader 1 km aggregates) for broader, high-level monitoring.
- To increase value, consider integrating LCM2007 with other environmental datasets and ensuring accessibility of underlying data for downstream users.
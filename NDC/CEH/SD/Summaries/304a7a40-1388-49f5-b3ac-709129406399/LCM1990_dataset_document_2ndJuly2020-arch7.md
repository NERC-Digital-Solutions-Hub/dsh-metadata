# Dataset documentation

- LCM1990 overview: Land Cover Map 1990 (LCM1990) is a parcel-based land cover map for the UK, classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats. It is built from Landsat-5 two-date composites (30 m) and uses a spatial framework aligned with LCM2007/2015 to enable cross-product compatibility and long-term change assessment.

## Key data products and structure

- Core data: Vector dataset (polygons with rich attributes) that can be rasterised to a 25 m raster; both GB and Northern Ireland versions exist.
- Raster products: 
  - 25 m raster (derived from the vector): 3-band, including dominant class, per-polygon mean confidence, and percentage area of the modal class.
  - 1 km rasters: dominant cover (1-band) for target and aggregate classes; percentage cover (21-band target, 10-band aggregate) for 1 km pixels.
- Outputs support diverse GIS analyses and mapping needs, from detailed polygon attributes to broader 1 km landscape summaries.

## Classes and labeling

- 21 classes mapped from Broad Habitats definitions; some classes subdivided for spectral clarity, for example:
  - Built-up Areas and Gardens into Urban and Suburban
  - Dwarf Shrub Heath into Heather and Heather grassland
  - Littoral Sediment into Littoral sediment and Saltmarsh
- Each parcel is assigned a unique geometry id (gid) to enable unambiguous communication and data linking.

## Data details and metadata

- Rich metadata per polygon:
  - Dominant class (mode) and full class composition per polygon (_hist)
  - Uncertainty measures (_conf, _stdev) and pixel counts (_n)
  - Source composite image (cmp) and processing details
- Per-polygon uncertainty: Random Forest classifier provides per-pixel probability, aggregated per polygon.
- Minimum mapping unit: parcels > 0.5 ha are mapped; parcels < 0.5 ha and linear features < 20 m are dissolved into surrounding areas.

## Data formats, projections, and access

- Formats:
  - Vector polygons with attached attributes
  - 25 m raster (GB NI), 8-bit unsigned GeoTIFFs
  - 1 km raster products (GB NI) with percentage covers
- Projections:
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)
- Access:
  - 25 m and 1 km rasters available via CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector product available on request under licence (fees may apply)
  - Official contact: spatialdata@ceh.ac.uk

## Citing and DOIs

- Each LCM1990 product has a DOI for citation, supporting reproducibility and tracking usage.
- Examples include DOIs for GB vector, GB 25 m raster, and several 1 km products; some DOIs are listed as pending.

## Data quality and validation

- QA checks ensure:
  - Correct projections and spatial completeness
  - Modal class present in all vector polygons
  - Consistency between documentation and data headings
  - Raster value ranges (0–100) and correct pixel sizes
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.

## Methodology and context

- Methodology aligned with LCM2015/LCM2007: object-based classification producing polygonal parcels with per-polygon statistics, enabling compatibility across LCM products and enabling 25-year land cover change analyses.
- Grassland and other Broad Habitats include discussion of spectral and ancillary data influences; limitations and caveats documented in appendices.

## Data provenance, usage notes, and limitations

- LCM1990 maps land cover (not always directly inferring land use); some land-use inferences may be ambiguous (e.g., grass used for recreation vs. grazing).
- Some coastal and mosaic habitats may be underestimated or misclassified due to patch size, spectral similarity, or data limitations.
- The documentation includes detailed appendices describing class interpretations, biodiversity broad habitats (Appendix 2), colour mappings (Appendix 3), and composite image usage (Appendix 4).

## Access, licensing, and support

- CEH platform provides data access; vector product access is via request with potential licensing conditions.
- Contact CEH for licensing details, access arrangements, and additional information.
- Acknowledgement and references provided for biodiversity habitat definitions and prior LCM projects.

## Additional context and resources

- Example figures illustrate differences between vector, 25 m raster, and 1 km products and the use of 1 km aggregates for UK-wide modelling.
- Projections and metadata are designed to support integration with other spatial datasets (e.g., meteorological data, species distributions) for GIS analyses.
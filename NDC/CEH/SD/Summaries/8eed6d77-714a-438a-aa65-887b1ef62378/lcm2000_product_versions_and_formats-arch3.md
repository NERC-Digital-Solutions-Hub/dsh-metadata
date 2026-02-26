# LCM2000

- LCM2000 is a parcel-based, all-UK land cover map, built from satellite imagery (principally Landsat) and extending the Land Cover Map of Great Britain (LCMGB) 1990 to cover Northern Ireland as well. It uses a hierarchical Broad Habitat classification (JNCC) and is produced in both vector and raster formats with multiple detail levels and resolutions. It is not directly comparable with the 1990 dataset due to different methods.

## Product scope and formats

- Vector data: polygons (land parcels) with attributes.
  - Level 2: standard detail with 26 Subclasses (most widely used).
  - Level 3: detail down to 72 Variant level (special arrangement with CEH for access and support).
  - Standard vector format is ESRI shapefile; GIS users may need Spatial Analyst.
- Raster data: derived from the vector base, available at:
  - 25 m: 26 Subclasses.
  - 1 km: Subclass level (26 Subclasses) with Dominant and Percentage values; and Aggregate class level (10 aggregates) with Dominant and Percentage values.
  - Standard raster format: GeoTIFF.
- Dataset is not suitable for estimating changes over the 10-year period between LCM1990 and LCM2000.

## Dataset coverage and nomenclature

- Coverage is on 100 km tiles; images are classified per parcel and then added to tiles.
- Hierarchical codes provide Subclass and Variant details.
- Subclass and Variant coding is designed to reflect Broad Habitat classes, with some areas where Variant-level detail depends on dominant land cover at imaging time.

## Vector attributes and processing history

- Each parcel includes:
  - SegID: unique parcel label (recommended to retain).
  - BHSub: dominant land cover at Subclass level.
  - BHSubVar: dominant land cover at Variant level (Level 3).
  - PerPixList: per-pixel list of top spectral subclasses (Level 3 only).
  - OpHistory: processing history for the segment (image dates, KBC rules, etc.).
  - TotPixels and CorePixels: pixel counts for the parcel and core area used for classification.
- OpHistory (processing history descriptor) contains six fields detailing input data, processing stages, KBC rules, and other notes (including scene, sensor, acquisition dates, cloud-hole patches, probability aggregation, and KBC rule counts).

## Colour and habitat descriptions

- Colour recipes are provided for display of the 26 Subclasses.
- Broad Habitat descriptions map each subclass to broader habitat categories (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, etc.), with distinctions such as wetland, aquatic, and urban categories.

## Edge overlaps, artefacts, and artefact management (Appendix 1)

- Construction from multiple overlapping images and cloud-hole patching created edge overlaps within 100 km tiles.
- Overlaps were removed through erosion/merging to a single parcel layer; edge parcels may appear in adjacent tiles.
- Artefacts can include:
  - Different imagery driving edge classifications.
  - Boundaries that differ across tile edges, causing attribute inconsistencies post-merge.
  - Small parcels and slivers arising from processing.
- Visual tidying options:
  - Dissolve boundaries between adjacent parcels of the same class (without dissolving across the entire dataset to preserve parcel-level metadata).
  - Clipping or merging tiles can cause loss of parcel-level attributes; use with care.
  - For Level 3 data, ensure Level 3 class information (bhsubvar) is preserved during dissolves.
- Strategies for edge management and sliver reduction:
  - Use select features to limit dissolving to edge areas.
  - Be mindful of attribute data validity after merges; first-input tile precedence can affect edge attributes.

## Customisation, philosophy, and data governance

- LCM2000 is intended as a data storage and analysis framework, not just a map.
- Users are encouraged to:
  - Extend and customize the database as needed.
  - Retain SegID for traceability and communication with data management.
  - Document and maintain provenance of any attribute changes; preserve source attributes or store changes in new fields.
  - Maintain an explicit lineage of data transformations and processing steps.
- Production philosophy: retain as much information as possible; preserve parcel-level metadata and processing history to support audits and future analyses.

## Accuracy, caveats, and usage notes

- LCM2000 contains inevitable inaccuracies due to data model, scale, resolution, interpretation, and class definitions.
- The product provides rich metadata to aid interpretation and governance; users should distinguish data-model and method differences from true inaccuracy.
- The dataset includes guidance on how to deal with artefacts and how to compare across versions, while recognising limitations in change detection and class distinctions.

## Further information and references

- Contact: Land Cover Map project at CEH Wallingford (spatialdata@ceh.ac.uk; +44 1491 838800).
- Methodology references:
  - Fuller et al. (2002) The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images.
  - Smith et al. (2001) Land Cover Map 2000: a parcel-based map from satellite images.
  - Jackson (2000) JNCC Report No. 307: Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- Additional documentation and the Land Cover Map home page: www.ceh.ac.uk/data/lcm.
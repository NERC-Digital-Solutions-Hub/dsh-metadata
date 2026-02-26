# Dataset documentation

- LCM1990 is a parcel-based UK land cover map produced from Landsat-5 data (30 m) and restructured to align with the LCM2007/LCM2015 framework, enabling a 25-year land cover change product.
- Purpose and scope
  - Provides a range of data products to support diverse LCM user needs.
  - Clarifies that LCM1990 maps land cover (not strictly land use) and uses Broad Habitat definitions as its classification basis.
  - Aims for compatibility with other LCM products to facilitate integration and change analysis.

## Data products and structure

- Vector data set
  - Polygons with rich attributes per parcel (e.g., dominant class, source image, uncertainty, pixel counts per class, and modal class percentage).
  - Approximately 6.7 million GB polygons and 0.9 million NI polygons.
  - Key attributes include gid (unique parcel ID), hist (class history per polygon), mode (LCM1990 target class), purity, conf, stdev, n, cmp (composite image).
- Raster data sets
  - 25 m raster: 3-band GeoTIFF per region (Great Britain and Northern Ireland)
    - Band 1: dominant class per polygon ( LC1990 target class)
    - Band 2: mean per-polygon classifier confidence
    - Band 3: percentage of polygon area covered by the modal class
  - 1 km rasters: aggregate products derived from 25 m data
    - Dominant cover at 1 km (target and aggregate classes)
    - Percentage cover at 1 km for target (21 bands) and aggregate (10 bands) classes
  - Two regional projections: GB in British National Grid; NI in Irish Grid
- Data formats and accessibility
  - Core product is the vector; 25 m raster derived from vector; 1 km products derived from 25 m raster.
  - 0.5 ha minimum mappable area; smaller parcels dissolved into surrounding landscape during processing.

## Class structure and mapping

- 21 LCM1990 classes (based on UK Broad Habitats definitions)
  - Examples: Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grasslands, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Open Water and Canals, Rivers and Streams, Montane, Inland Rock, Built-Up Areas and Gardens, Supralittoral/Littoral habitats, Urban/Suburban.
- Some classes are subdivided for spectral/heritage reasons (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Appendix notes provide expert guidance on spectrum interpretation and class-specific caveats (e.g., confusion between certain grassland types, coastal habitat distinctions).

## Metadata and uncertainty

- Each polygon in the vector includes a detailed metadata suite:
  - Dominant class, per-class pixel counts, modal class proportion, and classification confidence.
- Uncertainty is quantified as mean per-polygon vote-based confidence (from Random Forest), available in both vector (per-polygon) and 25 m raster bands.

## Spatial framework and comparability

- Spatial framework aligned with LCM2015 methods to maximise compatibility and enable long-term change analyses (up to 25 years).
- Data are designed to be interoperable with other CEH Land Cover Maps and national datasets (e.g., Countryside Survey, National Forest Inventory).

## Citing and DOIs

- All LCM1990 products have individual DOIs to enable clear, repeatable citation.
- Examples of DOIs (GB):
  - GB vector (vector, GB)
  - GB 25 m raster (GB 25m raster)
  - GB 1 km percentage cover (GB 1 km percentage target class)
  - GB 1 km dominant cover (GB 1 km dominant target class)
  - GB 1 km percentage cover (aggregate classes)
  - GB 1 km dominant cover (aggregate classes)
- Examples of DOIs (NI):
  - NI vector (vector, NI)
  - NI 25 m raster (NI 25m raster)
  - NI 1 km percentage cover (target & aggregate)
  - NI 1 km dominant cover (target & aggregate)
- Citation format example: Rowland et al. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. https://doi.org/...
- Full DOI tables are provided for both GB and NI products.

## Data access and licensing

- Access via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector product available on request; licences may apply and fees could be charged for some users/applications.
- Contact spatialdata@ceh.ac.uk for access details; data availability information at https://www.ceh.ac.uk/services/land-cover-map-1990.

## Quality assurance and validation

- QA process includes:
  - Projections and spatial completeness checks
  - Consistency of polygon modal class assignments
  - Metadata accuracy in vector products
  - Value range checks (0–100) for raster percentage products
  - Pixel size verification for all rasters
- Validation against independent datasets (e.g., Countryside Survey, National Forest Inventory) is performed, with results to be published separately.

## Practical notes for use

- The LCM1990 dataset is designed for integration with other CEH land cover products and for long-term change analyses.
- The vector product’s gid allows unambiguous communication and potential linking with other datasets.
- When using the data in publications, cite the corresponding DOIs and include author/date in the text and full DOI in references.

## References and further information

- Jackson, D.L. (2000). Guidance on the interpretation of the Biodiversity Broad Habitat Classification.
- Morton, D. et al. (2011). Final Report for LCM2007; Countryside Survey Technical Report.
- Rowland, C.S. et al. (2020a, 2020b). Land Cover Change 1990-2015 (25m raster, GB/NI). NERC Environmental Information Data Centre.
- Appendix materials (LCM1990 class definitions, colour mappings, and composite imagery notes) provide detailed guidance on class interpretation and mapping nuances.

## Access and contact

- Data access: CEH Environmental Information Platform (https://eip.ceh.ac.uk/)
- Licensing and full vector product requests: spatialdata@ceh.ac.uk
- Additional information: https://www.ceh.ac.uk/services/land-cover-map-1990
- Acknowledgement: NERC award NE/R016429/1 as part of UK-SCAPE National Capability.
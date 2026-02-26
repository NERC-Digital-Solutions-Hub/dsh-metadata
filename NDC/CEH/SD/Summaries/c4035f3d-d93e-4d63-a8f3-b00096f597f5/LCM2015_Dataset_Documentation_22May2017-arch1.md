# Land Cover Map 2015 (LCM2015) dataset documentation

- LCM2015 is a parcel-based UK land cover map classifying satellite data into 21 Broad Habitat classes, aligned with UK Biodiversity Action Plan definitions.
- Data sources: Landsat-8 (30 m) with AWIFS (60 m) as needed; two-date composites; spatial framework based on generalised cartography refined with border/ boundary data.
- Output aims: support a range of users with per-polygon (vector) and raster products; designed to facilitate change mapping and integration with other geospatial data.

## What the dataset covers

- UK-wide land cover mapping (GB and Northern Ireland) reflecting real-world boundaries.
- 21 target classes based on Broad Habitats; some classes divided for detail (e.g., Urban vs Suburban, Heather vs Heather grassland).
- LCM2015 updates the 2007 map (LCM2007) with methodological and data improvements to better support change analysis and continuity.

## Data products and formats

- Vector data set
  - Core product: polygons with 9 attributes (e.g., dominant class, uncertainty, pixel counts, gid).
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
- Raster data sets
  - 25 m raster: two-band image (band 1 = dominant class per polygon; band 2 = mean per-polygon probability from the classifier).
  - 1 km raster: derives dominant class and percentage cover for each class (both 21 target classes and 10 aggregate classes).
  - Separate data sets for Great Britain and Northern Ireland due to different projections.
- Data access formats
  - 1 km rasters available via CEH Environmental Information Platform.
  - Full vector and 25 m raster products available on request; licensing may apply.

## Key differences from LCM2007 (output data)

- Montane class removed; areas reclassified to Inland Rock or other upland habitats based on spectral data.
- Rough grassland class removed; grassland types now aligned with JNCC Broad Habitats without relying on soil data.
- 25 m raster now two-band (classification band + mean probability).
- Probability data simplified: vector stores mean polygon probability; 25 m raster band 2 stores the same; 1 km products do not include probability data.
- Spectral sub-classes removed; Random Forest classifier eliminates need for subclass training.
- Spatial framework: no segmentation-based polygons; per-pixel classification improves consistency for change mapping.
- Mixed woodland handling updated: training uses pure stands per-pixel classification; polygon labels reflect modal class, with pix_dist available for detailed exploration.

## Key differences in methodology

- Classification algorithm: Random Forest (LCM2015) vs Maximum Likelihood (LCM2007).
- Training data: stable initial set (areas classified the same in 2000 and 2007) augmented for coastal areas and difficult classes.
- Ancillary data: used as inputs rather than post-classification refinements; knowledge-based enhancements integrated into the classification.
- Output focus: LCM2015 emphasizes a per-pixel, repeatable approach suitable for change mapping.

## Data products in detail

- LCM2015 classes
  - 21 target classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, wetlands, urban/suburban, etc.).
  - Some classes subdivided or aggregated (e.g., Urban vs Suburban; Littoral/Littoral Sediment subdivisions).
- Metadata and uncertainty
  - Rich metadata at the polygon level; each polygon includes dominant class, per-class pixel counts, and mean probability.
  - Uncertainty is represented as probability estimates (0–255 scale) for polygons and per-polygon mean probability in vector; band 2 of 25 m raster also stores this information.
- Data scale and mapping
  - Minimum mappable area: >0.5 ha; polygons smaller than this are dissolved into surrounding areas.
  - 1 km products provide aggregate percentage covers and dominant classes for national-scale modelling.

## Data access, use, and citation

- UK data projections
  - GB vector and raster data in British National Grid; NI data in Irish National Grid.
- Access and licensing
  - 1 km raster data accessible via CEH EIP.
  - Full vector and 25 m raster available on request; license fees may apply.
- Citation and DOIs
  - Each LCM2015 product has a DOI for proper citation (separate DOIs for GB vector, GB 25 m raster, 1 km target classes, 1 km aggregate classes, NI vector, NI rasters, etc.).
  - Citing data with DOIs is encouraged to ensure reproducibility and track usage.

## Map structure and projections

- Core product and derived products built from a common vector dataset; rasters derived from the vector data.
- GB and NI products are provided separately to reflect different coordinate systems and extents.
- Appendix-level consistency with Broad Habitat definitions (JNCC) explains class interpretations and mappings.

## Caveats and intended use

- LCM2015 is not advised for current change mapping in its present form; differences across LCM series and classification changes can confound straightforward change detection.
- Differences from prior versions (e.g., removal of segmentation in the spatial framework, class removals/additions) can impact comparability over time.
- Users should consult product metadata and appendices for class definitions, color mappings, and interpretation guidance.

## Appendices and definitions

- Appendix 1 & 2 provide concise summaries of Broad Habitat definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Grasslands, Wetlands, Urban/Built-up habitats).
- Appendix 3: Standard colour mapping for LCM2015 classes (for visualisation consistency).
- Appendix 4: Composite images used in LCM2015 (reference for image sources and processing).

## Contact and further information

- Primary contact: CEH Spatial Data team (spatialdata@ceh.ac.uk); dataset information and access details available via CEH and CEH EIP portals.
- LCM2015 data paper and accompanying documentation provide deeper methodological context and usage notes.
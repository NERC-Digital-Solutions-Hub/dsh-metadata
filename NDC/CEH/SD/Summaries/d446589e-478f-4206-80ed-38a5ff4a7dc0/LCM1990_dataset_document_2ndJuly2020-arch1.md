# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from two-date Landsat-5 composites (30 m) and aligned with the LCM2015 spatial framework to enable long-term change analysis.

## Key data products

- Vector data set: polygons with rich attributes per parcel (dominant class, uncertainty, class breakdown, and metadata).
- 25 m raster: three bands per polygon (dominant class, per-polygon confidence, and percentage cover for the dominant class).
- 1 km raster products: aggregate and target-class percentage covers and dominant cover (GB and Northern Ireland separately).

## Spatial framework and compatibility

- Uses an updated LCM2007/LCM2015-based spatial framework for consistency and future change mapping (e.g., 1990–2015).
- Parcellation boundaries reflect real-world boundaries to improve interpretation and interoperability with other datasets.
- Minimum mappable unit: parcels >0.5 ha; smaller parcels and line features dissolved into surrounding landscape.

## Classes and labeling

- 21 LCM1990 target classes mapped from 21 Broad Habitat categories (based on JNCC Jackson 2000).
- Subdivisions:
  - Built-up Areas and Gardens: Urban and Suburban.
  - Dwarf Shrub Heath: Heather and Heather grassland.
  - Littoral Sediment Broad Habitat split into Littoral sediment and Saltmarsh (Saltmarsh is a Priority Habitat).

## Attributes and uncertainty

- Vector attributes include: gid (unique parcel ID), hist (class composition per polygon), mode (dominant class code), purity, conf (mean vote confidence 0–100), stdev, n (pixel count), cmp (composite image).
- Per-pixel probability from a Random Forest classifier included as mean polygon-level confidence (and in the 25 m raster).
- Raster products provide 25 m classification, confidence, and dominance metrics; 1 km products provide dominant and percentage cover values.

## Data formats and projections

- Core vector product plus derived raster products distributed as uncompressed GeoTIFFs.
- Projections:
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: TM75 Irish Grid (EPSG 29903).
- GB 25 m raster: grid size 25 m; GB 1 km raster: 1000 m; NI 25 m raster: 25 m; NI 1 km raster: 1000 m.

## Data access and licensing

- Access via CEH Environmental Information Platform (eip.ceh.ac.uk).
- 25 m and 1 km rasters available; full vector product available on request (licences may apply).
- Licence terms and potential fees depend on user type and application.

## Citing and DOIs

- Each LCM1990 product has its own DOI to support repeatable methods and usage tracking.
- Examples:
  - GB vector DOI; GB 25 m raster DOI; GB 1 km dominant/percentage DOIs (some pending).
  - NI vector DOI; NI 25 m raster DOI; NI 1 km products (some pending).
- Citations should include author(s), date, and full DOI (e.g., Rowland et al., 2020; DOI provided in Table 5 and Table 6).

## Quality assurance and validation

- QA checks cover projections, spatial completeness, modal class consistency, accurate metadata alignment, value ranges (0–100 for raster), and pixel size accuracy.
- Validation against independent datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results published separately.
- Field boundary changes are infrequent; mapping relies on established parcel framework and trained staff.

## Access channels and contact

- Data access: CEH Environmental Information Platform (eip.ceh.ac.uk).
- Vector product: available on request; contact spatialdata@ceh.ac.uk for details; note possible licence fees.
- Additional information and data citations: see LCM1990 data portal and associated journal publications.

## Appendices and further information

- Appendix 1: Class interpretations and mapping notes for LCM1990 classes (e.g., woodland types, grassland classifications, aquatic and coastal habitats).
- Appendix 2: Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000) used to derive LCM1990 classes.
- Appendix 3: Standard LCM color mapping by class.
- Appendix 4: Composite images used in LCM1990 production methodology.

## Summary takeaway for analysts

- LCM1990 provides a rich, multi-resolution, lineage-traceable data product set (vector and raster) with a robust metadata and uncertainty framework, designed for cross-compatibility with later LCM editions and suitable for modelling and pattern detection at multiple scales.
- Addressing common data-availability challenges, it offers scalable UK-wide coverage, explicit scale limits, and accessible DOIs for reproducibility, while acknowledging ongoing data access licensing considerations.
# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from Landsat-5 two-date composites (30 m resolution) and aligns with updated LCM2007 framework for compatibility and future change tracking (25-year span).
- The dataset supports multiple products (vector and raster) to suit diverse user needs, with rich metadata and uncertainty information.

## Data products and structure
- Vector data set
  - Polygons with attached attributes; approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Key attributes: gid (unique parcel identifier), hist (class composition per polygon), mode (dominant LCM1990 class 1–21), purity, conf (mean per-polygon classifier confidence 0–100), stdev, n (pixel count), cmp (composite image used).
- Raster data sets
  - 25 m raster: three bands per polygon (dominant class, mean confidence, percentage cover of modal class).
  - 1 km raster: dominant cover (target and aggregate classes) and percentage cover (target: 21 bands; aggregate: 10 bands). Values are integers; sums may deviate from 100 due to rounding and coastal effects.
  - GB and Northern Ireland provided separately with appropriate projections.
- Class structure and mapping
  - 21 target classes anchored to Broad Habitat definitions; some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - Minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha or lines under 20 m dissolved into surrounding landscape.
- Coordinate systems and projections
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: TM75 Irish Grid (EPSG 29903).
- Data availability and access
  - 25 m and 1 km rasters accessible via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH (licence may apply).

## Metadata, uncertainty, and quality
- Rich polygon metadata: dominant class, per-polygon pixel breakdown, and mean classification probability per polygon.
- Uncertainty captured via Random Forest per-pixel probabilities and per-polygon summaries (conf, stdev).
- Comprehensive QA checks (projections, spatial completeness, modal class presence, value ranges, pixel sizes).
- Validation against external datasets (Countryside Survey, National Forest Inventory) with results to be published separately.
- Vector framework based on 2007 OS MasterMap-derived structure, allowing compatibility with other LCM products and change-detection work.

## Citations, DOIs, and provenance
- Each LCM1990 product has a Digital Object Identifier (DOI) for precise citation and reproducibility.
- Examples include GB vector, GB 25 m raster, and GB/N Ireland 1 km products; NI products also have DOIs.
- Guidance provided on how to cite (author/date plus DOI) in publications.

## Access, licensing, and usage considerations
- Access through the CEH platform; full vector product on request; licence fees may apply for some users or applications.
- Intended for broad use across research, policy, and planning; supports integration with meteorological or species-distribution data for UK-wide analyses.
- Important considerations for data leaders: plan for vector vs raster workflows (vector offers richer metadata but larger files; 25 m raster is more storage- and processing-efficient), and account for classification uncertainty in analyses.

## Practical notes for data leadership and governance
- The dataset provides a robust, standards-based data asset with extensive metadata, enabling reproducible analyses and clear data provenance.
- DOIs and detailed class definitions facilitate transparent data citation and cross-project interoperability.
- The mixture of high-detail vector data and scalable 25 m and 1 km raster products supports both fine-grained analyses and UK-scale modelling, aiding strategic data planning and sector collaboration.
# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map created from two-date Landsat-5 composites (30 m resolution) to classify into 21 land cover classes.
- Based on UK Biodiversity Action Plan Broad Habitat definitions; replaces the earlier LCMGB; designed to be compatible with LCM2007 and LCM2015 to enable a 25-year land cover change product.
- Data are structured to support monitoring, data verification, quality assurance, and integration with other geospatial datasets.

## Data products and structure
- Vector data set (core product): polygons with rich metadata attached; GB contains ~6.7 million polygons, NI ~0.9 million; gid (geometry id) retained for unambiguous communication.
- 25 m raster: derived from the vector, provided as a 3-band GeoTIFF (band 1 = dominant class per polygon; band 2 = mean per-pixel classification confidence; band 3 = percentage of polygon area covered by the modal class).
- 1 km raster products: created by summarising 25 m rasters.
  - Dominant cover at 1 km for LCM1990 target classes (1-band).
  - Dominant cover at 1 km for LCM1990 aggregate classes (1-band).
  - Percentage cover at 1 km for LCM1990 target classes (21 bands).
  - Percentage cover at 1 km for LCM1990 aggregate classes (10 bands).
- Aggregate classes: a defined set of 1 km raster products (to reduce thematic detail where needed).

## Classification and spatial framework
- 21 LCM1990 classes aligned with Broad Habitats; several classes are subdivided for improved detail (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Spatial framework and methodology mirror LCM2015 to maximise compatibility and enable long-term change analyses.
- LCM1990 maps land cover (not necessarily land use); some land-use inferences may be ambiguous from spectral data alone.
- Minimum mappable area: polygons >0.5 ha; features smaller than this are dissolved into surrounding landscape.

## Metadata, uncertainty, and quality assurance
- Vector polygons include:
  - gid: unique parcel identifier.
  - hist: list of classes present in the polygon with pixel counts.
  - _mode: recommended display class (1–21).
  - _purity: percentage of polygon area covered by the modal class.
  - _conf: mean confidence from the Random Forest classifier (0–100).
  - _stdev: standard deviation of the uncertainty.
  - _n: number of pixels in polygon.
  - cmp: composite image reference used for classification.
- Uncertainty information: per-pixel probability from Random Forest is propagated to polygon and 25 m raster products.
- QA checks: projections, spatial completeness, modal class presence, value ranges (0–100 for rasters), pixel sizes; full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results published separately.
- The data are distributed with rich metadata to support traceability and reproducibility.

## Data formats and projections
- GB vector and raster data are in the British National Grid; NI data are in the Irish Grid (TM75) projections.
- Raster data specifics:
  - 25 m raster: 3-band GeoTIFF (band 1 = dominant class; band 2 = per-polygon confidence; band 3 = modal coverage percentage).
  - 1 km rasters: per-class percentage and dominant class products as described above.
- Data access formats:
  - 25 m and 1 km rasters via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector products available on request (licence may apply).

## Access, citation, and reuse
- Each LCM1990 product has its own DOI for formal citation:
  - GB vector, GB 25 m raster, GB 1 km percentage and dominant target/aggregate classes, NI vector, NI 25 m raster, NI 1 km percentage and dominant/aggregate classes (see Tables 5 and 6 in the document for exact DOIs).
- When using DOIs, cite with authorship and year in text and provide full DOI references in the references section.
- Example citation pattern: (Rowland et al., 2020) with the corresponding DOI entry for the product used.
- Access info and contact: spatialdata@ceh.ac.uk; additional information at https://eip.ceh.ac.uk/lcm/lcmdata and licensing details at https://www.ceh.ac.uk/services/land-cover-map-1990.

## Map projection and data access details
- Projections:
  - Great Britain: British National Grid (EPSG 27700) for GB vector and GB 25 m / 1 km rasters.
  - Northern Ireland: Irish Grid (TM75) for NI vector and NI 25 m / 1 km rasters (EPSG 29903).
- Access:
  - CEH Environmental Information Platform provides the 25 m and 1 km raster data.
  - The full vector product is available under licence on request; fees may apply for some users.

## Usage notes and guidance
- The 25 m raster’s band 2 confidence and band 3 percentage values enable assessment of classification certainty and boundary reliability within polygons.
- The presence of gid and detailed per-polygon histograms enables users to explore mixed or ambiguous areas (e.g., mixed woodland classifications).
- Some coastlines and mosaic landscapes may exhibit class blending; users should consult Appendix materials (class definitions and mappings) for interpretation nuance.
- The dataset provides a long-term framework for change detection and integration with other UK landscape datasets.

## Acknowledgements and references
- The work was supported by the Natural Environment Research Council under the UK-SCAPE programme.
- Key references include Jackson (2000) on Broad Habitat definitions, Morton et al. (2011) on LCM2007, and Rowland et al. (2020) for Land Cover Change 1990–2015.
- Further information and dataset details are available at the CEH data portal and associated DOIs.

## Contact and further information
- Data access: CEH Environmental Information Platform (https://eip.ceh.ac.uk/) and dataset pages (https://www.ceh.ac.uk/services/land-cover-map-1990).
- User queries: spatialdata@ceh.ac.uk.
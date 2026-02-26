# Dataset documentation

- This document describes Land Cover Map 1990 (LCM1990) data products, their structure, formats, metadata, quality assurance, and access details.

## Overview of LCM1990

- UK parcel-based land cover map created from satellite data (Landsat-5, 30 m). 
- Classifies into 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Built to be compatible with LCM2007 and LCM2015 frameworks to enable 25-year land cover change products.
- Distinguishes land cover (not necessarily land use); minimum mapping unit is >0.5 ha; parcels smaller than 0.5 ha or very short linear features are dissolved.
- Spatial framework relies on OS MasterMap for GB and NI equivalents, refined with rural boundary data.

## Data products and structure

- Vector data set: polygons with rich attributes; 6.7 million polygons in GB and 0.9 million in NI.
- Raster data sets derived from vector:
  - 25 m raster: 3-band (dominant class, per-polygon mean confidence, percent coverage by modal class).
  - 1 km raster: aggregate products and percentage coverage for both 21 target classes and 10 aggregate classes.
- Classes:
  - 21 LCM1990 target classes; some are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories split into coastal subtypes).
- Aggregates: 1 km products provide both dominant cover (1-band) and percentage cover (21 or 10 bands) for UK-wide modelling with other data (e.g., climate, species distribution).

## Data formats and content details

- Vector attributes (key ones): gid (unique parcel ID), _hist (list of classes within polygon with pixel counts), _mode (dominant class code 1–21), _purity (percentage of polygon covered by modal class), _conf (mean per-polygon classifier confidence 0–100), _stdev (uncertainty), _n (pixels in polygon), cmp (composite image source).
- Raster data:
  - 25 m: 3-band GeoTIFFs (band1 = dominant class; band2 = mean confidence; band3 = % coverage). Distributed for GB and NI with respective projections.
  - 1 km: rasters summarise 25 m data; GB and NI provided separately with coordinate systems and metadata in Tables 4 and related documentation.
- Spatial resolution and extents:
  - GB and NI provided separately to account for different projections (Great Britain: British National Grid; Northern Ireland: Irish Grid).
  - 25 m and 1 km products; coastal areas may have rounding effects in aggregation.
- Minimum mapping detail:
  - 0.5 ha minimum; features smaller than this are dissolved into surrounding landscape.

## Class mapping and metadata

- 21 LCM1990 target classes mapped to Broad Habitats (with appendix detailing definitions and cautionary notes about spectral limitations and field verification).
- Metadata-rich polygons include dominant class, per-polygon class breakdown, and classification probability.
- Uncertainty: per-pixel probability from Random Forest classifier, carried in both vector (per-polygon mean) and 25 m raster.

## Quality Assurance and validation

- QA checks ensure correct projections, spatial completeness, modal class presence in polygons, proper value ranges (0–100 for raster percentages), and correct pixel sizes.
- Full validation against other datasets and validation points has been conducted; results to be published separately.
- LCM1990 uses a stable parcel framework based on 2007 OS MasterMap data; field boundary changes are infrequent, limiting impact on accuracy.

## Data access and citation

- Access:
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request; licensing may apply; contact spatialdata@ceh.ac.uk.
- DOIs:
  - Each LCM1990 product (GB and NI, vector and raster, 1 km and 25 m, and aggregate/percentage covers) has a DOI for citation.
  - Example citation formats provided; DOIs enable reproducible methods and usage tracking.
- Provisional publications and further information:
  - CEH pages and contact details provided for data access and updates.
  - Journal papers and datasets related to LCM1990 and its role in the broader LCM family (1990–2015, GB and NI) are cited in the documentation.

## Projections, access, and provenance

- Data products are designed to be compatible with other LCMs (2007, 2015) to facilitate cross-version analyses and long-term change studies.
- Projections:
  - GB vector/raster: British National Grid (EPSG 27700).
  - NI vector/raster: Irish grid (TM75 Irish Grid, EPSG 29903).
- Provenance:
  - DOIs and detailed metadata accompany all major products; references include Jackson (2000), Morton et al. (2011), and Rowland et al. (2020).

## Appendices and supporting information

- Appendix 1–4 provide:
  - Detailed class interpretations and map-making caveats.
  - Broad Habitat definitions (JNCC/JNCC-backed classifications).
  - Color mapping recipes for visualisation.
  - Composite image metadata and usage notes for the classification process.

## Summary for analysts

- LCM1990 is a robust, archive-ready UK land cover product (21 classes) at 30 m resolution with vector (detailed polygons) and raster (25 m and 1 km) outputs.
- Rich metadata and per-polygon probability/uncertainty enable robust statistical analyses and modelling.
- Data are suitable for cross-temporal comparisons within the LCM family (1990–2015), with careful attention to class definitions, aggregation schemes, and spatial scale.
- Access is controlled with licensing for some outputs; DOIs enable precise citation and reproducibility.
- QA and validation frameworks are in place, with ongoing or forthcoming publications detailing accuracy assessments.
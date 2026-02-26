# Dataset documentation

## Overview
- Provides key information about Land Cover Map 1990 (LCM1990), a UK parcel-based land cover dataset produced from Landsat-5 two-date composites at 30m resolution.
- 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats (Jackson, 2000).
- Replaces LCMGB; aligns with LCM2015 framework to facilitate long-term change analyses (LCM1990, 2007, 2015 lineage).
- Data products include both vector (parcels) and raster formats; designed to be compatible with other geospatial datasets and to support multiple applications.
- Minimum mapped polygon size: >0.5 ha; smaller parcels and very small linear features are dissolved into surrounding landscape.

## Data products and formats
- Core products:
  - Vector data set: polygon features with rich attributes.
  - Raster data: 25m raster derived from the vector, plus 1km aggregated products.
- Raster products:
  - 25m raster: 3-band (band 1 = dominant class per polygon; band 2 = mean per-polygon classifier confidence; band 3 = percentage of polygon area covered by the dominant class).
  - 1km raster: dominant class (target and aggregate) and percentage cover for target (21 bands) and aggregate (10 bands).
- Spatial coverage:
  - Great Britain (GB) and Northern Ireland (NI) provided separately due to differing projections.

## Vector dataset details
- Structure: polygons with eight key attributes, including:
  - gid: unique geometry identifier for each parcel (recommended to retain).
  - _hist: list of classes present in the polygon with pixel counts.
  - _mode: recommended dominant LCM1990 class (1–21).
  - _purity, _conf, _stdev: uncertainty metrics from the classification process.
  - _n: number of pixels in the polygon.
  - cmp: composite image source indicator.
- Scale and scope: approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
- Metadata: rich per-polygon metadata, including dominant class and per-class pixel breakdowns.

## Uncertainty and quality information
- Per-pixel probability from the Random Forest classifier is included as mean per-polygon values (vector and 25m raster).
- QA checks cover projections, spatial completeness, modal class presence in polygons, data range validation (0–100 for rasters), and pixel size accuracy.
- Validation conducted against other datasets (e.g., Countryside Survey, National Forest Inventory); results reported in a separate publication.

## Class definitions and aggregation
- LCM1990 maps 21 classes, tied to Broad Habitat definitions; some classes are subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment and related coastal classes).
- Aggregates: 1km rasters include aggregated target and aggregate classes to support broader analyses and modelling.
- Note on land cover vs land use: Mapped classes reflect spectral land cover with caveats in inferring exact land use from imagery.

## Data access and citation
- Access:
  - 25m and 1km rasters available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence from CEH (licence fees may apply).
  - Contact: spatialdata@ceh.ac.uk; dataset information at https://www.ceh.ac.uk/services/land-cover-map-1990.
- DOIs and citation:
  - All LCM1990 products have individual DOIs; GB and NI products have separate DOIs listed in Tables 5 and 6.
  - Example citation format: (Rowland et al., 2020) with full DOI in references.
  - See provided tables for DOIs of GB vector, GB 25m raster, GB 1km percentage/dominant target/aggregate classes, NI equivalents.
- Projections:
  - GB vector/raster: British National Grid (EPSG 27700).
  - NI vector/raster: Irish Grid (TM75; EPSG 29903).

## Data structure: formats and metadata
- 25m raster: uncompressed GeoTIFF, 8-bit unsigned integer, with three bands as described.
- 1km raster: uncompressed GeoTIFF, 8-bit unsigned integer; includes dominant and percentage cover layers.
- Coordinate extents and pixel sizes specified in documentation (GB: 25m, 1km; NI: 25m, 1km).

## Practical considerations for use
- Minimum mapping unit and merging: parcels under 0.5 ha and very small features dissolved; users should consider this when analysing fine-scale patterns.
- Interpretation: 21 LCM1990 classes correspond to Broad Habitats; some spectral similarities across habitats can lead to misclassification in certain contexts.
- Colour mapping and class references: Appendix includes standard colour mapping recipes for visualization.

## Appendices at a glance
- Appendix 1: Commentary on how LCM1990 classes map to Broad Habitats (with caveats and field interpretation notes).
- Appendix 2: Summary of Biodiversity Action Plan (BAP) Broad Habitats definitions used for mapping.
- Appendix 3: Standard LCM colour mapping recipe (color codes for each class).
- Appendix 4: Composite image metadata (dates and sources for satellite composites used in classification).

## Additional information
- Data provenance and methodology repeatedly documented; production framework aligns with LCM2007/LCM2015 methodologies to support cross-era analyses.
- Further information and journal publication in preparation (data citations and methodological details).
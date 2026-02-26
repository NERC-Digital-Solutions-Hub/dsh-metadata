# The UKCEH Land Cover Map for 2020

## Overview
- LCM2020 is UK CEH’s land cover map, the eighth in the series, mapping 21 UKCEH Land Cover Classes derived from Biodiversity Broad Habitats (BAP).
- Production is automated using Bootstrap Training and Random Forest, combining Sentinel-2 Seasonal Composite Images with 10 Context Layers.
- Aims to support timely, comparable mapping and change detection; annual production helps distinguish real change from random errors.
- Validation indicates an overall accuracy of just over 79% (79.2%) at full thematic detail.

## Data Products and Formats
- Per region (Great Britain and Northern Ireland), four main data products are provided (eight datasets in total when split by region):
  - 10m Classified Pixels (GB and NI): classification results at 10m resolution; two-band output (land cover class and associated probability). The 10m pixels are not generalised to the Land Parcel Framework to preserve fine features; intended for specialist users who understand the implications.
  - Land Parcel Spatial Framework: generalized land parcels (~0.5 ha MMU) used to stabilise comparisons over time; parcels carry descriptive attributes.
  - 20m Classified Raster Product: per-parcel mean probability/confidence raster for 20m pixels.
  - 25m Rasterised Land Parcel Product: three-band raster carrying (band 1) dominant land cover class (_mode), (band 2) mean confidence (_conf), and (band 3) purity (_purity).
- Spatial references and extents:
  - Great Britain: EPSG 27700
  - Northern Ireland: EPSG 29903
- Datasets include both pixel-based products and parcel-based products, designed to support both detailed mapping and parcel-level analysis.

## Data Structure and Content
- Six main dataset groups by region (GB and NI) with corresponding extensions:
  - 10m Classified Pixels (GB/NI)
  - Land Parcel Product (GB/NI)
  - 20m Classified Raster Product (GB/NI)
  - 25m Rasterised Land Parcel Product (GB/NI)
- Classification outputs:
  - 10m pixel product: first band = most likely UKCEH Land Cover Class; second band = classification probability/confidence.
  - Parcel-level attributes in the Land Parcel dataset include _hist, _mode, _purity, _conf, _stdev, _agg, and n (number of pixels per parcel), among others.
- Parcel framework:
  - Land Parcels represent discrete real-world units (fields, parks, urban areas, etc.) with a minimum mappable unit of ~0.5 ha.
  - The Land Parcel Spatial Framework was updated post-LCM2015; gid identifiers may not align with LCM2015 for direct parcel-based comparisons.
  
## Seasonal Imagery and Context Information
- Seasonal Composite Images:
  - Derived from Google Earth Engine using Sentinel-2 reflectance; four seasons (winter, spring, summer, autumn) across nine Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 11, 12); data gaps (clouds) represented as nulls, with the classifier tolerant of partial data.
- Context Rasters (10m for GB; NI equivalents provided):
  - GB: height, aspect, slope; distance to nearest building, road, sea, freshwater; foreshore mask; tidal water mask; woodland mask.
  - NI: height, aspect, slope; urban mask; distance to coast, freshwater, road.
- Classification Scenes:
  - GB: 100x100 km tiles used to select and extract 36-band Seasonal Composite Images; combined with 10 context rasters to form 46-band GB Classification Scenes; 74 overlapping scenes classified independently; minor manual precedence decisions in overlaps.
  - NI: single 36-band Seasonal Composite Image combined with NI context rasters to produce a 43-band single Classification Scene per year.

## Methodology: Bootstrap Training and Random Forest
- Bootstrap Training:
  - Automatic training using historic LCM data (LCM2017–LCM2019) filtered to parcels with >99% purity across all three years; provides a large, wall-to-wall training set.
  - Training sets: GB ~941,027 objects; NI ~214,833 objects.
- Random Forest Classification:
  - Balanced training by drawing 10,000 samples per class with replacement from labeled parcels.
  - Class probabilities produced for each 10m pixel; the class with the highest probability is chosen.
  - Custom, in-house software integrates Weka with PostGIS and GDAL.
- Outputs and interpretation:
  - 10m pixel product includes class and confidence; users should consult the confidence band when using outputs for decision-making.

## Validation and Accuracy
- Validation approach:
  - Compared LCM2020 outputs to GB countryside survey data (2019–2020), open-source National Forest Inventory data, IACS data, and bespoke LCM validation points (34715 points in total).
  - Pixel-to-parcel intersections used to assess correspondence.
- Reported accuracy:
  - Overall accuracy: 79.2% (Appendix 4), with class-level producer and user accuracies detailed in the validation matrices.

## UKCEH Land Parcel Spatial Framework
- Framework purpose:
  - Provides stable, discrete units for change detection and longitudinal analysis.
- MMU and comparability:
  - Parcels ~0.5 ha; changes in parcel identifiers (gid) since LCM2015 may affect direct, year-to-year parcel ID comparisons.
- Spatial design:
  - Parcels generalise national cartography to reduce detail, ensuring most parcels are dominated by a single land cover type.

## Relationship to Biodiversity Action Plan (BAP) Broad Habitats
- The 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical.
- Crosswalk notes (Appendix 1 and 2) explain how UKCEH classes map to BAP Broad Habitats, including caveats where spectral separability is limited.
- The documentation emphasises that BAP terms are sometimes italicised when referring to BAP, while UKCEH Class names are capitalized.

## Usage Considerations and Limitations
- Data interpretation cautions:
  - The 10m Classified Pixels are not generalised with the Land Parcel Framework; validation was performed against the Land Parcel dataset, so users should be aware of potential differences when aggregating to parcels.
  - Small patches below the 0.5 ha MMU may be omitted in parcel datasets but present in pixel datasets; this is important for fine-scale mapping.
- Temporal dynamics:
  - Annual maps help separate false positives/false negatives from real change; random errors are expected to flicker over time, while persistent changes indicate real land-cover transitions.
- Data availability:
  - Datasets are produced for GB and NI with region-specific coordinate systems and extents; users should align analysis to the appropriate region and CRS.

## Practical Takeaways for GIS Specialists
- Use 10m Classified Pixels for high-detail mapping of land cover across the UK, mindful of the non-generalised nature relative to land parcels.
- Leverage the UKCEH Land Parcel Spatial Framework for stable change detection and parcel-level analysis, noting gid changes relative to earlier products.
- Consider 20m and 25m raster products for aggregated parcel analyses and compatibility with coarser-scale workflows.
- Consult the classification confidence band (_conf) and purity (_purity) metrics to assess reliability of parcel- and pixel-level classifications.
- Be aware of the BAP relationship context to align land cover classes with biodiversity reporting, while treating BAP terms as distinct from UKCEH class names where appropriate.
- Plan analyses with the regional specifics in mind (GB vs NI differences in context rasters, classification Scenes, and coordinate reference systems).
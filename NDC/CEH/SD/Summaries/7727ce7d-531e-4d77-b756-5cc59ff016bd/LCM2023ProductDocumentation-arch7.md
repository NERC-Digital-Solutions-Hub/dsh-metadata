# The UKCEH Land Cover Map for 2023

## Overview and purpose
- User guide for the UKCEH Land Cover Map 2023 (LCM2023).
- Product comprises seven datasets: three per region (Great Britain and Northern Ireland) plus a 1 km summary raster.
  - 10 m classified pixel dataset
  - Classified land parcel dataset
  - 25 m pixel rasterised land parcel dataset
  - Additional 1 km summary raster product covering GB and NI
- Aims to describe data production, validation, and data accuracy to support informed use.

## UKCEH Land Cover Classes and relationships
- LCM2023 defines 21 UKCEH Land Cover Classes, aligned with Biodiversity Action Plan (BAP) Broad Habitats but not identical.
- Clear guidance on aligning UKCEH classes with BAP Broad Habitats, including instances of splits and generalisations (Appendices 1–2).
- Full mapping details and class descriptions provided to aid interpretation and cross-walking to BAP/Habitat concepts.

## Datasets and product suite (Table/structure)
- Great Britain and Northern Ireland each have three geospatial datasets:
  - 10 m Classified Pixels (GB/NI)
  - Land Parcel Product (GB/NI)
  - 25 m Rasterised Land Parcels (GB/NI)
- A 1 km Summary Raster product covers GB and NI.
- Appendix 3 lists official dataset names and DOIs for each product.

## Data production and methodology
- Classification built from Classification Scenes that combine:
  - Sentinel-2 Seasonal Composite Images (4 seasons)
  - Context Rasters to reduce spectral confusion
- Bootstrap Training used to generate training data automatically from historic maps (LCM2020–2022) and a larger officer:
  - Training pixels sampled with >80% probability and consistent class across three years
  - Bootstrap data feed into a Random Forest classifier
- Seasonal Composite Images created using Google Earth Engine; spectral bands and resolutions detailed (Table 4).

## Classification and training details
- Classification Scenes:
  - Great Britain: 32 Classification Scenes (tile-based grid; ~100 x 100 km tiles; some expanded in tricky coastal regions)
  - Northern Ireland: single Classification Scene determined by NI land mass
- Bootstrap Training:
  - Uses historic LCM data to bootstrap new classifications
  - Large training samples help balance rare vs common classes
  - Some limitations for crops with rapid rotations (e.g., arable vs improved grassland)
- Random Forest classifier used; 10,000 samples per class per bag; balanced training via sampling with replacement
- Software: bespoke UKCEH tools integrating WEKA, PostGIS, and GDAL

## Data structure and content details
- 10 m Classified Pixel datasets:
  - Each pixel has two bands: 
    - Band 1: most likely UKCEH Land Cover Class (integer)
    - Band 2: associated class probability/confidence
  - Not generalised by Land Parcel Framework to preserve fine features (e.g., small patches)
  - Validation was performed against the 25 m Rasterised Land Parcel dataset
- 25 m Rasterised Land Parcel datasets:
  - Result of rasterising Land Parcel data; carries three parcel-level attributes:
    - _mode (dominant class), _conf (mean confidence), _purity (modal class purity)
  - Parcel identifier attributes include gid and ogc_fid (preferred to use gid)
- Land Parcel Product details:
  - GB and NI specifics: coordinate systems, extents, pixel counts, and bands
  - GB extents: 0–700000 E, 0–1300000 N; NI extents are truncated Irish Grid
  - MMU (minimum mapped unit) ~0.5 ha; parcels generalised from national cartography
- 1 km Summary rasters:
  - Dominant class per 1 km pixel (21 classes)
  - Percentage cover per class (21 bands) and per aggregate class (10 bands)
  - Integer percentages; sums can differ slightly from 100 due to rounding and coastal effects

## Context rasters and seasonal data
- Context Rasters (GB and NI) used to resolve spectral confusion:
  - GB: terrain height, aspect, slope; distances to buildings, roads, tidal water, freshwater; foreshore and binary masks for woodland and saltmarsh
  - NI: terrain height, aspect, slope; urban mask; distances to coast, freshwater, roads; foreshore and binary masks
- Seasonal Composite Images:
  - Four seasons, Sentinel-2 bands 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12
  - Cloud gaps handled by classifier without manual gap-filling

## Validation, accuracy, and known issues
- Formal validation: 33,107 reference points spanning all 21 classes
- Overall accuracy: 83%
- Known issues:
  - A small number of polygons missing from vector Land Parcel products (negligible impact on 1 km products; 10 m data unaffected)
- Data versioning and method changes noted; differences between maps can reflect real change or method changes

## Coordinate systems and extents
- Great Britain: British National Grid (EPSG: 27700)
- Northern Ireland: Irish Grid TM75 (EPSG: 29903)
- Parcel extents and pixel resolutions documented per dataset

## Citing and access
- Each LCM2023 dataset has a DOI; citations provided (Table of DOIs in the document)
- References for production methodology and prior years included (e.g., Marston et al., 2023–2024)
- Appendices include methodological notes, BAP habitat mappings, and colour palettes for mapping UKCEH Land Cover Classes (Appendices 5–6)

## Practical notes for GIS use
- The 10 m classified pixels provide detailed, high-resolution land cover maps with explicit confidence per pixel.
- The 25 m rasterised land parcels consolidate pixels into discrete parcels for stable time-series analysis; use parcel-level attributes for robust change detection.
- The 1 km rasters offer rapid, overview maps suitable for regional analyses and coupling with other 1 km-scale layers, with percentage cover limitations near coastlines.
- Context rasters and seasonal composites are essential for reducing misclassification in spectrally similar classes.
- When linking to historical data (LCM2015 or earlier), note potential mismatches in parcel identifiers due to updates in the UKCEH Land Parcel Spatial Framework.
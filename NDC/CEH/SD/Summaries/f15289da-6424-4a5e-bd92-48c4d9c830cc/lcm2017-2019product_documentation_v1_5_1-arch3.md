# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and Scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map suite provides a range of geospatial datasets representing UK-wide land cover.
- Aims to help users apply the data appropriately, understand production and validation decisions, and plan for future updates.

## What the data are and how they are structured
- Datasets included (one year produced for GB and NI, total 42 datasets):
  - 20m Classified Pixels (new), 25m Rasterised Land Parcels, Land Parcels (attributes), 1km Dominant Cover, 1km Dominant Aggregate Cover, 1km Percent Cover, 1km Percent Aggregate Cover.
- Class and aggregation structure:
  - 21 UKCEH Land Cover Classes (based on BAP Broad Habitats).
  - 10 UKCEH Aggregate Classes (generalised).
- Coordinate systems and extents:
  - GB: Great Britain National Grid (EPSG:27700).
  - NI: Irish Grid (EPSG:29903).
  - GB extents: 0–700,000 m E, 0–1,300,000 m N; NI extents defined similarly per grid.
- Pixel/parcel details:
  - 20m Classified Pixels: 2-band raster (class, per-pixel confidence 0–100); preserves fine landscape features.
  - Land Parcels: parcel-level attributes including histogram of pixel classes, modal class, purity, confidence, and counts.
  - 25m Rasterised Land Parcels: three-band raster (dominant class _mode, _conf, _purity).
  - 1km rasters: Percent Cover (21-band), Percent Aggregate Cover (10-band), Dominant Cover (1-band), Dominant Aggregate Cover (1-band).

## Production approach and data inputs
- Bootstrap Training and Random Forest (RF) classification:
  - Bootstrap Training uses historic UKCEH maps (LCM2015) to generate spectral training data for current classification.
  - Training samples balanced across classes to prevent dominance by common classes.
  - RF classifier applied to Classification Scenes to produce 20m Classified Pixels.
- Classification Scenes and inputs:
  - Seasonal Composite Images (Sentinel-2) per season (winter, spring, summer, autumn) created in Google Earth Engine from TOA reflectance.
  - Context Rasters (20m) to reduce spectral confusion (terrain, proximity to buildings/roads/sea/freshwater and coastal/foreshore masks, woodland presence).
  - GB Classification Scenes: 100x100 km tiles; NI: single 43-band scene per year.
- Land Parcel Spatial Framework:
  - Framework designed to represent discrete real-world units (≈0.5 ha MMU); used to summarize 20m pixels into parcels.
  - gid identifiers exist but are not consistent with LCM2015 parcels; most comparisons should use gid rather than parcel match.

## Production logistics and validation
- Automated production with minimal manual intervention:
  - No manual corrections in this release; visual checks and formal validation performed.
- Validation and accuracy:
  - Validation data: GB countryside survey (2019), National Forest Inventory, IACS, plus bespoke LCM validation points (total 22,325 points).
  - Reported overall accuracies (across 21 classes) on UK scale:
    - LCM2017: ~78.6%
    - LCM2018: ~79.6%
    - LCM2019: ~79.4%
  - Validation data limitations: points come from data sources with different purposes and class definitions; conversions to UKCEH classes introduce subjectivity.
- Interpretation notes:
  - Around 80% correspondence is considered impressive for fully automated, annual land cover maps; expect improvements as methods mature.

## Data relationships and class definitions
- Relationship to Biodiversity Action Plan (BAP) Broad Habitats:
  - 21 UKCEH Land Cover Classes align with BAP Broad Habitats; some mappings are approximate due to spectral detectability limits.
  - Appendix includes detailed mappings and notes on detection limitations for certain habitats (e.g., upland peatland vegetation, bracken, brackish waters).
- Terminology and presentation:
  - UKCEH Land Cover Classes are capitalised; BAP Broad Habitats are italicised when referred to.
  - Generalised land cover (UKCEH Aggregate Classes) provided for users who require less detail.

## Seasonal and input data specifics
- Seasonal Composite Images:
  - Generated from Sentinel-2 (TOA) with bands 2,3,4,5,6,7,8,11,12; reflectance per season used to form 46-band classification scenes for GB and 43-band scenes for NI.
  - TOA data chosen over surface reflectance (SR) after assessment; SR may be explored in future.
- Context Rasters (20m):
  - GB: height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland mask.
  - NI: height, aspect, slope; urban mask; distance to coast, freshwater, roads.
- Seasonal and classification strategy:
  - 74 overlapping GB classification scenes used to maximize training variety; NI uses a single scene per year.

## Future plans and ongoing development
- Annual release intention:
  - Plan to release a new LCM annually (2020, 2021) with bootstrap training reflecting multi-year majority signals.
- Data inputs and enhancements:
  - Ongoing review of input data (e.g., SR vs TOA) and potential expansion to additional data sources (e.g., radar/SAR) to improve gaps and robustness.
- Structural framework:
  - UKCEH Land Parcel Spatial Framework retained with minor internal reordering for performance; gid changes mean cross-year parcel comparisons should use gid.

## Practical considerations for monitoring frameworks
- Data provenance and governance:
  - Clear documentation of data lineage (Bootstrap Training, RF, Seasonal composites, context rasters) supporting reproducibility.
- Metadata and data quality:
  - Extensive metadata on datasets, coordinate systems, pixel sizes, extents, and class mappings; acknowledgment of potential metadata gaps and alignment issues between years.
- Data accessibility and transparency:
  - Public availability of multiple products (20m, 25m, 1km) across GB and NI; differences in parcel identifiers across years noted.
- Limitations and uncertainty:
  - Automated production introduces classification noise; some habitat classes are more challenging to detect spectrally (e.g., certain upland habitats, peatlands, brackish water).
  - Validation suggests room for improvement; ongoing efforts to refine training data and inputs.

## Appendices and supplementary material
- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats definitions and derivations.
- Appendix 3: RGB colour recipes for displaying Land Cover Classes.
- Appendix 4: Validation confusion matrices and accuracy metrics (detailed per-class producer’s and user’s accuracies; 2017–2019 comparisons).
- Appendix 5: Full dataset list and naming conventions by year and region.
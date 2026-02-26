# The UKCEH Land Cover Map for 2020

- UKCEH LCM2020 is the eighth UK land cover map, produced annually, consisting of six datasets for Great Britain and Northern Ireland: for each area, a 10m classified pixel dataset, a land parcel dataset, and a 25m pixel rasterised land parcel dataset (with additional 8-bit raster variants). The goal is to enable informed decision-making in policy and environmental monitoring, with emphasis on temporal consistency, comparability, and change detection.
- The map uses automatic classification via Bootstrap Training and a Random Forest classifier, enabling annual production without extensive manual corrections. Validation indicates an overall accuracy of about 79.2%.

## What the product includes

- 10m Classified Pixel datasets (GB and NI)
  - Pixels are classified into UKCEH Land Cover Classes; each pixel carries a class integer and an associated probability/confidence.
  - These pixels are not generalised by the Land Parcel Spatial Framework to preserve fine detail (e.g., small or narrow features). Intended for specialist users who understand the implications of the lack of generalisation.
- Classified Land Parcels (GB and NI)
  - Land parcels created by intersecting 10m classified pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - Parcel-level attributes and summary statistics are provided (e.g., histograms, modal class, confidence, aggregate class).
- 25m Pixel Rasterised Land Parcel datasets (GB and NI)
  - Per-parcel raster products with three bands: dominant land cover class (mode), mean confidence (conf), and parcel purity (purity).
- 8-bit Raster Products (GB and NI)
  - Additional raster-friendly representations of the land parcels.
- Dataset extents and projections
  - GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (EPSG: 29903).

## How the data are produced

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 data; four seasons (winter, spring, summer, autumn) with nine spectral bands; data gaps due to clouds are tolerated.
- Context Rasters
  - 10m context layers to reduce spectral confusion (e.g., terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal water, woodland masks). Separate sets for GB and NI.
- Classification Scenes and tiling
  - GB: 100x100 km tiles forming 36-band Seasonal Composite Images combined with 10 context layers to yield 46-band Classification Scenes; 74 overlapping scenes classified independently. Visual prioritisation resolves conflicts where scenes overlap.
  - NI: a single 100x100 km Classification Scene per year, combining a 36-band Sentinel-2 Seasonal Composite with 7 context rasters.
- Bootstrap Training and Random Forest
  - Bootstrap Training uses historic LCM maps (2017–2019) filtered to >99% purity to create training parcels; about 941,027 GB and 214,833 NI training objects.
  - Random Forest classifier trained with balanced pixel sampling (10,000 samples per class per training bag) to produce the 10m Classified Pixel product.
  - Software is bespoke, integrating Weka, PostGIS, and GDAL (all open source).

## The UKCEH Land Parcel Spatial Framework

- A long-standing framework (from LCM2007) to generalise cartography into land parcels (~0.5 ha MMU) to provide stable units for change detection.
- Updates re-ordered storage and indices; some parcel identifiers (gid) no longer match LCM2015, affecting direct year-to-year parcel ID comparisons.

## Relationship to biodiversity and habitat classifications

- The UKCEH Land Cover Classes (21 classes) map to UK Biodiversity Action Plan (BAP) Broad Habitats but are not identical; BAP terms are italicised when referenced.
- The mapping also provides generalised Land Cover Aggregates (UKCEH Aggregate Classes) in the Land Parcel product to support users who require a coarser classification.
- Appendix notes detail mappings between UKCEH classes and BAP Broad Habitats and highlight areas of potential spectral confusion (e.g., Bracken, Bog, Saltwater vs Freshwater).

## Validation and accuracy

- Validation dataset: GB countryside survey (2019–2020), open-source National Forest Inventory data, IACS data, and bespoke LCM validation points; total validation points around 34,715.
- Overall accuracy: 79.2% (Appendix 4), with class-level producer’s and user’s accuracies provided in the validation tables.

## Use, strengths, and limitations

- Strengths for monitoring frameworks
  - Annual, consistent production enabling change detection and time-series analyses.
  - Rich per-pixel probability/confidence and per-parcel summaries support uncertainty assessment and robust monitoring.
  - Clear, documented processing workflow (Bootstrap Training + RF, classification Scenes, context layers) supports reproducibility and auditing.
- Limitations and caveats
  - Some land cover classes remain spectrally confusable (e.g., Bog, Heather grassland, Saltmarsh; Saltwater vs Freshwater near coasts).
  - A number of small patches may fall below the MMU and be underrepresented in parcel data.
  - No manual corrections are performed at national scale to enable annual production; remaining errors are treated as potential real change over time.
  - Differences in parcel identifiers between LCM2015 and LCM2020 can affect direct year-by-year parcel ID comparisons.
- Practical guidance
  - The 10m pixel data provide detailed mapping at the cost of higher processing and interpretation complexity; the 25m parcel data offer a more stable, comparable unit for change detection and reporting.
  - Outputs include both classification results and associated confidence metrics to support governance and data quality assessments.

## Appendices and supporting material (highlights)

- Appendix 1: Notes on UKCEH Land Cover Classes (class-specific considerations and training-data guidance).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitat definitions and their relation to UKCEH classes.
- Appendix 3: Color recipes for displaying UKCEH Land Cover Classes (visualization guidance).
- Appendix 4: Correspondence matrices and validation results by class (detailed confusion and accuracy metrics).
- Appendix 5: Full list of LCM2020 datasets and metadata details.
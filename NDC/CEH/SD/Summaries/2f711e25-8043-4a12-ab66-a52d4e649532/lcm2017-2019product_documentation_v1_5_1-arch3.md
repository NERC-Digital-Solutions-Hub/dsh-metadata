# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- User guide accompanying UKCEH LCM2017, LCM2018, and LCM2019.
- Lands cover maps produced automatically to enable rapid understanding of UK land cover change.
- 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; annual releases planned to track change.
- Validation indicates maps are similar in quality to recent predecessor, with ongoing improvements planned.

## What the datasets include
- 20m Classified Pixels (new for these products): per-pixel classification results with class and confidence.
- Land Parcels: summary attributes derived by intersecting classified pixels with the UKCEH Land Parcel Spatial Framework (approximately 0.5 ha MMU).
- 25m Rasterised Land Parcels: three-band rasters (mode, confidence, purity) for each parcel.
- 1km rasters derived from parcels:
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- GB and Northern Ireland (NI) versions for each year; total of 42 datasets across three years.

## Production methodology
- Fully automatic classification using Bootstrap Training and Random Forest (RF) classifier.
- Bootstrap Training uses historic UKCEH LCM observations (from LCM2015, derived from LCM1990–LCM2007) to train RF models; targets balanced sampling across classes.
- For each year, classification is applied to 36-band Seasonal Composite Images (Sentinel-2 TOA) plus 20m Context Rasters to form Classification Scenes.
- GB uses a patchwork of overlapping 100x100 km Classification Scenes (74 scenes classified with overlaps to ensure robust training); NI uses a single 43-band scene per year.
- Processing software combines Weka (machine learning), PostGIS, and GDAL (open source).

## The UKCEH Land Parcel Spatial Framework
- Maintains the same land parcel geometries as LCM2015 (~0.5 ha MMU) but with reordered storage and new indices for speed.
- gid remains a stable parcel identifier within the framework; however, parcel IDs do not match LCM2015 when comparing datasets.
- Provides parcel-level attributes:
  - hist: per-land-parcel distribution of class occurrences
  - mode: most frequent class
  - purity: modal proportion
  - conf: mean class membership probability (0–100)
  - stdev: standard deviation of conf
  - n: number of 20m pixels intersecting the parcel
- Datasets include details on class composition and confidence, enabling change detection at parcel and landscape scales.

## Seasonal inputs and classification scenes
- Seasonal Composite Images created from Google Earth Engine using median TOA reflectance for four seasons (winter, spring, summer, autumn) from Sentinel-2 bands (2,3,4,5,6,7,8,11,12).
- Some seasonal gaps due to cloud are represented as null data; RF classifier tolerates missing data.
- Context Rasters used to reduce spectral confusion (e.g., terrain, urban proximity, distance to water, etc.).
- Sentinel-2 data were TOA-based in this production; surface reflectance (SR) was tested but TOA performed adequately for UKCEH Land Cover Classes.

## Context rasters and classification details
- GB 20m context rasters include height, aspect, slope; distance to buildings/roads/sea/freshwater; foreshore and tidal masks; woodland mask.
- NI context rasters include urban mask, distance to coast, freshwater, and roads.
- Aims to improve discrimination among spectrally similar classes (e.g., coastal vs inland features, urban vs non-urban).

## Data structure and presentation
- Classification Scenes: GB uses 100x100 km tiles; NI uses a single tile; total 74 GB scenes plus NI equivalents per year.
- 20m Classified Pixels preserve fine detail; Land Parcels aggregate into parcel-level attributes; 25m rasterise parcels for simplified visualization; 1km rasters summarize parcel data for larger-scale analyses.
- Figures and appendices provide visual examples of datasets and their relationships (e.g., 20m vs 25m vs 1km generalisation).

## Validation and accuracy
- Validation against GB countryside survey 2019 data, National Forest Inventory data, IACS, and manual-interpretation points (22,325 points total).
- Reported overall accuracy (producer and user accuracies consistent with class distributions):
  - LCM2017: ~78.6% overall accuracy
  - LCM2018: ~79.6% overall accuracy
  - LCM2019: ~79.4% overall accuracy
- Validation dataset is not a perfect gold standard; results reflect the best available indicators of reality with some misclassifications and class-level variance.

## Notable changes and considerations
- Manual corrections were not performed this cycle to enable annual production; prior maps included manual corrections in problematic regions.
- GID changes: parcel identifiers differ from LCM2015; cross-year parcel comparisons should use gid within the UKCEH Land Parcel Spatial Framework.
- Class definitions continue to reference UKCEH Land Cover Classes and UK BAP Broad Habitats; some cross-walking notes are provided in appendices to aid interpretation.
- Data presentation conventions and metadata updated (e.g., 20m Classified Pixels now include a confidence band; naming and attribute conventions updated to production software standards).

## Appendix highlights and guidance for users
- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; important for interpretation and cross-walking with field-based classifications.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Validation and confusion matrices (LCM2017, LCM2018, LCM2019) with class-level producer’s and user’s accuracies.
- Appendix 5: Full list of datasets per year and their dataset names, extents, and storage references.

## Future plans and access
- Annual release planned starting 2020 (LCM2020) with broader data coverage and continued bootstrap-based training.
- Ongoing assessment of alternative input data (e.g., additional optical sources or SAR) to address potential gaps and improve accuracy in cloud-prone seasons.
- Emphasis on data openness, governance, and clear communication of uncertainties to support monitoring frameworks and policy evaluation.
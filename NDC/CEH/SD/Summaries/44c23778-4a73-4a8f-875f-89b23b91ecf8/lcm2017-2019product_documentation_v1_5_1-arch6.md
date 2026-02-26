The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- Release of three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each product maps 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) aligned with LCM2015; designed for rapid, automated production without manual corrections.
- Data designed to support broad data use, change detection, and data-driven planning.

## Production philosophy and workflow
- Classifications produced automatically using Bootstrap Training plus a Random Forest (RF) classifier.
- Bootstrap Training uses historic UKCEH land cover observations (primarily from LCM2015) to generate training data; 99% purity threshold used to select training parcels from LCM2015.
- RF classifier trained on balanced samples (10,000 per class) to yield the 20m Classified Pixels product, which underpins all other datasets.
- Production emphasizes speed and consistency; no manual corrections were performed this cycle.
- Validation shows similar quality to the preceding LCM2015 map, with formal checks performed (Appendix 4).

## Datasets and data structure
- Total dataset suite replicated for Great Britain and Northern Ireland (GB and NI), with national grids:
  - GB: Great Britain position in British National Grid (EPSG: 27700)
  - NI: Northern Ireland position in Irish Grid (EPSG: 29903)
- Primary datasets (per year):
  - 20m Classified Pixels (new in 2017–2019): 2-band, 8-bit rasters. Band 1 = predicted class; Band 2 = class membership probability (0–100) indicating classification confidence.
  - Land Parcels: derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; includes parcel-level attributes:
    - gid, _hist (histogram of class counts per parcel), _mode (most frequent class), _purity (percent of modal class), _conf (mean class membership probability), _stdev, _n (number of pixels).
  - 25m Rasterised Land Parcels: 3-band rasters (band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km Raster datasets (per year):
    - 1km Percent Cover: 21-band raster (percent cover per class).
    - 1km Percent Aggregate Cover: 10-band raster (aggregate class coverage).
    - 1km Dominant Cover: 1-band raster (dominant class per 1km cell).
    - 1km Dominant Aggregate Cover: not always available in all years.
- Data lineage: 20m Classified Pixels feed the Land Parcels and, via summarisation, the 25m, 1km products. A total of 42 datasets (GB + NI) across three years.

## Spatial and temporal coverage
- Great Britain Classification Scenes:
  - GB Classification Scenes: 100x100 km tiles; 74 overlapping scenes per year classified to ensure balanced training across regions.
  - Seasonal Composite Images: Sentinel-2 TOA reflectance, median per season, for winter, spring, summer, autumn.
- Northern Ireland:
  - A single 43-band Classification Scene per year, determined by NI extent.
- Seasonal inputs derived from Google Earth Engine; gaps due to cloud are represented and handled by the RF to tolerate incomplete spectral data.

## Satellite inputs and context
- Sentinel-2 Seasonal Composite Images (TOA used; future potential for surface reflectance and SAR data exist).
- Context Rasters (GB 20m; NI varies slightly):
  - GB: height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal masks; woodland mask.
  - NI: height, aspect, slope; urban mask; distance to coast, freshwater, road.
- Context rasters are used to reduce spectral confusion and improve classification of spectrally similar classes (e.g., coastal vs inland features, urban vs vegetated surfaces).

## Classification Scenes and parcel framework
- UKCEH Land Parcel Spatial Framework maintained, with minor reordering and indexing for processing speed; parcel geometry remains the same as LCM2015, but parcel identifiers (gid) do not match LCM2015 for direct parcel-to-parcel comparisons.
- LCM2017–2019 land parcels have a minimum area of ~0.5 ha (MMU). Summary datasets enable change detection over time, while the 20m Classified Pixels preserve finer landscape detail for users needing high granularity.

## Validation and accuracy
- UK-scale validation against GB countryside survey (2019), National Forest Inventory, IACS validation points:
  - LCM2017: 78.6% overall accuracy
  - LCM2018: 79.6% overall accuracy
  - LCM2019: 79.4% overall accuracy
- Validation dataset comprised 22,325 points; results indicate roughly 80% correspondence to UKCEH 21-class outputs, with acknowledged caveats due to crosswalk between legacy classifications and current UKCEH classes.
- Validation figures are intended as indicators of quality; some misclassifications and cross-class ambiguities exist due to evolving class definitions and training data.

## Class definitions and relationships
- 21 UKCEH Land Cover Classes aligned with BAP Broad Habitats; general relationships and notes are provided (Appendices 1–2) to aid interpretation and cross-walking with BAP definitions.
- Appendix 3 provides recommended RGB color mappings for display.

## Access, formats, and practical notes for data use
- Data are designed for self-serve analyses and broad data exploration; suitable for policy, planning, and environmental monitoring at multiple resolutions (20m, 25m, 1km).
- Key caveats:
  - GID values differ from LCM2015; direct parcel-id comparisons across years require GID-based matching.
  - No manual accuracy corrections were applied; results inherently include classification noise typical of automated approaches.
  - TOA inputs were used rather than SR in this release; potential for future revisions as input data improve.
  - Some smaller land cover patches may be below MMU and may be underrepresented in parcel summaries.
- Appendices and Dataset List:
  - Appendix 5 lists full dataset inventories per year and per GB/NI.

## Future plans and uptake
- Intention to release a new LCM annually (LCM2020 planned for 2021).
- Bootstrap Training and production methods are expected to evolve; future maps may incorporate additional data sources (e.g., Sentinel-1, higher-resolution inputs) and refined upland vegetation/habitat classifications.
- Ongoing validation and resource improvements planned to enhance accuracy and usability.
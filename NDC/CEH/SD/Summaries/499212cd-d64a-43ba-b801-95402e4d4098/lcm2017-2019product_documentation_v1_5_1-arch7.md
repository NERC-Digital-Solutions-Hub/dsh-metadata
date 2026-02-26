# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a range of geospatial datasets and 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with a near one-to-one relationship to the 2015 classes.
  - Classifications produced automatically using Bootstrap Training and Random Forest; no manual corrections in this release.
  - Annual map production is intended going forward; validation performed to ensure quality comparable with recent predecessors.

- Class structure and terminology
  - 21 UKCEH Land Cover Classes (mapped from BAP Broad Habitats) and 10 UKCEH Aggregate Classes.
  - Clear definitions and relationships between UKCEH Land Cover Classes and BAP Broad Habitats; emphasis on consistency for change detection and cross-year comparisons.
  - Generalised outputs (UKCEH Aggregate Classes) available alongside detailed classes.

- Production approach and key concepts
  - Bootstrap Training: automatic sampling of historical land cover observations (from LCM2015) to train the classifier, enabling automatic yearly maps without new field data.
  - Random Forest (RF) classifier used to generate 20 m classified pixels; training data balanced across classes.
  - Seasonal Sentinel-2 composites (TOA reflectance) used per season (winter, spring, summer, autumn) to form Classification Scenes with 9 spectral bands plus 10 Context Rasters.
  - Google Earth Engine deployed for processing; emphasis on rapid UK-wide production and handling cloud gaps without manual gap filling.
  - Context Rasters (20 m) provide ancillary information to reduce spectral confusion (e.g., height, slope, distance to roads/buildings, coast, freshwater, urban/foreshore masks, etc.).

- Classification architecture and tiling
  - Great Britain: 100 x 100 km classification tiles; 36-band Seasonal Composite Images combined with 20 m Context Rasters to create 46-band GB Classification Scenes; 74 overlapping scenes classified independently; visual inspection used to select best results where overlaps occur.
  - Northern Ireland: single 43-band Classification Scene per year (36 spectral bands + 7 context layers) covering the minimum bounding rectangle of NI land mass.
  - Focus on ensuring balanced representation of classes during RF training and reducing spatial phenology bias through tiling.

- UK Land Parcel Spatial Framework
  - Land Parcel framework exists to summarise 20 m Classified Pixels into parcels (approx. 0.5 ha MMU); used to produce Land Parcels, 25 m Rasterised Land Parcels, and 1 km rasters.
  - gid provides a stable parcel identifier, but gids differ from LCM2015; cross-version parcel comparisons should use gid for 2017–2019.
  - Minor attribute changes since LCM2015; main attributes include hist, mode, purity, conf, stdev, n.

- Datasets and data products (GB and NI)
  - 20 m Classified Pixels: new RF classification outputs per pixel; band 1 = most likely class; band 2 = confidence (0–100).
  - Land Parcels: summarises 20 m pixels within the UKCEH Land Parcel Spatial Framework; attributes include gid, hist (class occurrence per parcel), mode, purity (percentage), conf, stdev, n.
  - 25 m Rasterised Land Parcels: 3-band rasters (band 1 = modal class; band 2 = parcel-averaged class membership probability; band 3 = purity).
  - 1 km rasters (intermediate summaries):
    - 1 km Percent Cover: 21-band raster of per-class percentage cover.
    - 1 km Percent Aggregate Cover: 10-band raster for aggregate classes.
    - 1 km Dominant Cover: single-band raster of dominant class per 1 km cell.
    - 1 km Dominant Aggregate Cover: single-band raster of dominant aggregate class per 1 km cell.
  - Dataset extents and coordinate systems
    - Great Britain datasets in British National Grid (EPSG:27700).
    - Northern Ireland datasets in Irish grid (TM75 / EPSG:29903).
    - GB extent: Min East 0, Max East 700,000 m; Min North 0, Max North 1,300,000 m.
    - NI extent: Min East 180,000 m, Max East 400,000 m; Min North 300,000 m, Max North 500,000 m.
  - Pixel and band specifics
    - 20 m Classified Pixels: 2 bands (class and confidence 0–100); 8-bit raster; 21 classes.
    - 25 m Rasterised Land Parcels: 3 bands (mode, conf, purity); 8-bit rasters; 21 classes.
    - 1 km rasters: 21-band Percent Cover; 10-band Percent Aggregate Cover; 1-band Dominant and Dominant Aggregate; all 8-bit.

- Seasonal inputs and spectral bands
  - Sentinel-2 seasonal composites created from TOA reflectance (4 seasons; 9 bands used).
  - Bands include coastal aerosol, blue, green, red, vegetation red edge, NIR, water vapour/ cirrus, SWIR, etc. Reconstruction focuses on phenology and spectral separation of land cover types.
  - Spatial resolution for 20 m and 25 m products; 1 km products aggregate to 1 km grid.

- Validation and accuracy
  - UK-scale validation using 22,325 points across GB/NI from multiple sources (Countryside Survey 2019, open data inventories, bespoke validation points).
  - Reported overall accuracies around:
    - LCM2017: ~78.6%
    - LCM2018: ~79.6%
    - LCM2019: ~79.4%
  - Note: same validation dataset used for all three products; accuracies reflect currency and class-mapping adjustments; ~80% correspondence is considered strong for automatic maps.

- Practical notes and caveats for GIS use
  - No manual accuracy corrections applied this release to enable annual updates; classification results may contain random, year-to-year noise that should persist for real land cover change signals.
  - Land Parcel identifiers (gid) differ from LCM2015; cross-year parcel comparisons require gid rather than parcel overlap.
  - Some gaps may appear in seasonal data due to cloud; the methodology tolerates partial spectral information and aims to minimize manual gap filling; future work may incorporate SAR data (e.g., Sentinel-1) to fill gaps.
  - The 20 m Classified Pixels output preserves fine landscape features (narrow patches and lines) that may be smoothed in parcel-based summaries.

- Appendices and references (highlights)
  - Appendix 1–2: notes on UKCEH Land Cover Classes and representative BAP Broad Habitats, including class-level detection considerations and limitations.
  - Appendix 3: recommended RGB color recipes for displaying the 21 UKCEH Land Cover Classes.
  - Appendix 4: validation tables (summary); includes producer’s and user’s accuracies by class and confusion details.
  - Appendix 5: full list of datasets per LCM year (dataset names and GB/NI scope).

- Availability and workflow implications for GIS specialists
  - Provides a comprehensive, year-on-year set of linked raster products and parcel-based attributes suitable for change detection, landscape analysis, and policy-oriented mapping.
  - Suitable for map-based data products, spatial analyses, and integration with other GIS datasets due to standardized coordinate systems and well-documented class definitions.
  - Encourages use of the 20 m Classified Pixels for detailed landscape representation and the parcel framework for standardized temporal comparisons.
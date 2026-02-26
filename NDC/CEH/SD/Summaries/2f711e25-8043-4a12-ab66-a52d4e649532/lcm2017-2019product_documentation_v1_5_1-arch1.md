# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - Introduces three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
  - Each map contains 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
  - Production is fully automatic, using Bootstrap Training and Random Forest (RF) classification to generate UK-wide maps rapidly.
  - Data rely on Sentinel-2 Seasonal Composite Images (TOA) plus 20m Context Rasters to produce Classification Scenes.
  - Goal: enable annual updates and informed spatial analyses; minimal manual corrections to maintain automation.

- Key concepts and terminology
  - Classification Scene: multi-layer raster combining Seasonal Composite Images with Context Rasters for RF classification.
  - Seasonal Composite Image: four-season spectral representation from Sentinel-2.
  - Bootstrap Training: automatic generation of training data from historic LCMs (primarily LCM2015) to seed RF classification for new maps.
  - Land Parcel Spatial Framework: fixed spatial framework (min ~0.5 ha) used to summarise 20m classified pixels into parcel-level attributes.
  - UKCEH Land Cover Classes vs UK BAP Broad Habitats: mapped classes align with 21 UKCEH Classes, closely related to BAP Broad Habitats but not exact BAP definitions; emphasis on maintaining consistency for change detection.

- Production workflow and dataset structure
  - Bootstrap Training and Random Forest
    - Training data derived from UKCEH LCM2015; RF classifier trained with 10,000 samples per class, balanced via sampling with replacement.
    - Bootstrap Training aims to leverage majority signals over time (2017–2019) for subsequent maps.
  - Classification Scenes and tiling
    - Great Britain: classification conducted on 100x100 km tiles, resulting in 74 overlapping GB Classification Scenes per year (46 bands per scene: 36 spectral + 10 context).
    - Northern Ireland: single 43-band Classification Scene per year (36 spectral + 7 context).
  - UKCEH Land Parcel Spatial Framework
    - Maintains ~0.5 ha minimum parcel size; parcels are consistent with LCM2015 but gid values differ between generations.
    - Framework enables parcel-based summaries and change detection; not all features are guaranteed to be visible at current resolution.
  - Dataset suite (42 datasets in total across years)
    - 20m Classified Pixels (GB and NI): new in LCM2017–2019; RF classification with per-pixel class probability (band 2 scaled 0–100).
    - Land Parcels: parcel-level attributes linked to 20m pixels (hist, mode, purity, conf, stdev, n).
    - 25m Rasterised Land Parcels: three-band raster (mode, conf, purity) summarising parcel data.
    - 1km Raster products:
      - 1km Percent Cover (21-band)
      - 1km Percent Aggregate Cover (10-band)
      - 1km Dominant Cover (1-band)
      - 1km Dominant Aggregate Cover (1-band)
  - Geographic extents and CRS
    - Great Britain: British National Grid (EPSG:27700)
    - Northern Ireland: Irish Grid (EPSG:29903)
    - GB extent: min East 0 to max East 700,000 m; min North 0 to max North 1,300,000 m
    - NI extent: specific NI bounds (approx. East 180,000–400,000; North 300,000–500,000)

- Data inputs and imagery
  - Sentinel-2 Seasonal Composite Images: median TOA reflectance per season (winter, spring, summer, autumn) at 20 m resolution; used despite occasional seasonal gaps due to cloud.
  - Context Rasters (GB = 10 layers; NI = 7 layers): terrain (Height, Aspect, Slope) and proximity masks (buildings, roads, coast, freshwater, urban/foreshore, etc.).
  - Decision on data type: TOA was used rather than surface reflectance (SR) because SR did not improve classification for this particular land cover schema in this release.

- Classification approach and validation
  - Random Forest classification driven by Bootstrap Training; aims to balance classes to avoid bias toward common classes.
  - Visual checks and formal validation performed (Appendix 4); roughly on par with the previous LCM2015 in quality.
  - Validation data sources: GB countryside survey 2019, open data (National Forest Inventory), IACS, and bespoke LCM validation points (total n ≈ 22,325 points).
  - Reported accuracy (UK scale, cross-year comparison)
    - LCM2017: ~78.6% overall
    - LCM2018: ~79.6% overall
    - LCM2019: ~79.4% overall
  - Notes on validation
    - Validation data are not perfect ground truth; cross-walking between validation classes and UKCEH classes introduces some subjectivity.
    - Validation currency varies by product; still, ~80% correspondence is considered impressive given automatic production.

- Class definitions and documentation
  - UKCEH Land Cover Classes are mapped from UK BAP Broad Habitats with careful cross-walks (Tables and Appendices detail relationships).
  - Appendix notes include guidance on difficult-to-detect upland and coastal classes, and how certain classes are detected or confused spectrally.
  - Appendix 3 provides recommended RGB color mappings for displaying the 21 land cover classes.
  - Appendix 5 lists the full dataset inventory per year and region (GB and NI datasets).

- Practical considerations for analysts
  - Annual products enable change detection and trend analysis, with 2017–2019 as bootstrap training sources for subsequent maps.
  - The 20m Classified Pixels layer preserves fine-grained landscape features; the Land Parcels and 25m Rasterised formats provide convenient aggregated views for regional analyses.
  - 1km rasters offer quick summary metrics (percent cover, dominant classes) for large-area assessments.
  - Cross-year parcel identifiers (gid) differ between releases; cross-year comparisons should use the Land Parcel Spatial Framework or spatial overlap rather than direct gid matching.
  - While automated, the datasets include validation notes and caveats that should inform uncertainty analyses and interpretation.

- Future directions and plans
  - Intend to continue annual releases; envisaged bootstrap from majority signals across the most recent years.
  - Exploration of additional input sources (e.g., Sentinel-1 SAR, alternative optical sources) and potential improvements to training data as data availability evolves.

- References and provenance
  - Core methods: Bootstrap Training, Random Forest (Breiman, 2001)
  - Supporting research and methodological context: Carrasco et al. (2019), Frank et al. (WEKA), Jackson (2000) on BAP, Morton et al. (2011), Smith et al. (2007)
  - Appendices document detailed class definitions and literature-backed notes on habitat mappings and detection challenges.
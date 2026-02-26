# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide accompanying the release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Land cover described using 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with a goal of rapid, automated UK-wide mapping.
  - Maps produced automatically (Bootstrap Training + Random Forest) with no manual corrections this round; visual checks and formal validation were performed to ensure quality comparable to the previous LCM2015.
  - Aims include enabling time-series analysis for environmental monitoring and policy evaluation.

- Data products and structure
  - 20m Classified Pixels: new 2-band rasters per pixel (class and per-pixel confidence 0–100) for detailed mapping.
  - Land Parcels: parcel-level attributes derived from the 20m classified data (gid, hist, mode, purity, conf, stdev, n); designed to summarize parcel-level land cover.
  - 25m Rasterised Land Parcels: three-band rasters (band 1 mode, band 2 conf, band 3 purity) summarising parcels at 25 m resolution.
  - 1km Raster Datasets: 
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
  - Spatial coverage and formats: Great Britain (EPSG:27700) and Northern Ireland (EPSG:29903); multiple datasets per year (total 42 datasets across 3 years).

- Production methodology
  - Bootstrap Training: automatic training data derived from UKCEH LCM2015 (sampling parcels with purity ≥ 99%), enabling rapid production without fresh field data.
  - Random Forest classification: balanced training (10,000 samples per class) to yield 20m Classified Pixels and subsequent products.
  - Seasonal Composite Imagery: Sentinel-2 seasonal medians (winter, spring, summer, autumn) derived from Google Earth Engine; four-season TOA reflectance used (surface reflectance not adopted in this release).
  - Context rasters: 20m contextual layers to reduce spectral confusion (terrain, proximity to buildings/roads/sea/freshwater, foreshore and tidal masks, coastal/urban context, etc.).
  - Classification Scenes: 
    - Great Britain: 74 overlapping 100x100 km classification tiles to generate 46-band scenes; each scene trained and classified independently with intentional overlaps for robust results.
    - Northern Ireland: a single 43-band classification scene per year determined by the minimum bounding rectangle of NI land mass.
  - UKCEH Land Parcel Spatial Framework: fixed framework for parcel-based summaries; transfers of parcel identifiers (gid) may not match LCM2015, but parcel-based comparisons can be done via gid; framework maintains a 0.5 ha minimum parcel size (MMU).

- Data quality, validation, and limitations
  - Validation: UK-scale validation against GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points total).
  - Reported accuracy (overall): 
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Notes on validation: points derived from datasets with different purposes; some class conversions were needed; results are indicators of reality rather than absolute truth; accuracy is expected to improve as methods mature.
  - No manual corrections were applied to the classification step in this release; automatic classification drives the time-series capability, with visual checks and formal validation providing quality assurance.

- Spatial and temporal context
  - Seasonal imagery and context layers designed to support robust discrimination across land cover types and reduce confounding spectral signals.
  - The time-series aspect is enabled by annual production (2017–2019) and the Bootstrap Training approach, with plans to continue annual releases (LCM2020, LCM2021) using majority signals across recent years.

- Data interpretation, usage, and notes
  - UKCEH Land Cover Classes are aligned with UK BAP Broad Habitats where possible, with some refinements to balance remote-sensing detection with historical continuity.
  - Users should account for differences between 21 UKCEH Classes and 10 UKCEH Aggregate Classes; Appendix materials provide mappings and descriptions for interpretation.
  - 20m Classified Pixels preserve finer landscape features (unlike the 25m parcel-aggregated products); 25m and 1km products provide useful generalized summaries for broad-scale analyses.
  - MMU considerations and potential gaps: some very small patches may be underrepresented; seasonal gaps can occur in cloud-prone years, though the production method tolerates partial spectral information.

- Appendices and supporting materials
  - Appendix 1–2: Definitions and notes on UKCEH Land Cover Classes and relationships to BAP Broad Habitats; detection considerations and caveats.
  - Appendix 3: Recommended RGB color scheme for displaying classes.
  - Appendix 4: Validation and confusion matrices (illustrative) for LCM2017, LCM2018, and LCM2019.
  - Appendix 5: Full dataset lists and dataset-specific metadata for LCM2017–LCM2019.

- Practical implications for environmental monitoring
  - Provides a consistent, repeatable, year-by-year data product suitable for trend analysis and policy performance assessment.
  - Enables integration with other environmental datasets through a standard Spatial Framework (Land Parcels) and well-documented metadata.
  - Supports data-sharing objectives by providing underlying training and classification methodology, while noting gid changes across releases.
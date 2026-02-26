# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, LCM2019.
  - 21 UKCEH Land Cover Classes based on BAP Broad Habitats; designed for broad change detection and cross-year comparability.
  - Maps produced automatically via Bootstrap Training plus Random Forest; intended to enable rapid, near‑annual updates.
  - Provides guidance on production decisions, validation, future plans, and appropriate use.

- Data model and datasets
  - 20m Classified Pixels (GB and NI): 2-band 8‑bit rasters per year; band 1 = most likely class, band 2 = class membership probability (0–100).
  - Land Parcels: 21 UKCEH Land Cover Classes; attributes include gid, _hist (class frequencies), _mode (dominant class), _purity (percent), _conf (mean membership probability 0–100), _stdev, _n. Note: gid differs from LCM2015; parcel structure fixed to UKCEH framework.
  - 25m Rasterised Land Parcels: 3-band rasters; bands = _mode, _conf, _purity.
  - 1km rasters (GB and NI): 
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Extents and projections: GB (EPSG:27700) and NI (EPSG:29903).
  - Dataset counts: 42 datasets across years (GB and NI variants).

- Production approach and provenance
  - Bootstrap Training: automatic, minimal-field data approach; Bootstrap sets derived from historic UKCEH maps (LCM2015 bootstrap used for 2017–2019). Future years plan to use multi-year majority signals (e.g., 2017–2019, then 2018–2020).
  - Classification: Random Forest (RF) trained on balanced samples (10,000 per class per Classification Scene) using historic training data; production software combines WEKA, PostGIS, and GDAL.
  - Seasonal inputs: Sentinel-2 Seasonal Composite Images (TOA reflectance, 20 m) per season (winter, spring, summer, autumn) plus 20 m Context Rasters to reduce spectral confusion.
  - Context rasters (20 m): terrain (height, aspect, slope) and proximity masks (buildings, roads, sea, freshwater, foreshore, urban/woodland indicators).
  - Seasonal completeness: some cloud gaps; classifier tolerates missing seasons; potential future use of SAR or alternative sources to fill gaps.
  - Parcels framework: UKCEH Land Parcel Spatial Framework retained from LCM2015 with minor indexing updates; MMU ~0.5 ha; intended as a fixed structure for change detection but not the only possible summarisation mechanism.

- Data quality, validation, and limitations
  - Validation: UK-scale validation using 22,325 points against GB countryside survey data, NFI data, IACS, and interpretive points.
  - Reported accuracy (across 2017–2019, 21-class maps):
    - LCM2017: ~78.6%
    - LCM2018: ~79.6%
    - LCM2019: ~79.4%
  - Notes:
    - Validation points are not an absolute truth; conversions between validation classes and UKCEH classes introduce subjectivity.
    - No manual corrections were applied in these releases; classification is entirely automatic, with visual checks and formal validation.
    - Approximately 80% overall correspondence is considered strong given automatic mapping; expect improvements as methods mature.
  - Class definitions and terminology are aligned with Appendix guidance; some distinctions (e.g., BAP vs UKCEH classes) may be nuanced when interpreting spectral signals.

- Spatial, temporal, and thematic specifics
  - 20m Classified Pixels preserve detailed landscape features; 25m Land Parcels summarise into coarser grids for broad-level mapping.
  - 1km products provide grid-aggregated summaries (percent, dominant, and partial dominants) for cross-year comparisons and broad-scale analyses.
  - The Seasonal Composite Images leverage 9 Sentinel-2 bands with spectral and context information to drive classification; some bands are not used where data gaps exist.
  - The mapping framework includes detailed Appendix guidance on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; careful interpretation is advised where direct spectral separation is challenging (e.g., upland peatland vegetation, saltwater vs freshwater mix).

- Update cadence, versioning, and governance
  - Annual production goal: aim to release a new LCM each year (LCM2017–2019 preview demonstrates feasibility and logic for yearly updates).
  - Version and provenance: clear documentation of dataset lineage, including bootstrap source, RF training, and attribute definitions; changes to parcel identifiers mean cross-year parcel comparisons should use gid (not previous LCM identifiers).
  - Data stewardship implications: documentation of data lineage, attribute semantics, spatial framework, and validation context essential for data governance, reproducibility, and cross-collection interoperability.

- Metadata, documentation, and usage guidance
  - Datasets include extensive metadata: coordinate systems, pixel sizes, class counts, band counts, and per-dataset descriptions; Tables 2–4 outline land parcel metadata, raster extents, and additional attributes.
  - Appendix guidance covers class relationships to BAP Broad Habitats, recommended RGB color recipes for display, and detailed confusion matrices and accuracies by class.
  - Practical considerations for data stewards:
    - Be aware of the gid mismatch with LCM2015 when building longitudinal analyses; use gid-based comparisons for LCM2017–LCM2019.
    - Understand the 0.5 ha MMU and how it influences detection of small patches, especially in 20 m vs 25 m products.
    - Recognise that 20 m Classified Pixels retain detailed features not present in 25 m summaries, affecting downstream analyses.

- Known limitations and challenges
  - Incomplete or evolving user needs alignment; potential disparities between user expectations and automated outputs.
  - Timeliness and access to data creators or data sources for training data and validation.
  - Handling of many systems and formats, and the need to integrate new data sources as technologies evolve (e.g., potential use of Sentinel-1, SAR, or SR inputs in future releases).
  - Some classes remain spectrally confusable; context rasters and seasonal signals mitigate but do not eliminate confusion (e.g., various grassland types, peatlands, coastal vs inland water).

- Practical takeaways for Data Stewards
  - The LCM2017–LCM2019 data suite provides a robust, annually updating framework with clearly defined datasets, metadata, and validation context suitable for large-scale land cover governance and change monitoring.
  - Governance tasks include maintaining clear lineage, updating metadata with any changes in parcel identifiers or attribute names, and communicating limitations to data users.
  - Ensure alignment with institutional data policies, particularly around classification semantics, cross-year comparability, and usage of the 20 m vs 25 m products for specific analyses.
  - Plan for ongoing evaluation and potential integration of new data sources to fill seasonal gaps and improve classification in challenging landscapes.
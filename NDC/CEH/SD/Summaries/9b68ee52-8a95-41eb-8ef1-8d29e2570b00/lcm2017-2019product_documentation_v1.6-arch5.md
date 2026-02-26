# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

- Purpose: User guide for three UKCEH Land Cover Maps (LCMs) LCM2017, LCM2018 and LCM2019. Each map is a suite of geospatial datasets (21 UKCEH Land Cover Classes based on BAP Broad Habitats) produced automatically using Bootstrap Training and a Random Forest classifier. Seasonal Sentinel-2 imagery (TOA) plus 20m Context Rasters generated Classification Scenes. No manual corrections were applied this time; aims to enable rapid, annually updated UK-wide land cover mapping with validated quality control.

- Production approach and rationale:
  - Bootstrap Training: Uses historical LCM2015 (and bootstrap samples from majority signals) to train the RF classifier; automatic, self-starting learning without new field campaigns.
  - Random Forest classification: Balances training data across 21 classes to improve performance for rarer classes.
  - Seasonal Composite Images: Four-season Sentinel-2 TOA reflectance (20m) merged with 20m Context Rasters to form Classification Scenes; robust to cloud gaps and suitable for annual updates.
  - Context Rasters: Include terrain (Height, Aspect, Slope) and proximity masks (buildings, roads, sea, freshwater, foreshore, urban/rural features) to help disambiguate spectrally similar classes.

- Data products and structure (GB and NI; per year 2017–2019):
  - 20m Classified Pixels (GB and NI) – 2-band rasters:
    - Band 1: most likely UKCEH Land Cover Class (21 classes for GB; 21/10 for NI as applicable).
    - Band 2: class membership probability (0–100) indicating classification confidence.
  - Land Parcels – attribute-rich vector-like structure summarized from 20m Classified Pixels via the UKCEH Land Parcel Spatial Framework; 0.5 ha MMU; gid-based identifiers; key attributes include:
    - _hist (pixel frequency distribution per class within parcel)
    - _mode (dominant class)
    - _purity (parcel-level purity percentage)
    - _conf (mean per-pixel membership confidence)
    - _stdev (uncertainty)
    - _n (npix, number of intersecting pixels)
    - gid (unique parcel identifier; note gid values differ from LCM2015)
  - 25m Rasterised Land Parcels – 3-band rasters (band 1: _mode; band 2: _conf; band 3: _purity).
  - 1km rasters (GB and NI):
    - 1km Percent Cover – 21-band (percent cover per class)
    - 1km Percent Aggregate Cover – 10-band (aggregate class percent cover)
    - 1km Dominant Cover – single band (dominant class)
    - 1km Dominant Aggregate Cover – single band (dominant aggregate class)
  - Dataset extent and formats:
    - GB: British National Grid (EPSG:27700)
    - NI: Irish National Grid (EPSG:29903)
    - Pixel sizes: 20m, 25m (land parcels), 1km (summary rasters)
    - 42 datasets total across years and regions (GB and NI per year)

- Dataset specifics and notable changes since LCM2015:
  - 20m Classified Pixels: New addition in 2017–2019; preserves landscape detail by maintaining 20m resolution before summarisation into parcels.
  - Land Parcels: Attributes reorganised to align with production software; gid values no longer match LCM2015 for parcel comparisons; parcel framework remains the UKCEH Spatial Framework with MMU ~0.5 ha; provides a fixed structure for time-series comparison and change detection.
  - 25m Rasterised Land Parcels: Purity now included as a third band (besides mode and conf) to convey parcel-level confidence.
  - 1km rasters: Summaries computed from 25m parcels; rounding applied to percent values (sum may deviate from 100% due to rounding and coastal partial coverage).
  - Classification approach: All maps (2017–2019) classified automatically without manual corrections; visual checks and formal validation performed (Appendix 5).

- Context and production details:
  - Classification Scenes: GB produced in overlapping 100x100 km tiles; NI produced in a single 43-band scene; each scene is trained and classified independently; overlaps used to optimize training balance; final results resolved by visual inspection where overlaps occurred.
  - Seasonal Composite Images: Sentinel-2 bands (TOA) used to create four-season reflectance composites; clouds can leave gaps, but the RF classifier tolerates partial spectral information; future work may incorporate alternative sources (e.g., Sentinel-1) to fill gaps.
  - Context Rasters (GB vs NI): GB uses 10 context rasters (terrain, urban, coast, etc.); NI uses 7–10 context rasters adapted to available data.
  - UK Land Parcel Spatial Framework: Maintains consistent parcel geometry with LCM2015; 0.5 ha MMU; geometry unchanged but storage/indexing updated for performance; differences limit cross-year parcel-to-parcel comparisons unless using gid across 2017–2019.

- Validation and accuracy (UK scale):
  - Validation dataset: approximately 22,325 points using GB countryside survey 2019, National Forest Inventory, IACS, and bespoke LCM validation points.
  - Overall accuracy:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Notes: Validation uses cross-warmed data sources with some class mapping; results provide a robust indicator of performance but are not an absolute truth; accuracy scales expected to improve as methods mature.

- Governance, provenance, and metadata:
  - Data lineage: Bootstrap Training dataset derived from LCM2015; RF model trained on balanced samples; outputs feed the next map’s bootstrap.
  - Data provenance: Datasets prepared for GB and NI; year-specific copies for 2017, 2018, 2019; full list of datasets provided (Appendix 6).
  - Metadata considerations include: coordinate systems, extents, class definitions, and cross-walks to BAP Broad Habitats (Appendix 1–2); detailed confusion matrices and producer/user accuracies (Appendix 5).
  - Color schemes and symbology provided for display (Appendix 3–4) to support consistent visualization.

- Practical use and caveats for data stewardship:
  - Automation emphasis: No manual region-specific corrections; users should expect typical remote-sensing classification noise and year-to-year changes reflecting real dynamics.
  - Class-specific challenges: Difficult for some upland and coastal classes (e.g., Bog, Fen, Saltmarsh, Neutral Grassland) due to spectral similarity and MMU constraints; context rasters mitigate some misclassification.
  - Cross-year comparisons: Parcel identifiers (gid) differ from LCM2015; parcel-based time-series analysis should rely on gid-based comparisons (LCM2017–2019); direct parcel ID matching with LCM2015 is not supported.
  - Data governance considerations: Data are provided at national scale with regional splits; users should account for patchiness in coastal and water features and the lack of manual corrections when integrating with other datasets.

- Future plans and ongoing development:
  - Annual release trajectory: The team intends to release a new LCM each year (as stated in Introduction).
  - Enhancements: Ongoing review of input satellite products (TOA vs SR) and potential expansion to additional data sources (e.g., Sentinel-1) to handle gaps and potentially improve thematic detail.
  - Bootstrap evolution: Future maps (LCM2020, LCM2021) to use bootstrap from 2017–2019 majority signals; 2018–2020 signals for subsequent updates.

- Appendices at a glance (context for data interpretation):
  - Appendix 1–2: Biodiversity Action Plan Broad Habitats detail and relation to UKCEH Land Cover Classes.
  - Appendix 3–4: Recommended color recipes for displaying UKCEH Land Cover Classes; color-blind friendly options.
  - Appendix 5: Confusion matrices for LCM2017–LCM2019 (detailed class-level accuracy, user/producer accuracies, and cross-class confusion).
  - Appendix 6: Full list of datasets by year and product type (GB and NI).
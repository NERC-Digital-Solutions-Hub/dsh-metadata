# 1.1 Satellite imagery and Pre-processing

- Data sources and data products
  - Sentinel 1A (SAR) used, Level 1 Ground Range Detected (GRD) format, Interferometric wide swath mode, VV and VH polarisation, 20x22 m resolution, 10x10 m pixel spacing.
  - Ground control points collected during field visits.
  - Data downloaded from Alaska Satellite Facility (ASF) portal.

- Pre-processing workflow (completed in SNAP)
  - Apply orbit file to update metadata with accurate orbital state vectors.
  - Thermal noise removal to reduce noise floor and improve continuity between sub-swaths.
  - Calibration to compute backscatter intensity.
  - Speckle filtering (refined Lee filter) to reduce grainy noise.
  - If multiple scenes, mosaic and subset to study area.
  - Outputs are pre-processed SAR images ready for analysis.

- Water-body extraction methodology
  - Water bodies extracted from pre-processed SAR using thresholding on backscatter values (water appears darker).
  - Thresholds determined manually per study area and month after inspecting histograms; thresholds are site/date specific (Table 1).
  - Bi-modal/histogram characteristics vary with land/water composition and seasons.
  - For each month/site, pixels with backscatter below threshold classified as water (1), otherwise non-water (0).

- Threshold handling and monsoon adjustment
  - Thresholds were largely similar across months, with notable changes during the monsoon when water bodies increase and thresholds drop.
  - A common average threshold was applied to all months except monsoon months (Table 2 shows region-specific averages and variability).

- Monthly water-body mapping and combination
  - Water pixels from multiple images (when available) are combined using an OR approach to produce a monthly water-body map named “S1A”.

- Ground Control Points (GCPs)
  - Ground-reference points collected in Aug 2018, Dec 2017, and Nov 2018 for Shivamogga, Sindhudurg, and Wayanad via Open Data Kit (ODK).

- Region-focused context (Shivamogga, Sindhudurg, Wayanad)
  - Each region has defined spatial extents (CRS-WGS84) and is accompanied by detailed lists of Sentinel-1A raw data acquisitions (dates and image IDs) used to derive water maps for 2017 and 2018, as documented in Tables 3–8.
  - No data were available for certain months in some years; gaps are noted in the acquisition tables.

- Documentation and references
  - Results and methodology are contextualized with references on thermal-noise removal, flood monitoring using SAR data, and accuracy assessment best practices (Park et al., 2018; DeVries et al., 2020; Stehman & Foody, 2019).

---

# 1.2 Region-specific data and acquisition details

- Shivamogga
  - Extensive list of 2017 and 2018 S1A IW_GRDH acquisitions across multiple dates (Tables 3 and 4).
  - Ground truth points collected August 2018.

- Sindhudurg
  - Comprehensive 2017 acquisitions (Table 5) and 2018 acquisitions (Table 6) spanning multiple months; ground truth data collected November 2018.

- Wayanad
  - 2017 acquisitions detailed in Table 7 and 2018 acquisitions in Table 8; ground truth data collection aligned with field validation efforts.

- Note on data coverage
  - Some months lack data in certain regions (e.g., no data in some months of 2017/2018 for specific regions); this influenced monthly mapping decisions and threshold application.

---

# 1.3 Accuracy assessment

- Reference data and ground truth
  - A total of 3,202 reference points used: 890 Shivamogga, 705 Sindhudurg, 1,606 Wayanad.
  - Water references included lakes, rivers, ponds, reservoirs, streams, and flood-affected fields; non-water references included built-up, forest, grassland, plantation, fallow land, and agricultural land.
  - Cloud-affected points identified by JRC quality tags were masked (affecting Shivamogga data).

- Accuracy metrics and evaluation approach
  - Overall accuracy and error metrics computed via a monthly surface-water area confusion matrix following Stehman & Foody (2019).
  - Metrics reported: overall accuracy, producer (omission) accuracy, user (commission) accuracy, and standard errors.
  - Separate matrices evaluated for S1A and JRC water maps; post-cloud masking adjustments applied where applicable.

- Key results by region and month
  - Shivamogga (August 2018)
    - Overall accuracy: 98.64% (SE 0.34%)
    - Not-water class: high producer accuracy around 99.19% (SE 0.21%), user accuracy ~99.32% (SE 0.30%)
    - Water class: producer ~92.46% (SE 3.11%), user ~91.16% (SE 2.35%)
  - Sindhudurg (December 2017)
    - Overall accuracy: 99.02% (SE 0.08%)
    - Not-water class: producer ~100% (SE 0%), user ~100% (SE 0%)
    - Water class: producer ~79.96% (SE 9.25%), user ~70.15% (SE 0.0%)
  - Wayanad (November 2018)
    - Overall accuracy: 99.84% (SE 0.11%)
    - Not-water class: producer ~100% (SE 0%), user ~99.81% (SE 0.11%)
    - Water class: producer ~79.96% (noted with SE 9.25% in table; user 100% in this map)
- Overall takeaway
  - The monthly water maps demonstrate high overall accuracy (generally >99% in Not-water, and strong performance for water delineation with acceptable user/producer trade-offs), with some variability in water-class accuracy driven by limited water-reference points and monsoon-season dynamics.
- Methodological rigor
  - Accuracy assessment integrated field-based ground-truth data, cloud-masking considerations, and standard errors to quantify reliability.
  - Threshold-based water mapping complemented by region-specific calibration and monsoon adjustments to improve consistency across months.
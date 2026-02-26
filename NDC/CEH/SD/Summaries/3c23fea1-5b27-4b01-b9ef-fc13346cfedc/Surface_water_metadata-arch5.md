# 1.1 Satellite imagery and Pre-processing

- Purpose and data scope
  - Study uses Sentinel-1A (SAR) data to map surface water bodies and pre-process them for analysis.
  - Data sources: Sentinel 1A raw data downloaded from Alaska Satellite Facility (ASF) in Level 1 Ground Range Detected (GRD) format.
  - Sensor specifics: C-Band SAR, VV and VH polarizations, two viewing angles, ground-range projection, 20x22 m resolution with 10x10 m pixel spacing.
  - Study areas include Shivamogga, Sindhudurg, and Wayanad in India; ground control points collected for validation.

- Pre-processing workflow (SNAP)
  - Apply orbit file to update meta data with accurate satellite position/velocity.
  - Thermal noise removal to reduce background energy and improve continuity across sub-swaths.
  - Calibration to convert to backscatter intensity using sensor parameters in GRD metadata.
  - Speckle filtering (refined Lee filter) to reduce grainy noise.
  - Slice assembly and mosaicking across multiple scenes; subset to study area.
  - Water extraction performed on pre-processed data using a thresholding approach on backscatter values.

- Water-body extraction approach
  - Water bodies identified as dark features with low backscatter; thresholds are determined manually via trial-and-error per study area and month.
  - Histogram analysis (bi-modal or uni-modal) guides threshold selection for each area and month.
  - Threshold values are listed per site/date (Table 1). Values below threshold classified as water; above threshold as non-water.
  - Seasonal variation: thresholds are generally similar across months, but monsoon months show increased water presence and lower thresholds; a common average threshold is applied for all non-monsoon months (Table 2).
  - Monthly water maps are produced by combining water pixels from all images (a pixel is water if identified as water in any image); the resulting product is referred to as S1A water body map.

- Ground truth and accuracy assessment data
  - Ground Control Points (GCPs) collected in August 2018 (Shivamogga), December 2017 (Sindhudurg), and November 2018 (Wayanad) using Open Data Kit (ODK).
  - GCPs used to inform accuracy assessment and validation of water/not-water classification.

- Regional study details (Shivamogga, Sindhudurg, Wayanad)
  - Shivamogga: spatial extent defined in WGS84; multiple Sentinel-1A raw data entries used across 2017 and 2018 for water-body extraction (Tables 3–4).
  - Sindhudurg: spatial extent defined in WGS84; multiple Sentinel-1A raw data entries used across 2017 and 2018 (Tables 5–6).
  - Wayanad: spatial extent defined in WGS84; multiple Sentinel-1A raw data entries used across 2017 and 2018 (Tables 7–8).

- Accuracy assessment methodology
  - A total of 3,202 reference points (890 Shivamogga, 705 Sindhudurg, 1,606 Wayanad) covering water and non-water classes.
  - Reference data include water features (lakes, rivers, ponds, reservoirs, streams, inundated fields) and non-water classes (built-up, forest, grassland, agriculture, etc.).
  - Accuracy metrics reported via confusion matrices based on monthly surface water maps aligned with field survey months.
  - Cloud-covered points in JRC maps are masked where applicable.

- Reported accuracy results (select highlights)
  - Shivamogga water map (August 2018): overall accuracy ~98.64% (SE ≈ 0.34%). Not-water producer accuracy ~99.19% (with very high user accuracy ~99.32%), water user accuracy ~91.16% with variable values for water producer accuracy (~92–99% range in the table).
  - Sindhudurg water map (December 2017): overall accuracy ~99.02% (SE ≈ 0.08%). Not-water producer accuracy ~99.58%, water producer accuracy ~100% in the reported figures; water user accuracy ~70.15% (reflecting lower accuracy in water class).
  - Wayanad water map (November 2018): overall accuracy ~99.84% (SE ≈ 0.11%). Water user accuracy at 100% with some wide confidence intervals for producer accuracy (≈79.96% with large SE ≈ 9.25%); non-water accuracy near 99.81%.
  - Across regions, overall accuracies are consistently high (roughly 99%), with some variability in the ability to correctly classify water pixels (water producer/user accuracies vary).

- Data product and governance implications
  - Primary data product: monthly S1A water body maps for the studied regions, created via threshold-based water-body extraction on pre-processed Sentinel-1A GRD data.
  - Documentation includes explicit threshold values by region/date (Table 1) and region/month average thresholds (Table 2), enabling reproducibility and auditing.
  - Data provenance includes source data (ASF Sentinel-1A GRD), processing steps (orbit, noise removal, calibration, speckle filtering, mosaicking), and the water-class thresholding method.
  - Cloud/quality considerations: field-validation points were partially masked where cloud-affected per JRC quality tags; data gaps exist in some months (no data for certain periods).
  - Ground truth and validation: GCPs provide a critical reference layer for assessing accuracy; the study uses a documented methodology for error assessment (Stehman & Foody 2019) and reports standard errors for accuracy estimates.

- References and methodological grounding
  - Park et al. (2018) on thermal noise removal for Sentinel-1 TOPSAR cross-polarization.
  - DeVries et al. (2020) on flood monitoring using Sentinel-1 and Landsat.
  - Stehman & Foody (2019) on accuracy assessment in land-cover products.

- Key governance takeaways for Data Stewards
  - Maintain detailed metadata on data sources (ASF, Sentinel-1A), processing chain (SNAP steps, parameters), and thresholding logic (region/date, monsoon adjustments).
  - Preserve reproducibility by documenting software versions, orbit files, calibration settings, and filtering choices.
  - Ensure quality assurance with ground-truth data (GCPs) and transparent accuracy reporting (confusion matrices, SE).
  - Track data availability and gaps (months with missing data) to support discovery and reuse.
  - Provide clear data products (monthly water maps) with provenance, thresholds, and validation results to enable reuse by data users and other systems.

- Data subject to limitations
  - Threshold-based water delineation may require region- and season-specific tuning; monsoon months show notable threshold shifts.
  - Some regions exhibit lower water-class accuracy (e.g., Sindhudurg water user accuracy ~70%), necessitating caution in water extent interpretation for those months.
  - Data gaps during certain months limit continuous temporal analysis.

- Conclusion for Data Stewards
  - The study demonstrates a transparent, threshold-driven workflow for deriving water-body maps from Sentinel-1A SAR data with extensive documentation of processing steps, thresholds, validation data, and accuracy outcomes.
  - The approach emphasizes reproducibility, metadata richness, and robust quality assessment—core principles for governance, storage, sharing, and reuse of similar dataset collections.
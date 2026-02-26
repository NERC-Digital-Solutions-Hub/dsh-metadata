# Water bodies mapping using Sentinel-1A SAR data: Methods, thresholds, ground control points, and accuracy assessment for Shivamogga, Sindhudurg and Wayanad

- Purpose and scope
  - Develop monthly water body maps (S1A) for three study regions (Shivamogga, Sindhudurg, Wayanad) using Sentinel-1A SAR data to monitor surface water dynamics.
  - Assess accuracy against field-collected ground truth to inform monitoring decisions.

- Data and pre-processing
  - Data sources
    - Sentinel-1A, Level-1 Ground Range Detected (GRD) Interferometric Wide Swath (IW) mode, C-Band, VV and VH polarization; resolution 20x22 m, pixel spacing 10x10 m.
    - Raw data downloaded from Alaska Satellite Facility.
  - Pre-processing workflow (via SNAP)
    - Apply orbit file for accurate geometry.
    - Remove thermal noise to reduce noise floor.
    - Radiometric calibration to backscatter intensity (sigma0).
    - Speckle filtering (refined Lee filter) to reduce graininess.
    - Slice assembly and mosaicking if scenes span multiple acquisitions; subset to study area.
  - Water body extraction
    - Water vs non-water classified by thresholding backscatter values (lower backscatter indicates water).
    - Thresholds defined per region and per month; thresholds adjusted manually through histogram analysis; thresholds summarized in monthly/site tables.
    - For months with consistent land/water mix, a common average threshold used; monsoon months use month-specific thresholds due to seasonal changes in water extent.
  - Output
    - Monthly water maps per region (S1A maps) produced by combining water detections from multiple images within a month.

- Thresholds and regional specifics
  - Thresholding approach
    - Thresholds applied to backscatter values; values < threshold classified as water (1); values ≥ threshold classified as not water (0).
  - Monsoon adjustments
    - Monsoon months show larger water extent; thresholds adapted to reflect these changes; when stable, a common average threshold applied.
  - Example region-specific averages (years 2017 and 2018)
    - Shivamogga: approximately -17.5 to -17.0 with regional standard deviations around 0.38–0.80.
    - Sindhudurg: approximately -17.4 to -17.9 with regional standard deviations around 0.65–0.68.
    - Wayanad: approximately -17.7 to -18.0 with regional standard deviations around 0.72–1.21.
  - Thresholds and data quality
    - Table-based thresholds show similar values across months, with notable decreases during monsoon months.
    - Table 2 reports the average thresholds and standard deviations used for non-monsoon months per region.

- Ground truth data and study sites
  - Ground control points (GCPs)
    - Collected to validate water vs not-water classes using Open Data Kit (ODK) in Aug 2018 (Shivamogga), Dec 2017 (Sindhudurg), and Nov 2018 (Wayanad).
  - Regional extents
    - Shivamogga, Sindhudurg, and Wayanad each have clearly defined spatial extents in WGS84.
  - Reference classes for validation
    - Water references include lakes, rivers, ponds, reservoirs, streams, and inundated fields.
    - Non-water references include built-up areas, forest, grassland, plantation, fallow and agricultural land.

- Accuracy assessment
  - Reference data and methods
    - 3,202 reference points in total: Shivamogga (890), Sindhudurg (705), Wayanad (1,606).
    - Validation using a monthly, area-based confusion matrix following Stehman and Foody (2019) with standard errors.
    - Cloud-contaminated reference points were masked (e.g., 859 Shivamogga points removed in August 2018 due to cloud).
  - Key accuracy metrics
    - Shivamogga water map (August 2018): overall accuracy 98.64% (SE 0.34%); Not water producer accuracy ~99.19% (SE 0.21%); Water producer accuracy ~92.46% (SE 3.11%); Not water user accuracy ~99.32% (SE 0.30%); Water user accuracy ~91.16% (SE 2.35%).
    - Sindhudurg water map (December 2017): overall accuracy 99.02% (SE 0.08%); Not water user accuracy 100% (SE 0); Water user accuracy ~70.15% (SE 0.00%); Not water producer accuracy ~99.58% (SE 0.08%); Water producer accuracy ~99.0% (SE not shown).
    - Wayanad water map (November 2018): overall accuracy 99.84% (SE 0.11%); Not water user accuracy ~99.81% (SE 0.11%); Water user accuracy 100% (SE 0); Not water producer accuracy ~100% (SE 0); Water producer accuracy ~79.96% (SE 9.25%).
  - Implications of accuracy results
    - High overall accuracies (>98%) across all regions indicate robust mapping of water bodies at monthly scales.
    - Not-water class generally exhibits very high producer accuracy; water class producer accuracy varies (notably lower in Sindhudurg and Wayanad), reflecting challenges in detecting smaller or highly dynamic water features.
    - Cloud coverage can reduce reference sample size and affect validation.

- Data governance, openness, and practical considerations
  - Data and reproducibility
    - Thresholds, acquisition dates, and reference data are documented ( Tables 1–8; thresholds by region and month).
    - Ground truth points and methodology enable replication, though full public sharing of all raw SAR data and processed outputs is subject to data-source restrictions.
  - Data gaps and data management
    - Some months lack data in certain regions; data gaps influence monitoring cadence and completeness.
    - Seasonal variability (monsoon) necessitates adaptive thresholding and potentially multiple-image aggregation to ensure reliable mapping.
  - Implications for monitoring frameworks
    - Demonstrates an end-to-end workflow from data acquisition and processing to monthly waterbody mapping and accuracy assessment.
    - Highlights the need for region-specific calibration, seasonality considerations, and transparent reporting of thresholds and validation results.
    - Emphasizes the importance of ground truth to assess performance and build trust in monitoring outputs for policy evaluation and decision-making.
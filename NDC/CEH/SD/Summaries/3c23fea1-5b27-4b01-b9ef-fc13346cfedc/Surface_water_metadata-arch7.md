# 1.1 Satellite imagery and Pre-processing

- Objective and scope
  - Describe the preprocessing and analysis workflow to derive monthly water body maps from Sentinel-1A SAR data for three study regions, with ground-truth validation.
  - Map production (S1A) combines water detections from two images per month to produce a monthly water extent.

- Data sources and characteristics
  - Sentinel-1A SAR (C-Band) in Interferometric Wide Swath mode, Level-1 GRD, VV and VH polarizations.
  - Spatial resolution: 20x22 m, pixel spacing 10x10 m; multiple viewing angles; projected to ground range.
  - Acquisition facility: Alaska Satellite Facility (ASF) data portal.

- Pre-processing workflow (using SNAP)
  - Apply orbit file to update state vectors for accurate position/velocity.
  - Thermal noise removal to reduce backscatter floor and inter-slice discontinuities.
  - Calibration to compute backscatter intensity from GRD metadata.
  - Speckle filtering (refined Lee) to reduce grainy noise.
  - If needed, mosaic two scenes and subset to study extent.

- Water body extraction method
  - Water bodies extracted by applying a backscatter threshold to pre-processed data.
  - Thresholds are site- and month-specific (Table 1). Values are chosen manually per study area and month.
  - Thresholds reflect water generally having low backscatter in SAR imagery.
  - Monsoon months show substantial changes in water extent; average thresholds are applied to all non-monsoon months (Table 2).

- Thresholds and thresholds handling
  - Site- and month-specific values provided (e.g., Shivamogga, Sindhudurg, Wayanad across multiple months/years).
  - Common average thresholds applied outside monsoon months to maintain consistency (with standard deviations reported).

- Monthly water map production (S1A)
  - Water pixel = 1 if identified as water in either of the two images for the month; otherwise 0.
  - Resulting monthly water map is referred to as S1A.

- Ground control points (GCPs)
  - Water and non-water reference points collected in August 2018, December 2017, and November 2018 for Shivamogga, Sindhudurg, and Wayanad using Open Data Kit (ODK).

- 1.2 Data: Region-specific details

  - 1.2.1 Shivamogga
    - Spatial extent defined in CRS-WGS84 with precise corner coordinates.
    - Sentinel-1A raw data used for 2017 and 2018 (long lists of acquisition dates) to extract water bodies.
    - Data availability notes include months with multiple scenes and months with no data.

  - 1.2.2 Sindhudurg
    - Spatial extent defined in CRS-WGS84 with precise corner coordinates.
    - Comprehensive lists of 2017 and 2018 Sentinel-1A acquisitions used for water extraction.
    - Some months have no data (explicitly documented).

  - 1.2.3 Wayanad
    - Spatial extent defined in CRS-WGS84 with precise corner coordinates.
    - Extensive lists of 2017 and 2018 Sentinel-1A acquisitions used for water extraction.
    - Some months have no data (explicitly documented).

- 1.3 Accuracy assessment

  - Reference data and points
    - Total of 3,202 ground reference points: 890 Shivamogga, 705 Sindhudurg, 1,606 Wayanad.
    - Water reference points include lakes, rivers, ponds, reservoirs, streams, and inundated agricultural fields.
    - Non-water reference points include built-up areas, forest, grassland, plantations, fallow land, and agriculture.

  - Validation approach
    - Accuracy assessed using a monthly surface water area map confusion matrix (per Stehman & Foody, 2019) matching field survey months.
    - Metrics computed: overall accuracy, producer’s accuracy ( omission error ), and user’s accuracy ( commission error ), with standard errors.
    - Cloud-covered points from the JRC map were masked out where applicable (Shivamogga: 859 points removed; Sindhudurg and Wayanad: none removed).

  - Regional accuracy highlights
    - Shivamogga (August 2018): overall accuracy 98.64% (SE 0.34%).
    - Sindhudurg (December 2017): overall accuracy 99.02% (SE 0.08%); producer and user accuracies reported with high reliability.
    - Wayanad (November 2018): overall accuracy 99.84% (SE 0.11%); very high producer and user accuracies.

  - Notes on data limitations
    - Cloud masking reduces available reference points (notably Shivamogga).
    - Some months have missing SAR data, affecting temporal completeness in certain regions.

- Key references for methods
  - Park, Korosov, Babiker, Sandven, & Won (2018) on efficient thermal noise removal for Sentinel-1 TOPSAR.
  - DeVries et al. (2020) on flood monitoring using Sentinel-1 and Landsat.
  - Stehman & Foody (2019) on accuracy assessment of land cover products.

- Summary of significance for GIS specialists
  - Provides a replicable workflow for producing monthly water body maps from Sentinel-1A SAR with region-specific thresholds.
  - Demonstrates integration of multi-date SAR imagery, threshold-based classification, and cross-image synthesis to enhance water detection.
  - Validates results with substantial ground truth points and reports high accuracy across three study regions, acknowledging monsoon dynamics and data gaps.
# Satellite imagery and Pre-processing

- Objective: Map surface water bodies using Sentinel-1A SAR data (VV and VH, C-Band) to produce monthly water maps for Shivamogga, Sindhudurg, and Wayanad; assess accuracy against ground truth.
- Data and area:
  - Sentinel-1A Level 1 Ground Range Detected (GRD) data, Interferometric Wide Swath, 20x22 m resolution (10x10 m pixel spacing), VV and VH polarisation.
  - Ground control points collected during field visits.
  - Raw data downloaded from Alaska Satellite Facility.

- Pre-processing workflow (via SNAP):
  - Apply orbit file to update metadata with accurate position/velocity.
  - Thermal noise removal to reduce background energy and inter-swatch discontinuities.
  - Calibration to compute backscatter intensity.
  - Speckle filtering with refined Lee filter.
  - Slice assembly and mosaic of scenes; subset cropping to study area.

- Water body extraction approach:
  - Water bodies extracted from pre-processed SAR data using thresholding (threshold per study area and per month; Table 1 lists values).
  - Thresholds: water classified where backscatter is below threshold; values provided for multiple study areas and months.
  - Seasonal adjustment: thresholds largely similar across most months; during monsoon months water area increases and thresholds decrease substantially. A common average threshold was applied to all non-monsoon months (Table 2).
  - Monthly water maps: for each month, pixels identified as water in either image are combined to produce a monthly water map referred to as S1A.

- Ground Control Points (GCPs):
  - Water/not-water reference points collected Aug 2018 (Shivamogga), Dec 2017 (Sindhudurg), and Nov 2018 (Wayanad) using Open Data Kit.

- Regional acquisition details (selected highlights):
  - Shivamogga: spatial extents in WGS84; multiple 2017 and 2018 S1A acquisitions listed in Tables 3 and 4.
  - Sindhudurg: spatial extents in WGS84; acquisitions listed in Tables 5 and 6.
  - Wayanad: spatial extents in WGS84; acquisitions listed in Tables 7 and 8.
  - Note: Tables provide dense lists of raw data IDs and dates used for water body extraction.

- Accuracy assessment:
  - Ground reference: 3,202 points total (Shivamogga 890, Sindhudurg 705, Wayanad 1,606); includes water and non-water classes (lakes, rivers, ponds, reservoirs, inundated fields vs. built-up, forest, etc.).
  - Method: monthly surface water maps evaluated using a percentage-area based confusion matrix per Stehman & Foody (2019); cloud-affected points masked according to JRC quality tag where applicable.
  - Results:
    - Shivamogga, August 2018: overall accuracy 98.64% (SE 0.34%). Not-water user 99.32% (SE 0.30); Not-water producer 99.19% (SE 0.21). Water user 91.16% (SE 2.35); Water producer 92.46% (SE 3.11).
    - Sindhudurg, December 2017: overall accuracy 99.58% (SE 0.08%). Not-water user 100% (SE 0); Water user 70.15% (SE 0.??); Water producer 100% (SE 0).
    - Wayanad, November 2018: overall accuracy 99.84% (SE 0.11%). Not-water user 99.81% (SE 0.11); Not-water producer ~100% (SE 0); Water user 100% (SE 0); Water producer ~79.96% (SE 9.25).
  - Summary: Overall accuracies are very high across regions, with high performance for the Not-water class and strong, though sometimes lower, performance for the Water class depending on region and month.

- Key takeaways for data-focused analysts:
  - A SAR-based water mapping workflow can achieve very high overall accuracy (≥98.6%) with careful pre-processing and threshold tuning.
  - Thresholds may need seasonal adjustment, particularly during monsoons when water extent increases.
  - Combining multiple images per month (logical OR) helps to create robust monthly water maps.
  - Ground truth collection via open data kits and cloud-masked reference points is essential for credible accuracy assessment.
  - Documentation and reproducibility are supported by explicit data sources, acquisition lists, and referenced accuracy methodology.

- References:
  - Park, J. W., Korosov, A. A., et al. Efficient Thermal Noise Removal for Sentinel-1 TOPSAR Cross-Polarization Channel. IEEE TGRS. 2018.
  - DeVries, B., Huang, C., et al. Rapid and robust monitoring of flood events using Sentinel-1 and Landsat data on Google Earth Engine. Remote Sensing of Environment. 2020.
  - Stehman, S. V., & Foody, G. M. Key issues in rigorous accuracy assessment of land cover products. Remote Sensing of Environment. 2019.
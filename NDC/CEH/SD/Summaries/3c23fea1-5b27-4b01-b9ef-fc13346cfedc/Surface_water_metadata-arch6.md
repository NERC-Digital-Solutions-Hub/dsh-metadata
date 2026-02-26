# 1.1 Satellite imagery and Pre-processing

## Overview
- Describes acquisition, preprocessing, water-body extraction, ground control validation, and accuracy assessment for Sentinel-1A data across three regions (Shivamogga, Sindhudurg, Wayanad).

## Data and Study Area
- Data: Sentinel-1A Ground Range Detected (GRD), C-Band, VV and VH polarisation, Interferometric Wide Swath mode, 20x22 m resolution (10x10 m pixel spacing).
- Pre-processing platform: Sentinel Application Platform (SNAP).
- Ground control points collected in Aug 2018, Dec 2017, and Nov 2018.
- Regions and extents (WGS84 CRS):
  - Shivamogga
  - Sindhudurg
  - Wayanad

## Data Acquisition and Pre-processing
- Data sources: Sentinel-1A raw data downloaded from Alaska Satellite Facility.
- Pre-processing steps: apply orbit file, thermal noise removal, calibration, speckle filtering (refined Lee), slice assembly (mosaic if multiple scenes), and subset/cropping.
- Water body extraction: binary classification by thresholding calibrated backscatter; thresholds are site- and month-specific (Table 1), with thresholds derived from backscatter histograms (water appears darker).
- Monsoon adjustments: thresholds were largely similar across years, but monsoon months required different thresholds; a common average threshold was applied to all non-monsoon months (Table 2).

## Water Body Extraction Details
- Pixel value scheme: water = 1, not water = 0.
- Thresholds table (Table 1) lists region-specific and date-specific backscatter thresholds; averages and standard deviations (Table 2) summarize non-monsoon thresholds by region/year.
- Monthly water-body maps are produced by fusing pixels identified as water in either of the images (referred to as S1A maps).

## Ground Control Points
- Reference points for validation: water vs. not-water classes (lakes, rivers, ponds, reservoirs, inundated fields vs. built-up, forest, grassland, agriculture).
- Cloud-affected reference points removed using JRC quality tags (e.g., Shivamogga: 859 points removed; Sindhudurg and Wayanad had none removed).

## Region-Specific Data (Shivamogga, Sindhudurg, Wayanad)
- Shivamogga: spatial extent provided; extensive lists of 2017 and 2018 S1A acquisitions used to extract water bodies; data gaps noted (no data in November 2017).
- Sindhudurg: spatial extent provided; comprehensive 2017 and 2018 acquisition lists; data gaps noted (e.g., 2018 months with no data in certain periods).
- Wayanad: spatial extent provided; comprehensive 2017 and 2018 acquisition lists; data gaps noted (e.g., months with no data in 2018).

## Accuracy Assessment
- Validation used 3,202 reference points: Shivamogga (890), Sindhudurg (705), Wayanad (1,606).
- Reference points included various water and non-water classes; cloud-masked where applicable.
- Method: monthly surface-water maps evaluated with a percentage-area confusion matrix following Stehman and Foody (2019); metrics reported: overall accuracy, producer (omission) accuracy, and user (commission) accuracy with standard errors.

## Results by Region (Accuracy)
- Shivamogga water-body map (August 2018)
  - Overall accuracy: 98.64% (SE 0.34%)
  - Not water: high producer and user accuracies (Not water producer ~99.19%; Not water user ~99.32%)
  - Water class: user accuracy ~91.16%; producer accuracy not shown clearly in excerpt
- Sindhudurg water-body map (December 2017)
  - Overall accuracy: 99.58% (SE 0.08%)
  - Not water: producer ~100%; user ~100%
  - Water: producer ~70.15%; user ~70.15% (indicating more misclassifications for water)
- Wayanad water-body map (November 2018)
  - Overall accuracy: 99.84% (SE 0.11%)
  - Not water: user ~99.81%; producer ~100%
  - Water: user 100%; producer ~79.96% (high uncertainty with fewer water reference points)

## Notes and References
- Threshold consistency: most months had similar thresholds across regions/years; monsoon months required adjusted thresholds.
- References for methods and validation:
  - Park, J. W., Korosov, A. A., et al. (2018). Efficient Thermal Noise Removal for Sentinel-1 TOPSAR Cross-Polarization Channel.
  - DeVries, B., Huang, C., et al. (2020). Flood monitoring using Sentinel-1 and Landsat data.
  - Stehman, S. V., & Foody, G. M. (2019). Accuracy assessment in land cover products.
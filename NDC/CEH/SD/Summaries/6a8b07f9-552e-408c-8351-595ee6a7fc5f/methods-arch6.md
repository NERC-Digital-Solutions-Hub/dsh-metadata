# Biomass maps of Mabalane, Gurue, and Maruppa, Mozambique

## Overview
- Dataset representing aboveground woody biomass (tC/ha) for three Mozambican study areas: Mabalane, Gurue, and Maruppa.
- Each dataset consists of three GeoTIFF layers corresponding to years: 2007, 2010, and 2014.
- Each pixel value is biomass in tonnes of carbon per hectare; no-data value is -18.00000. Negative values may occur due to noise.
- Individual layers can be extracted for year-specific analyses.

## Data structure
- Three stacked GeoTIFF layers per dataset:
  - Band 1: 2007
  - Band 2: 2010
  - Band 3: 2014
- Biomass layer values converted to carbon density (tC/ha) using Ryan et al. 2012 equation; note this calibration is based on central/northern Mozambique and not locally validated.

## Methods and quality control
- Method follows Ryan et al. 2012 and 2014; updated to handle PALSAR 2 data.
- Data derived from three ALOS PALSAR HV scenes per year (2007, 2010, 2014).
- Processing steps:
  - Calibration, terrain correction, and despeckling (3x3 GammaMAP) in SNAP v2.0; output at 15 m pixel size.
  - Each scene georeferenced to a mosaicked, pansharpened Landsat 8 image (Sept 2014) using ENVI v4.8.
  - Georeferencing based on manually selected tie points distributed around each image.
- Accuracy: Table 1 reports RMS errors and tie-point counts for each scene (2014, 2010, 2007) with respective acquisition dates and image IDs.
- Acknowledgment for data sources: JAXA provided ALOS PALSAR data via the 4th Research Agreement; ESA also provided ALOS data.
- Recommendations:
  - Mask out flooded/wet areas and urban areas where biomass estimates are less reliable.
  - Consider increasing pixel size (e.g., 30–60 m) to reduce noise.
  - Validate biomass estimates against plot data to assess map accuracy.

## Data quality and caveats
- Biomass estimates may be unreliable in flooded/wet environments and urban regions.
- Local calibration is recommended to improve accuracy; the current tC/ha values are not locally validated.
- Coregistration effectiveness is limited; georeferencing prior to mosaicking is important, and ALOS-2 generally offers better localization than ALOS-1.

## Usage and attribution
- Outputs should be acknowledged with data providers:
  - JAXA and ESA for ALOS PALSAR imagery.
  - ESPA acknowledgment separately.
- For best results, users should:
  - Extract year-specific layers for analysis.
  - Mask unreliable zones (flooded, urban).
  - Validate against local plot data where possible.

## References
- Ryan, C. M., et al. (2012). Quantifying small-scale deforestation and forest degradation in African woodlands using radar imagery.
- Ryan, C. M., Berry, N. J., & Joshi, N. (2014). Quantifying the causes of deforestation and degradation and creating transparent REDD+ baselines: A method and case study from central Mozambique.
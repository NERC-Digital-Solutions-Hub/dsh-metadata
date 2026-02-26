# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland extent, peat thickness, and peatland carbon storage for the Lowland Peruvian Amazon.
- Published by Hastie, A. et al. (2022) in Nature Geoscience: Risks to carbon storage from land-use change revealed by peat thickness maps of Peru.

## Datasets and file contents
- Eight GeoTIFF rasters (WGS84, EPSG:4326) representing different peatland and land cover properties:
  - CSAP_5.1_Landcover_LPA_50m.tif: Predicted land cover class (Band 1) with coded values:
    - -9999: no prediction (outside study area)
    - 0: Pole forest
    - 1: Open savanna-like peatland
    - 2: Palm swamp
    - 3: Open water
    - 4: Seasonally flooded forest
    - 5: Terra firme forest
    - 6: Urban areas/river beaches
    - 7: White-sand forest
  - CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif: Peat carbon storage in Mt ha-1 (5th percentile)
  - CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif: Peat carbon storage in Mt ha-1 (95th percentile)
  - CSAP_5.4_Peat_carbon_LPA_100m.tif: Peat carbon storage in Mt ha-1 (median)
  - CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif: Peat thickness in cm (5th percentile)
  - CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif: Peat thickness in cm (95th percentile)
  - CSAP_5.7_Peat_thickness_median_LPA_100m.tif: Peat thickness in cm (median)
  - CSAP_5.8_Peatland_Extent_LPA_50m.tif: Peatland presence (1 = present)

## Methods and data sources
- Training and validation: 1,128 ground reference points for vegetation type, peat presence/absence, and peat thickness (where applicable) were split 50/50 for model development and validation.
- Input layers: stack of seven remote sensing layers including two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM DEM, and a previous land-cover map.
- Outputs: predictive models for land cover, peatland extent, peat thickness, and peat carbon storage, with peat carbon informed by laboratory peat measurements.
- Quality control: 5% and 95% confidence intervals calculated; datasets peer-reviewed.

## Data format and coordinate reference system
- Format: GeoTIFF rasters
- CRS: WGS84, unprojected (EPSG:4326)

## Geographical scope and location
- Extent: longitudes -77.78 to -66.07; latitudes -14.67 to -0.04
- Area of study: Lowland Peruvian Amazon

## Provenance and documentation
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com)
- Project/funding: UKRI-NERC grant NE/R000751/1; Principal Investigator Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Source publication: Hastie et al. 2022, Nature Geoscience (Risks to carbon storage from land-use change revealed by peat thickness maps of Peru)
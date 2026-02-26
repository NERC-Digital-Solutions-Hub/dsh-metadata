# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland extent, peat thickness, and peatland carbon storage for the Lowland Peruvian Amazon (LPA).
- Published by Hastie, A. et al. (2022) in Nature Geoscience: Risks to carbon storage from land-use change revealed by peat thickness maps of Peru.
- Data designed to support assessment of carbon storage risk due to land-use change and to inform decision-making.

## Datasets included (filenames)
- CSAP_5.1_Landcover_LPA_50m.tif (predicted land cover)
- CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif (peat carbon, 5th percentile)
- CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif (peat carbon, 95th percentile)
- CSAP_5.4_Peat_carbon_LPA_100m.tif (peat carbon, median)
- CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif (peat thickness, 5th percentile)
- CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif (peat thickness, 95th percentile)
- CSAP_5.7_Peat_thickness_median_LPA_100m.tif (peat thickness, median)
- CSAP_5.8_Peatland_Extent_LPA_50m.tif (peatland presence/absence)

## Methods (collection and generation)
- Ground-reference dataset: 1,128 points of vegetation type, peat presence/absence, and peat thickness where available.
- Data split: 50% for training, 50% for validation.
- Predictors: stack of seven remote-sensing layers, including two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM elevation, and a prior land-cover map.
- Modeling aims: predict land cover, peatland extent, peat thickness, and, with laboratory peat data, peat carbon storage.
- Data and methods described in detail in the associated publication.

## Quality control
- Uncertainty estimates: 5% and 95% confidence intervals calculated using established methods.
- Peer-reviewed datasets.

## Data structure and format
- File type: GeoTIFF raster.
- Datum: WGS84 (EPSG:4326); unprojected coordinates.

## Variable details and units
- Landcover_LPA_50m.tif (Band 1): predicted land cover class
  - Codes: -9999 outside study area; 0 pole forest; 1 open savanna-like peatland; 2 palm swamp; 3 open water; 4 seasonally flooded forest; 5 terra firme forest; 6 urban areas/river beaches; 7 white-sand forest.
- Peat_carbon_5th_perc_LPA_100m.tif (Band 1): peat carbon storage in Mt ha-1 (5th percentile)
- Peat_carbon_95th_perc_LPA_100m.tif (Band 1): peat carbon storage in Mt ha-1 (95th percentile)
- Peat_carbon_LPA_100m.tif (Band 1): peat carbon storage in Mt ha-1 (median)
- Peat_thickness_5th_perc_LPA_100m.tif (Band 1): peat thickness in cm (5th percentile)
- Peat_thickness_95th_perc_LPA_100m.tif (Band 1): peat thickness in cm (95th percentile)
- Peat_thickness_median_LPA_100m.tif (Band 1): peat thickness in cm (median)
- Peatland_Extent_LPA_50m.tif (Band 1): 1 indicates presence of peat

## Geographic scope
- Spatial extent: longitude -77.78 to -66.07 degrees; latitude -14.67 to -0.04 degrees.

## Authors, contact, and funding
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com)
- Project and funding: UKRI-NERC, grant NE/R000751/1; Principal Investigator Dr Ian Lawson (itl2@st-andrews.ac.uk)
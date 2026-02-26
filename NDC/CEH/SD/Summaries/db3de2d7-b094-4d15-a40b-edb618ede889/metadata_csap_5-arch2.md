# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland extent, peat thickness, and peat carbon storage for the Lowland Peruvian Amazon (LPA).
- Published by Hastie, A. et al. (2022) in Nature Geoscience; aims to reveal risks to carbon storage from land-use change.
- Data designed to support monitoring of environmental health and policy performance over time.

## Data products (files and what they contain)
- CSAP_5.1_Landcover_LPA_50m.tif — predicted land cover class (band 1) with coded categories (e.g., Pole forest, Open savanna-like peatland, Palm swamp, Open water, etc.).
- CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif — peat carbon storage, 5th percentile (Mt ha^-1, band 1).
- CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif — peat carbon storage, 95th percentile (Mt ha^-1, band 1).
- CSAP_5.4_Peat_carbon_LPA_100m.tif — median peat carbon storage (Mt ha^-1, band 1).
- CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif — peat thickness, 5th percentile (cm, band 1).
- CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif — peat thickness, 95th percentile (cm, band 1).
- CSAP_5.7_Peat_thickness_median_LPA_100m.tif — median peat thickness (cm, band 1).
- CSAP_5.8_Peatland_Extent_LPA_50m.tif — presence of peat (1 = peat present, 0 elsewhere) (band 1).

## Methods and data inputs
- Ground reference points: 1,128 observations of vegetation type, peat presence/absence, and peat thickness used to train (50%) and validate (50%) predictive models.
- Input data: stack of seven remote-sensing layers, including two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM elevation, and a previous land-cover map.
- Ground-truth measurements of peat carbon used to inform carbon storage predictions.

## Quality control and validation
- Estimates of uncertainty via 5% and 95% confidence intervals (calculated with published methods).
- Datasets peer-reviewed prior to publication.

## Data structure and formats
- GeoTIFF rasters, WGS84 datum (EPSG:4326), unprojected coordinates.
- Geographic extent: roughly from -77.78 to -66.07 degrees longitude, and -14.67 to -0.04 degrees latitude.

## Content details (bands and units)
- Landcover: band 1 contains categorical class codes (-9999 outside study area; 0 Pole forest; 1 Open savanna-like peatland; 2 Palm swamp; 3 Open water; 4 Seasonally flooded forest; 5 Terra firme forest; 6 Urban areas/river beaches; 7 White-sand forest).
- Peat carbon: band 1 in Mt ha^-1 for 5th percentile, 95th percentile, and median.
- Peat thickness: band 1 in cm for 5th percentile, 95th percentile, and median.
- Peatland extent: band 1 with value 1 indicating peat presence.

## Geographic coverage
- Lowland Peruvian Amazonia (LPA).

## Access, authors, and funding
- Author/contact: Dr Adam Hastie (adamhastie@hotmail.com).
- Project and funding: UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson (itl2@st-andrews.ac.uk).
- Data generation and publication aligned with data-sharing practices and storage in appropriate data portals.
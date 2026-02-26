# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland presence, peat thickness, and peatland carbon storage for the Lowland Peruvian Amazon (LPA).
- Published by Hastie, A. et al. (2022) in Nature Geoscience: Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. DOI: https://doi.org/10.1038/s41561-022-00923-4.
- Ground-reference data: 1,128 points used to train (50%) and validate (50%) models, covering vegetation type, peat presence/absence, and peat thickness where applicable.
- Inputs: stack of seven remote-sensing layers (two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM DEM, and a previous land-cover map).

## Data products (files and resolutions)
- CSAP_5.1_LPA_50m.tif — Predicted land cover class (50 m resolution) with coded categories.
- CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif — Peat carbon storage, 5th percentile (Mt ha-1), 100 m resolution.
- CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif — Peat carbon storage, 95th percentile (Mt ha-1), 100 m resolution.
- CSAP_5.4_Peat_carbon_LPA_100m.tif — Peat carbon storage, median estimate (Mt ha-1), 100 m resolution.
- CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif — Peat thickness, 5th percentile (cm), 100 m resolution.
- CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif — Peat thickness, 95th percentile (cm), 100 m resolution.
- CSAP_5.7_Peat_thickness_median_LPA_100m.tif — Peat thickness, median (cm), 100 m resolution.
- CSAP_5.8_Peatland_Extent_LPA_50m.tif — Presence of peatland (1 = present), 50 m resolution.

## Methods and quality assurance
- Models trained and validated with 1,128 ground-reference points across vegetation type, peat presence/absence, and peat thickness.
- Validation approach used with 50/50 train/validate split; 5th and 95th percentile confidence intervals calculated using established methods.
- Outputs are peer-reviewed and published; data linked to a published Nature Geoscience article.

## Data structure and metadata
- File format: GeoTIFF raster.
- Datum/coordinate system: WGS84 (EPSG:4326), unprojected.
- Band 1 of each file contains the primary value (e.g., land cover class, carbon storage, or peat thickness) expressed in the specified units.

## Geographic coverage
- Extent in decimal degrees: longitude -77.78 to -66.07; latitude -14.67 to -0.04.
- Focused on the Lowland Peruvian Amazon region.

## Provenance, contact, and funding
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com).
- Project/funding: UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson (itl2@st-andrews.ac.uk).

## How to use and potential applications
- Data can support policy, land-use planning, conservation, and carbon storage risk assessments by providing:
  - Spatially explicit predictions of land-cover types.
  - Uncertainty ranges for peat carbon storage and peat thickness (5th/95th percentiles).
  - Maps of peatland extent to identify priority areas for protection or restoration.
- Outputs can be integrated with other datasets to create self-serve data products, dashboards, or reports for decision-making.
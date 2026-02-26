# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland extent, peat thickness, and peat carbon storage for the Lowland Peruvian Amazon (LPA).
- Published by Hastie, A. et al. (2022) in Nature Geoscience, accompanying the article on risks to carbon storage from land-use change.
- Data support understanding how peatlands respond to land-use changes and help quantify carbon storage dynamics in this region.

## Data products
- CSAP_5.1_Landcover_LPA_50m.tif — Predicted land cover class (5 m? note: 50 m resolution for landcover) with codes:
  - -9999: no prediction (outside study area)
  - 0: Pole forest
  - 1: Open savanna-like peatland
  - 2: Palm swamp
  - 3: Open water
  - 4: Seasonally flooded forest
  - 5: Terra firme forest
  - 6: Urban areas/river beaches
  - 7: White-sand forest
- CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif — Peat carbon storage (Mt ha-1) at 5th percentile.
- CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif — Peat carbon storage (Mt ha-1) at 95th percentile.
- CSAP_5.4_Peat_carbon_LPA_100m.tif — Peat carbon storage (Mt ha-1) median estimate.
- CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif — Peat thickness (cm) at 5th percentile.
- CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif — Peat thickness (cm) at 95th percentile.
- CSAP_5.7_Peat_thickness_median_LPA_100m.tif — Peat thickness (cm) median.
- CSAP_5.8_Peatland_Extent_LPA_50m.tif — Peatland presence (1 = peatland present).

## Methods and validation
- 1,128 ground reference points for vegetation type, peat presence/absence, and peat thickness (where applicable) used to train (50%) and validate (50%) predictive models.
- Models leveraged seven remote-sensing layers: two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM elevation, and a previous land-cover map; peat carbon estimates derived from laboratory peat measurements.
- Quality control included 5% and 95% confidence intervals calculated with established methods; datasets peer-reviewed.

## Data structure and access
- File format: GeoTIFF rasters.
- Datum: WGS84 (EPSG:4326); coordinates unprojected.
- Spatial resolution: Landcover at 50 m; peat carbon, thickness, and extent at 100 m (with some products at specific percentile/median estimates).

## Data content and interpretation
- Landcover (CSAP_5.1): Band 1 contains predicted land cover class codes as listed above.
- Peat carbon (CSAP_5.2–5.4): Band 1 provides peat carbon storage in megatonnes per hectare (Mt ha-1) for 5th percentile, 95th percentile, and median estimates.
- Peat thickness (CSAP_5.5–5.7): Band 1 provides predicted peat thickness in centimeters for 5th percentile, 95th percentile, and median.
- Peatland extent (CSAP_5.8): Band 1 uses a binary flag where 1 indicates presence of peat.
  
## Geography
- Study area extent roughly between longitudes -77.78 to -66.07 and latitudes -14.67 to -0.04.

## Author, project, and funding
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com).
- Project/funding: UKRI-NERC grant NE/R000751/1; Principal Investigator Dr Ian Lawson (itl2@st-andrews.ac.uk).

## Relevance for Data Leaders
- Demonstrates end-to-end data product development: data collection, model training/validation, multi-criteria predictive outputs, and explicit uncertainty (percentiles).
- Provides a clear data lineage and multi-resolution outputs that can be integrated into broader data ecosystems for policy analysis, planning, and conservation strategies.
- Highlights importance of metadata clarity, data provenance, and peer-reviewed quality for building trusted data assets.
- Offers a model for coordinating cross-disciplinary data (remote sensing, field measurements, genesis of carbon estimates) and encouraging shared data products across networks.
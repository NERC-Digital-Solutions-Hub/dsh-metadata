# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial datasets predicting land cover, peatland extent, peat thickness, and peat carbon storage for the Lowland Peruvian Amazon (LPA).
- Published by Hastie, A. et al. (2022) in Nature Geoscience: Risks to carbon storage from land-use change revealed by peat thickness maps of Peru.
- Data products supports monitoring of carbon storage risk due to land-use change and informs policy evaluation and future decision-making.

## Data products and formats
- Landcover_LPA_50m.tif
  - Band 1: Predicted land cover class
  - Values: -9999 (no prediction), 0 Pole forest, 1 Open savanna-like peatland, 2 Palm swamp, 3 Open water, 4 Seasonally flooded forest, 5 Terra firme forest, 6 Urban areas/river beaches, 7 White-sand forest
- Peat_carbon_5th_perc_LPA_100m.tif
  - Band 1: Peat carbon storage in Mt ha-1 (5th percentile)
- Peat_carbon_95th_perc_LPA_100m.tif
  - Band 1: Peat carbon storage in Mt ha-1 (95th percentile)
- Peat_carbon_LPA_100m.tif
  - Band 1: Peat carbon storage in Mt ha-1 (median)
- Peat_thickness_5th_perc_LPA_100m.tif
  - Band 1: Predicted peat thickness in cm (5th percentile)
- Peat_thickness_95th_perc_LPA_100m.tif
  - Band 1: Predicted peat thickness in cm (95th percentile)
- Peat_thickness_median_LPA_100m.tif
  - Band 1: Predicted peat thickness in cm (median)
- Peatland_Extent_LPA_50m.tif
  - Band 1: Presence of peat (1 = peat present)
- Coordinate system: GeoTIFF rasters, WGS84 (EPSG:4326), unprojected

## Methods and data sources
- Ground reference data: 1,128 points for vegetation type, peat presence/absence, and peat thickness.
- Modeling approach: train (50%) and validation (50%) with predictive models for land cover, peatland extent, peat thickness, and peat carbon storage (using lab-measured peat carbon where applicable).
- Input data: stack of seven remote sensing layers including two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM elevation, and a previous land-cover map.
- Model validation: 5% and 95% confidence intervals calculated using established methods; results peer-reviewed.

## Geographic scope
- Study area extent: Lowland Peruvian Amazonia
- Location bounds: Longitude -77.78 to -66.07 degrees; Latitude -14.67 to -0.04 degrees

## Data provenance and access
- Authors/Contact: Dr Adam Hastie (adamhastie@hotmail.com)
- Project/funding: UKRI-NERC grant NE/R000751/1; Principal Investigator Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Access: Published datasets accompanying the Nature Geoscience article; doi: 10.1038/s41561-022-00923-4

## Relevance for monitoring frameworks
- Provides quantified, spatially explicit predictors of land cover, peat extent, thickness, and carbon storage with uncertainty bounds (5th/95th percentiles) suitable for monitoring policy outcomes and risks.
- Enables assessment of carbon storage vulnerability to land-use change in the LPA and supports scenario analysis and dashboard reporting.
- Well-documented file structures, unit definitions, and coordinate system aid data integration into monitoring dashboards and governance processes.

## Practical considerations for implementation
- Metadata and data governance: dataset descriptions include clear band definitions and units; provenance and contact details available to support reproducibility and data sharing.
- Data updates: current as of publication; ongoing monitoring would require repeat measurements and revalidation to maintain up-to-date assessments.
- Accessibility: data tied to a peer-reviewed publication with a DOI; direct access via the article or by contacting the author.
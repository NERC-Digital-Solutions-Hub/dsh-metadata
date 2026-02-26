# Peatland maps: predicted vegetation and peat properties for lowland Peruvian Amazonia

## Overview
- Spatial prediction datasets for land cover, peatland extent, peat thickness, and peat carbon storage in the Lowland Peruvian Amazon (LPA).
- Derived from 1,128 ground reference points used to train and validate models (50% training, 50% validation).
- Input stack includes seven remote sensing layers: two Sentinel-2 indices, three ALOS PALSAR-2 bands, SRTM elevation, and a previous land-cover map.
- Published by Hastie, A. et al. (2022) in Nature Geoscience; DOI: https://doi.org/10.1038/s41561-022-00923-4.

## Datasets included (file list and purpose)
- CSAP_5.1_Landcover_LPA_50m.tif — predicted land cover class (Band 1) with coded categories (e.g., pole forest, open savanna-like peatland, palm swamp, open water, seasonally flooded forest, terra firme forest, urban areas/river beaches, white-sand forest); -9999 indicates outside study area.
- CSAP_5.2_Peat_carbon_5th_perc_LPA_100m.tif — peat carbon storage in Mt ha-1 (5th percentile).
- CSAP_5.3_Peat_carbon_95th_perc_LPA_100m.tif — peat carbon storage in Mt ha-1 (95th percentile).
- CSAP_5.4_Peat_carbon_LPA_100m.tif — peat carbon storage in Mt ha-1 (median estimate).
- CSAP_5.5_Peat_thickness_5th_perc_LPA_100m.tif — peat thickness (cm) 5th percentile.
- CSAP_5.6_Peat_thickness_95th_perc_LPA_100m.tif — peat thickness (cm) 95th percentile.
- CSAP_5.7_Peat_thickness_median_LPA_100m.tif — peat thickness (cm) median.
- CSAP_5.8_Peatland_Extent_LPA_50m.tif — peat presence indicator (1 = peat present).
- Geographic scope: lon -77.78 to -66.07; lat -14.67 to -0.04.

## Data structure and value encoding
- All files are GeoTIFF rasters with WGS84 (EPSG:4326) coordinates.
- Land cover (CSAP_5.1): Band 1 encodes 0–7 categories and -9999 for outside area.
- Peat carbon rasters (5th, 95th, median): Band 1 stores peat carbon in Mt ha-1.
- Peat thickness rasters (5th, 95th, median): Band 1 stores peat thickness in cm.
- Peatland extent (CSAP_5.8): Band 1 with 1 indicating presence.

## Methods and quality control
- Ground truth: 1,128 points for vegetation type, peat presence/absence, and peat thickness (where applicable).
- Model training/validation: 50% each.
- Model inputs: stack of seven remote sensing layers plus reference data and prior land-cover map.
- Validation: 5% and 95% confidence intervals calculated; methods align with prior publications; datasets peer-reviewed.

## Provenance and contact
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com).
- Project/Funding: UKRI-NERC grant NE/R000751/1; PI Dr Ian Lawson (itl2@st-andrews.ac.uk).
- Publication reference: Hastie et al., 2022, Nature Geoscience; DOI linked above.

## Data governance and stewardship considerations
- Data lineage and reproducibility supported by documented sampling, model inputs, and validation approach.
- Metadata should capture: data provenance, spatial extent, resolution, data products (percentiles and medians), units, and potential limitations/uncertainties.
- Update and maintenance: need clear processes to incorporate new ground truth data or revised input layers; track versioning and notify data users of any updates.
- Access and reuse: datasets are peer-reviewed and published; consider deposition in data portals with clear licensing and any sharing restrictions.
- Usage constraints: uncertainties reflected by percentile rasters (5th/95th) and median values; users should refer to the original Nature Geoscience publication for methodological details.

## Usage notes for data stewards
- Ensure consistent metadata across all rasters (extent, resolution, CRS, band definitions, value meanings).
- Maintain alignment between land cover classes and regional/national schemas if integrating with other datasets.
- Provide guidance on interpretation of percentile rasters and how to use median estimates for applications.
- Document any data processing steps undertaken post-publication (e.g., reformatting, reprojecting) to preserve auditability.
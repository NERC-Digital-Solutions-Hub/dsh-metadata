# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA

## Overview
- Data type: Information derived from Sentinel-2 imagery
- Size: 1.93 Mb
- Processed by: Stephen Dugdale
- Interpreted by: All authors
- Collection purpose: Quantify burn severity following wildfire in restored and unrestored sites

## Data Description
- Two 10 m resolution TIFF rasters comprising Normalised Burn Ratio (NBR) values for the study area
- Dates: pre-fire (June 2020) and post-fire (June 2021)

## Processing Methodology
- Source imagery: Sentinel-2A and 2B from Copernicus Data Hub
- Bands used: B08 (10 m) and B12 (20 m)
- Band12 upscaled to 10 m using CNN-based super-resolution (Lanaras et al., 2018)
- NBR calculation: NBR = (B08 - B12) / (B08 + B12)
- Burn severity metric: delta NBR = postfire NBR (June 2021) - prefire NBR (June 2020)
- Interpretation: Higher NBR values indicate healthy vegetation; lower values indicate burnt areas or bare ground

## Quality Control
- Data checked against Sentinel-2 QC bands; no quality issues noted

## Acquisition Dates and Dataset Structure
- Acquisition dates: 26 June 2020 and 26 June 2021
- Dataset structure: Two separate TIFF files
  - NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
  - NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif
- Pixel values correspond to Normalised Burn Ratio (NBR); high values = healthy vegetation, lower values = burnt/bare ground

## Usage Notes
- Delta NBR can be used to quantify burn severity across restored and unrestored sites
- Suitable for map-based data visualisations and GIS analyses at 10 m resolution
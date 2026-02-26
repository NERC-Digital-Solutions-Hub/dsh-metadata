# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: quantify burn severity following wildfire in restored and unrestored sites.
- Data type: information derived from Sentinel-2 imagery; two 10 m resolution TIFF rasters of Normalised Burn Ratio (NBR) values.
- Study scope: prefire and postfire comparisons for the South Fork McKenzie River area.
- Interpretation: lower NBR values indicate burnt areas or bare ground; higher values indicate healthy vegetation; burn severity derived via delta NBR (postfire minus prefire).

## Data details
- Size: 1.93 Mb
- Processed by: Stephen Dugdale
- Interpreted by: All authors
- Acquisition dates: 26 June 2020 (prefire) and 26 June 2021 (postfire)
- Location coordinates: Lat/Long 44.17, -122.30
- Dataset consists of two separate TIFF files containing NBR values

## Processing methodology
- Data sources: Sentinel-2A and Sentinel-2B images from Copernicus Data Hub
- Bands used: Band 8 (10 m) and Band 12 (initially 20 m; upscaled to 10 m)
- Upscaling: CNN-based super-resolution upscaling of Band 12 to match 10 m resolution (as per Lanaras et al., 2018)
- NBR calculation: NBR = (B08 - B12) / (B08 + B12)
- Burn severity metric: delta NBR = postfire NBR (June 2021) − prefire NBR (June 2020)
- Quality interpretation: higher NBR values indicate healthier vegetation; lower values indicate burnt areas or bare ground

## Quality control
- Data checked against Sentinel-2 QC bands; no quality issues noted

## Dataset structure and file names
- NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
- NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif
- Pixel values represent NBR; healthy values indicate vegetation
- NBR values are derived with the applied super-resolution method; “SuperRes” indicates the upscaled band12

## Usage notes
- Intended to quantify burn severity and support restoration assessment at study sites
- Can be used to compare pre- and post-fire conditions and to identify areas of greater burn impact via delta NBR

## Access and provenance
- Source data: Copernicus Data Hub
- Processing/interpretation: as detailed (Stephen Dugdale and authors)
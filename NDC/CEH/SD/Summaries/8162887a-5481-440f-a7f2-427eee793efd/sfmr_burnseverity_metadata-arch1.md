Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: quantify burn severity following wildfire in restored and unrestored sites.
- Location: South Fork McKenzie River, Oregon; coordinates 44.17, -122.30.
- Data type: information derived from Sentinel-2 imagery.
- Processing by: Stephen Dugdale; interpretation by all authors.

## Data Details
- Data type and scope: two 10 m resolution .tif rasters of Normalised Burn Ratio (NBR) values for the study area, captured before (June 2020) and after (June 2021) the wildfire.
- Size: 1.93 MB.
- Interpretation: NBR values indicate vegetation health (high = healthy vegetation; low = burnt areas or bare ground).
- Purpose of comparison: delta NBR (postfire minus prefire) to quantify vegetation burn relative to pre-burn state.

## Processing Methodology
- Data sources: Sentinel-2A and Sentinel-2B images from Copernicus Data Hub; acquisition dates 26 June 2020 and 26 June 2021.
- Bands used: B08 (10 m) and B12 (initially 20 m); to match 10 m resolution, B12 upscaled via CNN-based super-resolution (Lanaras et al., 2018).
- NBR calculation: NBR = (B08 - B12) / (B08 + B12).
- Burn severity metric: delta NBR = postfire NBR − prefire NBR (lower values indicate greater burn severity relative to pre-burn state).
- Quality control: dataset checked against Sentinel-2 QC bands; no quality issues noted.

## Dataset Structure
- Files:
  - NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
  - NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif
- Each pixel value represents NBR; healthy vegetation corresponds to higher values, burnt areas to lower values.

## Potential Uses
- Compare burn severity between restored and unrestored sites.
- Inform ecological recovery assessments and restoration planning.
- Integrate into broader analyses predicting wildfire impacts or informing management decisions.

## Data Access & Source
- Source: Copernicus Data Hub.
- Processing and interpretation: as described above.
- Study location reference: South Fork McKenzie River, Oregon (lat/long provided).
# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA.

- Aim: Quantify burn severity following wildfire in restored and unrestored sites using Sentinel-2 imagery.
- Data type: Information derived from Sentinel-2 imagery.
- Size: 1.93 MB.
- Processed by: Stephen Dugdale.
- Interpreted by: All authors.

## Data Description
- Two 10 m resolution .tif raster images of Normalised Burn Ratio (NBR) for the study area:
  - Pre-fire: June 2020
  - Post-fire: June 2021
- NBR interpretation: Higher values indicate healthy vegetation; lower values indicate burnt areas or bare ground.
- Burn severity is quantified via delta NBR = post-fire NBR minus pre-fire NBR.

## Processing Methodology
- Sentinel-2A and 2B data acquired in June 2020 and June 2021 from the Copernicus Data Hub.
- NBR calculation: NBR = (B08 - B12) / (B08 + B12), using Band 8 (10 m) and Band 12 (20 m).
- Band 12 upscaling: CNN-based super-resolution upscaling applied to Band 12 to achieve 10 m resolution (Lanaras et al., 2018).
- NBR-based burn severity references: higher NBR values indicate healthy vegetation; lower values indicate burnt areas (Keeley, 2009).

## Quality Control
- Quality checks performed against Sentinel-2 QC bands; no quality issues identified.

## Dataset Structure
- NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
- NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif
- Each pixel value corresponds to the Normalised Burn Ratio (NBR).

## Acquisition Dates
- 26 June 2020 (pre-fire)
- 26 June 2021 (post-fire)

## Collection Purpose
- To quantify burn severity following wildfire in restored and unrestored sites.

## Interpretation Notes
- Delta NBR (post-fire minus pre-fire) provides a measure of vegetation burn relative to the pre-burnt state.

## Reuse Considerations for Analysts Monitoring the Environment
- Supports temporal monitoring of environmental health and policy performance at the study site.
- Value can be enhanced by integrating with additional datasets (e.g., topography, land cover, fire history) and by ensuring underlying data remain accessible through appropriate data portals.
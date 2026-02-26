# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA

- Purpose: Quantify burn severity following wildfire in restored and unrestored sites within the study area.
- Data type and size: Information derived from Sentinel-2 imagery; dataset size 1.93 Mb.
- Processed by / interpreted by: Processed by Stephen Dugdale; interpreted by all authors.
- Acquisition dates: 26 June 2020 (pre-fire) and 26 June 2021 (post-fire).

## Data description and structure

- Format: Two 10 m resolution .tif raster images containing Normalised Burn Ratio (NBR) values.
- Study area: South Fork McKenzie River, Oregon, USA.
- Pre-fire and post-fire rasters:
  - NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif (June 2020)
  - NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif (June 2021)
- NBR interpretation: Higher values indicate healthier vegetation; lower values indicate burnt areas or bare ground.
- Delta NBR: Postfire NBR minus prefire NBR to quantify vegetation burn relative to the pre-burn state.

## Processing methodology

- Data sources: Sentinel-2A and Sentinel-2B imagery obtained from Copernicus Data Hub.
- Bands used for NBR: Band 8 (10 m) and Band 12 (20 m).
- Resolution alignment: Band 12 upscaled to 10 m via CNN-based super-resolution (Lanaras et al., 2018) to match Band 8.
- NBR calculation: NBR = (B08 - B12) / (B08 + B12).
- Burn severity metric: Delta NBR computed as postfire NBR minus prefire NBR.

## Quality control and metadata

- Quality checks: Data verified against Sentinel-2 QC bands; no quality issues noted.
- Metadata / provenance: Acquisition dates documented; dataset structure clearly labeled with file names indicating sensor, date, and processing (super-resolution) status.

## Relevance for monitoring frameworks

- Provides a clear, repeatable metric (delta NBR) for assessing burn severity over time and across restored vs unrestored sites.
- Demonstrates end-to-end workflow from satellite data to a ready-to-use burn severity product, suitable for integration into monitoring dashboards and policy evaluation.
- Grounded in transparent data sources and processing steps, supporting reproducibility and data provenance in monitoring programs.
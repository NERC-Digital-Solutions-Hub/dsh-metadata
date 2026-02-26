# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: quantify burn severity following wildfire in restored and unrestored sites.
- Data type: Normalised Burn Ratio (NBR) rasters derived from Sentinel-2 imagery; two 10 m resolution TIFFs representing pre-fire (June 2020) and post-fire (June 2021) states.

## Data details
- Size: 1.93 MB
- Processed by: Stephen Dugdale
- Interpreted by: All authors
- Acquisition dates: 26 June 2020 and 2021
- Dataset structure: two separate TIFF files
  - NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
  - NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif
- Data interpretation: pixel values reflect NBR; higher values indicate healthy vegetation, lower values indicate burnt areas.

## Processing methodology
- Source imagery: Sentinel-2A and Sentinel-2B from Copernicus Data Hub.
- Bands used: B08 (10 m) and B12 (20 m). Band 12 upscaled to 10 m via CNN-based super-resolution (Lanaras et al., 2018).
- NBR calculation: NBR = (B08 - B12) / (B08 + B12).
- Burn severity metric: delta NBR = postfire NBR (June 2021) − prefire NBR (June 2020); lower postfire values indicate greater burn impact.
- Interpretation basis: Keeley (2009) for burn severity context.

## Quality control and provenance
- Quality control: checked against Sentinel-2 QC bands; no issues found.
- Provenance: derived from Copernicus Sentinel-2 imagery; data processed and interpreted by project team (Stephen Dugdale and collaborators).

## Usage and metadata considerations
- Collection purpose: quantify burn severity to assess impacts across restored and unrestored sites.
- Potential uses: post-fire assessment, restoration planning, comparative analyses across sites and time.
- Metadata/discoverability: explicit file names and source references (Copernicus hub) support traceability and re-use.
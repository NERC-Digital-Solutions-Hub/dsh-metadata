# Sentinel-2 derived burn severity data for the South Fork McKenzie River in Oregon, USA

## Purpose and scope
- Collection purpose: quantify burn severity following wildfire in restored and unrestored sites.

## Data Description and Format
- Data type: information derived from Sentinel-2 imagery.
- Size: 1.93 MB.
- Spatial resolution: 10 m.
- Study location: area bounded by the coordinates around 44.17 N, -122.30 W.
- Structure: two separate 10 m TIFF rasters of Normalised Burn Ratio (NBR) values.
- Pre-fire and post-fire coverage: one image from June 2020 (pre-fire) and one from June 2021 (post-fire).
- Pixel interpretation: higher NBR values indicate healthy vegetation; lower values indicate burnt areas or bare ground.
- File names:
  - NBR_S2A_MSIL2A_20200626T185921_N0214_R013_T10TEP_SuperRes.tif
  - NBR_S2B_MSIL2A_20210626T185919_N0300_R013_T10TEP_SuperRes.tif

## Processing Methodology
- Data sources: Sentinel-2A and Sentinel-2B from the Copernicus Data Hub; acquisition dates 26 June 2020 and 26 June 2021.
- NBR calculation: NBR = (B08 - B12) / (B08 + B12), where B08 is band 8 (10 m) and B12 is band 12 (20 m).
- Resolution matching: Band 12 upscaled to 10 m using CNN-based super-resolution (Lanaras et al., 2018).
- Burn severity metric: delta NBR calculated as post-fire NBR minus pre-fire NBR.
- Quality control: data checked against Sentinel-2 QC bands; no quality issues noted.

## Data Provenance and Contact
- Processed by: Stephen Dugdale.
- Interpreted by: All authors.
- Documentation aligns with standard sensor-derived burn severity workflows and provides explicit processing steps and references.

## Governance and Stewardship Considerations
- Metadata clarity: includes acquisition dates, data sources, file names, processing steps, and interpretation guidance.
- Formats and standards: uses widely supported TIFF rasters with explicit NBR methodology and delta-NBR approach.
- Reusability: clearly documented workflow (sensor inputs, upscaling method, NBR calculation, delta NBR) supports reproducibility and discovery.
- Updatability and sharing: dataset structure and provenance facilitate cataloging and potential inclusion in data portals; QC step supports reliability.
- Limitations to note for users: reliance on super-resolution for band 12 and use of delta NBR as the burn severity proxy; describes specific study area and dates, which may constrain generalization.
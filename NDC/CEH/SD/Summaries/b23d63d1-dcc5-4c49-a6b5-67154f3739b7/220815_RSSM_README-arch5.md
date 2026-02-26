# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

## Overview
- Relative Surface Soil Moisture (rSSM) dataset for Thames Valley, UK, covering Oct 2015 – Sep 2021.
- rSSM ranges from 0% (driest) to 100% (wettest) and is derived from Sentinel-1 SAR backscatter (σ0) using the TU-Wien Change Detection Algorithm (TWCDA).
- Created with MATLAB R2021a; accessible via other platforms (e.g., Python, QGIS) for testing and viewing.
- Open Access Publication supporting methodology: Maslanka et al., 2022.

## Dataset Description
- Format: a single NetCDF file containing 610 variables.
- Temporal coverage: all dates in YYYYMMDD format (extensive time series within 2015–2021).
- Spatial reference: EPSG 4326.
- Content: rSSM values per pixel for each timestamp, plus latitude/longitude grids.
- Intended use: assessing soil moisture variations across landscapes; suitable for applications like Natural Flood Management (NFM) planning and climate/soil moisture research.
- Documentation and provenance linked to a public Open Access Publication detailing the retrieval approach.

## Methodology

### A. Pre-processing
- Sentinel-1 data geocoded and radiometrically corrected using ESA SNAP.
- Processing steps include orbital corrections, thermal/border noise removal, radiometric calibration, refined Lee speckle filtering, and terrain correction (SRTM 3 Sec).
- Frames over the area of interest stitched to create a single radar file per scan day; Local Incidence Angle (LIA) data also subset and prepared for normalization.

### B. Backscatter Normalisation
- σ0 is normalized to a common incidence angle Θ (40°) to remove LIA dependencies.
- Two approaches for the normalization factor β:
  - Direct regression slope (βd) when observations span a sufficient range of LIAs.
  - Monthly varying normalization βr derived via a multiple regression model: βr = aS + b(mean σ°) + c(dB/°) with constants a, b, c.
- Novel aspect: monthly varying normalisation instead of a single, time-invariant parameter, improving cross-time comparability.

### C. Dynamic Backscatter Masking
- Mask out extreme σ0 values unlikely to carry soil moisture signals using thresholds of -5 to -22 dB.
- Additional masking for areas classified as Artificial (Urban/Suburban) and Freshwater.

### D. Spatial Averaging
- Original IW mode resolution (5×20 m; ~20×22 m) is upscaled to coarser grids to reduce heterogeneity effects from vegetation, crop structure, roughness, etc.
- Aggregation performed by arithmetic mean to 1 km, 500 m, 250 m, and 100 m resolutions.
- Coarser resolutions maintain strong correlation (≥0.7) with in-situ measurements, enabling broader land-use evaluations (e.g., for NFM).

### E. Wet and Dry Threshold
- Wet/dry thresholds (σ°w and σ°d) are statistically derived from the time series to represent the upper/lower backscatter bounds.
- Use 10th/90th percentiles of normalized backscatter to map to 0%/100% rSSM; outliers can be set to No Data or clipped to 0%/100%.
- To handle short time series and potential outliers, extreme events are mitigated to ensure robust rSSM.

## Dataset Metadata
- File structure: NetCDF with 610 variables (e.g., V002–V606 and beyond) representing spatial-temporal data points and coordinates; includes both lat/lon references and per-timestep rSSM values.
- Timestamps: dates in YYYYMMDD format.
- Spatial layout: detailed per-timestep rSSM fields aligned with the included lat/lon grids.
- Referenced datasets and standards cited in the accompanying documentation and references.

## Data Access and Reuse
- Open Access publication supports reproducibility and provides methodological details for data creators/sharers and data stewards.
- Dataset notes that MATLAB V2021a was used for production, with cross-platform testing possible via Python or QGIS.
- Clear lineage from Sentinel-1 data through preprocessing, normalisation, masking, spatial averaging, and thresholding to final rSSM values.

## Governance, Quality, and Stewardship Considerations
- Monthly varying normalisation βr enhances data consistency over time but introduces complexity in governance and replication; ensure metadata captures normalization scheme used for each timetable.
- Data quality depends on:
  - Accurate geocoding/radiometric correction (SNAP workflow adherence).
  - Robust LIA normalization and threshold selection (wet/dry thresholds derived statistically per pixel).
  - Handling of No Data, clipping, and outliers at the 0–100% bounds.
- Interoperability considerations:
  - Coarser spatial resolutions recommended for comparative analyses across land uses and for integration with other hydrological or ecological datasets.
  - Standardized time format and EPSG:4326 ensure compatibility with common geospatial tools and catalogues.
- Stewardship notes:
  - Maintain provenance links to the OAP and the Maslanka et al. (2022) methodology to support reproducibility.
  - Document any future updates to processing steps, normalization approach, or thresholding to preserve data lineage.

## References
- Maslanka, W., Morrison, K., White, K., Verhoef, A., Clark, J. (2022). Retrieval of Sub-Kilometric Relative Surface Soil Moisture With Sentinel-1 Utilizing Different Backscatter Normalization Factors. IEEE Transactions on Geoscience and Remote Sensing.
- Bauer-Marschallinger et al. (2019, 2021). Sentinel-1 backscatter models and soil moisture retrieval discussions.
- Pathe et al. (2009); Wagner et al. (1999a, 1999b); Rowland et al. (2017); Sabel et al. (2010); additional related works cited in the document.
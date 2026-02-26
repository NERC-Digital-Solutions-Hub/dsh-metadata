# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

- Time period and purpose
  - Spatially explicit relative Surface Soil Moisture (rSSM) estimates for Thames Valley, UK, from October 2015 to September 2021.
  - rSSM values range from 0% (dryest) to 100% (wettest) within the time series.

- Data provenance and access
  - Created with Sentinel-1 data; tested with Matlab R2021a (and also opened in Python, QGIS).
  - Dataset is delivered in a single NetCDF file containing multiple variables (610 total).

- Core algorithm and concept
  - rSSM retrieval uses the TU-Wien Change Detection Algorithm (TWCDA), linking backscatter changes to soil moisture while assuming other backscatter-affecting factors (e.g., roughness, geometry) are temporally constant.
  - Backscatter values σ0(Θ, t) are used, where Θ is a reference incidence angle (40°). Normalized backscatter is linearly scaled between wet and dry references to obtain rSSM(t).

- Pre-processing workflow (geolocation and calibration)
  - Sentinel-1 data geocoded and radiometrically corrected using ESA SNAP workflows.
  - Processing steps include orbital corrections, removal of thermal and border noise, radiometric calibration, Refined Lee speckle filtering, and terrain correction with SRTM 3Sec.
  - Data subset to the area of interest; frames stitched to form a single radar file per scan day when necessary.
  - Local Incidence Angle (LIA) data are subset and prepared for normalization.

- Backscatter normalization and LIA handling
  - Normalization to a common incidence angle Θ (40°) to remove LIA dependency:
    - σ0(Θ, t) = σ0(θ, t) − β(θ − Θ) [dB]
  - Normalization parameter β estimated in two ways:
    - Direct regression slope (βd) using θ–σ0 relationships.
    - Multiple regression slope (βr) using a, b, c constants with factors like S (non-normalization sensitivity) and mean backscatter.
  - Novel approach: monthly varying normalization parameters (βd and βr) applied to orbits in individual months, enhancing temporal adaptation.

- Dynamic backscatter masking
  - Excludes extreme backscatter values likely not containing usable soil moisture signals:
    - Thresholds set at -5 dB (upper) and -22 dB (lower).
  - Additional masks for Artificial (Urban/Suburban) and Freshwater areas.

- Spatial averaging (scaling to coarser grids)
  - To reduce heterogeneity effects from vegetation, roughness, and other factors, upscaling from native IW resolution to coarser grids.
  - Aggregation by arithmetic mean to 1 km, 500 m, 250 m, and 100 m resolutions.
  - Coarser resolutions show higher correlation (≥ 0.7) with in-situ measurements in prior studies, aiding use in natural flood management (NFM) and land-use assessments.

- Wet and dry threshold estimation
  - Wet/dry thresholds (σw(Θ), σd(Θ)) required to anchor rSSM time series.
  - Thresholds estimated statistically from the available time series (10th and 90th percentiles assumed to correspond to 0% and 100% rSSM respectively).
  - To handle outliers and short time series, extreme values can push rSSM beyond 0–100%; values within ±20% of the limits are capped at 0% or 100%, while values outside the 20% buffer are set to No Data.

- Dataset structure and metadata
  - File format: NetCDF with 610 variables.
  - Dates: YYYYMMDD format for each timestep.
  - Coordinate reference system: EPSG 4326 (lat/lon).
  - Data organization: per-timestep rSSM values across the Thames Valley, with lat/lon grids corresponding to the selected spatial resolutions.
  - The dataset includes documentation on variable naming conventions and a long list of timestep-specific variables (rSSM values) across the study period.

- Practical considerations for GIS specialists
  - Multi-resolution product options (1 km to 100 m) suitable for different land-use and policy analysis scales.
  - Relative moisture product (0–100%) suitable for comparative mapping, trend analysis, and integration with other spatial datasets.
  - NetCDF format supports integration with common GIS tools; units are in percentage terms for rSSM.
  - Monthly varying normalization improves temporal fidelity, especially in heterogeneous landscapes.

- References and provenance
  - Underlying methodology influenced by: TU-Wien Change Detection Algorithm literature, Sentinel-1 backscatter normalization work, and related soil moisture retrieval studies.
  - Related publications and data standards cited, including Maslanka et al. 2022 (IEEE TGRS) and Bauer-Marschallinger et al. (2019, 2021), among others.
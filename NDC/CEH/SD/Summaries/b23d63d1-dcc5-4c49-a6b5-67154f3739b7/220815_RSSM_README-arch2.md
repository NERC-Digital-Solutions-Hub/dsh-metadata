# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

- Purpose and scope
  - Provides relative Surface Soil Moisture (rSSM) estimates for the Thames Valley, UK, from October 2015 to September 2021.
  - Outputs a 0% (driest) to 100% (wettest) scale of relative soil moisture per pixel over time.
  - Intended to support environmental monitoring and assessment of hydrological conditions and policy performance over time.

- Data sources and methodology
  - Derived from Sentinel-1 radar backscatter (σ0) time series.
  - Uses the TU-Wien Change Detection Algorithm (TWCDA) to attribute backscatter changes to soil moisture changes, assuming other factors (roughness, geometry) are temporally constant.
  - rSSM(t) conceptually follows: normalized σ0 at time t, scaled between dry and wet backscatter references.

- Pre-processing and data preparation
  - Geocoding and radiometric correction performed with ESA SNAP; includes orbital corrections, border noise and thermal corrections, radiometric calibration.
  - Speckle filtering (Refined Lee) and terrain correction (SRTM 3Sec); data subset to area of interest; stitching of frames to create a single radar file per scan day; Local Incidence Angle (LIA) data used for normalization.

- Backscatter normalization and normalization strategy
  - σ0 is normalized to a common incidence angle Θ (40°) to remove LIA dependency.
  - Normalization parameter β is computed per pixel; applied to convert σ0(θ,t) to σ0(Θ,t).
  - Two methods to estimate the normalization slope:
    - Direct regression slope (βd) and
    - Multiple regression slope (βr) with coefficients a, b, c.
  - Novel monthly variability: normalization parameters can vary by month (monthly parameterization) to better capture temporal changes.

- Dynamic masking and data quality controls
  - Dynamic masking to remove non-informative values: thresholds set at -5 dB (upper) and -22 dB (lower).
  - Additional masks for Artificial (Urban/Suburban) and Freshwater areas.
  - Wet and dry thresholds derived from 10th and 90th percentiles of the normalized backscatter; safeguards ensure rSSM stays within 0–100% and outliers are handled (values ±20% from limits clipped to 0% or 100%; values beyond 20% buffer → NoData).

- Spatial resolution and aggregation
  - Original IW mode resolution is 5 x 20 m; data are upscaled to coarser grids to reduce heterogeneity.
  - Resolutions used: 1 km, 500 m, 250 m, 100 m.
  - Spatial averaging is performed using arithmetic mean.
  - Coarser resolutions maintain strong relationships with in-situ measurements (high correlation reported at 0.7+).

- Temporal coverage and data product details
  - Single NetCDF file containing 610 variables.
  - Dates formatted as YYYYMMDD; coordinate reference system is EPSG 4326.
  - rSSM values are stored per timestep (per date) and per spatial location.

- Validation and references
  - Methodology builds on established soil moisture retrieval literature (e.g., TU-Wien CDA, Sentinel-1 backscatter normalization models).
  - Related works cited include global backscatter models, high-resolution soil moisture retrievals, and validation studies with in-situ data.

- Practical considerations for analysts
  - Open to testing and use with Python, QGIS, or other GIS/analysis platforms.
  - Dataset designed for consistent environmental health monitoring and policy performance assessment over multi-year periods.
  - Enables integration with other environmental datasets to enhance data value and accessibility of underlying data.

- Key references and open access links
  - Maslanka et al., 2022: Retrieval of Sub-Kilometric Relative Surface Soil Moisture With Sentinel-1 Utilizing Different Backscatter Normalization Factors (IEEE TGRS).
  - Bauer-Marschallinger et al., 2019-2021; Pathe et al.; Wagner et al.; Rowland et al.; plus additional supporting literature on backscatter models and soil moisture retrieval.
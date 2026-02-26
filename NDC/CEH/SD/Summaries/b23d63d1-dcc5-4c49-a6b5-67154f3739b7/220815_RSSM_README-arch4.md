# Supporting Documentation for Relative surface soil moisture for the Thames Valley, United Kingdom, October 2015 to September 2021

- Purpose and scope
  - Provides relative surface soil moisture (rSSM) estimates for Thames Valley, UK, from Oct 2015 to Sep 2021.
  - rSSM values range 0% (dryest) to 100% (wettest) across the time series.
  - Based on Sentinel-1 radar backscatter (σ0) and the TU-Wien Change Detection Algorithm (TWCDA).

- Key methodological approach
  - Changes in backscatter are treated as changes in soil moisture, while other factors (surface roughness, geometry) are assumed temporally constant.
  - Backscatter is normalized to a reference incidence angle (Θ = 40°) to remove incident-angle dependencies, enabling time-series comparisons.
  - rSSM(t) is derived by linearly scaling the normalized backscatter between dry and wet reference values.

- Data processing workflow (A–E)

  - A. Pre-processing the raw Sentinel-1 data
    - Geocoding and radiometric correction using ESA SNAP.
    - Steps include orbital corrections, noise removals, radiometric calibration, Refined Lee speckle filter, and terrain correction with SRTM 3Sec.
    - Data subset to area of interest; frames stitched if needed; Local Incidence Angle (LIA) data aligned for normalization.

  - B. Backscatter Normalisation
    - Normalize σ0 to a common angle to remove LIA effects so variations reflect ground conditions (moisture).
    - Reference angle Θ = 40°.
    - Normalization options:
      - Direct regression slope (βd): simple linear relation between θ and σ0°.
      - Multiple linear regression (βr): βr = aS + bσ̄° + c[dB/°], with constants a, b, c derived from data.
    - Innovation: monthly-varying normalization parameterization (βd and βr recalculated for individual months), allowing temporal dynamics in the normalization factor.

  - C. Dynamic Backscatter Masking
    - Remove extreme σ0 values unlikely to contain moisture information: thresholds set to -5 dB (upper) and -22 dB (lower).
    - Mask areas classified as Artificial (Urban/Suburban) and Freshwater.

  - D. Spatial Averaging
    - Default 5×20 m Sentinel-1 IW resolution upscales to coarser grids to reduce heterogeneity effects (vegetation, texture, roughness).
    - Aggregation options include 1 km, 500 m, 250 m, and 100 m.
    - Coarser resolutions show high correlation (≥ 0.7) with in-situ measurements, supporting use for land-use and NFM assessments.

  - E. Wet and Dry Threshold
    - Wet/dry thresholds σ°w(Θ) and σ°d(Θ) derived statistically from the time series (10th and 90th percentiles) to reflect moist/dry extremes.
    - rSSM is linearly scaled between these thresholds.
    - Outliers near extremes handled: rSSM values outside 0–100% corrected; values within ±20% of the limits set to 0% or 100%; values beyond the ±20% buffer assigned No Data.

- Dataset structure and metadata

  - File format and content
    - Stored in a single NetCDF file containing about 610 variables.
    - Dates are encoded as YYYYMMDD, with coordinates in EPSG 4326.
    - Variables are organized by timestep (e.g., V003, V004, etc.) and include latitude/longitude reference variables.

  - Temporal and spatial resolution
    - Time span: 20151002 to 20210930.
    - Spatial resolutions: 1 km, 500 m, 250 m, and 100 m (in addition to the native 5×20 m σ0 resolution used in processing).

  - Data provenance and tools
    - Dataset creation and testing performed with Matlab R2021a; Opened/tested with Python and QGIS.
    - Pre-processing and processing workflow aligned with established references and prior TU-Wien/σ0 backscatter methods.

- Use cases and relevance for data strategy

  - Provides a co-owned, transparent product for assessing soil moisture dynamics in a key UK valley, useful for water/resource management and environmental planning.
  - Monthly-varying normalization enhances data reliability for monitoring over time and across changing platforms/orbits.
  - The data product supports collaboration within a broader data community by detailing processing steps, thresholds, and QA/QC approaches, aiding discoverability and reusability.
  - The NetCDF format and comprehensive metadata support integration into organisational data systems, enabling scalable dissemination and iterative improvement.

- Core references
  - Maslanka et al., 2022: Retrieval of Sub-Kilometric Relative Surface Soil Moisture With Sentinel-1 Utilizing Different Backscatter Normalization Factors.
  - Bauer-Marschallinger et al., 2019/2021; Wagner et al., 1999a/b; Pathe et al., 2009; Rowland et al., 2017; Maslanka et al., 2022; and related works on Sentinel-1 backscatter normalization and soil moisture retrieval.
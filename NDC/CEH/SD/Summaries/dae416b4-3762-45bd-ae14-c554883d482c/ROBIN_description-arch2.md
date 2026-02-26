# Amplitude maps provide an indication of net ecosystem phenology since the satellite observations integrate the greenness variations across the plant individuals within each pixel.

- Aim
  - Map the average amplitude of annual vegetation greenness cycles to indicate the degree of synchronization of leaf life cycles among plants within each pixel.
  - Use MODIS NDVI and EVI time series (2001–2013) to derive robust amplitude measures via spectral analysis.
  - Validate interpretation with independent data and provide outputs suitable for monitoring environmental health and policy performance over time.

- Data and period
  - Input: MODIS vegetation indices (NDVI and EVI) from the 13-year, 16-day time series (2001–2013) at 500 m and 1 km resolutions.
  - Source: MOD13A1 product provided by USGS LP DAAC / NASA EOSDIS.
  - Coverage: Mesoamerica and South America.
  - Coordinate system: Sinusoidal projection; resolutions 0.5 km, 1 km, and 0.5 degree.

- Methodology and processing
  - Quality control: exclude data not flagged as good, NDVI/EVI < 0.01, and outliers beyond ±3 standard deviations.
  - Data sufficiency: require at least 100 valid observations with at least one per month (out of 320 possible) to proceed.
  - Pre-processing: linear detrending; split-cosine taper on the first and last 5% of the time series.
  - Spectral analysis: Lomb-Scargle Transform (handles irregular spacing) to derive periodograms; three-point Hanning smoothing to stabilize estimates.
  - Detection threshold: consider an annual cycle detected if the spectral peak exceeds the 95% confidence level.
  - Output metric: average amplitude, defined as maximum minus minimum of the annual cycle, derived from the power spectral estimates.
  - Output format: amplitude maps (per pixel) presenting the strength of the annual phenology signal.

- Outputs and interpretation
  - Amplitude maps showing the degree of annual greenness variation within pixels.
  - Legend includes:
    - -3 water bodies
    - -2 not enough data
    - -1 not significant
    - 0–1 amplitude of phenological signal
  - Interpretation notes:
    - High amplitude → strong, synchronized leaf phenology within the pixel.
    - Low amplitude → weak synchronization or constant canopy with leaf turnover strategies.
    - Areas without significant annual variation may still contain individuals with well-defined phenology or diverse leaf turnover strategies.

- Evaluation and validation
  - Compare amplitude distributions with the independent IGBP land cover map (class-based histograms).
  - Validate against published in situ observations describing canopy leaf flush/fall, LAI, and litter fall relative to amplitude values.
  - Cross-checks support interpretation that higher amplitude aligns with certain phenological patterns observed in situ.

- Data quality, reproducibility, and access
  - Uses well-established MODIS products and standard, replicable processing steps (quality screening, detrending, Lomb-Scargle, significance testing).
  - Outputs are suitable for inclusion in environmental monitoring portals and for informing policy-relevant assessments.
  - Acknowledges data sources (MOD13A1) and data providers (NASA LP DAAC / USGS EROS) and standard references for methodology.
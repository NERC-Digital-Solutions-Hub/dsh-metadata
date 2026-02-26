# Human impact on long-term organic carbon export to rivers

- Overview of the dataset
  - Monthly dissolved organic carbon (DOC) concentration data for the Thames River, UK, from 1883 to 2014.
  - Colour data collected 1883–1990; DOC data 1990–2014; DOC 1883–1905 estimated from colour via calibration.
  - Measurements taken at the Thames basin outlet upstream of London; basin area ~9,948 km².
  - Finding: fluvial DOC concentration shows an upward trend across the full study period.
  - Data are provided as one main table plus one supporting metadata file.

- Study site and data collection context
  - Measurement locations: Hampton (colour) and Teddington (DOC), with long-term urban and population growth in the Thames catchment.
  - Catchment characteristics: temperate, lowland, mineral soils; urban centers (e.g., Oxford, Reading); significant wastewater influence (STWs, tertiary treatment since 2003 for the largest 36 works upstream of the tidal limit).
  - Predominantly rural land use upstream of London (87.7% in 2007).

- Measurement techniques and data streams
  - Colour measurements (1883–1974): Burgess method (tube-based comparison against a standard solution).
  - Colour measurements (1974–1990): Hazen units, via absorptiometry; Hazen units correlated closely with Burgess units (approx. 2.2 Burgess units = 1 Hazen unit).
  - DOC measurements (1883–1905): eudiometric/oxidation-based methods; early OC quantification.
  - DOC measurements (1990–2014): Harmonised Monitoring Scheme (HMS) with standardized methods; 1974–1990 data integrated from multiple agencies.
  - Data sources and accessibility: 1974 onward available via data.gov.uk dataset on historical UK water-quality sampling HMS data.

- Calibration and data processing
  - Calibration between colour and DOC conducted for 1899–1905 (weekly samples): DOC = 0.0955 × Colour + 0.2103; R² = 0.66; n = 194.
  - The calibration relied on a stationary colour–DOC relationship over time, though later work indicates the relationship has shifted since 1974.
  - Using calibration, DOC time series were extended back to 1883–1990; DOC data from other sources (1883–1905 Grand Junction Water Company; 1990–1998 Thames Water; 1998–2014 EA) used for cross-validation and consistency checks.

- Data provenance and metadata
  - Data provenance spans multiple periods, methods, and measuring bodies:
    - 1883–1905: Colour, Burgess method; Grand Junction Water Company (daily colour, weekly OC).
    - 1905–1974: Colour, Burgess; London Metropolitan Water Board (daily to weekly notes).
    - 1974–1988: Colour, Hazen; Thames Water Authority; sampling frequency from monthly to weekly.
    - 1974–1990: Colour; Environment Agency; 1974–1985 weekly, 1985–1990 monthly.
    - 1990–1998: DOC, mg/L; Thames Water; approx. monthly.
    - 1998–2014: DOC, mg/L; Environment Agency; approx. monthly.
  - Documentation includes data table plus metadata file; key references and calibration validation discussed.

- Data quality, limitations, and interpretation
  - Calibration assumes stationarity; historical shifts in the color–DOC relationship since 1974 suggest potential biases if unadjusted.
  - Data heterogeneity: different measurement methods across periods; unit transitions (Burgess to Hazen) and method changes require careful harmonization.
  - Spatial scope is at the outlet of the Thames basin (not upstream within all tributaries); may reflect urban input and wastewater treatment changes (e.g., tertiary treatment since 2003).
  - Overall trend interpretation should consider changing data collection methods, measurement sensitivity, and potential non-stationarity in relationships over time.

- Implications for data strategy and governance (Data Leaders perspective)
  - The study exemplifies long-term data integration across heterogeneous sources, time-varying methods, and evolving standards.
  - Highlights importance of:
    - Comprehensive metadata and provenance to support data discoverability and reuse.
    - Clear documentation of calibration relationships and their limitations, including stationarity assumptions.
    - Cross-validation with independent datasets to assess consistency over time.
    - Transparent handling of units, measurement techniques, and period-specific data quality.
  - Recommendations for data leadership:
    - Establish robust data lineage and versioning when consolidating multi-decade time series.
    - Maintain explicit notes on methodological shifts and their impact on derived variables.
    - Facilitate access to supporting datasets (e.g., HMS data, data.gov.uk resources) to enable reproducibility.
    - Consider non-stationarity in long-term environmental relationships and plan for recalibration as methods evolve.
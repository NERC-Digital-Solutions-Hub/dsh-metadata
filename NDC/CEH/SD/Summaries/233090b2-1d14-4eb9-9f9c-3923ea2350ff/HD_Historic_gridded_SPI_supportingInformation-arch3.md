# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

- Brief description
  - A 5km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, covering 1862–2015.
  - SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, for all twelve calendar months.
  - Uses a gamma distribution fitted to historical precipitation with a standard period of 1961–2010; results expressed as normal scores (mean 0, stdev 1) with no units.
  - Stored in NetCDF4 format on the British National Grid; values limited to -5 to +5.

- Context and projects
  - Produced as part of two major initiatives: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts (UK drought history and tools).
  - Historic Droughts Inventory provides a cross-disciplinary knowledge base: hydro-meteorological timelines and references to droughts from the 19th century to present, intended for use by policy makers, regulators, water companies, and industry.
  - Aims to enable consistent, transparent drought planning and monitoring across sectors.

- Data sources and provenance
  - Met Office 5km monthly rainfall gridded data used to derive SPI.
  - Data sources include UKCP09 data (1910–1959 and 2001–2011), Met Office daily grids converted to monthly grids (1960–2000), unpublished updates (2012–2015), and rescued data (1862–1909).
  - Version 4 updates underlying rainfall data from prior versions (CEHGEAR-based data in earlier versions).

- Methodology
  - For each location, SPIs are derived for 7 durations across 12 months, yielding 84 time series per grid cell.
  - Gamma distribution fitted via L-moments (instead of maximum likelihood) to annual precipitation totals for each duration-month combination.
  - Calculation performed with an R-based approach (modified SCI package) to produce normal scores.
  - Handling and caveats:
    - Although gamma distribution is standard for SPI, recent work suggests alternatives (e.g., Pearson Type III, Tweedie) may be more adequate for some UK cases.
    - For durations > 12 months, overlapping data can induce autocorrelation; SPIs remain comparative indicators, but trend analyses should account for serial correlation.
    - Extreme SPI values are truncated at ±5.
  - Standardization period for distribution fitting: 1961–2010.
  - Data span for SPI grids: 1862–2015.

- Dataset format and structure
  - NetCDF4 format following CEH gridded dataset conventions.
  - Grid layout: two-dimensional UK grids with twelve monthly grids per year; one yearly file per accumulation period.
  - Projection: British National Grid.
  - SPI values are unitless normal scores, range typically within -5 to +5.

- Versioning and notes
  - Version 4 supersedes v2 and v3 due to minor data file errors in earlier releases.
  - Noted changes include updated monthly rainfall grids for 1960–2000 and the addition of the 9-month accumulation period; broader underlying rainfall data updated to Met Office 5km inputs.

- Data governance and usage considerations for monitoring frameworks
  - Provides a consistent, policy-relevant drought indicator set across multiple time scales for UK drought monitoring and early warning.
  - Useful as a reference for cross-sector planning, drought risk assessment, and historical context in regulatory and water resource decisions.
  - Important to document metadata provenance, data sources, and methodological choices (gamma distribution with L-moments, alternative distributions under consideration) to inform governance and potential future data governance improvements.

- Acknowledgements and references
  - Joint output from DrIVER, Historic Droughts, and IMPETUS projects; funded by UK research councils (specific grant numbers provided in the document).
  - References include foundational SPI methodology and related data sets and tools used in computation and interpretation.
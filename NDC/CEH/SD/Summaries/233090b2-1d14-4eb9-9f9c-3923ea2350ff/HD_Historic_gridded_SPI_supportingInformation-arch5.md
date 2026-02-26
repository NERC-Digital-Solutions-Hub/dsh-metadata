# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

- Purpose and scope
  - Provides 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, indicating meteorological drought severity across multiple time scales.
  - SPI computed for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with a separate grid for each calendar month; standard distribution fitting uses 1961-2010.
  - Spatial coverage: UK; temporal coverage: 1862–2015; data format: NetCDF4.

- Context and aims for data stewardship
  - Part of two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts (UK drought history and management tools), supporting drought research and decision-making.
  - The Historic Droughts Inventory serves as a knowledge base for multi-sector understanding of past droughts, combining hydro-meteorological timelines with references to droughts from diverse sources.

- Data sources and provenance
  - Met Office 5 km monthly rainfall gridded data used as the primary input.
  - Data sources include: UKCP09-derived grids (1910–1959, 2001–2011), Met Office daily grids (1960–2000), unpublished updates (2012–2015), rescued data for 1862–1909.
  - Sourcing rationale: updates to improve historical rainfall coverage and data quality feeding SPI calculations.

- Methodology and quality considerations
  - SPI calculation follows McKee et al. (1993): for each location, 7 durations × 12 months yield 84 time series per grid cell.
  - Distribution fitting: gamma distribution estimated with L-moments (via a modified R SCI package) to convert to normal scores (mean 0, SD 1). Values truncated at abs(SPI) ≤ 5 due to extreme-data uncertainty.
  - Note on distribution choice: gamma distribution is widely used and recommended for Europe, but UK-specific studies indicate it may not always pass normality tests; alternative distributions (e.g., Pearson type 3, Tweedie) may be explored in future updates.
  - Temporal and statistical caveats:
    - For periods longer than 12 months, accumulation time series overlap, introducing autocorrelation.
    - Consecutive SPIs across months can also be autocorrelated; users should adjust analyses that assume independence (e.g., certain frequency analyses or trend tests).
  - Versioning note: This is version 4; v2 and v3 superseded due to minor data errors; changes from earlier work include revised underlying rainfall data and an added 9-month accumulation period.

- Data organization and format
  - Storage: NetCDF4, CEH gridded-dataset conventions.
  - Structure: two-dimensional UK grids with 12 monthly grids per year; one file per accumulation period.
  - Projection: British National Grid.
  - Units: SPIs are standard scores with no units, range limited to -5 to +5.

- Version history and rationale
  - Version 4: underlying monthly rainfall data (1960–2000) updated; new monthly rainfall grids derived from daily data; added 9-month accumulation; period covered: 1862–2015.
  - Prior versions superseded due to minor data issues (v2 and v3).

- Acknowledgements and governance
  - Acknowledges support from DrIVER, Historic Droughts, IMPETUS; specific grant numbers included.
  - Outputs designed to enable cross-sector policy planning, drought monitoring, and long-term water resource management.

- Practical implications for data stewardship
  - Ensure documentation reflects the provenance, update history, and methodological choices (including justification for gamma distribution and L-moment fitting).
  - Maintain metadata on data sources, versioning, and caveats related to autocorrelation and potential alternatives for future releases.
  - Preserve accessibility of NetCDF4 SPI files and link to the overarching Historic Droughts Inventory and DrIVER context for discovery and reuse.
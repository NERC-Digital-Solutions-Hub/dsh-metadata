# Supporting Information

- Overview
  - Time series dataset of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas, covering 1961–2012 with a standard fitting period of 1961–2010.
  - SPI calculated for six accumulation periods (1, 3, 6, 12, 18, 24 months) across all twelve calendar months, resulting in 72 time series per IHU (across durations and months). Data stored in CSV format.

- Dataset content and scope
  - SPI values are “normal scores” from a standard normal distribution (mean 0, std dev 1) with no units.
  - SPI values are truncated to the range [-5, +5]; -9999 denotes No Data.
  - 9-column CSV structure: RID, POLYGONID (IHU area ID for joins), THEDATETIME (date), and six SPI columns corresponding to the six accumulation periods (1, 3, 6, 12, 18, 24 months).

- Purpose and use
  - Derived to populate a CEH droughts portal; enables study of drought or wet periods within specific IHUs.
  - SPI at different time scales supports interpretation of short-, medium-, and long-term moisture conditions and related hydrological impacts (soil moisture, crops, streamflow, reservoirs).

- Data sources and provenance
  - IHU hydrometric areas (UK) as spatial reference units.
  - CEH-GEAR: 1 km resolution daily/monthly areal rainfall estimates used to derive area-averaged rainfall time series for each IHU, enabling SPI computation.
  - Data cited and integrated from Kral et al. (2015) for IHU delineation and Tanguy et al. (2014/2015) for CEH-GEAR rainfall datasets.

- Calculation method and technical notes
  - SPI computed per McKee et al. (1993) using cumulative precipitation over each accumulation period ending in a given month.
  - Gamma distribution fitted to each time series using L-moments (instead of maximum likelihood) due to occasional poor fits; gamma remains widely used in drought studies.
  - Parameter estimation via modified R SCI package to apply L-moments; normalization to standard normal scores.
  - Acknowledges limitations: some UK cases show gamma misfit; alternative distributions (e.g., Pearson-type 3, Tweedie) may perform better in some contexts; future updates may use different distributions.
  - Autocorrelation considerations: overlapping data for longer accumulation periods causes serial correlation; caution advised for trend analyses relying on independence assumptions.

- Temporal and spatial coverage
  - Spatial:  IHUs (hydrometric areas) representing coarsest spatial units in IHU; polyon-based join key provided (POLYGONID).
  - Temporal: 1961–2012 for SPI values; distribution fitting uses 1961–2010 as standard period.
  - Data start year chosen due to CEH-GEAR data density and rainfall data uncertainty pre-1961.

- Format, metadata, and data quality
  - CSV format; 9 columns with clearly defined fields; -9999 indicates No Data.
  - SPI values are unitless and bounded (approximately within -5 to +5 in practice).
  - Serial correlation and overlapping sample issues documented; users should account for these when performing frequency analysis or trend studies.

- Governance and data management implications
  - Clear lineage: CEH-GEAR rainfall inputs, IHU delineations, and SPI computation methodology documented; potential for future versioning if alternative distributions are adopted.
  - Data are prepared for portal integration; POLYGONID facilitates joining with spatial shapefiles for reproducible governance and data discovery.
  - Researchers and data stewards should note distribution choices, data limitations, and autocorrelation when sharing, archiving, or re-using the dataset.

- References (key sources for provenance and methods)
  - Kral, Fry, Dixon (IHU delineation)
  - Tanguy et al. (CEH-GEAR rainfall data)
  - McKee, Doesken, Kleist (SPI definition)
  - Stagge et al. (distributions for drought indices)
  - Gudmundsson & Stagge (SCI package for SPI/SPEI)
  - Haynes et al. Lincoln Declaration on Drought Indices
  - Barker et al. (drought indicators for UK)
  - Svensson et al., Tanguy et al. (ongoing methodological work)
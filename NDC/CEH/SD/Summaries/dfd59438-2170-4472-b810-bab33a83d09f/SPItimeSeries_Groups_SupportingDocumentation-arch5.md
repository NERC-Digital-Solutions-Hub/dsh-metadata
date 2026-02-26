# I. Brief Description of the dataset:

- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups, covering 1961–2012, stored in CSV format.
- SPI calculated for accumulation periods 1, 3, 6, 12, 18, and 24 months, each for all twelve calendar months (72 time series per IHU group).
- The gamma distribution (fitted using L-moments) is used to derive SPI; distribution fitting period is 1961–2010.
- SPI values are transformed to normal scores (mean 0, SD 1), unitless, truncated to -5 to +5. No Data is coded as -9999.
- Dataset built to support a CEH droughts portal by aggregating rainfall SPIs over IHU groups.

- Data sources:
  - IHU groups (Kral et al., 2015) within UK Integrated Hydrological Units.
  - CEH-GEAR rainfall grids (Tanguy et al., 2014; Keller et al., 2015) used to derive area-averaged rainfall time series for each IHU group.

- Data structure and format:
  - CSV file with 9 columns: RID (row ID), POLYGONID (IHU group ID, for shapefile joins), THEDATETIME (date/time), and six SPI columns (one per accumulation period).
  - SPI values are the six normal-score SPI values corresponding to the six durations ending at each month.

- Methodology and notes:
  - SPI for each accumulation period ends in the month of the cumulative period (e.g., 6-month SPI for July 1998 uses precipitation Jan–Jul 1998).
  - Calculation uses the SCI R package (modified to employ L-moments for parameter estimation).
  - Autocorrelation implications: overlapping time periods (especially for >12-month SPI) induce serial correlation; concatenating monthly SPIs can also be autocorrelated.
  - While gamma distribution is widely used, some studies suggest alternatives (e.g., Pearson type 3, Tweedie) may be more appropriate for UK data; current dataset uses gamma with caveats noted.

- Temporal scope and rationale:
  - Standard fitting period: 1961–2010.
  - Derivation period: 1961–2012; earlier data are less reliable due to sparse raingauge coverage in CEH-GEAR.

- Data provenance and usage context:
  - Drought monitoring and spatially explicit drought assessment via the CEH drought portal.
  - SPI interpretation varies by timescale (short-term vs. long-term drought/wetness; guidance on interpretation provided by drought literature).

- Limitations and caveats:
  - Potential non-independence due to overlapping data and serial correlation.
  - Uncertainty in rainfall data prior to 1960s; possible distribution misfit in some cases.
  - Future versions may use alternative distributions if justified.

- Metadata and joinability:
  - POLYGONID enables joining to IHU shapefiles; RID provides row-level identification.
# Supporting Information

## Overview
- Presents the Standardised Precipitation Index (SPI) time series for Integrated Hydrological Units (IHU) groups in the UK, updated from CEH-GEAR rainfall data to Met Office 5km rainfall grids.
- Temporal coverage: 1862–2015 (standard period for gamma fit: 1961–2010).
- SPI is calculated for multiple accumulation periods: 1, 3, 6, 12, 18, and 24 months, each for all twelve calendar months.
- Data are stored as CSV with SPI values transformed to normal scores (mean 0, stdev 1) and truncated at +/-5.
- This dataset supports drought monitoring and analysis via the CEH droughts portal, enabling study of drought/wet periods over specific IHU areas.

## Data provenance and sources
- Data sources:
  - IHU groups (Kral et al., 2015) as the spatial framework.
  - Met Office 5km monthly rainfall gridded data, combining UKCP09 data (1910–2011), unpublished 2012–2015 updates, and Historic Droughts project restorations (1862–1909).
- Underlying rainfall data updated to improve quality of historic precipitation grids, while the SPI calculation methodology remains the same as in earlier work.
- Acknowledgments to the DrIVER and Historic Droughts projects and IMPETUS.

## Methodology and data processing
- SPI computation follows McKee et al. (1993): based on the cumulative probability of precipitation for a given accumulation period ending in a specific month.
- For each location, SPI is calculated for six durations (1, 3, 6, 12, 18, 24 months) across 12 calendar months, yielding 72 time series per location.
- Distribution fitting:
  - Gamma distribution used to model precipitation accumulations (widely used in Europe); parameters estimated with L-moments (via a modified R SCI package to use L-moments instead of MLE).
  - Transformation to a standard normal distribution yields the SPI “normal scores.”
  - Values are truncated at |SPI| > 5.
  - Standard reference period for fitting: 1961–2010.
- Notes on limitations:
  - UK-specific studies suggest gamma may not always be the best fit; alternatives like Pearson type 3 or Tweedie may be more appropriate in some cases.
  - For accumulation periods > 12 months, longer overlapping data can introduce autocorrelation; SPIs for consecutive months may also be autocorrelated due to overlapping data.
  - While SPIs indicate relative severity for a given period, caution is needed when conducting frequency or trend analyses because of serial dependence.

## Data format and contents
- Format: CSV.
- Key columns:
  - RID: row identifier.
  - POLYGONID: IHU group ID (use for joining with IHU shapefiles).
  - THEDATETIME: date/time (end of the accumulation period).
  - Columns 4–9: six temporal aggregations of SPI (as normal scores, unitsless, range roughly within -5 to +5; -9999 indicates No Data).
- Highlights:
  - SPI values are unitless standardized scores (mean 0, stdev 1).
  - Range limitation: typically within -5 to +5.
  - Data reflect six aggregation periods across twelve months, producing multiple time-series per location.

## Quality, limitations, and governance considerations
- Data quality and interpretation:
  - Dependence on historic, digitised rainfall data; distribution choice (gamma) and potential model misfit in some UK regions.
  - Autocorrelation considerations for long-duration SPIs and for serially concatenated series; impact on trend or frequency analyses.
- Data management:
  - Versioning is important due to underlying rainfall data updates (switch from CEH-GEAR to Met Office grids); maintain provenance and change logs.
  - Metadata should support join operations with IHU group definitions via POLYGONID.
  - Documentation should clearly state the standard fitting window (1961–2010) and the data period (1862–2015) along with any caveats.
- Reuse guidance:
  - Suitable for drought portal analytics, historical drought/wetness mapping, and multi-scalar drought assessment, with appropriate statistical treatment for autocorrelation in trend analyses.

## Governance and stewardship considerations
- Ensure reproducibility by preserving:
  - The exact underlying rainfall data source and version.
  - The SPI calculation method (gamma with L-moments, SCI package modification).
  - The fitting window (1961–2010) and the handling of out-of-range values.
- Plan for future updates:
  - If alternative distributions are adopted, clearly version and document the change.
  - Maintain a changelog describing data source updates and any methodological refinements.
- Data accessibility:
  - Use POLYGONID for reliable joins to spatial shapefiles; provide clear user guidance for integrating with GIS workflows.
  - Document data availability and any embargo or access restrictions.

## References
- Barker, L.J., Hannaford, J., Svensson, C., Tanguy, M. (2015). A preliminary assessment of meteorological and hydrological drought indicators for application to catchments across the UK.
- Gudmundsson, L. & Stagge, J. H. (2014). Package 'SCI': Standardized Climate Indices such as SPI, SRI or SPEI.
- Hayes, M., Svoboda, M., Wall, N., Widhalm, M. (2011). The Lincoln Declaration on Drought Indices: Universal Meteorological Drought Index Recommended.
- Keller, V. D. J., et al. (2015). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
- Kral, F., Fry, M., Dixon, H. (2015). Integrated Hydrological Units of the United Kingdom: Groups.
- McKee, T. B., Doesken, N. J., Kleist, J. (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- National Drought Mitigation Center (2015). Interpretation of Standardized Precipitation Index Maps.
- Stagge, J. H., et al. (2015). Candidate Distributions for Climatological Drought Indices (SPI and SPEI).
- Svensson, C., Hannaford, J., Prosdocimi, I. (2016). Statistical distributions for monthly aggregations of precipitation and streamflow in drought indicator applications.
- Tanguy, M., Kral., F., Fry, M., Svensson, C., Hannaford, J. (2015). Standardised Precipitation Index time series for Integrated Hydrological Units Groups (1961-2012). 
- Tanguy, M., Dixon, H., Prosdocimi, I., Morris, D. G., Keller, V. D. J. (2014). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2012) [CEH-GEAR].
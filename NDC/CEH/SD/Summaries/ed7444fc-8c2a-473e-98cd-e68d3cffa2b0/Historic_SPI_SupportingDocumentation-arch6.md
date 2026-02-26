# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## Overview
- Provides 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom from 1862 to 2015.
- SPI is a drought index based on precipitation probability across multiple accumulation periods.
- Outputs are prepared to support spatial analysis of droughts, their propagation, and identification of affected areas.

## Data and scope
- Accumulation periods: 1, 3, 6, 12, 18, 24 months; each period has 12 calendar months, yielding 72 time series per grid cell.
- Standard period for fitting the distribution: 1961-2010.
- Data format: NetCDF4, 2D grids covering the UK; British National Grid projection.
- Output values: SPI normal scores (mean 0, standard deviation 1), unitless; range limited to -5 to +5.
- Temporal coverage: 1862–2015.

## Data sources
- Met Office 5 km monthly rainfall grids.
- Data composition: UKCP09 data (1910–2011), unpublished 2012–2015 updates, and historic rainfall data (1862–1909) rescued for the Historic Droughts project.

## Methodology
- SPI calculation follows McKee et al. (1993): for each location and accumulation period, build a time series from monthly precipitation totals ending in the month of interest.
- A gamma distribution is fitted to each time series using L-moments (via a modified R SCI package) to estimate parameters.
- Transformation to normal scores yields SPI values with no units.
- Extreme values (|SPI| > 5) are truncated to the +/-5 limit.
- Note: for accumulation periods >12 months, overlapping data introduce autocorrelation; SPIs, while indicating drought/severity for a period, are not independent for frequency analysis.
- Serial correlation considerations: concatenation of successive SPIs can be highly autocorrelated; use caution for trend analyses.

## Data format and structure
- File structure: one NetCDF4 file per accumulation period; each file contains 12 monthly grids per year.
- Spatial structure: UK-wide grids at 5 km resolution, projected on the British National Grid.
- Data conventions: CEH gridded dataset conventions.
- Outputs are the “normal scores” SPI values, without physical units.

## Usage considerations
- Appropriate for cross-disciplinary drought analysis, spatial drought mapping, and identifying regions with extreme moisture deficits or excess rainfall.
- Useful to study drought propagation over time and across space, and to inform water management and drought planning.
- Users should account for potential autocorrelation in long-duration SPIs and consider alternative distributions (e.g., Pearson type 3, Tweedie) for future updates, as gamma may not always be the best fit for UK data.

## Acknowledgments
- Historic Droughts project (NERC grant NE/L01016X/1).
- DRIVER project (NE/L010038/1) and IMPETUS (NE/L010267/1).
- Collaboration enables digitisation and provision of historic rainfall data for UK drought analysis.

## References
- Barker, L.J., Hannaford, J., Svensson, C., Tanguy, M. (2015). A preliminary assessment of meteorological and hydrological drought indicators for application to catchments across the UK.
- Gudmundsson, L. & Stagge, J. H. (2014). Package 'SCI': Standardized Climate Indices such as SPI, SRI or SPEI.
- Hayes, M. et al. (2011). The Lincoln Declaration on Drought Indices: Universal Meteorological Drought Index Recommended.
- Keller, V. D. J. et al. (2015). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK.
- McKee, T. B. et al. (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- National Drought Mitigation Center (2015). Interpretation of Standardized Precipitation Index Maps.
- Stagge, J. H. et al. (2015). Candidate Distributions for Climatological Drought Indices (SPI and SPEI).
- Svensson, C. et al. (2017). Statistical distributions for monthly aggregations of precipitation and streamflow in drought indicator applications.
- Tanguy, M. et al. (2015). Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961–2010 for Great Britain.
- Tanguy, M. et al. (2014-2015). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (CEH-GEAR).
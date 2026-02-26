# About the UK Butterfly Monitoring Scheme

## Overview
- Jointly organized and funded by Butterfly Conservation, Centre for Ecology and Hydrology (CEH), British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- Relies on volunteer data and has monitored butterfly populations in the UK since 1976.
- Aims to provide annual population status and trend information to inform biodiversity policy and status assessments.
- Data collection is multi-component and site-based, including:
  - Standard butterfly transects (Pollard walks)
  - Reduced effort surveys (single-species transects and alternative methods)
  - Wider Countryside Butterfly Survey (WCBS)

## Nature of data collected and trend analysis
- Data are used to create abundance indices (relative measures) rather than absolute counts.
- Indices combine counts from all components to produce species-wide trends, using the Generalised Abundance Index (GAI) with weighting by the proportion of the flight period surveyed.
- All counts from a season are used to estimate seasonal patterns and to extrapolate for gaps, with observed data weighted more heavily than extrapolated data.
- Outputs include long- and short-term trends for all species with sufficient data, provided as CSV files.
- Key metrics in the download:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years in the trend)
  - F_LIN_B / F_LIN_SE / F_LIN_P (overall trend slope, its SE, and P-value)
  - F_TRENDETAIL (trend description: Rapid decline, Rapid increase, or Stable)
  - F_FULL_R (overall percent change)
  - T20_LIN_B / T20_LIN_SE / T20_LIN_P / T20_TRENDDETAIL / T20_20_R (20-year trend metrics)
  - T10_LIN_B / T10_LIN_SE / T10_LIN_P / T10_TRENDDETAIL / T10_10_R (10-year trend metrics)

## Quality control
- Field data collected on standard forms; entered online via the UKBMS data entry site or via Transect Walker before uploading to a central database.
- Automated checks flag data entry errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators validate data and monitor for questionable records throughout the season.
- After preliminary validation, further automated and manual validation steps assess distributions, flight periods, site introductions, extreme or unexpected counts.
- Corrections are implemented through queries and coordination with recorders/transit coordinators, with edits applied to the main UKBMS dataset.

## Details of this data download
- Provides long- and short-term trends for all species with sufficient data.
- Data delivered as a CSV file.
- Column descriptions include:
  - Vernacular and scientific names (COMMON_NAME, SCI_NAME)
  - NYEARS (years in the series)
  - Trend metrics (F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL)
  - Overall change (F_FULL_R) and recent-period trends (T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R)
  - 10-year equivalents (T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R)

## Licence and attribution
- Data download is provided under the Open Government Licence (OGL), permitting free use with few conditions.
- Citations and the Digital Object Identifier must be included in publications using the data.
- Attribution statement to be included: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners offer advisory support and interpretation assistance.
- Opportunities for co-authorship and intellectual input in publications resulting from UKBMS data.
- Contact:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - CEH: Marc Botham (ukbms@ceh.ac.uk)
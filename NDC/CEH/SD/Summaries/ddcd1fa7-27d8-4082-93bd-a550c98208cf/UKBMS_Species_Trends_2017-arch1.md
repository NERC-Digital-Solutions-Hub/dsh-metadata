# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with substantial volunteer contributions.
- It provides annual, site-based monitoring data plus sampling in randomly selected 1 km squares to track butterfly population status across the UK since 1976.
- The scheme includes three sampling components:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts across a 5 m band from April–September; ~2000 sites.
  - Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts focusing on specific species or methods.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel 1-km transects with 2–4 visits per year (primarily for common habitats like farmland); ~750 squares annually.
- Results from components are integrated to form comprehensive species trends and inform biodiversity policy questions.

## Nature of data collected and trend analysis

- Data are summarized as abundance indices (relative measures of population size) rather than absolute counts, reflecting the proportion of butterflies observed at a site.
- A Generalised Abundance Index (GAI) method (2016) combines site indices into species-level collated indices, weighting site-year data by the proportion of the species’ flight period surveyed to emphasize observed data over extrapolated data.
- The seasonal pattern is estimated from all season counts (Pollard walks, reduced surveys, WCBS) to account for gaps and provide robust trend estimates.
- Foundational references: Pollard & Yates (1993) and Dennis et al. (2016).

## Quality control

- Field data are recorded on standard forms and entered online or via Transect Walker, then uploaded to a central database.
- Automated and manual validation steps include checks for extreme counts, out-of-period records, and records outside known ranges; regional coordinators review data for questionable entries.
- Ongoing quality assurance involves queries and discussions with coordinators/recorder to correct errors before final integration.

## Details of this data download

- Provides long- and short-term trends in collated indices for all species with sufficient data, delivered as a CSV file.
- Columns include:
  - COMMON_NAME (vernacular, per Emmet & Heath)
  - SCI_NAME (scientific name, Fauna Europaea v2.2)
  - NYEARS (number of years in the series)
  - F_LIN_B, F_LIN_SE, F_LIN_P (linear trend slope, its SE, and P-value for all-years trend)
  - F_TRENDETAIL (trend description for the full series)
  - F_FULL_R (percent change over the full series)
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year trend metrics and description)
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year trend metrics and description)
- Descriptive notes clarify naming conventions and data sources within the UKBMS framework.

## Licence and attribution statement

- The data download is provided under the Open Government Licence (OGL), enabling free use with minimal conditions.
- Citations and DOIs must be included in reports/publications using the data.
- Attribution statement to be included with any derived information or images: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer advisory support on dataset usage and interpretation, with openness to co-authorships and intellectual input for scientific outputs.
- Primary contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
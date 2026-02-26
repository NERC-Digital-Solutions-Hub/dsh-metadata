# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is a collaborative, long-running program coordinated by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with extensive volunteer participation.
- Purpose: provide annual, site-based population status data for butterflies to support biodiversity monitoring and policy questions.
- Since 1976, UKBMS has monitored changes across the United Kingdom with data from around 2,500 active sites each year.

## Data collection and spatial scope

- Three complementary sampling methods:
  - Standard butterfly transects (Pollard walks): fixed routes (2–4 km), 26 counts per year from April to September, covering a 5 m wide band; almost 2,000 sites sampled annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares; two parallel 1 km transects, 2–3 visits per year (minimum 2 visits in July/August), ~750 squares sampled annually.
  - Targeted surveys: single-species transects, timed counts, egg/larval web counts, and other non-transect methods focused on specific species.
- Spatial data are organized at multiple scales (sites and 1 km squares), enabling both fine-grained and landscape-level analyses.
- All sampling methods are analyzed together to provide species-level insights.

## Data processing and trend analysis

- Abundance indices are relative measures derived from counts rather than absolute population sizes.
- Collated species indices are produced using the Generalised Abundance Index (GAI) method (2016) with an adjustment weighting each site-year by the proportion of the species’ flight period surveyed, ensuring observed data have greater influence than extrapolated data.
- The seasonal pattern is estimated from all counts (Pollard walks, reduced surveys, WCBS) to extrapolate gaps and produce a robust annual index per species.

## Quality control

- Field data are collected on standard forms and entered online via the UKBMS data entry system or Transect Walker.
- Automatic checks flag unusual counts or records outside known flight periods; regional transect coordinators perform ongoing validation.
- Additional validation queries screen for species outside known distributions, atypical flight times, first-time site records, and extreme abundances; edits are applied to the main UKBMS dataset as needed.

## Details of this data download

- Provides long-term and short-term trends in collated indices for all species with sufficient data, as CSV files.
- Long-term series run from 1976 to the year indicated in the file name; some species start later due to data gaps.
- Key columns include:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years in the series)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL, F_FULL_R (long-term slope, its SE, p-value, trend detail, and percent change)
  - T20_LIN_B/SE/P, T20_TRENDDETAIL, T20_20_R (20-year slope, trend description, percent change)
  - T10_LIN_B/SE/P, T10_TRENDDETAIL, T10_10_R (10-year slope, trend description, percent change)
- File format: comma-separated values (.csv)

## Licence and attribution

- Data are provided under the Open Government Licence (OGL), enabling free use with minimal conditions.
- Required: proper citation (including DOI) in any reports or publications describing research using the data.
- Attribution statement to include with data-derived outputs: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS partners offer advisory support and interpretation assistance.
- Co-authorship and intellectual input on scientific outputs are welcome.
- Contacts:
  - UK Centre for Ecology & Hydrology — Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation — Transect co-ordinator: transect@butterfly-conservation.org

## GIS-oriented notes for map-based data products

- Rich, map-ready potential: site-level and 1 km square data enable spatial visualization of trends across the UK.
- Data products include species-specific indices and trends (long-term, 20-year, and 10-year), suitable for thematic mapping, time-series dashboards, and corridor/landscape analyses.
- Caution: indices are relative abundance measures, not absolute counts; consider metadata on detection probability and flight-period coverage when interpreting maps.
- Data quality and provenance are well-documented, with automated and manual validation steps, enhancing reliability for GIS analyses.

## Practical considerations and limitations

- Data gaps exist for earlier years for some species; start years vary by species based on data sufficiency.
- Indices depend on multiple sampling methods; harmonization relies on the GAI approach with weighting to emphasize observed data.
- While highly useful for trend mapping and policy-relevant visuals, users should be mindful of detection biases and the relative nature of abundance indices.
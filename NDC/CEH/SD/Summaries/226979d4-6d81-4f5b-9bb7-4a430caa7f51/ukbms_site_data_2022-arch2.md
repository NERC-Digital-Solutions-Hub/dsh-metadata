# UK Butterfly Monitoring Scheme

## Aim and context for analysis
- Provides annual, site-based data on butterfly population status to support assessment of environmental health and biodiversity policy performance over time.
- Coordinated by Butterfly Conservation, CEH, BTO, and JNCC with volunteer contributors; active since 1976, covering over 3000 sites annually.
- Outputs are used to understand trends and inform policy, with data and outputs presented via reports, maps, and charts.

## Data collection and methods (nature of data)
- Sampling framework includes:
  - Standard butterfly transects (Pollard walks): fixed-route transects, 2–4 km, 5 m wide band, weekly counts (up to 26 per year).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel transects, 2–3 visits per year.
  - Targeted surveys: single-species transects, timed counts, egg/larval counts, and other methods for specific species.
- Data from all sampling methods are combined for analysis.
- Types of data yield abundance indices (relative measures) rather than absolute population sizes.

## Trend analysis and indices
- Indices are derived from counts along transects to form site indices, reflective of a constant proportion of actual population; detection varies by species.
- Overall species indices (collated indices) produced using the Generalised Abundance Index (GAI) method (developed 2016) with a weighting scheme:
  - Data from each site/year weighted by the proportion of the species’ flight period surveyed.
  - Seasonal patterns estimated from all counts (Pollard walks, WCBS, reduced surveys) to extrapolate gaps, with observed data given more weight than extrapolated data.

## Quality control and data integrity
- Field data recorded on standard forms and entered online via the UKBMS data site or Transect Walker.
- Automated checks flag potential errors (e.g., unusually high counts, records outside flight periods); regional coordinators review data throughout the season.
- Further validation checks target records of out-of-range distributions, atypical abundances, first-time site records, or large deviations; corrections made via queries and coordinator/recorder input.

## This data download: scope and content
- Provides location and attribute data for UK sites monitored under UKBMS from 1976–2022; sensitive sites omitted.
- Format: comma-separated (.csv) file.
- Key columns and meanings:
  - Site_number, Site_name, Gridreference, Easting, Northing
  - Length, Country, N_Sections
  - N_Yrs_surveyed, First_year_surveyed, Last_year_surveyed
  - Survey_type (UKBMS vs WCBS)

## Licence and attribution
- Data released under Open Government Licence (OGL) for free use and reuse with few conditions.
- Must include citation details (DOI) in references and attribution: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.”
- Since 2017, submitters consented to data being available under OGL; note possible historic data IP constraints for some records.

## Collaboration and contact
- UKBMS partners offer advisory support and collaboration, including co-authorship opportunities for resulting publications.
- Contacts:
  - Marc Botham, UKBMS, ukbms@ceh.ac.uk
  - Butterfly Conservation Transect Co-ordinator, transect@butterfly-conservation.org

## Key challenges and analyst implications
- Increasing the value of datasets by integrating UKBMS data with other relevant environmental data (beyond single-use analyses).
- Enhancing access to the underlying data to enable broader scrutiny, replication, and policy-relevant analyses.
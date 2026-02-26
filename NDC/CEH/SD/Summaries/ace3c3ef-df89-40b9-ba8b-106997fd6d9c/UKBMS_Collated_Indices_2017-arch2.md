# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee. It relies on volunteers and has operated since 1976, monitoring butterfly population changes across the UK with data from over 2,500 actively recorded sites each year.
- Purpose: provide annual population status data to understand biodiversity trends and inform policy questions.

## Purpose and scope

- Combines site-based monitoring with random-squares sampling to produce standardized, comparable data over time.
- Data support analysis of population trends and policy-relevant biodiversity questions.
- Results from different components are analyzed together to produce unified species indices.

## Data collection and components

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide recording all species weekly from April to September (about 26 counts/year), across almost 2,000 sites.
- Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts focusing on particular species or life stages.
- Wider Countryside Butterfly Survey (WCBS): uses the same transect method as Pollard walks but with stratified-random 1 km squares; 2–4 visits per square (including July/August and some springs), around 750 squares sampled annually.
- All components feed into a single UKBMS dataset; data from Pollard, reduced surveys, and WCBS are combined for analyses.

## Nature of data and trend analysis

- Outputs are abundance indices (relative measures of population size), not absolute counts.
- Site indices reflect a constant proportion of the population at each site; detectability varies by species.
- Collated species indices are produced using the Generalised Abundance Index (GAI) method (2016) with a site-by-year weighting that accounts for the proportion of the species’ flight period surveyed; uses all counts to model seasonal patterns and extrapolate to gaps, with observed data weighted more heavily than extrapolated data.

## Quality control

- Field data recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker.
- Automatic checks flag potential errors (e.g., abnormally high counts, records outside known flight periods).
- Regional transect coordinators review data; ongoing validation during the season.
- Further automated/manual validation checks for records outside distribution ranges, out-of-period records, first-time site records, or anomalous abundances; corrections are applied through queries and coordination with recorders.

## Details of this data download

- Contains annual collated indices of abundance for species with sufficient data from 1976–2017 (early years may be missing for some species due to insufficient data).
- Format: CSV file.
- Columns described:
  - SPECIES CODE: unique numeric code per species
  - SPECIES: scientific name (Fauna Europaea, v2.2)
  - COMMON NAME: vernacular names (Emmet & Heath, 1990)
  - YEAR: year of the Collated Index
  - NO. SITES: number of sites contributing to the index that year
  - COLLATED INDEX: log10 of the Collated Index (LCI), scaled so the average across the series equals 2
  - YEAR RANK: year’s rank of the Collated Index for that species (1 = best year)
  - TIME PERIOD: time period used to produce the indices
  - COUNTRY: country source for regional collated index

## Licence and attribution

- Data is provided under an Open Government Licence (OGL).
- Must include citation with the dataset’s DOI in any reports/publications using the data.
- Attribution statement to accompany derived information: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS Partners offer guidance on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conferences, or posters resulting from UKBMS data.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee. Volunteers contribute the data.
- Purpose: provide annual data on butterfly population status to understand changes and answer policy questions related to biodiversity status and trends.
- Operational history: monitoring since 1976 with over 2,500 actively recorded sites each year.

## Data collection and sampling framework
- Components:
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km), ~5 m wide band, 26 counts per year from April to September.
  - Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares with two parallel transects, 2–4 visits per year.
- Scale:
  - >2,000 standard transects; WCBS ~750 squares annually.
- Data capture:
  - Field data recorded on standard forms, then entered online using UKBMS MyData or Transect Walker software; uploaded to a central database.
- Data flow:
  - Regional transect coordinators validate and quality-check data throughout the season.

## Nature of data and trend analysis
- Data are analyzed as abundance indices (relative measures) rather than absolute population sizes.
- Indices are produced by combining site indices across transects and years using the Generalised Abundance Index (GAI) method (2016), with weighting by the proportion of the species flight period observed at each site each year.
- The method uses all counts in a season to estimate the seasonal pattern and accounts for gaps in recording, giving more weight to observed data.

## Quality control
- Multi-stage validation:
  - In-field checks and online data-entry checks for aberrant counts or out-of-season records.
  - Regional coordinators review records; automated and manual validation procedures run after data entry.
  - Additional queries check distribution range, flight period, first records at a site, and unusual abundances; edits are made to the main dataset as needed.

## Details of this data download
- Content: annual collated indices of abundance for UK butterfly species with sufficient data, from 1976 to 2018 (some early years excluded due to insufficient data).
- Format: CSV file.
- Columns:
  - SPECIES CODE: numeric identifier
  - SPECIES: scientific name (Fauna Europaea, v2.2)
  - COMMON NAME: vernacular name (Emmet & Heath, Moths and Butterflies of GB&Ireland)
  - YEAR: year of the collated index
  - NO. SITES: number of sites contributing
  - COLLATED INDEX: log10 collated index (LCI), scaled so the average over the series equals 2
  - YEAR RANK: rank of CI value within the species’ years
  - TIME PERIOD: time period used to produce the indices
  - COUNTRY: country data used for regional indices
- Note: collated indices were not calculated for some early years due to data insufficiency.

## Licence and attribution statement
- Licence: Open Government Licence (OGL), allowing free use and reuse with few conditions.
- Citation: include the dataset citation and DOI in any publications using the data.
- Attribution: include the statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, Centre for Ecology & Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee.”

## Offer of collaboration and contact details
- The UKBMS partners offer advisory support and interpretation assistance, potential co-authorship, and collaboration for publications, conferences, or posters.
- Contacts:
  - Tom Brereton (Butterfly Conservation): tbrereton@butterfly-conservation.org
  - Marc Botham (Centre for Ecology & Hydrology): ukbms@ceh.ac.uk
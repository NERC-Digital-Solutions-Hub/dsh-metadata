# About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- It has collected annual data on butterfly population status since 1976, with over 3,000 sites actively recorded each year.
- Data from all sampling methods are analyzed together to understand biodiversity trends and inform policy questions.

## Data collection methods
- Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km) with a 5 m wide band, weekly counts from April to September (up to 26 counts/year); typically 45 minutes to 2 hours per walk; 2,000+ sites by 2022.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects; 2–3 visits per year (min. 2 visits in July/August); ~800 squares sampled per year.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, eggs and larval webs) focused on particular species.

## Nature of data and trend analysis
- Data are used to create abundance indices (relative measures) rather than absolute population sizes.
- Collated indices for each species are produced using the Generalised Abundance Index (GAI) method (2016) with a weighting adjustment reflecting the proportion of the flight period surveyed at each site/year.
- All counts from Pollard walks, WCBS, and reduced surveys inform a seasonal count pattern used to extrapolate gaps and derive year-specific indices; weighting emphasizes observed data over extrapolated data.

## Quality control
- Field data are collected on standard forms and entered online via the UKBMS data entry site or Transect Walker.
- Automatic checks flag potential errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators validate data; ongoing checks during the season; additional automated and manual validation ensures records are plausible (e.g., distribution range, flight period, new site records).
- Any data edits are discussed with coordinators or recorders before updating the main dataset.

## Details of this data download
- Provides annual collated indices of abundance for species with sufficient data from 1976–2022 (not all early years have collated indices due to data limitations).
- Format: comma-separated values (.csv).
- Key columns:
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name
  - COMMON_NAME: common name
  - YEAR: year of the collated index
  - N_SITES: number of contributing sites
  - COLLATED_INDEX: log10 of the Collated Index, scaled so the series average equals 2
  - YEAR_RANK: year-specific rank of the collated index for the species
  - TIME_PERIOD: time period used for the indices
  - COUNTRY: country data used for regional indices
- Descriptions and taxonomy follow established checklists and references.

## Licence and attribution statement
- Distributed under an Open Government Licence (OGL), permitting free use with few conditions.
- Must include citation with DOI as specified in the metadata record when describing research using the data.
- Attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners can advise on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conferences, or posters resulting from UKBMS data.
- Contact:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org
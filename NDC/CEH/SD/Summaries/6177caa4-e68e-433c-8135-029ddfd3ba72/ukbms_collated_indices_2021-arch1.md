# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: provide annual data on butterfly population status across the UK to inform biodiversity policy questions and track changes since 1976.
- Population sampling framework:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m wide band, weekly counts (ideally 26 per year) across ~2,000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel 1 km transects, 2–3 visits per year (targeting common habitats, ~800 squares/year).
  - Targeted surveys: single-species transects, alternative methods, including timed counts and egg/larval web counts.
- Data integration: data from all sampling methods are combined for analysis to produce species- and site-level indices.
- Data collected since 1976: ongoing, large-scale, site-based monitoring with over 2,500 active sites annually (at least in later years).

## Nature of data collected and trend analysis

- UKBMS produces abundance indices (relative measures of population size, not absolute counts).
- Collation method: Generalised Abundance Index (GAI, 2016) with a weighting scheme that emphasizes observed counts proportional to the species’ flight period sampled at each site/year.
- The GAI-based method uses counts from all methods to estimate seasonal patterns and extrapolate gaps, with greater weight given to observed data over extrapolated data.
- Indices allow comparisons over time and across sites, and have shown relation to more intensive measures like mark-release-recapture.

## Quality control

- Field data recorded on standard forms, entered online via UKBMS MyData or Transect Walker, then uploaded to a central database.
- Built-in automatic checks flag abnormally high counts or out-of-season records; coordinators review and may adjust.
- Regional transect coordinators validate data throughout the season; additional automated and manual validations check:
  - Records outside known distribution or out of flight period
  - First-time records at a site
  - Extreme or unusual abundances
- Any data edits are documented; corrections are made to the main UKBMS dataset after review.

## Details of this data download

- Contains annual collated indices of abundance for UK species with sufficient data from 1976–2021 (some earlier years excluded due to limited data).
- File format: comma-separated values (.csv).
- Columns described:
  - SPECIES CODE: unique numeric code per species
  - SPECIES: scientific name (taxonomy references cited)
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - NO. SITES: number of sites contributing to the index
  - COLLATED INDEX: the Collated Index (CI), presented as log10(CI) and scaled so the series average equals 2
  - YEAR RANK: rank of CI within the species’ years of data (1 = best year)
  - TIME PERIOD: period used to generate the CI
  - COUNTRY: country origin of regional CI
- Notes: Indices are relative; some species have different detectability (e.g., Marbled White vs. Dingy Skipper). Data include references to supporting methodologies and taxonomic checklists.

## Licence and attribution statement

- Data are provided under the Open Government Licence (OGL), permitting free use with minimal conditions.
- Must cite the dataset with the DOI as provided in the metadata record.
- Attribution: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, Centre for Ecology & Hydrology, British Trust for Ornithology, and Joint Nature Conservation Committee.”

## Offer of collaboration and contact details

- UKBMS partners offer collaboration and interpretation support; co-authorship and intellectual input in publications are welcome.
- Contacts:
  - UK Centre for Ecology & Hydrology – Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation – Transect Co-ordinator: transect@butterfly-conservation.org
# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with substantial volunteer contributions.
- Purpose: provide annual data on butterfly population status from a wide-scale, site-based monitoring program to inform biodiversity status and policy questions.

## What it is and how it works (GIS-relevant structure)

- Spatial sampling framework comprises:
  - Standard butterfly transects (Pollard walks) at sites chosen by recorders; monitored weekly (up to 26 times/year) along fixed routes, typically 2–4 km, within a 5 m wide band.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects; 2–3 visits/year to sample common habitats.
  - Targeted surveys: single-species transects or alternative methods (timed counts, egg/larval web counts) for specific species.
- Coverage: UK-wide with data from over 3,000 active sites annually; WCBS samples around 800 squares/year.
- Data from all sampling methods are analyzed together to produce national and species-level indices.

## Data content and indices (how data are represented)

- Data are abundance indices (relative measures) rather than absolute counts.
- Site indices reflect a constant proportion of butterflies at a site; detectability varies by species.
- Collated indices for species are produced using the Generalised Abundance Index (GAI) with a weighting adjustment so site-year data are weighted by the proportion of the species flight period surveyed.
- The seasonal pattern across counts is used to estimate annual indices and account for recording gaps; observed data have a stronger influence than extrapolated data.
- Time span for downloadable data: 1976–2022 (where data are sufficiently complete in the latest year).

## Data quality and validation (ensuring GIS-ready data)

- Field data collection on standard forms; online entry via UKBMS data site or Transect Walker; uploaded to a central database.
- Automatic checks during entry (e.g., unusually high counts, out-of-season records).
- Regional coordinators review records; ongoing validation throughout the season.
- Additional automated/manual validation checks against known distributions and flight periods; discrepancies are queried and corrected before final dataset updates.

## Details of this data download (how to use it in GIS)

- Content: annual collated indices of abundance for each species with sufficient data (1976–2022 where available).
- File format: comma-separated values (.csv).
- Columns and meanings:
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per latest taxonomic checklists)
  - COMMON_NAME: vernacular name
  - YEAR: year of the collated index
  - N_SITES: number of sites contributing to the index that year
  - COLLATED_INDEX: log10 of the collated index, scaled so the mean equals 2
  - YEAR_RANK: year-specific rank of the collated index for the species
  - TIME_PERIOD: data period used for the collated index
  - COUNTRY: country context for regional collated index
- Notes: indices are relative and provide a consistent basis for temporal trend analysis across the UK.

## Licence and attribution

- Licence: Open Government Licence (OGL) for free use and reuse with few conditions.
- Citation requirements: include the provided citation and DOI in publications using the data.
- Attribution: contains UKBMS data © Butterfly Conservation, CEH, BTO, JNCC; include the attribution statement when distributing information or images derived from the data.

## Offer of collaboration and contact details

- UKBMS Partners offer guidance on dataset details and interpretation of outputs.
- Collaboration: potential co-authorship and intellectual input for publications, conference materials, etc.
- Contacts:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation: transect@butterfly-conservation.org
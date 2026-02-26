# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee, with credit due to volunteers contributing data since 1976.
- It provides annual data on butterfly population status across the UK, combining site-based monitoring with random 1 km square sampling, and is used to understand biodiversity trends and inform policy questions.
- The scheme features multiple components that are analyzed together to produce overall indicators of butterfly abundance.

## Nature of data collected and trend analysis
- Data are summarized as abundance indices, representing relative, not absolute, population size.
- Indices are derived from counts along transects and from other survey methods, then combined into species-specific collated indices using the Generalised Abundance Index (GAI) with a weighting that emphasizes observed data proportional to the surveyed flight period.
- The UKBMS integrates data from standard transects (Pollard walks), reduced-effort surveys (single-species transects, timed counts, egg/larval web counts), and the Wider Countryside Butterfly Survey (WCBS).
- WCBS uses stratified-random 1 km square sampling with two parallel transects per square and fewer visits, enhancing sampling of common habitats; WCBS started in 2009 and currently samples around 750 squares annually.
- The scheme covers over 2,000 standard transect sites each year, with ongoing development of methods to account for sampling gaps and ensure robust trend estimates.

## Quality control
- Data are collected on standard forms and entered into the UKBMS database via online systems or custom software (Transect Walker).
- Automatic checks flag potential errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review data, performing continuous validation throughout the season.
- Further automated and manual validation screens ensure records are within known distributions, flight periods, and expected abundances; discrepancies are resolved through data queries and communications with recorders.

## Details of this data download
- Provides annual collated indices of abundance for UK butterfly species with sufficient data from 1976–2018 (some early years excluded due to data gaps).
- Data are delivered as a CSV file with columns:
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (as per Fauna Europaea)
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - NO. SITES: number of sites contributing to the index that year
  - COLLATED INDEX: log10 of the collated index; scaled so the average across all years is 2
  - YEAR RANK: rank of the year for that species (1 = best year)
  - TIME PERIOD: time period used to compute the indices
  - COUNTRY: country used for regional indices
- The collated index provides a relative measure of population changes over time.

## Licence and attribution statement
- The dataset is provided under the Open Government Licence (OGL).
- Users must include the required citation with any publications, including the DOI, and include the attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners offer guidance on dataset interpretation and potential collaboration, including co-authorship opportunities for publications or presentations.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
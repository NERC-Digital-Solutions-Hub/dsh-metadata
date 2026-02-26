# About the UK Butterfly Monitoring Scheme

- A collaborative program funded and organized by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee. Volunteers contribute data.
- Purpose: produce annual population status data for UK butterflies to understand trends and inform biodiversity policy.
- History: operational since 1976, with over 2,500 active sites each year.
- All components are analyzed together to produce unified indicators.

## Data collection and components

- Sampling framework includes:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m wide band, weekly counts Apr–Sept, ~26 counts/year at ~2,000 sites.
  - Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel 1 km transects, 2–4 visits per year (July/August emphasized), ~750 squares/year.
- All components use similar transect methodology and feed into a common UKBMS dataset.
- Data collection methods emphasize habitat variation and species-specific survey approaches.

## Data processing: indices and methods

- Data are abundance indices (relative measures, not absolute counts).
- Site indices reflect a constant proportion of individuals observed; detectability varies by species.
- Collated indices per species use the Generalised Abundance Index (GAI) methodology (2016) with a weighting scheme:
  - Data from each site/year weighted by the proportion of the species’ flight period surveyed.
  - All seasonal counts are used to model the seasonal pattern and extrapolate gaps, with observed data given more influence than extrapolated data.

## Quality control and validation

- Field data captured on standard forms, entered online via UKBMS data entry site or Transect Walker, then uploaded to a central database.
- Automated checks flag improbable entries (e.g., unusually high counts, records outside flight periods).
- Regional transect coordinators review and validate data; validation continues during the season.
- Additional automated/manual checks assess distributional plausibility, abnormal timing, first-time site records, and extreme values.
- Corrections are performed via targeted queries; edits are applied to the main UKBMS dataset as needed.

## Data download details

- This download provides annual collated indices of abundance for species with sufficient data from 1976–2017 (some early years excluded due to data gaps).
- Data delivered as a CSV with columns:
  - SPECIES CODE, SPECIES (scientific name), COMMON NAME
  - YEAR, NO. SITES
  - COLLATED INDEX (log10 scale; average standardized to 2)
  - YEAR RANK, TIME PERIOD, COUNTRY
- TIME PERIOD indicates data used to produce the collated indices; COUNTRY reflects the regional data source.

## Licence and attribution

- Data are provided under the Open Government Licence (OGL).
- Citations/DOIs must be included in publications using the data.
- Attribution to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact

- UKBMS partners offer advice on dataset details and interpretation; open to collaboration and co-authorship on publications.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
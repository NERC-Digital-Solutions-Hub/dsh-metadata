# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- It provides annual data on butterfly population status across the UK from site-based monitoring, using multiple sampling methods and a long-running history since 1976.
- Over 2,500 sites are actively recorded each year, and all data collection methods are analyzed together to understand trends and inform biodiversity policy.

## Data collection and structure relevant to GIS

- Sampling frameworks include:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide counts, up to 26 visits per year.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year.
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts.
- Data are processed to produce abundance indices (relative measures rather than absolute counts). Indices are derived from counts across all methods and years.
- The Generalised Abundance Index (GAI) method is used to combine site indices into collated indices per species, with weighting by the proportion of the species flight period surveyed each year to emphasize observed data.
- Geographic scope includes site-level data and country-level summaries; the dataset discussed here includes annual collated indices for species across the UK, with data contributed from multiple site types.

## Quality control

- Field data are recorded on standard forms and entered online or via Transect Walker before database upload.
- Built-in automatic checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators perform ongoing verification and validation, supplemented by automated and manual validation procedures.
- Data corrections are performed via queries and discussions with coordinators or recorders as needed.

## Details of this data download

- Data cover annual collated indices of abundance for each species in the UK from 1976–2019 (some earlier years lack collated indices due to insufficient data).
- File format: CSV.
- Columns include:
  - SPECIES CODE (unique numeric code)
  - SPECIES (scientific name)
  - COMMON NAME
  - YEAR
  - NO. SITES (sites contributing data for that species/year)
  - COLLATED INDEX (log10 scale; indexed so the overall mean is 2)
  - YEAR RANK (relative rank of the year for that species)
  - TIME PERIOD
  - COUNTRY
- The collated indices are designed to enable relative trend analysis across years and species.

## Licence and attribution statement

- Data are provided under the Open Government Licence (OGL), allowing free use with standard conditions.
- Citations must include the dataset’s DOI as per metadata, and attribution should read: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset use and interpretation, and are open to collaboration and co-authorship on publications resulting from UKBMS data.
- Contact:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect Co-ordinator): transect@butterfly-conservation.org
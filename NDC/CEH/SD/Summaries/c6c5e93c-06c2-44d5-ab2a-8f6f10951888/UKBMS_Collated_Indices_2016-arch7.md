# The UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects annual butterfly data from over 2,000 UK sites, using fixed transect-based methods to estimate populations and generate national and site-level indices.
- Data support a range of species- and habitat-focused analyses, with indices and trends produced through specialized statistical methods.

## Data collection methods

- All-species transects: fixed-route 2–4 km transects, 5 m wide bands, 26 counts per year from April to September; routes fixed to enable year-to-year comparison; counts typically between 10:45 and 15:45 under suitable weather.
- Single-species transects: follow all-species method but recorded only for focal species on a few weeks.
- Timed counts and egg/larval web counts: counts of a focal species over set periods/areas; weather and time windows similar to transects.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort survey with two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits (minimum two in July/August); based on the BTO’s Breeding Bird Survey methodology.

## Data collection workflow and storage

- Field data recorded on standard forms; entered online via UKBMS data entry site or Transect Walker (free download).
- Data input by recorders or regional transect coordinators; regional coordinators compile data for their region.
- Online data and Transect Walker outputs uploaded to an Oracle database containing all records.

## Analytical methods

- WCBS-wide species: two-stage model using all survey data to estimate annual seasonal flight patterns (Stage 1 uses a generalized additive model, GAM) and to derive a seasonally adjusted set of counts; Stage 2 fits a model to annual counts with seasonal values as an offset to estimate annual abundance changes.
- Habitat specialists and regular migrants: GAM used to impute missing values and compute site indices; site indices are combined to form a national Collated Index via a log-linear regression to handle missing years and varying site participation; Collated Indices updated annually as new data are added.
- Types and definitions: Wider countryside species are mobile across various habitats; habitat specialists are restricted to semi-natural habitats; regular migrants overwinter abroad; Red Admiral status is noted as migratory in most of the UK but resident in parts of the south and west.

## Nature and units of recorded values

- Site indices: relative measures of population size (not absolute); act as a constant proportion of true population size and vary by species.
- Collated Indices: presented as the logarithm (Log10) of the Collated Index; values are scaled so the average index over the full series equals 2 for a relative temporal comparison.

## Quality control

- Transect Walker includes automatic checks for data-entry errors (e.g., unusually high counts, flight-period incongruities).
- Regional coordinators review records; online data are continuously validated; automated and manual validation includes cross-checks for out-of-range records, first-time site entries, extreme values, and comparisons with known distributions (Butterflies for the New Millennium) and existing UKBMS data.
- The Collated Indices are stored as CSV files and accompany dataset metadata.

## Data structure and metadata

- Key Collated Index dataset columns: 
  - Species (scientific name per Fauna Europaea v2.2)
  - Common name
  - Year
  - No. Sites (number of contributing sites)
  - Collated Index
  - Time period (data used to produce the Collated Indices)
- Some early years lack Collated Indices due to insufficient data; the number of contributing years is noted for each species’ trend.
# The UK Butterfly Monitoring Scheme (UKBMS)

- Aims and scope: UKBMS collates butterfly monitoring data across the UK from over 2,000 sites per year to estimate population abundance and trends, informing policy, management decisions, and conservation actions.

## Data collection methods

- All-species transects (standard method):
  - Fixed-route linear transects at sites; all butterfly species counted along the route weekly.
  - Transect length typically 2–4 km; 45 minutes to 2 hours to walk; divided into habitat/management sections.
  - Recording band: fixed-width (about 5 m) along the transect; counting April to September; aim for 26 counts per year.
  - Transects are fixed to allow year-to-year comparison; routes sampled to represent habitat types and management.
  - Weather constraints: counts conducted 10:45–15:45 only when butterfly activity is suitable (dry, wind < Beaufort 5, temperature criteria with sunshine or overcast conditions).

- Single-species transects:
  - Follow the all-species protocol but recorded only during selected weeks for specific focal species.

- Timed counts and egg/larval web counts:
  - Timed counts: fixed area and period to estimate abundance of a focal species.
  - Egg/larval web counts: count eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).

- Wider Countryside Butterfly Survey (WCBS):
  - Reduced-effort sampling to cover wider countryside habitats (established 2009).
  - Based on BTO Breeding Bird Survey method; two parallel 1-km transects in randomly selected 1-km squares.
  - Each square subdivided into 10 sections; 2–4 visits total (minimum 2 visits in July/August; spring visits encouraged).

- Data capture and management:
  - Field data recorded on standard forms; entered online via UKBMS data site or Transect Walker software.
  - Regional transect coordinators compile data for their region; data entered into an Oracle database.

## Analytical methods

- For wider countryside species (mobile, broad habitat range): two-stage model using all survey data.
  - Stage 1: Generalised additive model (GAM) to estimate the annual seasonal flight pattern; daily values are normalised to yield a year-specific seasonal pattern.
  - Stage 2: Model fitted to full annual counts with seasonal values as an offset to estimate annual abundance changes, accounting for varying seasonality.
  - Method described in Dennis et al. 2013.

- For habitat specialists and regular migrants (less WCBS data, more reduced-effort data):
  - General Additive Model (GAM) to impute missing values and compute a site index.
  - Collated Index (CI) derived by combining site indices; log-linear regression used to estimate missing values when not all sites are monitored each year.
  - Collated Indices (CIs) updated annually as more data are added; CIs calculated for species recorded at five or more sites per year.
  - Note: Some early years lack CI due to insufficient data, resulting in shorter trend series for some species.

## Nature and units of recorded values

- Site indices: a relative measure of population size (not absolute); approximate proportional relationship to true population size; some species are easier to detect than others.
- Collated Indices (CIs): presented as log10 of the Collated Index (LCI); scaled so that the average index over the entire series equals 2 for each species, providing a relative time series of population size.

## Quality control and data governance

- In-field and regional validation:
  - Transect Walker performs automatic plausibility checks (e.g., abnormally high counts, species outside flight period).
  - Regional coordinators review records; continuous validation during the season.
  - Additional automated and manual validation to flag records outside known distribution, out of flight period, new site records, or anomalous abundances.

- Data storage and documentation:
  - Collated Indices stored as CSV files; dataset includes columns for Species (scientific name per Fauna Europaea v2.2), Common name, Year, Number of Sites contributing, Collated Index, and Time period used for the CI.

## Data structure and key columns

- Species: scientific name (Fauna Europaea v2.2)
- Common name: vernacular name
- Year: year for which the CI is calculated
- No. Sites: number of contributing sites for that year
- Collated Index: CI value for the species in that year
- Time period: data period used to compute the CI

## Notable notes for users

- Collated Indices can change retrospectively as additional data are received and incorporated.
- Some species have shorter trend records due to earlier data gaps or insufficient site coverage.
- Data are designed to be comparable across years through fixed transect methods and standardized analytical approaches.
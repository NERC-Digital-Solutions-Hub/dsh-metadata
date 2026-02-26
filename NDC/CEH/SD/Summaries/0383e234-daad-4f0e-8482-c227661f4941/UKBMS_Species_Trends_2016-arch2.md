# The UK Butterfly Monitoring Scheme (UKBMS)

- What it is: A long-running UK-wide monitoring program collecting butterfly counts from over 2,000 sites annually to assess environmental health and policy outcomes related to butterflies.

- Site coverage and sampling design:
  - All-species transects (Pollard walks): fixed routes 2–4 km long, 5 m width, 26 counts per year from April to September, conducted weekly under suitable weather (specific criteria for temperature, wind, sunshine).
  - Fixed transect design allows year-to-year comparability; routes sample habitat and management types.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling of wider countryside habitats (farmland, etc.), using two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits per year (minimum 2 in July/August; spring visits encouraged).
  - Other methods: single-species transects, timed counts, and egg/larval web counts for particular species.

- Data collection and flow:
  - Field data recorded on standard forms; entered online via UKBMS data portal or Transect Walker software.
  - Data uploaded to an Oracle database; regional transect coordinators compile and deliver data for their regions.
  - Quality checks include automatic validation in Transect Walker and ongoing regional review; additional automated/manual validation targets outliers, out-of-range distributions, atypical flight periods, first-time site records, and extreme counts.

- Analytical methods (two parallel approaches):
  - Wider Countryside species (WCBS and similar data):
    - Two-stage model using all season counts to estimate the seasonal flight pattern (via generalized additive model, GAM) and to compute an annual seasonal offset.
    - Stage two fits a model to annual counts with seasonal values as offsets to derive annual abundance changes over time.
    - This method uses all available counts to produce a Collated Index (CI) for each species.
  - Habitat specialists and regular migrants:
    - GAM-based imputation for missing values and site index calculation; aggregation across sites yields a national annual index (Collated Index).
    - A log-linear regression on CI to produce trends across the UK since 1976.
  - Trends and timeframes:
    - Species trends calculated for whole series (1976–2016), last 20 years (1997–2016), and last 10 years (2007–2016).
    - Some early years lack CI for certain species due to insufficient data.

- Nature and units of recorded values:
  - Site indices: relative measures of population size (not absolute); relate to other abundance measures and reflect detectability differences by species.
  - Collated Indices: presented as Log10(CI); scaled so the average index over the series equals 2 for relative comparison.
  - Trends: expressed as the slope of the CI over the specified period; includes accompanying P-values and qualitative trend descriptions (e.g., Rapid decline, Rapid increase, Stable).

- Data quality and storage formats:
  - Data quality: layered validation (automatic checks, regional coordinators, and cross-checks against known distributions and flight periods).
  - Storage and formats: Species Trends stored as CSV with fields including scientific and common names, number of years, slope, standard errors, P-values, trend descriptions, and percentage changes; additional yearly metrics include 20-year and 10-year slopes, errors, P-values, trends, and percentage changes.
  - Data references and formatting notes (e.g., taxonomic naming conventions and standard references) accompany the stored data.

- Key outputs for monitoring and policy:
  - Species-specific trends across multiple time windows to inform conservation status and habitat management decisions.
  - Standardized indices and trends enable temporal comparisons and integration with broader environmental health indicators.
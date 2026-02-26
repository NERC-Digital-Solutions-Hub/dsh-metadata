# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly abundance and trends.
- Data collection relies on fixed protocol transects and sampling regimes to enable year-to-year comparability and robust trend analysis.

## Monitoring framework and scope

- All-species transects form the core methodology, with fixed routes sampled weekly during suitable butterfly activity periods.
- Transects are 2–4 km long, divided into habitat/management units, and surveyed in a 5 m wide band with typically 26 counts per year (April–September).
- Weather and time constraints apply (10:45–15:45; conditions enabling butterfly activity; specific temperature and sunshine thresholds).
- Wider Countryside Butterfly Survey (WCBS) provides a reduced-effort sampling regime (two parallel 1-km transects in randomly selected 1-km squares) to broaden habitat coverage.

## Data collection design

- Data are recorded on standard forms in the field and entered online via the UKBMS data entry site or via Transect Walker (free software).
- Regional transect coordinators compile data for each region; data are uploaded to an Oracle database.
- WCBS sampling uses the fixed-route methodology of all-species transects but with fewer visits (2–4 visits, depending on the year).

## Data collection methods

- Field recording forms are used in situ; data are entered by recorders or coordinators.
- Data submission routes include online entry and Transect Walker, with centralized processing by regional coordinators.
- The database infrastructure stores all records, enabling integration across sites and years.

## Analytical methods and indices

- Two analytical paths are used, depending on species group:
  - Wider Countryside species (mobile species across multiple habitats): a two-stage model using all survey data. Stage 1 applies a generalized additive model (GAM) to estimate the annual seasonal flight pattern for each species; Stage 2 fits a model to the full annual counts with seasonal values as an offset to derive annual abundance changes and trends. This approach yields a Collated Index per species.
  - Habitat specialists and regular migrants (less data from WCBS or reduced-effort sampling): a GAM imputes missing values to produce a site index, which is then aggregated to a national Collated Index using log-linear regression to handle year- and site-effects and incomplete data.
- Indices and trends:
  - Collated Indices are calculated for species with data from five or more sites per year.
  - Site indices are relative measures of population size; Collated Indices are presented as the logarithm (Log10) of the index (LCI) to enable comparison over time.
  - National trends are derived by regressing the Collated Indices over time, with analyses reported for the full time series (1976–2016), the last 20 years (1997–2016), and the last 10 years (2007–2016).

## Nature and units of recorded values

- Site indices: relative measures of population size (not absolute counts), proportional to the number of butterflies present.
- Collated Indices: log-transformed values (Log10 Collated Index) standardized so the average index equals 2 across the series.
- Trends: reported as slopes (change per year) of the Collated Index; accompanying p-values determine whether trends are rapid declines, rapid increases, or stable.

## Quality control and validation

- In-field automatic checks (Transect Walker) flag potential data entry errors (e.g., abnormally high counts, records outside flight periods).
- Regional coordinators review data for questionable records; validation continues throughout the season.
- Additional automated and manual validation steps target records outside known distributions, flight periods, first-time site records, and extreme values.

## Data storage, format, and metadata

- Data are stored in an Oracle database; outputs include national indices and trends.
- The Species Trends data are stored as a CSV with columns covering:
  - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
  - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
  - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
- The dataset includes taxonomic naming following Fauna Europaea and common naming references; trends include descriptive classifications (e.g., Rapid decline, Rapid increase, Stable) based on slope and significance.

## Limitations and notes

- Some species have shorter or interrupted time series due to missing years or insufficient sites contributing data.
- Collated Indices for certain years or species may be updated retrospectively as more data are integrated.
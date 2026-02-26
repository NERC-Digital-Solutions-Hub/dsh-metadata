# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, using multiple standardized methods to estimate butterfly abundance.

- Sampling methods
  - All-species transects (Pollard walk): fixed-route line transect, 2–4 km long, 45 minutes to 2 hours, weekly counts from April to September, weather-constrained (dry, Beaufort <5, temperature thresholds with sunshine or overcast conditions). Transects fixed to allow year-to-year comparisons; counts recorded in a 5 m wide band.
  - Single-species transects: follow the all-species methodology but only for focal species during select weeks.
  - Timed counts: counts of a focal species over a set period and area, weather-constrained.
  - Egg/larval web counts: counts of eggs or larval webs for species in suitable habitat.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in wider habitats (farmland), two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits per year with minimum two visits in July/August.

- Data collection in the field and entry
  - Data recorded on standard forms; entered online via UKBMS data entry site or Transect Walker software.
  - Data entry performed by recorder or regional transect coordinator; coordinators aggregate site data for their region.
  - Online data and Transect Walker files uploaded to an Oracle database.

- Analytical methods (national indices and trends)
  - For wider countryside species:
    - Two-stage model using all survey data.
    - Stage 1: Generalised additive model (GAM) to estimate annual seasonal flight patterns; daily values normalised to a common across-sites seasonal pattern per year.
    - Stage 2: Model fitted to full annual counts with seasonal values as an offset to estimate annual abundance changes, accounting for varying seasonality.
    - Described in Dennis et al. (2013).
  - For habitat specialists and regular migrants:
    - GAM to impute missing values and calculate a site index for each species.
    - Collated Index: aggregated across sites to derive a national annual index; updated annually as new data are added; indices available for species recorded at five or more sites per year.
    - Trend calculation: linear regression on collated indices to produce overall trends since 1976, over the last 20 years (1997–2016) and last 10 years (2007–2016).

- Data formats and units
  - Site indices are relative measures proportional to population size; not absolute counts.
  - Collated Indices are presented as Log10 Collated Index (LCI), scaled so the average index over the series equals 2.
  - Trends expressed as slope (change per year) on the Collated Index.
  - Time horizons: 1976–2016 for long-term trends; 1997–2016 (20 years) and 2007–2016 (10 years) for recent trends.

- Quality control and validation
  - Automatic checks in Transect Walker flag unusual counts or out-of-period records.
  - Regional transect coordinators review records; continuous checks during the season.
  - Further automated and manual validation to flag out-of-range distributions, non-typical flight periods, first-time site records, extreme abundances, or unusual site-year deviations.

- Data storage and fields
  - Species Trends stored as CSV with columns including:
    - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
    - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
    - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
  - Trends categorized as Rapid decline, Rapid increase, or Stable based on slope and P-value thresholds (≤0.05 indicating significant change).

- Definitions and scope
  - Wider countryside species: mobile species across varied habitats.
  - Habitat specialists: low-mobility species restricted to semi-natural habitats.
  - Regular migrants: species overwintering outside the UK; typically migrant to the UK annually.

- Notes and limitations
  - Collated indices for some early years are incomplete due to data availability from contributing sites.
  - Some species have shorter trend series if insufficient data exist across years.
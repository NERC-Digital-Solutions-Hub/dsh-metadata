# Experimental design/sampling regime

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
- Data collection includes multiple methods to estimate butterfly abundance, using standardized protocols to enable year-to-year comparison.

## Data collection methods and transects
- All-species transects (Pollard walks): fixed-route line transects at a site, recording all butterflies along a 2–4 km route on a weekly basis from April to September; counts occur in a fixed width band (typically 5 m) and require suitable weather (dry, wind < Beaufort 5, temperature thresholds with sun or overcast conditions). Transects are designed to sample habitat/management units and remain fixed to enable comparison across years; typically yield about 26 counts per year.
- Single-species transects: follow the all-species transect methodology but record only during a few weeks within the focal species’ flight period.
- Timed counts and egg/larval web counts: record abundance of a particular species over a set period/area or count eggs/larval webs in suitable habitats.
- Wider Countryside Butterfly Survey (WCBS): established in 2009 as a reduced-effort survey to sample wider countryside habitats (farmland, etc.). Based on the BTO Breeding Bird Survey design, using two parallel 1-km transects within randomly selected 1-km squares; involves 2–4 visits per year with a minimum of 2 visits in July/August (spring visits encouraged). WCBS uses the fixed-route transect methodology of all-species transects.

## Data collection and entry
- Data are recorded on standard field forms and entered online via ukbms.org/mydata or into the Transect Walker software (free download).
- Data entry can be done by the recorder or a regional transect coordinator; each transect coordinator aggregates data for their region.
- Online data and Transect Walker outputs are uploaded into an Oracle database that stores all records.

## Analytical methods
- Two main approaches are used to generate national indices for species:
  - Wider countryside species: uses all counts from all survey types in a two-stage model. Stage 1 applies a generalized additive model (GAM) to estimate annual seasonal flight patterns; Stage 2 uses these seasonal values as an offset in a model fitted to the full annual counts to estimate annual abundance changes. This method is described in Dennis et al. 2013.
  - Habitat specialists and regular migrants: when data from WCBS and reduced-effort methods are limited, a GAM imputes missing values to create a site index. Site indices are combined to derive a national annual index (Collated Index). A log-linear regression is then used on collated indices to produce species trends over time (since 1976). Trends are computed for:
    - the full time series (1976–2013),
    - the last 20 years (1993–2013), and
    - the last 10 years (2003–2013).
- Collated Indices are updated annually as more data are incorporated; some species have shorter series due to data gaps or limited years contributing to the trend analysis.

## Nature and units of recorded values
- Site indices are a relative measure of population size (not absolute) and relate closely to other abundance measures (e.g., mark-release-recapture).
- Collated Indices are presented as the logarithm of the Collated Index (Log10 Collated Index, LCI), scaled so the average index over the full series equals 2.
- Trends are reported as the slope (change per year) of the Collated Index; additional metrics include the overall percent change over the series.
- Species categories:
  - Wider countryside species: mobile species across a wide range of habitats.
  - Habitat specialists: low mobility species largely restricted to semi-natural habitats.
  - Regular migrants: species that do not overwinter in the UK but migrate from continental Europe each year.

## Quality control
- The Transect Walker system includes automatic checks to flag data-entry errors (e.g., abnormally high counts, records outside known flight periods).
- Regional transect coordinators review records for each region; data can be validated continuously during the season.
- Additional validation checks address records outside known distribution ranges, unusual flight periods, first-time site records, or anomalous abundances.

## Format and structure of stored data
- Species trends are stored as a CSV file with fields including:
  - SCI_NAME (scientific name), COMMON_NAME (vernacular name)
  - NYEARS (number of years used in the trend)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL (slope, standard error, p-value, trend description)
  - F_FULL_R (percentage change over the full series)
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year slope, its SE, p-value, trend, and 20-year % change)
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year slope, its SE, p-value, trend, and 10-year % change)
- The dataset provides both long-term and recent-term trends to assess population dynamics over multiple timescales.
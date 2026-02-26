# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites across the UK annually to monitor butterfly populations.
- Utilizes fixed-route transects and standardized methods to estimate abundance and trends for multiple species.

## Data collection methods
- All-species transects: fixed-route line transects (2–4 km) with 5 m width, 26 counts/year, sampled weekly from April to September.
  - Transects sampled under suitable butterfly activity: weather-based criteria (e.g., wind, temperature, sunshine).
  - Transect routes fixed to enable year-to-year comparisons; routes segmented by habitat/management units.
- Single-species transects: follow all-species methodology but recorded only for focal species during select weeks.
- Timed counts and egg/larval web counts: record species abundance over a set time/area or count eggs/larval webs in suitable habitat.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort survey since 2009, two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum two in July/August; spring visits encouraged).

## Data recording and entry workflow
- Field data recorded on standard forms.
- Online entry via UKBMS data entry site or Transect Walker software.
- Local region transect coordinators compile data from multiple sites; data uploaded to an Oracle database.

## Analytical methods and indices
- For wider countryside species:
  - Two-stage model using all season data to estimate annual seasonal flight patterns; daily values normalized to a common seasonal pattern across sites but varying by year.
  - Second stage uses observed counts with seasonal offsets to estimate annual changes in abundance and trends.
  - Detailed methodology described in Dennis et al. 2013.
- For habitat specialists and regular migrants (with less WCBS data):
  - General Additive Model (GAM) to impute missing values and calculate site indices.
  - Site indices combined to derive national Collated Indices; a log-linear regression model estimates missing values due to incomplete site coverage.
  - Collated Indices updated annually as new data arrive; indices for a species are calculated when data exist from at least five sites per year.
- Species classifications:
  - Wider countryside species: mobile, broad habitat range.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK; arrive annually from Europe.

## Data quality, validation, and governance
- Quality control:
  - Automatic checks in Transect Walker flag anomalous counts or out-of-season records.
  - Regional transect coordinators validate records; ongoing checks throughout the season.
  - Additional automated/manual validation to flag records outside known distribution, unusual abundances, or first-time site records.
- Data storage and format:
  - Collated Indices stored as CSV files.
  - Columns include species (scientific name), common name, year, number of contributing sites, Collated Index, and time period used for the index.

## Data interpretation and units
- Site indices are relative measures of population size, proportional to actual abundance.
- Collated Indices are presented as log10 values (Log10 Collated Index, LCI) with species-specific scaling so the average index across the series equals 2.
- Indices may be updated retrospectively as historical data are added, which can slightly revise past trends.

## Notes and references
- Data and methods hinge on established statistical approaches (GAMs, two-stage seasonal models) and prior methodological work (e.g., Dennis et al. 2013; Rothery & Roy 2001; Moss & Pollard 1993).
- Data completeness varies by species and year, with some early years lacking Collated Indices due to insufficient data.
# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK.
- Data collection methods include:
  - All-species transects (Pollard walks): fixed-route 2–4 km counts, weekly, Apr–Sep, across habitats, to enable year-to-year comparisons.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in farmland and wider habitats, established in 2009; two parallel 1-km transects within randomly selected 1-km squares, 2–4 visits per season.
  - Single-species transects, timed counts, and egg/larval web counts used for select species.
- Transects are conducted only under suitable butterfly activity conditions (weather criteria specified).
- Data are recorded in the field, entered online or via Transect Walker software, and uploaded to an Oracle database.

## Data collection and management
- Field data are recorded on standard forms; upload to UKBMS data entry site or Transect Walker.
- District/region transect coordinators compile data for their areas; data are then stored in an Oracle database.
- Online data and Transect Walker files are centralised and validated during and after collection.

## Data types and sampling definitions
- All-species transects account for more than half of UKBMS sites; WCBS provides broader countryside coverage.
- Species definitions:
  - Wider countryside species: mobile, widespread habitats.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK; arrive from continental Europe yearly.
- Data and indices may be updated as more data are received; some species have shorter series if early years lacked collated indices.

## Analytical methods
- Two distinct approaches by species group:
  - Wider countryside species:
    - Use all survey data (across survey types) with a two-stage model.
    - Stage 1: Generalised Additive Model (GAM) estimates the annual seasonal flight pattern.
    - Stage 2: Uses seasonal values as an offset in a model to estimate annual abundance changes and trends.
    - Described in Dennis et al. 2013.
  - Habitat specialists and regular migrants:
    - GAMs impute missing values and compute a site index.
    - Combine site indices to produce a national Collated Index.
    - Log-linear regression accounts for year and site effects to estimate missing values.
    - Collated Indices are updated annually; some years may have fewer contributing sites.
- Collated Indices reflect relative abundance rather than absolute counts.

## Indices and data presentation
- Site indices: relative measures of population size, proportional to actual abundance.
- Collated Indices: presented as the log10 of the Collated Index (LCI) for each species.
- Indices are scaled so that the average index over the full series equals 2, enabling relative comparisons over time.

## Quality control and validation
- Automatic checks in Transect Walker flag anomalous counts and out-of-season records; recorders may adjust entries.
- Regional coordinators review data for each site and continuously validate online entries.
- Additional validation checks include:
  - Records outside known distribution ranges.
  - Records outside known flight periods.
  - First-time site records.
  - Extreme or unusual abundances.
- Data handling includes verification against external datasets (e.g., Butterflies for the New Millennium).

## Data format and availability
- Collated Indices stored as CSV files.
- Key columns include:
  - Species (scientific name per Fauna Europaea)
  - Common name
  - Year
  - No. Sites (sites contributing to the index)
  - Collated Index (the value for that species/year)
  - Time period (data used to produce the indices)
- The dataset documents the number of years contributing to each species’ trend, acknowledging early years with insufficient data.
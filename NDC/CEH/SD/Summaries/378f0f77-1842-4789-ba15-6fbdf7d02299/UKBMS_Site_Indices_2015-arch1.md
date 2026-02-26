# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 2,000 sites annually across the UK.
- Data include both all-species transects and reduced-effort surveys, with additional methods for specific species and habitat contexts.

## Data collection methods
- All-species transects (Pollard walk)
  - Fixed-route line transect at a site; 2–4 km long; 45 minutes to 2 hours to walk.
  - Record all butterfly species within a fixed 5 m wide band along the transect.
  - Conducted weekly from early April to late September; weather conditions must enable butterfly activity.
  - Transects are habitat- or management-specific and fixed to enable year-to-year comparisons.
- Single-species transects
  - Follow the all-species transect methodology but focus on a focal species during a subset of weeks.
- Timed counts and egg/larval web counts
  - Timed counts: record a species’ abundance over a set period and area under suitable weather.
  - Egg/larval counts: count eggs or larval webs in areas of suitable habitat (e.g., Marsh Fritillary).
- Wider Countryside Butterfly Survey (WCBS)
  - Established in 2009; reduced-effort survey sampling wider countryside habitats (farmland).
  - Based on the BTO Breeding Bird Survey design: two parallel 1-km transects per 1-km square, subdivided into 10 sections.
  - Usually 2–4 visits, with a minimum of 2 visits in July/August; spring visits encouraged.

## Data collection and entry
- Field data recorded on standard forms.
- Entered online via UKBMS data entry site or Transect Walker software (free download).
- Data entry performed by recorders or regional transect coordinators.
- Transect coordinators compile data for all sites in their region; online data and Transect Walker files are uploaded to an Oracle database.

## Calculation and handling of site indices
- Site indices are calculated only for sites with sufficient monitoring visits (or for timed/egg/larval counts where counts are near peak).
- WCBS sites are excluded from index calculations due to insufficient visits for reliable indices.
- For transect sites, a General Additive Model (GAM) is used to impute missing values and to calculate a site index.
- Site indices are a relative measure of population size, proportional to the actual population size rather than an absolute count.

## Nature and units of recorded values
- Site Index represents a relative size of the population at a site and year.
- The index correlates with more intensive population size measures (e.g., mark-release-recapture) and may vary by species due to detectability differences.
- Values reflect the proportion of butterflies present relative to the modeled expectation for that site.

## Quality control and validation
- Automatic checks in Transect Walker flag potential data-entry errors (e.g., abnormally high counts, species outside flight period).
- Regional transect coordinators review records for the region; ongoing validation throughout the season.
- Additional automated/manual validation steps include checks for:
  - Records outside known distribution ranges (using BNM/UKBMS data).
  - Records outside normal flight periods.
  - First-time recordings at a site.
  - Extreme or atypical abundances for a given site/time.

## Data format and storage
- Site Indices stored as a text file (.txt).
- Columns include:
  - Species (scientific name per Fauna Europaea, v2.2)
  - Common name (per Emmet & Heath, 1990)
  - Year (year of the calculated site index)
  - Site Index (relative index value)
- If a species at a site/year cannot yield an accurate index due to insufficient monitoring, the value is set to -2.
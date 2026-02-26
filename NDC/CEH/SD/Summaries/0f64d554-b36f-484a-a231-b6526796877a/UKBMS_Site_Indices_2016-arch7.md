# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

## Overview and GIS relevance
- UKBMS provides annual site indices for butterfly populations across the UK, enabling map-based visualization and spatial analysis of relative population trends.
- Data cover over 2,000 monitoring sites per year, with fixed transect routes to support year-to-year comparisons.
- Indices are relative measures, suitable for integration with other spatial datasets for conservation planning and policy analysis.

## Data collected and methods
- All-species transects
  - Fixed-route line transect (2–4 km long) walked weekly during suitable weather from April to September.
  - 5 m wide count band along the transect; routes chosen to reflect habitat types and management; routes fixed for comparability.
  - Accounts for over half of UKBMS sites annually (1,000+ sites).
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort sampling in wider habitats (farmland, countryside).
  - Two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year.
- Single-species transects
  - Same methodology as all-species transects but focused on a focal species during parts of its flight period.
- Timed counts and egg/larval web counts
  - Structured counts for particular species, including eggs and larval webs, conducted within defined areas and times.
- Data recording in the field
  - Standard forms; online data entry via UKBMS MyData or Transect Walker software.
  - Data uploaded to an Oracle database; regional transect coordinators compile site data per region.

## Data processing and modelling
- Site indices are calculated for sites with sufficient monitoring visits.
- General Additive Models (GAM) are used to impute missing values and compute site indices for transect sites.
- Indices are adjusted for time of year and the size of the habitat/site.
- WCBS sites are excluded from site index calculations due to insufficient visits for reliable indices.

## Data quality and validation
- In-field automatic checks (Transect Walker) flag improbable counts or records outside flight periods; reporters can adjust.
- Regional coordinators validate records; online data also subject to ongoing checks.
- Additional automated and manual validations target out-of-range distributions, atypical flight periods, first-time at a site occurrences, and anomalous abundances.

## Data format and structure
- Data are stored as CSV files with the following columns:
  - Species (scientific name, Fauna Europaea standard)
  - Common name (vernacular, Emmet & Heath standard)
  - Year (year of the site index)
  - Siteno (unique site identifier)
  - Site Index (relative index value)
- If a site could not provide an accurate index for a species in a year, the value is set to -2.

## Spatial scope and scale
- Geographic coverage: United Kingdom (UK).
- Sites: over 2,000 per year; transects typically 2–4 km with weekly counts; WCBS uses two 1-km transects within randomly selected 1-km squares.

## Access, licensing, and citation
- Data access and reuse/licensing conditions available at: https://doi.org/10.5285/0f64d554b36f-484a-a231-b6526796877a
- Data must be cited as:
  Botham, M.; Roy, D.; Brereton, T.; Middlebrook, I.; Randle, Z. (2017). United Kingdom Butterfly Monitoring Scheme: site indices data 2016. NERC Environmental Information Data Centre. https://doi.org/10.5285/0f64d554-b36f-484a-a231-b6526796877a

## Notes on interpretation and usage
- Site indices provide relative population size and are best used for comparing trends across sites and years rather than as absolute counts.
- Indices from transect data are robust for longitudinal comparisons due to fixed-route designs and standardized protocols.
- Data integration with other GIS layers may require linking via siteno and consistent regional classifications.

## References
- Emmet, A.M. & Heath, J. (1990). The Moths and Butterflies of Great Britain and Ireland. Vol 7 Part 1.
- Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation.
- Rothery, P. & Roy, D.B. (2001). Application of generalized additive models to butterfly transect count data. Journal of Applied Statistics.
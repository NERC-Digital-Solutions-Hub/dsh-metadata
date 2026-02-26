# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

## Overview
- Dataset describes site indices from the UK Butterfly Monitoring Scheme (UKBMS) for 2016, covering over 2,000 monitoring sites across the UK.
- Indices are a relative measure of population size, enabling year-to-year comparisons and linkage to more intensive population measures.
- Data support monitoring, evaluation of environmental health measures, and informing future policy decisions.

## Data access and licensing
- Data and reuse/licensing conditions available at: https://doi.org/10.5285/0f64d554b36f-484a-a231-b6526796877a
- Citation required if data are used: Botham, M.; Roy, D.; Brereton, T.; Middlebrook, I.; Randle, Z. (2017). United Kingdom Butterfly Monitoring Scheme: site indices data 2016. NERC Environmental Information Data Centre. https://doi.org/10.5285/0f64d554-b36f-484a-a231-b6526796877a

## Data description
- UKBMS collects data from thousands of sites annually using standardized methods (Pollard walk transects, Wider Countryside Butterfly Survey, etc.).
- Site indices are calculated for species at sites where monitoring is sufficient; WCBS indices are excluded due to limited visits for reliable indices.
- Data include species-level site indices across years, enabling temporal trend analyses.

## Data collection methods
- All-species transects: fixed-route, 2–4 km walks, 5 m recording band, weekly counts from early April to late September (approx. 26 counts/year), weather-conditioned.
- Single-species transects: similar methodology but focused on a focal species during portions of its flight period.
- Timed counts and egg/larval web counts: species-focused counts over fixed times/areas and lifecycle stages.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in farmland and wider habitats (2 parallel 1-km transects per 1-km square), 2–4 visits per season.

## Data management and processing
- Field data collected on standard forms and entered online via UKBMS or Transect Walker software.
- Regional transect coordinators compile and verify data; online entries are uploaded to an Oracle database.
- Site indices are computed using General Additive Models (GAM) to impute missing values for transect sites with sufficient data, while WCBS sites are excluded from site index calculations.

## Quality control
- Automated checks in Transect Walker flag unusual or out-of-period records; recorders may adjust entries.
- Regional coordinators review data for plausibility; ongoing validation through automated queries (e.g., out-of-range distributions, atypical abundances).

## Data format and metadata
- Site indices stored as comma-separated values (.csv).
- Key columns: Species (scientific name per Fauna Europaea), Common name, Year, Site number, Site Index.
- If a site-year lacks enough data to calculate an index for a species, the value is recorded as -2.

## Interpretation and limitations
- Site indices are relative indicators of population size rather than absolute counts.
- Indices are designed to be comparable across years and scale with other population measures (e.g., mark-release-recapture).
- Data gaps and the need for robust metadata/gov governance may affect data usability and comparability.

## References
- Emmet, A.M. & Heath, J. (1990). The Moths and Butterflies of Great Britain and Ireland, Volume 7 part 1.
- Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation.
- Rothery, P. & Roy, D.B. (2001). Application of generalized additive models to butterfly transect count data.
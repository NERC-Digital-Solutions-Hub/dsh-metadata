# UK Butterfly Monitoring Scheme data download

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC), with thanks to volunteers.
- Purpose: annual, site-based monitoring of butterfly population status using multiple sampling frameworks to produce trend-aware data for biodiversity policy questions.
- Scope: since 1976, the scheme covers over 2,500 actively recorded sites per year; data from all sampling methods are analyzed together.
- Data focus: abundance indices are derived as relative measures of population size, integrated across sites and methods; indices are produced using the Generalised Abundance Index (GAI) method with weighting for survey effort.

## Data collected and processing
- Sampling frameworks:
  - Standard butterfly transects (Pollard walks): fixed routes 2–4 km, weekly counts (up to 26 per year) across habitats.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year.
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts using alternative methods.
- Data handling and analysis:
  - Counts are converted to site-level indices and then to species-level indices using GAI, with year-site weighting based on the proportion of the species flight period surveyed.
  - All counts from Pollard walks, WCBS, and reduced surveys are used to model seasonal patterns and fill gaps in observation data.
- Data quality controls:
  - Field forms and online entry with automatic checks (e.g., out-of-range counts, dates outside flight period).
  - Regional transect coordinators perform ongoing validation; additional automated/manual checks target out-of-range distributions or atypical abundances.
  - Edits to the main UKBMS dataset are made after data queries and coordination with reporters when necessary.

## Details of this data download
- Content: location and attribute data for every UK site monitored under UKBMS from 1976 to 2020; sensitive sites are excluded.
- Format: comma-separated value (CSV) file.
- Key columns:
  - Site number, Site name
  - Gridreference, Easting, Northing
  - Length (transect length in metres, if provided)
  - Country
  - No. Sections
  - No. Yrs surveyed (up to 2021)
  - First year surveyed
  - Last year surveyed
  - Survey type (UKBMS standard or WCBS)

## Licence and attribution
- Licence: Open Government Licence (OGL), enabling free use with few conditions.
- Attribution: must include the formal citation with DOI in any publications; include the attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.
- Submissions since 2017: data submitters have agreed to OGL at submission; historical data may have third-party IP considerations—notify if any objections arise.

## Offer of collaboration and contact details
- UKBMS Partners offer guidance on dataset use and interpretation of outputs.
- Collaboration: potential for co-authorship and intellectual input in publications, presentations, or posters using UKBMS data.
- Contact:
  - UKBMS: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: transect@butterfly-conservation.org
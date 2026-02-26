# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
- Data are primarily gathered through fixed transects (Pollard walks) and complement with other standardized methods for certain species or contexts.
- Site indices provide a relative measure of butterfly population size rather than absolute counts.

## Data collection and methods
- All-species transects: fixed-route line transects (typically 2–4 km) walked weekly from April to September under suitable weather, with counts in a 5 m wide band. Transects are kept fixed to enable year-to-year comparisons; each site aims for about 26 counts per year.
- Wider Countryside Butterfly Survey (WCBS): a reduced-effort sampling method to cover broader habitats, using two parallel 1-km transects within randomly chosen 1-km squares, with 2–4 visits per year.
- Single-species transects: follow the all-species method but record only for the focal species during selected weeks.
- Timed counts and egg/larval web counts: used for specific species; counts occur within defined times and conditions.
- Timing constraints: walks occur between 10:45 and 15:45, with weather and temperature criteria for activity.

## Data recording and storage
- Field data are collected on standard forms and entered online via the UKBMS data entry site or via Transect Walker software.
- Data are uploaded to an Oracle database. Regional transect coordinators compile data for all sites in their region.
- Site indices are calculated using a General Additive Model (GAM) to impute missing values for transect sites; WCBS sites are excluded from site index calculations due to limited visits.

## Nature and units of recorded values
- Site indices are relative measures of population size, not absolute counts, and are proportional to the true abundance.
- Relative indices can vary by species due to detectability.

## Quality control
- Automatic checks in Transect Walker flag inconsistent or erroneous entries (e.g., abnormally high counts, out-of-season records).
- Regional coordinators validate data; online entries undergo ongoing review.
- Additional automated and manual validation checks include ensuring species records align with known distributions, flight periods, first sightings, and typical abundances.

## Format and content of stored data
- Site indices are stored as comma-separated values (.csv) with columns:
  - Species (scientific name)
  - Common name
  - Year
  - Site number (SiteNo)
  - Site Index
- If a site-year-species combination cannot yield a reliable index due to insufficient monitoring, the value is recorded as -2.

## Data access, licensing, and citation
- Data and reuse/licensing details are available at: https://doi.org/10.5285/0f64d554b36f-484a-a231-b6526796877a
- If you use the data, citation required:
  - Botham, M.; Roy, D.; Brereton, T.; Middlebrook, I.; Randle, Z. (2017). United Kingdom Butterfly Monitoring Scheme: site indices data 2016. NERC Environmental Information Data Centre. https://doi.org/10.5285/0f64d554-b36f-484a-a231-b6526796877a

## Key outputs and uses
- Provides year-over-year site indices to monitor environmental health and policy performance related to butterfly populations.
- Supports data-driven assessments of habitat quality, management effectiveness, and broader biodiversity trends.
- Serves as a standardized, central dataset for researchers and policymakers to scrutinize environmental indicators over time.

## Considerations for analysts monitoring the environment
- Emphasis on standardized methodologies to enable comparability across years and sites.
- Indices are relative measures, requiring consideration when integrating with absolute-population datasets.
- Challenges include enhancing dataset value through integration with other data and ensuring broad accessibility to underlying data used to generate outputs.
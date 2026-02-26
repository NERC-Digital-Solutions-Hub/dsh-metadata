# UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- A long-running, nationally coordinated monitoring program collecting butterfly data from over 1,000 sites across the UK each year.
- Uses standardized methods to produce site-level indices and a national Collated Index per species, enabling temporal trends and environmental health assessments.
- Data are stored, quality-checked, and made available for scrutiny and policy evaluation.

## Experimental design and sampling regime
- All-species transects: fixed-route line transects (typically 2–4 km) sampled weekly from early April to late September; 26 counts per year in a fixed 5 m belt, under suitable weather; routes are habitat-representative and fixed for year-to-year comparability.
- Transects are conducted between 10:45 and 15:45, only when butterfly activity conditions are met (dry, Beaufort wind < 5, temperature thresholds with sunshine or overcast).
- Single-species transects follow the same methodology but record only one focal species for one or more weeks in the flight period.
- Timed counts and egg/larval web counts provide alternative abundance measures for specific species and habitats.

## Data collection methods
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free download) by the recorder or regional transect coordinator.
- Transect Walker files uploaded to an Oracle database housing all records, with regional coordinators responsible for data submission and initial checks.

## Analytical methods
- After validation, missing values are imputed and site indices are calculated using Generalized Additive Models (GAM).
- Site indices from all sampling methods are combined to form a national Collated Index for each species.
- Because some years/sites are incomplete, a loglinear regression model estimates missing values and derives trends, accounting for year effects and site effects.
- Collated Indices are updated annually as new data are incorporated; indices for species are calculated for those recorded at five or more sites per year.

## Nature and units of recorded values
- Site indices are relative measures of population size (not absolute counts) and reflect a constant proportion of the actual population, varying by species’ detectability.
- Collated Indices are presented as the log10 of the Collated Index (LCI), with species-specific scaling so the average index over the series equals 2.

## Quality control
- In-field automatic checks in Transect Walker flag improbable records (e.g., unusually high counts, flights outside known periods).
- Regional coordinators review data for questionable entries; subsequent automated and manual validations check for records outside known distributions, abnormal flight periods, new site entries, and extreme or unusual abundances.

## Format of stored data
- Collated Indices are stored as CSV files with columns including: Species, Common name, Year, No. Sites, Collated Index, Time period.
- Data definitions align with standard taxonomic references (e.g., Fauna Europaea) and established butterfly literature, ensuring consistent naming and periodization.
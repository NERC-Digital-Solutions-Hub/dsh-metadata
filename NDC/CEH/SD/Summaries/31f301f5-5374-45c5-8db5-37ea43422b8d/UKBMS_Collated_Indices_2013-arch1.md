# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Primary method is all-species transects (Pollard walks): fixed routes 2–4 km long, sampled weekly from early April to late September (ideally 26 counts per year) in a 5 m wide band.
- Transects are fixed to enable year-to-year comparisons and are divided into habitat/management units.
- Weather and time constraints restrict sampling to: 10:45–15:45, dry conditions, wind < Beaufort 5, and temperature thresholds (≥13°C with ≥60% sunshine, or ≥17°C if overcast).

## Data collection methods
- Field data recorded on standard forms.
- Entries generated in Transect Walker (free software); data input by the recorder or regional transect coordinator.
- Each transect coordinator compiles data for all sites in their region.
- Transect Walker files are uploaded into a central Oracle database.

## Analytical methods
- After validation, a General Additive Model (GAM) imputes missing values and calculates a site index.
- All site indices across methods are combined to form a national annual Collated Index for each species.
- Since not all sites are monitored every year, a loglinear regression model estimates missing values and adjusts for year effects (weather) and site effects (population size at sites).
- Collated Indices are updated annually as new data are received; indices for species require data from at least five sites per year.

## Nature and units of recorded values
- Site indices: relative measures of population size, not absolute counts.
- Collated Indices are expressed as the log10 of the Collated Index (LCI) and are scaled so the mean across the series equals 2 for each species.

## Quality control
- Automatic checks in Transect Walker flag anomalous counts or records outside known flight periods.
- Regional coordinators validate records using local knowledge.
- Additional automated/manual validation screens for: records outside distribution ranges, out of flight period, first-time site records, extreme or atypical abundances.

## Format of stored data
- Collated Indices stored as CSV files.
- Columns include: Species (scientific name), Common name, Year, No. Sites, Collated Index, Time period (data used).
# UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 1,000 sites annually across the UK.
- Data support national trend indices; involve standardized field methods, data validation, and statistical modeling.

## Experimental design and sampling regime
- All-species transects (Pollard walks): fixed-route line transects (2–4 km) sampled weekly Apr–Sep; 5 m wide band; ~26 counts per year; routes fixed to allow year-to-year comparison; sites chosen to sample habitat types and management.
- Timing and conditions: surveys conducted 10:45 am–3:45 pm under suitable weather (e.g., dry; wind ≤ Beaufort 5; temperature ≥ 13°C with ≥ 60% sunshine, or ≥ 17°C if overcast).
- Transects also divided into habitat/management sections for recording.
- Single-species transects replicate all-species method but record only one focal species for one or more weeks.
- Timed counts and egg/larval web counts provide additional data for specific species and habitats.

## Data collection and storage
- Field data recorded on standard forms; entered into Transect Walker software (free download from UKBMS site).
- Data input can be by the recorder or a regional transect coordinator; coordinators compile data for their region.
- Transect Walker data uploaded to an Oracle database housing all records.

## Analytical methods
- After validation, a General Additive Model (GAM) imputes missing values and yields a site index per site.
- Site indices across methods are combined to produce a national annual index per species (Collated Index) using a loglinear regression to handle missing years/sites and year/site effects.
- Indices are updated annually as new data arrive; only species monitored at five or more sites per year receive Collated Indices.

## Nature and units of recorded values
- Site indices are relative measures of population size, proportional to actual abundance; not absolute counts.
- Collated Indices are expressed as the Log10 of the Collated Index (LCI); values are scaled so the average index over the series equals 2, enabling comparison of relative population changes over time.
- Some species’ detectability varies (e.g., more conspicuous vs cryptic species).

## Quality control
- In-run automatic checks in Transect Walker flag data entry anomalies (e.g., unusually high counts, flights outside known periods).
- Regional coordinators review data for questionable entries; data undergo further automated and manual validation.
- Additional checks include ensuring records fit known distribution ranges, normal flight periods, new-site observations, and detecting extreme or unusual abundances.

## Format of stored data
- Collated Indices stored as CSV files with columns:
  - Species (scientific name per Fauna Europaea)
  - Common name
  - Year
  - No. Sites (sites contributing to the Collated Index that year)
  - Collated Index
  - Time period (data used to produce the Collated Indices)
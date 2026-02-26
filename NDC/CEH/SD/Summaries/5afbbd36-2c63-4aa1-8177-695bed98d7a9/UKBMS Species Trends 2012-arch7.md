# Experimental design/sampling regime

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Data include estimates of butterfly abundance using fixed transects and other standardized methods, enabling year-to-year comparisons and national indices.

## Study design and sampling
- All-species transects: fixed-route line transects (2–4 km) sampled weekly from April to September under suitable weather, yielding ideally 26 counts per year.
  - Transects are fixed to sample habitat types and management; divided into sections by habitat/management units.
  - Counts cover a fixed width band (typically 5 m) along the transect.
- Weather and site constraints: observations occur between 10:45 and 15:45 under conditions suitable for butterfly activity (specific wind, temperature, and sunshine criteria).
- Fixed-route approach enables consistent year-to-year comparisons.
- Single-species transects: similar methodology but conducted only in a few weeks for focal species.
- Timed counts and egg/larval web counts: alternative methods for particular species or life stages.

## Data collection and processing
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free download) by the recorder or regional transect coordinator.
- Transect Walker files uploaded to an Oracle database housing all records.

## Analytical methods
- Data validation precedes analysis.
- General Additive Model (GAM) used to impute missing values and compute site indices.
- Site indices aggregated to produce a national Collated Index (LCI: log10 of Collated Index) per species.
- To address incomplete monitoring, a log-linear regression model estimates missing values to derive trends.
- Trends are calculated for:
  - The full series (1976–2012)
  - The last 20 years (1993–2012)
  - The last 10 years (2003–2012)
- Some species have shorter trend series due to insufficient data in early years.

## Data products and units
- Site indices are relative measures of population size, scaled to be comparable across time and species.
- Collated Indices are presented as Log10 Transformations (LCI) with yearly updates as new data are received.
- Trend metrics include:
  - Series slope, standard error, p-value, trend description, and percentage change.
  - 20-year and 10-year slopes, errors, p-values, trend descriptions, and percentage changes.
- Data format example: species-level trends stored in a CSV with columns for species, common name, years analyzed, slope, standard error, p-value, trend text, and percentage changes (including 20-year and 10-year metrics).

## Quality control
- Automatic checks in Transect Walker flag improbable counts and records outside known flight periods.
- Regional transect coordinators perform initial validation with local knowledge.
- Additional automated/manual validation screens for out-of-range records, records outside known distributions, first-time site records, and anomalous abundances.

## Data storage and accessibility
- Field data flow: paper forms → Transect Walker → Oracle database.
- Derived Trend data: stored as CSV files with defined columns describing species trends and statistics.
- Supporting documentation and data references linked to UKBMS resources (e.g., website) for access and updates.
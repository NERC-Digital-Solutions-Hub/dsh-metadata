# IRONCHEMISTRYDATA

## Overview
- A multi-file dataset detailing iron chemistry measurements from multiple sampling sites with associated date and location metadata.
- Includes both field/lab measurements and dialysate concentrations at different molecular weight cutoffs (3.5 kDa, 10 kDa, 15 kDa).
- Data presented with explicit variable names and units; notes capture data quality issues and detection limits.
- Designed to support data exploration, combination of datasets, and creation of data products (dashboards, reports) for end users.

## Data structure by file

- IRONCHEMISTRYDATA1.csv
  - Variables include: SampleSite, SampleDate, pHfield, pHfinal, DOC (mg dm3), Na (µeq dm3), Mg (µeq dm3), Ca (µeq dm3), Cl (µeq dm3), NO3 (µeq dm3), SO4 (µeq dm3), alkalinity (typo: alklinity; µeq dm3), total_Fe (µg dm3), total_Fe_II (µg dm3), filtered_Fe (µg dm3), filtered_Fe_II (µg dm3), total_monomeric_Al (µg dm3), total_acid_reactive_Al (µg dm3).
  - Note: Includes Explanation/Units metadata for each variable.

- IRONCHEMISTRYDATA2.csv
  - Variables include: SampleSite, SampleDate, 3_5kDa_dialysates_Fe (µg dm3), 3_5kDa_dialysates_Fe_II (µg dm3), 3_5kDa_dialysates_DOC (mg dm3), 3_5kDa_dialysates_monomeric_Al (µg dm3).

- IRONCHEMISTRYDATA3.csv
  - Variables include: SampleSite, SampleDate, 10kDa_dialysates (µg dm3), 10kDa_dialysates_Fe_II (µg dm3), 10kDa_dialysates_DOC (mg dm3), 10kDa_dialysates_monomeric_Al (µg dm3).

- IRONCHEMISTRYDATA4.csv
  - Variables include: SampleSite, SampleDate, 15kDa_dialysates_Fe (µg dm3), 15kDa_dialysates_Fe_II (µg dm3), 15kDa_dialysates_DOC (mg dm3), 15kDa_dialysates_monomeric_Al (µg dm3).

## Common fields and notes
- Common fields across files: SampleSite (name of site), SampleDate (date sample was collected).
- Explanation and Units metadata accompany each field.
- Notes section includes data quality indicators:
  - Not measured
  - Measurement was not made for some reason
  - Insufficient sample to perform analysis
  - Result was below limit of detection stated
  - Symbol "<" used to indicate detection limit considerations

## Location metadata
- Geographic context for sampling sites with coordinates (Easting, Northing):
  - Pool X, Pool Y, Roudsea Wood, River Hodder, Whitray Beck tributary, River Lune, River Ribble, Gais Gill, River Eden, Black Burn, River Tees, Wad Hazel Sike
- Each entry includes Easting and Northing values to enable spatial analyses or mapping.

## Data quality and preparation considerations
- Potential issues:
  - Patchy data and variations in format across files.
  - Not all analytes measured at every site/date.
  - Some fields potentially contain typographical inconsistencies (e.g., alkalinity labeled as alklinity).
  - Handling of censored data at detection limits (values reported as below detection or "<" indicators).
- Recommended steps for use:
  - Harmonize units and confirm unit consistency across files.
  - Merge datasets on SampleSite and SampleDate where appropriate.
  - Flag and address missing values, Not measured entries, and detection-limit-censored data.
  - Validate location metadata for spatial analyses and link to samples as needed.

## Potential analyses and outputs for end users
- Cross-file integration to compare iron speciation (total vs. Fe II, filtered vs. total) with aluminum species across different molecular weight dialysates.
- Spatial analysis of iron and aluminum metrics by site using location coordinates.
- Temporal analyses by SampleDate to identify trends or anomalies in pH, DOC, and metal concentrations.
- Exploration of relationships between pH (field and final), alkalinity, and metal speciation.
- Dashboards or pivot-table reports enabling end users to self-serve: filter by site, date range, or dialysate fraction and compare key metrics (e.g., Fe_total, Fe_II, Al_total, Al_mononeric) across molecular weight cutoffs.
# DailyUrineParameters.csv ReadMe

## Overview
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Purpose: Document dataset for daily nitrogen excretion, urine volume, and urine event frequency calculations
- Reuse note: If data are reused please ensure it is fully cited

## Data curation and filtering
- Excluded observations with zero urination events
- Two replicate sheep (sheep 1 and 5) removed due to infrequency of urine events

## Time window and calculations
- DailyNExcretion, DailyVol, and DailyFrequency calculated assuming time spent in the urine collection apparatus (typically 10:00–16:00) represents a 24 h period
- Sites: semi-improved pasture and improved pasture
- Seasons: spring, summer, autumn (semi-improved); autumn (improved)

## Data headers / variables
- Site: Semi-improved or improved pasture
- Season: Season of collection (spring, summer, autumn for semi-improved; autumn for improved)
- Sheep_ID: Numeric identifier for replicate sheep
- Date: Date of urine collection (dd/mm/yyyy)
- DailyNExcretion: Calculated daily nitrogen excretion (based on time in collection apparatus)
- DailyVol: Estimated daily urine volume (liters per sheep per day)
- DailyFrequency: Estimated frequency of urine events (events per sheep per day)

## Data provenance and citation
- Clearly cite the original source if data are reused

## Data quality and limitations
- Assumption that the 10:00–16:00 collection window represents a full 24 h period may affect accuracy
- Exclusion of zero-event observations and two low-frequency sheep may bias representativeness
- Data come from two pasture sites with differing seasons; note potential interoperability considerations

## Governance considerations for Data Stewards
- Ensure comprehensive metadata (units, methods, time window, site, season, IDs, dates)
- Document data transformations and filtering steps (e.g., removal of zero events and specific sheep)
- Maintain data lineage and versioning; track any reprocessing
- Align with data sharing policies and any embargo or access constraints
- Prepare for upload to data portals/catalogues to aid discoverability

## Reuse guidance
- Provide full citation and version information
- Document method of calculation for DailyNExcretion, DailyVol, and DailyFrequency
- Include collection window assumptions and any site/season context relevant to interpretation
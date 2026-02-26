# DailyUrineParameters.csv ReadMe

## Overview
- Project: Uplands-N2O; Grant NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Purpose: Describes the DailyUrineParameters.csv dataset; notes data filtering and how daily N excretion, volume, and frequency were calculated.
- Data filtering: Excluded observations with zero urination events.
- Replicate handling: Two replicate sheep (sheep 1 and 5) removed due to infrequent urine events.
- Time-based calculations: Daily calculations assume the time spent in the urine collection apparatus (typically 10:00–16:00) is representative of a 24-hour period.

## Data Curation and Filtering
- Exclude zero urination events.
- Remove two replicate sheep due to infrequent urine events.
- Use a daytime collection window (roughly 10:00–16:00) to scale measurements to a 24-hour period.

## Data Structure and Headers
- Site: Semi-improved or improved pasture
- Season: Spring, summer, or autumn (at semi-improved site) and autumn at the improved site
- Sheep_ID: Identifier for each replicate sheep
- Date: Date of urine collection (dd/mm/yyyy)
- DailyNExcretion: Calculated daily nitrogen excretion based on time in the collection apparatus
- DailyVol: Estimated daily urine volume (liters per sheep per day) based on time in the apparatus
- DailyFrequency: Estimated daily urine event frequency (events per sheep per day) based on time in the apparatus

## Calculations and Assumptions
- DailyNExcretion: Derived from observed urine within the collection window
- DailyVol: Estimated from time spent in the apparatus
- DailyFrequency: Estimated from time spent in the apparatus

## Usage and Attribution
- Data reuse: Please ensure full citation of the data source.

## Considerations for Data Leaders
- Representativeness: Calculations assume that daytime collection time reflects a 24-hour period; this may introduce bias.
- Data selection: Excluding zero events and two replicates could affect generalizability and downstream analyses.
- Metadata and provenance: clear documentation of site, season, and date supports traceability and reuse across networks.
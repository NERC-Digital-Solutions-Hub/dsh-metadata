# UrineNExcretionPerPatch.csv ReadMe

- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Usage note: If data are reused please ensure it is fully cited

## Overview

- This ReadMe describes the data file UrineNExcretionPerPatch.csv and its preprocessing.
- The data capture N excretion from urine events in sheep under different pasture conditions and seasons.

## Data filtering and handling

- Observations with zero urination events were excluded.
- Two replicate sheep (sheep 1 and 5) were removed due to infrequent urine events.
- Daily N excretion calculations were derived from individual urine events by assuming the time spent in the urine collection apparatus (typically 10:00–16:00) is representative of a 24-hour period.

## Data structure and variables

- Site: Semi-improved or improved pasture
- Season: Season of collection; values are spring, summer, or autumn for the semi-improved site and autumn for the improved site
- Sheep_ID: Identifier for the replicate sheep
- Date: Date of urine collection (dd/mm/yyyy)
- Vol_ml: Volume of an individual urine event in milliliters
- NContent: N content of the urine event in g N per liter
- Nexcreted: Total nitrogen excreted in the urine event in grams of N

## Calculations and assumptions

- Daily N excretion is estimated by aggregating per-event measurements under the assumption that the collection period reflects a 24-hour period.
- Time window for collection (10:00–16:00) is treated as representative of a full day for volume and frequency calculations.

## Site, season, and sampling details

- Site categories:
  - Semi-improved pasture: Seasonal data include spring, summer, and autumn
  - Improved pasture: Seasonal data include autumn only
- Sheep_IDs correspond to replicates; two replicates were excluded due to low event frequency.

## Data provenance and usage

- Data come from the Uplands-N2O project and are intended for analysis of nitrogen excretion patterns.
- Full citation is required when reusing the data.
- The dataset documents both the raw event-level measurements and the derived daily excretion estimates under stated assumptions.
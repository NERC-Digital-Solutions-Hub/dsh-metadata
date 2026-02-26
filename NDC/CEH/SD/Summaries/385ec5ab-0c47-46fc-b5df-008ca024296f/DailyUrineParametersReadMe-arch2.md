# DailyUrineParameters.csv ReadMe

## Overview
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Purpose: Metadata and calculation methods for daily nitrogen excretion data in sheep, enabling estimation of daily N excretion, urine volume, and urine event frequency across pasture sites and seasons.

## Data content and scope
- Sites: Semi-improved pasture and improved pasture
- Seasons: Spring, Summer, Autumn at the semi-improved site; Autumn at the improved site
- Subjects: Replicate sheep (with some replicates filtered)
- Observations: Urine collection data with calculated daily metrics

## Data fields / headers
- Site: Semi-improved or improved pasture
- Season: Spring, Summer, Autumn (semi-improved) or Autumn (improved)
- Sheep_ID: Identifier for replicate sheep
- Date: Date of urine collection (dd/mm/yyyy)
- DailyNExcretion: Calculated daily nitrogen excretion based on time spent in urine collection apparatus
- DailyVol: Estimated daily urine volume (liters sheep-1 day-1) based on time spent in urine collection apparatus
- DailyFrequency: Estimated urine event frequency (urine events sheep-1 day-1) based on time spent in urine collection apparatus

## Data processing and quality assurance
- Data filtered to exclude observations with zero urination events
- Two replicate sheep (sheep 1 and 5) removed due to relatively infrequent urine events
- Calculations assume the time spent in the collection apparatus represents a 24-hour period

## Calculation and interpretation notes
- DailyNExcretion, DailyVol, and DailyFrequency are derived from observed time in the collection window
- Collection window typically used is 10:00 to 16:00 to represent a 24-hour period

## Usage and citation
- If data are reused, ensure full citation of the source
- This dataset is prepared for standardised analysis and sharing via appropriate data portals

## Project and authorship
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors (as listed above)
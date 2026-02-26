# DailyUrineParameters.csv ReadMe

## Overview
- Project: Uplands-N2O, Grant NE/M015351/1.
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick.
- Note: If data are reused, ensure the citation is fully provided.

## Data scope and purpose
- Data describe daily nitrogen excretion, urine volume, and urine event frequency in sheep.
- Observations with zero urination events were excluded.
- Two replicate sheep (sheep 1 and 5) were removed due to infrequent urine events.
- Daily metrics are estimated by assuming the time spent in the urine collection apparatus (typically 10:00–16:00) represents a 24-hour period.

## Data description and headers
- Site: Semi-improved or improved pasture.
- Season: Spring, Summer or Autumn at the semi-improved site; Autumn at the improved site.
- Sheep_ID: Identifier for each replicate sheep.
- Date: Date of urine collection (dd/mm/yyyy).
- DailyNExcretion: Calculated daily nitrogen excretion based on time in collection apparatus.
- DailyVol: Estimated daily urine volume (liters per sheep per day) based on time in collection apparatus.
- DailyFrequency: Estimated urine event frequency (events per sheep per day) based on time in collection apparatus.

## Data handling and quality notes
- Exclusion criteria: zero urination events and two low-frequency replicates.
- Calculations assume the collection period reflects a 24-hour period for each sheep.

## Reuse and citation
- If data are reused, ensure a full citation to the original source is provided.

## GIS-related considerations
- Data are suitable for map-based visualization of nitrogen excretion patterns across sites and seasons.
- Potential visualizations: spatial distribution by Site, temporal trends by Date/Season, and per-sheep metrics (DailyNExcretion, DailyVol, DailyFrequency).
- Useful fields for GIS: Site, Season, Date, Sheep_ID, and the derived DailyNExcretion, DailyVol, and DailyFrequency.
# UrineNExcretionPerPatch.csv ReadMe

## Overview
- Project: Uplands-N2O; Grant NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Purpose: Provide data on daily nitrogen excretion from urine events in sheep across pasture patches
- Data cleaning: Zero-urination observations removed; two replicates (sheep 1 and 5) removed due to infrequent urine events

## Data content and structure
- Site: Semi-improved or improved pasture
- Season: Season of collection; spring/summer/autumn at semi-improved site and autumn at the improved site
- Sheep_ID: Identifier for replicate sheep
- Date: Urine collection date (dd/mm/yyyy)
- Vol_ml: Volume of each urine event (ml)
- NContent: Nitrogen concentration in urine (g N per L)
- Nexcreted: Total N excreted per urine event (g N)

## Data processing and daily excretion
- Daily N excretion calculated by summing Nexcreted across urine events within the typical collection window (10:00–16:00), assumed representative of a 24 h period
- This approach converts event-level data into an estimate of daily N excretion per patch/season/sheep

## Filtering and data quality
- Excluded observations with zero urine events
- Excluded two replicate sheep due to low frequency of urine events (Sheep 1 and Sheep 5)

## Interpretation, usage, and citation
- Enables comparisons of N excretion by Site and Season, as well as across individual sheep
- Suitable for self-serve analyses via dashboards or pivot tables
- If data are reused, ensure full citation of the source
- Note: Season mapping differs by Site (semi-improved vs. improved) and should be considered in analyses

## Metadata and notes
- Data headers and unit definitions provided for clarity
- Data derived from the Uplands-N2O project; data collection times and assumptions stated for daily excretion estimation
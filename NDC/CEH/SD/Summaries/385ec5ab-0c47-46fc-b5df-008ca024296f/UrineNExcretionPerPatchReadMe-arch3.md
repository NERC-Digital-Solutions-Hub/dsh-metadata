# UrineNExcretionPerPatch.csv ReadMe

## Overview
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Purpose: Data on nitrogen excretion via urine from sheep, used for environmental monitoring and evaluation related to N excretion.
- Reuse note: If data are reused please ensure it is fully cited.

## Data scope
- Data type: Urine excretion measurements from replicate sheep on pasture.
- Data processing: Excluded observations with zero urination events.
- Replicates: Two replicate sheep (sheep 1 and 5) removed due to infrequent urine events.
- Daily calculations: Daily N excretion, volume, and frequency calculated assuming that urine collection (between 10:00 and 16:00) represents a 24 h period.
- Sites: Semi-improved pasture or improved pasture.
- Seasons: Spring, Summer, or Autumn at semi-improved site, and Autumn at the improved site.

## Data fields / columns
- Site: Semi-improved or improved pasture
- Season: Spring, Summer, or Autumn (as above)
- Sheep_ID: Identifier for replicate sheep
- Date: Date of urine collection (dd/mm/yyyy)
- Vol_ml: Volume of an individual urine event (in ml)
- NContent: Nitrogen content of urine (g N per liter)
- Nexcreted: Total nitrogen excreted in each urine event (in g N)

## Data processing and methodological notes
- Time window:  Urine collection assumed to occur between 10:00 and 16:00 for a given day and extrapolated to a 24 h period.
- Data exclusions: Zero urination events removed; two low-frequency replicates removed (sheep 1 and 5).
- Calculations: Daily N excretion, urine volume, and frequency derived from event-level data.
- Data provenance: Data originate from the Uplands-N2O project; consistent with project aims to monitor environmental N fluxes via urine-derived N excretion.

## Metadata, quality, and governance considerations
- Metadata availability: Core fields and definitions provided; additional metadata may be necessary for full interoperability.
- Data quality: Exclusions and assumptions documented; emphasis on representing 24 h period from a defined collection window.
- Data sharing and governance: Noted requirement to cite data when reused; any broader data governance steps (e.g., sharing, openness) would need to be defined at the dataset level.
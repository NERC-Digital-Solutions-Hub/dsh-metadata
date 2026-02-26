# Western Ghats Leaf Water Potential measurements - seasonal cycle

## Overview
- Time-series dataset of pre-dawn and mid-day leaf water potentials for 10 plant species (trees and herbs) from Sep 2020 to May 2021.
- Measurements taken every three months; used alongside hydraulic conductance vulnerability curves to indicate a tree’s safe operating space under drought and high vapor pressure deficit (VPD) conditions.
- Site near Sirsi, Western Ghats, India.

## Study Site and Context
- Location: Sirsi area, Western Ghats, India
- Coordinates: 14.49 N, 74.75 E
- Elevation: 538 meters

## Methods
- Instrument: Scholander pressure chamber (Model 1505D, PMS Instrument, Oregon, USA)
- Procedure: leaf detached, inserted inverted, petiole fixed airtight; pressure at which liquid exudes observed to determine leaf water potential (interpreted as negative MPa).
- Sampling times: predawn (4:00–6:00 am) and mid-day (12:30–3:00 pm)
- Scope: 10 species (including trees and plants); measurements from detached leaves

## Data Structure and Content
- Format: CSV file
- Core variables (columns):
  - species: scientific name
  - id: species initial
  - replicate_treeID: Tree ID
  - Time_in_day: PreDawn or MidDay
  - leaf_water_potential_Mpa: leaf water potential in MPa
  - number_of_leaves_measured: count
  - Month: abbreviated month
  - Year: four-digit year
  - Notes: miscellaneous notes
- Temporal coverage: Sep 2020 to May 2021
- Data notes: measured at three-month intervals; time-of-day measurements included

## Spatial and Data Integration Context
- Spatial scope is site-level; data can be linked to individual trees via replicate_treeID.
- Designed to be combinable with related data from the project (e.g., hydraulic conductance vulnerability curves) for integrated analysis of drought response in GIS-enabled workflows.

## Data Quality and Gaps
- Quality control: measurements repeated and checked by the team.
- Gaps: missing replicate numbers for November sampling; blank cells indicate missing data.

## GIS-Related Usage and Considerations
- Potential uses:
  - Map spatial distribution of leaf water potential by species and time of day
  - Analyze temporal trends (seasonal/dry-season responses) across the site
  - Combine with environmental layers (VPD, rainfall, soil moisture) and the related hydraulic data to model plant water stress
- Important notes for GIS work:
  - Units are MPa (leaf water potential), with negative values representing tension
  - Time_in_day differentiates pre-dawn vs. mid-day measurements
  - Ensure handling of missing data where replicate_treeID or other fields are blank

## Related Data
- This dataset can be integrated with hydraulic conductance vulnerability curves collected in the same project for comprehensive drought-response analyses.
# Western Ghats Leaf Water Potential measurements - seasonal cycle

## Overview
- Time-series dataset of pre-dawn and mid-day leaf water potentials for 10 plant species (including trees and plants).
- Span: September 2020 to May 2021; measurements every three months.
- Leaf water potential measured on detached leaves using a Scholander pressure chamber.
- Purpose: along with hydraulic conductance vulnerability curves measured in the project, to indicate a tree’s safe operating space under dry and high vapor pressure deficit (VPD) conditions.

## Location and Sampling Design
- Site: near Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Species: 10 species; data include species name and a tree/plant identifier.
- Sampling structure: time-series per tree, with data organized by replicate_treeID.

## Data Structure and Variables
- Core columns:
  - Species
  - id (initial of species)
  - replicate_treeID (Tree ID)
  - Time_in_day (PreDawn or MidDay)
  - leaf_water_potential_Mpa (MPa)
  - number_of_leaves_measured
  - Month (abbreviated)
  - Year (YYYY)
  - Notes
- Data notes: Blank cells indicate missing data; missing replicate numbers in November were not recorded.

## Methods and Measurements
- Instrument: Scholander pressure chamber (Model 1505D, PMS Instrument, Oregon, USA).
- Procedure: Leaf inserted in chamber, petiole fixed; pressure applied until liquid exudes from leaf petiole; negative of this pressure is interpreted as leaf water potential.
- Timing: Predawn measurements collected 4–6 am; mid-day measurements 12:30 pm–3 pm.
- Data quality: Leaf potentials were measured multiple times and checked by the team.

## Data Quality and Gaps
- Replicate numbers missing for November sampling (not recorded at the time).
- Blank cells indicate missing data for corresponding variables.

## Potential Analyses and Uses (Analyst Perspective)
- Examine species-specific patterns in leaf water potential and contrasts between pre-dawn and mid-day values.
- Integrate with hydraulic conductance vulnerability curves to model each species’ safe operating space under drought and high VPD.
- Develop predictive models of drought tolerance and potential risk under climate scenarios.
- Cross-species comparisons and temporal trends to inform conservation, forestry decisions, or ecological studies.
- Data gaps at local scales and potential need for supplementary datasets to improve analyses.
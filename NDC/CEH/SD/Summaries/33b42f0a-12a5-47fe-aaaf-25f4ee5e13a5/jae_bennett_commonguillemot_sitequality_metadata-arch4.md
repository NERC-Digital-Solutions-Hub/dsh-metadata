# JAE_Bennett_CommonGuillemot_sitequality

## Overview
- This collection includes four CSV files describing Guillemot site quality metrics across subcolonies and years.
- Files cover occupancy and quality, average quality and breeding success, new site establishment, and site-phase categorisations.
- All files denote missing values with 'NA'.

## Files and key fields

- JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
  - Site.number: Breeding site ID
  - Subcolony: Sub-colony ID
  - Year: Year of study
  - Subcolony.size: Sub-colony size in breeding pairs
  - Wholecolony.size: Whole colony size in breeding pairs
  - Occupancy.status: 1 if occupied, 0 if unoccupied in that year
  - Quality: Average breeding success (chicks fledged per breeding attempt) at a breeding site (excluding the current year)
  - Trend.phase: Population trend direction for the sub-colony (positive, neutral, negative)
  - Trend.slope: Change in sub-colony size over time during a Trend.phase period (pairs per year)
  - Colonisation.phase: Sub-colony status (Colonisation, Decline, Recolonisation)
  - Mean.size.scale: Sub-colony size mean-centred and scaled per sub-colony
  - Mean.trend.scale: Sub-colony trend mean-centred and scaled per sub-colony
  - Mean.whole.colony.size.scale: Whole colony size mean-centred and scaled
  - Mean.whole.colony.trend.scale: Whole colony trend mean-centred and scaled

- JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
  - Subcolony: Sub-colony ID
  - Year: Year of study
  - Quality: Average breeding success at a breeding site (excluding the current year)
  - Successful.breeding: Total number of successful breeding attempts for each sub-colony in each year
  - Unsuccessful.breeding: Total number of unsuccessful breeding attempts for each sub-colony in each year
  - Mean.size.scale: Sub-colony size mean-centred and scaled per sub-colony
  - Mean.trend.scale: Sub-colony trend mean-centred and scaled per sub-colony
  - Mean.whole.colony.size.scale: Whole colony size mean-centred and scaled
  - Mean.whole.colony.trend.scale: Whole colony trend mean-centred and scaled

- JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
  - Subcolony: Sub-colony ID
  - Year: Year of study
  - Colonisation.phase: Period type (Colonisation, Decline, Recolonisation)
  - No.new.sites: Number of newly-established breeding sites in that sub-colony in that year
  - No.not.new.sites: Number of occupied breeding sites in that sub-colony in that year that were not newly-established
  - Mean.size.scale: Sub-colony size mean-centred and scaled for each sub-colony

- JAE_Bennett_CommonGuillemot_sitequality_phases.csv
  - Subcolony: Sub-colony ID
  - Year: Year of study
  - Subcolony.size: Sub-colony size in breeding pairs
  - Colonisation.phase: Period type (Colonisation, Decline, Recolonisation)
  - Reocc.new: Whether the row pertains to 'Reoccupied' or 'New' breeding sites at that sub-colony in that year
  - Prop.sites: Proportion of breeding sites in the current row's category 'Reocc.new' established in that sub-colony that year
  - No.established: Number of breeding sites in the current row's category 'Reocc.new' established in that sub-colony that year
  - No.not.established: Number of sites not in the current row's category 'Reocc.new' established in that sub-colony that year
  - Pop.trend.phase: Whole colony trend phase (Colonisation, Decline, Recolonisation)
  - Mean.quality: Mean site quality for sites summarised in this row

## How this supports Data Leaders
- Provides a modular data asset representing occupancy, quality, and dynamics of Guillemot subcolonies, enabling:
  - End-to-end data understanding from subcolony to whole-colony scales.
  - Tracking of user/researcher needs through repeated yearly measurements and derived scales.
  - Identification of data gaps and granularity requirements (e.g., subcolony vs. whole-colony metrics).
  - Structured data discovery via clearly named fields and standardized scaling (mean-centred and scaled metrics).
  - Iterative product improvement through linkage of occupancy, quality, and colonisation phases to guide analyses and reporting.

## Data quality and preparation considerations
- Missing values are represented as 'NA' across all files.
- Several metrics are mean-centred and scaled at the subcolony or colony level to support cross-subcolony comparisons.
- Derived indicators include trend phase, colonisation phase, and proportions of site establishment (Reocc./New).

## Notes for data governance and usage
- Ensure consistent interpretation of categorical fields (e.g., Colonisation.phase, Reocc.new) across analyses.
- When combining files, align on Subcolony and Year to maintain temporal and spatial context.
- Be mindful of different base definitions: occupancy vs. quality vs. breeding success; treat each as related but distinct signals.
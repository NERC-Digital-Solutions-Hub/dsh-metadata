# JAE_Bennett_CommonGuillemot_sitequality_data_files

## Overview
- A set of CSV data files describing breeding site quality, occupancy, colonisation dynamics, and sub-colony/colony metrics for common Guillemots.
- Designed to support GIS-based visualization and spatial-temporal analyses of breeding sites, subcolonies, and colony trends.
- Null values are denoted as NA.

## Data files and key fields

- JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
  - Site.number: Breeding site ID
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Subcolony.size: sub-colony size (breeding pairs)
  - Wholecolony.size: whole colony size (breeding pairs)
  - Occupancy.status: 1 if occupied, 0 if unoccupied
  - Quality: average breeding success (chicks fledged per breeding attempt) at a site (excluding current year)
  - Trend.phase: sub-colony population trend (Positive, Neutral, Negative)
  - Trend.slope: change in sub-colony size per year during Trend.phase
  - Colonisation.phase: Colonisation, Decline, or Recolonisation
  - Mean.size.scale: subcolony size, mean-centered and scaled per sub-colony
  - Mean.trend.scale: subcolony trend, mean-centered and scaled per sub-colony
  - Mean.whole.colony.size.scale: whole colony size, mean-centered and scaled
  - Mean.whole.colony.trend.scale: whole colony trend, mean-centered and scaled

- JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Quality: average breeding success at a breeding site (excluding current year)
  - Successful.breeding: total successful breeding attempts per sub-colony per year
  - Unsuccessful.breeding: total unsuccessful breeding attempts per sub-colony per year
  - Mean.size.scale: subcolony size, mean-centered and scaled
  - Mean.trend.scale: subcolony trend, mean-centered and scaled
  - Mean.whole.colony.size.scale: whole colony size, mean-centered and scaled
  - Mean.whole.colony.trend.scale: whole colony trend, mean-centered and scaled

- JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Colonisation.phase: Colonisation, Decline, or Recolonisation
  - No.new.sites: number of newly-established breeding sites in that sub-colony/year
  - No.not.new.sites: number of occupied sites in that sub-colony/year that were not newly-established
  - Mean.size.scale: subcolony size, mean-centered and scaled

- JAE_Bennett_CommonGuillemot_sitequality_phases.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Subcolony.size: sub-colony size (breeding pairs)
  - Colonisation.phase: Colonisation, Decline, or Recolonisation
  - Reocc.new: whether row pertains to 'Reoccupied' or 'New' breeding sites
  - Prop.sites: proportion of breeding sites in the current category 'Reocc.new' established that year
  - No.established: number of sites in the current category established that year
  - No.not.established: number of sites not in the current category established that year
  - Pop.trend.phase: whole colony trend phase (Colonisation, Decline, or Recolonisation)
  - Mean.quality: mean site quality for sites summarised in this row

## Data handling and preparation
- Data come from multiple sources and resolutions (subcolony vs. whole colony).
- Many derived, scaled variables are included (mean-centred and scaled) for GIS analysis and comparison across subcolonies.
- NA denotes missing values; careful handling needed during joins and visualizations.

## GIS usage considerations
- Potential map layers:
  - Occupancy: binary or categorical (occupied vs unoccupied) per site/year.
  - Quality: choropleth by site/subcolony or by year.
  - Subcolony size and whole-colony size (scaled values) for normalization across subcolonies.
  - Trend phase and slope to show directional changes over time.
  - Colonisation phase and Reocc.new status to illustrate emergence and recolonisation dynamics.
  - New sites vs not-new sites to map site establishment patterns.
- Temporal analysis:
  - Time-series visualization by year to show changes in occupancy, quality, and colony trends.
- Data alignment:
  - Ensure consistent identifiers (Site.number, Subcolony) when joining files.
  - Use mean-centered/scaled fields for cross-subcolony comparisons.
- Data quality:
  - Handle NA values appropriately in rasters or vector layers.
  - Be mindful of differing resolutions between subcolony-level and whole-colony metrics.

## Challenges and cautions for GIS specialists
- Data are distributed across several files with varying resolutions and schemas.
- Inconsistent data standards and missing values can complicate integration.
- Large or complex datasets may require chunking or staged processing.
- Cleaning and transforming data to a GIS-ready state is often required (e.g., aligning IDs, normalizing scales).

## Practical takeaways
- Leverage occupancy and quality fields for multiple map products.
- Use mean-centred and scaled metrics to compare subcolonies on a common scale.
- Combine site-level (occupancy/quality) with colony-level indicators (Colony phase, trends) for comprehensive spatial-temporal storytelling.
# JAE_Bennett_CommonGuillemot_sitequality

- Purpose and scope
  - A dataset suite for monitoring Guillemot site quality and occupancy over time to assess environmental health and policy performance.
  - Designed for analysts with environmental monitoring responsibilities, using standardized measures and trend analysis to compare subcolony and colony dynamics.

- Data handling note
  - Null values are indicated by 'NA' across all data files.

- Data files and key content
  - JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
    - Core identifiers and measures:
      - Site.number: Breeding site ID
      - Subcolony: Sub-colony ID
      - Year: year of study
      - Subcolony.size: Sub-colony size in breeding pairs
      - Wholecolony.size: Whole colony size in breeding pairs
      - Occupancy.status: Occupied (1) or unoccupied (0) in that year
      - Quality: Average breeding success (chicks fledged per breeding attempt) at a breeding site excluding the current year
      - Trend.phase: Population trend direction in sub-colony (positive, neutral, negative)
      - Trend.slope: Change in sub-colony size over time during a Trend.phase period (pairs per year)
      - Colonisation.phase: Sub-colony period (Colonisation, Decline, Recolonisation)
      - Mean.size.scale: Sub-colony size mean-centred and scaled per sub-colony
      - Mean.trend.scale: Sub-colony trend mean-centred and scaled per sub-colony
      - Mean.whole.colony.size.scale: Whole colony size mean-centred and scaled
      - Mean.whole.colony.trend.scale: Whole colony trend mean-centred and scaled

  - JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
    - Focused on quality and breeding outcomes:
      - Subcolony: Sub-colony ID
      - Year: year of study
      - Quality: Average breeding success at a breeding site excluding the current year
      - Successful.breeding: Total number of successful breeding attempts for each sub-colony in each year
      - Unsuccessful.breeding: Total number of unsuccessful breeding attempts for each sub-colony in each year
      - Mean.size.scale: Sub-colony size mean-centred and scaled per sub-colony
      - Mean.trend.scale: Sub-colony trend mean-centred and scaled per sub-colony
      - Mean.whole.colony.size.scale: Whole colony size mean-centred and scaled
      - Mean.whole.colony.trend.scale: Whole colony trend mean-centred and scaled

  - JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
    - New site establishment data:
      - Subcolony: Sub-colony ID
      - Year: year of study
      - Colonisation.phase: Period (Colonisation, Decline, Recolonisation)
      - No.new.sites: Number of breeding sites newly established in that sub-colony in that year
      - No.not.new.sites: Number of sites occupied in that sub-colony in that year that were not newly-established
      - Mean.size.scale: Sub-colony size mean-centred and scaled for each sub-colony

  - JAE_Bennett_CommonGuillemot_sitequality_phases.csv
    - Phase-level context and site establishment details:
      - Subcolony: Sub-colony ID
      - Year: year of study
      - Subcolony.size: Sub-colony size in breeding pairs
      - Colonisation.phase: Period of Colonisation, Decline, or Recolonisation
      - Reocc.new: Indicates Reoccupied or New breeding sites at that sub-colony in that year
      - Prop.sites: Proportion of breeding sites in the current row's Reocc.new category established in that sub-colony in that year
      - No.established: Number of breeding sites in the current row's Reocc.new category established in that sub-colony in that year
      - No.not.established: Number of sites not in the current row's category established in that sub-colony in that year
      - Pop.trend.phase: Whole colony trend phase (Colonisation, Decline, Recolonisation)
      - Mean.quality: Mean site quality of sites summarized in this row

- How the data supports environmental monitoring and analysis
  - Enables tracking of occupancy dynamics and breeding success across subcolonies and years.
  - Facilitates assessment of colonisation and recolonisation processes and their relationship to overall population health.
  - Provides standardized, scaled metrics (mean-centred and scaled) to compare subcolonies and to integrate with other environmental indicators.
  - Supports combined analyses across files (e.g., linking occupancy, quality, breeding outcomes, and new site establishment for holistic site quality assessment).

- Practical use for analysts
  - Monitor temporal trends in occupancy, colony size, and breeding success to evaluate environmental health and policy outcomes.
  - Analyze colonisation phases and the emergence of new breeding sites as indicators of habitat suitability and population recovery or decline.
  - Use scaled metrics to compare subcolonies and to aggregate findings at the whole-colony level.
  - Link site-level data with broader environmental datasets to enhance inference about drivers and impacts.

- Considerations and challenges
  - Ensure consistent interpretation of coded fields (e.g., 1/0 for occupancy, phase labels for Colonisation/Decline/Recolonisation, and Reocc.new categories).
  - Be mindful that Quality metrics exclude the current year, which affects year-to-year comparisons.
  - Data integration across files requires careful alignment on Subcolony and Year to build comprehensive site-quality profiles.
  - Aim to increase data value by combining these datasets with other relevant environmental data and by ensuring accessible underlying data for validation and reuse.
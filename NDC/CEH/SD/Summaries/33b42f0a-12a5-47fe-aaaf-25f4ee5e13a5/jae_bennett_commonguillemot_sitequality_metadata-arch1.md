# JAE Bennett Common Guillemot Site Quality Data

- Overview
  - A set of related CSV files describing breeding site quality, occupancy, site colonisation phases, and related metrics for Guillemots.
  - All null values are indicated by NA.
  - Data focus on sub-colonies and whole colonies, with size, occupancy, quality, and trend measures across years.

- Data files and key columns
  - JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
    - Site.number: Breeding site ID
    - Subcolony: Sub-colony ID
    - Year: year of study
    - Subcolony.size: Sub-colony size (breeding pairs)
    - Wholecolony.size: Whole colony size (breeding pairs)
    - Occupancy.status: 1 = occupied, 0 = unoccupied (in that year)
    - Quality: average breeding success (chicks fledged per breeding attempt) at a breeding site excluding the current year
    - Trend.phase: population trend direction for the sub-colony (positive, neutral, negative)
    - Trend.slope: change in sub-colony size per year within a Trend.phase
    - Colonisation.phase: Colonisation, Decline, or Recolonisation
    - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony
    - Mean.trend.scale: sub-colony trend mean-centred and scaled for each sub-colony
    - Mean.whole.colony.size.scale: whole colony size mean-centred and scaled
    - Mean.whole.colony.trend.scale: whole colony trend mean-centred and scaled

  - JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
    - Subcolony: Sub-colony ID
    - Year: year of study
    - Quality: average breeding success at a breeding site excluding the current year
    - Successful.breeding: total number of successful breeding attempts for each sub-colony in that year
    - Unsuccessful.breeding: total number of unsuccessful breeding attempts for each sub-colony in that year
    - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony
    - Mean.trend.scale: sub-colony trend mean-centred and scaled for each sub-colony
    - Mean.whole.colony.size.scale: whole colony size mean-centred and scaled
    - Mean.whole.colony.trend.scale: whole colony trend mean-centred and scaled

  - JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
    - Subcolony: Sub-colony ID
    - Year: year of study
    - Colonisation.phase: Colonisation, Decline, or Recolonisation
    - No.new.sites: number of breeding sites newly established in that sub-colony in that year
    - No.not.new.sites: number of sites that were occupied in that sub-colony in that year that were not newly-established
    - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony

  - JAE_Bennett_CommonGuillemot_sitequality_phases.csv
    - Subcolony: Sub-colony ID
    - Year: year of study
    - Subcolony.size: Sub-colony size (breeding pairs)
    - Colonisation.phase: Colonisation, Decline, or Recolonisation
    - Reocc.new: whether the data row pertains to 'Reoccupied' or 'New' breeding sites at that sub-colony in that year
    - Prop.sites: proportion of breeding sites in the current row's category 'Reocc.new' established in that sub-colony in that year
    - No.established: number of breeding sites in the current row's category 'Reocc.new' that were established in that sub-colony in that year
    - No.not.established: number of sites not in the current row's category 'Reocc.new' established in that sub-colony in that year
    - Pop.trend.phase: whole colony trend direction (Colonisation, Decline, or Recolonisation)
    - Mean.quality: mean site quality of sites summarized in this row

- Common structure and scaling
  - Several size, trend, and colony-wide metrics are mean-centred and scaled per sub-colony or per colony to support comparative analyses.
  - Variables cover occupancy, colonisation status, site quality, and breeding success (with breakdowns into successful vs. unsuccessful).

- Analytical opportunities and considerations
  - Potential to correlate occupancy and colonisation phases with site quality and breeding success.
  - Use of mean-centred/scaled metrics to compare trajectories across sub-colonies.
  - Examination of how new sites emerge and how established sites contribute to overall colony trends.
  - Combine occupancy, quality, and phase data to model predictors of successful breeding and colonisation outcomes.
  - Manage NA values consistently across datasets when merging (as indicated by NA encoding).

- Data quality and usage notes
  - Data are tabular with clearly defined per-year observations across sub-colonies and colonies.
  - Some fields rely on excluding current-year data (e.g., Quality in occupancy file, Successful/Unsuccessful breeding).
  - Metadata includes scaling details to aid replication and cross-site comparisons.

- Practical implications for analysts
  - The suite enables multi-level analyses (sub-colony and whole-colony) over time.
  - Facilitates development of predictive models of site occupancy, colonisation events, and breeding success.
  - Encourages transparency and reproducibility through explicit scaling metadata and clear column definitions.
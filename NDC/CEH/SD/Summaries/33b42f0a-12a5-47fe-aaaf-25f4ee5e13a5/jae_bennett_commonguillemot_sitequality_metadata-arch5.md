# JAE_Bennett_CommonGuillemot_sitequality

## Overview
- A set of four CSV files documenting Guillemot site quality, occupancy, and colony dynamics across subcolonies and years.
- Data focus on occupancy status, breeding success, site establishment, and colonisation phases, with both raw and derived (scaled) metrics.
- Null values are indicated as NA across all files.

## Files and Key Variables

- JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
  - Site.number: Breeding site ID
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Subcolony.size: Sub-colony size in breeding pairs
  - Wholecolony.size: Whole colony size in breeding pairs
  - Occupancy.status: 1 if occupied, 0 if unoccupied
  - Quality: average breeding success (chicks fledged per breeding attempt) at a breeding site excluding the current year
  - Trend.phase: population trend direction for the sub-colony (positive, neutral, negative)
  - Trend.slope: change in sub-colony size per year during Trend.phase
  - Colonisation.phase: period of Colonisation, Decline, or Recolonisation
  - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony
  - Mean.trend.scale: sub-colony trend mean-centred and scaled for each sub-colony
  - Mean.whole.colony.size.scale: whole colony size mean-centred and scaled
  - Mean.whole.colony.trend.scale: whole colony trend mean-centred and scaled

- JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Quality: average breeding success at a breeding site excluding the current year
  - Successful.breeding: total number of successful breeding attempts for each sub-colony in each year
  - Unsuccessful.breeding: total number of unsuccessful breeding attempts for each sub-colony in each year
  - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony
  - Mean.trend.scale: sub-colony trend mean-centred and scaled for each sub-colony
  - Mean.whole.colony.size.scale: whole colony size mean-centred and scaled
  - Mean.whole.colony.trend.scale: whole colony trend mean-centred and scaled

- JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Colonisation.phase: period of Colonisation, Decline, or Recolonisation
  - No.new.sites: number of breeding sites newly established in the sub-colony that year
  - No.not.new.sites: number of occupied sites in the sub-colony that were not newly-established
  - Mean.size.scale: sub-colony size mean-centred and scaled for each sub-colony

- JAE_Bennett_CommonGuillemot_sitequality_phases.csv
  - Subcolony: Sub-colony ID
  - Year: year of study
  - Subcolony.size: Sub-colony size in breeding pairs
  - Colonisation.phase: period of Colonisation, Decline, or Recolonisation
  - Reocc.new: whether the row pertains to 'Reoccupied' or 'New' breeding sites at that sub-colony in that year
  - Prop.sites: proportion of breeding sites in the current row's category 'Reocc.new' established in that sub-colony in that year
  - No.established: number of breeding sites in the current row's category 'Reocc.new' established in that sub-colony in that year
  - No.not.established: number of sites not in the current row's category 'Reocc.new' established in that sub-colony in that year
  - Pop.trend.phase: overall colony trend phase (Colonisation, Decline, or Recolonisation)
  - Mean.quality: mean site quality of sites summarised in this row

## Data quality and standardisation

- Consistent missing-value marker: NA across all files.
- Derived scaling: Mean.*.scale fields provide mean-centred and scaled metrics for cross-site comparability (per sub-colony or per whole colony).
- Categorical encodings: Occupancy.status (binary), Trend.phase, Colonisation.phase, Reocc.new categorize temporal and state information.
- Temporal linkage: files are indexed by Year and Subcolony, enabling longitudinal analyses and cross-file joins on Subcolony and Year.
- Documentation of derived fields facilitates reproducibility and reuse across studies and portals.

## Governance and Stewardship Considerations

- Metadata completeness: the files include explicit definitions for each variable and derived scales; ensure persistent metadata alignment if files are updated.
- Data integration: multiple files share common identifiers (Subcolony, Year); establish a standardized schema and join keys for discovery and analysis.
- Update and provenance: plan for versioning and clear provenance of any data transformations (e.g., how Scale metrics are computed).
- Data completeness and timeliness: anticipate potential delays in data submission from various data creators; address gaps to avoid incomplete pictures of user needs.
- Interoperability: maintain consistent naming, units, and category codes across files to ease integration with other datasets.
- Access and sharing policies: define who may access site-level details, especially if any breeding-site data could be sensitive; document embargoes or restrictions if applicable.

## Practical Implications for Discovery and Reuse

- Strong suitability for longitudinal and cross-site analyses of site quality, occupancy, and colonisation dynamics.
- Scaled metrics enable comparisons across subcolonies with differing sizes and trends.
- Clear, model-ready variables (Quality, Mean.quality, Successful.breeding, etc.) support reproductive success analyses and habitat management assessments.
- Users should join files on Subcolony and Year to build holistic view of each subcolony’s status and the colony as a whole.
- The presence of both raw counts (e.g., No.new.sites) and derived scales supports both descriptive summaries and multivariate modeling.

## Summary of Purpose

- This dataset collection provides comprehensive, longitudinal measures of Guillemot site quality, occupancy, and colonisation dynamics at the subcolony level, with standardized scales to support cross-site comparisons and integration into data portals for discovery, governance, and reuse by researchers and practitioners.
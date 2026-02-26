# JAE Bennett Common Guillemot site quality data files

- Purpose and scope
  - A set of CSV data files describing site quality, occupancy, colonisation dynamics, and sub-colony/colony scales for Common Guillemots.
  - Intended to support monitoring, evaluation of policy/actions, and informing future decisions.
  - Null values are coded as 'NA'.

- Files and key variables
  - JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
    - Site.number (breeding site ID), Subcolony (sub-colony ID), Year, Subcolony.size, Wholecolony.size
    - Occupancy.status (1 = occupied, 0 = unoccupied)
    - Quality (average breeding success excluding current year)
    - Trend.phase (positive/neutral/negative), Trend.slope (change in sub-colony size per year)
    - Colonisation.phase (Colonisation/Decline/Recolonisation)
    - Mean.size.scale, Mean.trend.scale, Mean.whole.colony.size.scale, Mean.whole.colony.trend.scale (sub-colony and colony means centred and scaled)
  - JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
    - Subcolony, Year, Quality (mean site quality excluding current year)
    - Successful.breeding, Unsuccessful.breeding (counts per sub-colony/year)
    - Mean.size.scale, Mean.trend.scale, Mean.whole.colony.size.scale, Mean.whole.colony.trend.scale (centred/scaled metrics)
  - JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
    - Subcolony, Year, Colonisation.phase
    - No.new.sites (newly established breeding sites that year)
    - No.not.new.sites (occupied sites that were not newly established)
    - Mean.size.scale (sub-colony size centred/scaled)
  - JAE_Bennett_CommonGuillemot_sitequality_phases.csv
    - Subcolony, Year, Subcolony.size
    - Colonisation.phase (Colonisation/Decline/Recolonisation)
    - Reocc.new (Reoccupied or New sites in that year)
    - Prop.sites (proportion of sites in the current row's Reocc.new category established that year)
    - No.established, No.not.established (numbers established in that year within the category)
    - Pop.trend.phase (Colony-wide Colonisation/Decline/Recolonisation)
    - Mean.quality (mean site quality for the sites summarized in the row)

- Data structure and standardisation
  - Several metrics are mean-centred and scaled within each sub-colony or colony (e.g., Mean.size.scale, Mean.trend.scale, Mean.whole.colony.size.scale, Mean.whole.colony.trend.scale).
  - Consistent use of categorical descriptors for phases (Colonisation, Decline, Recolonisation) and for sub-colony dynamics (Reocc.new, New).

- Data quality, metadata, and governance considerations
  - Metadata gaps may hinder quick verification of dataset suitability; some fields rely on precise definitions and consistent categorisation across years.
  - Some data require transformation to be ready for analysis (scaling, centering, and alignment of sub-colony vs. colony-level metrics).
  - Openness and sharing of underlying data should be considered alongside quality assurance, data cleaning, and provenance.

- How this supports monitoring and decision-making
  - Provides longitudinal indicators of occupancy, breeding success (quality), and productivity (successful vs. unsuccessful breeding).
  - Captures spatial dynamics via subcolony and colony-scale trends, including colonisation and recolonisation events.
  - Enables monitoring dashboards and reporting through standardized, comparable measures (scaled metrics) across sub-colonies and years.
  - Supports analysis of data gaps (new vs. established sites) and the effectiveness of colonisation processes.

- Practical considerations for use by monitoring framework authors
  - Verify and harmonise metadata across files to ensure consistent interpretation of columns and scales.
  - Ensure timely data updates to maintain up-to-date trend assessments and governance.
  - Address barriers to data sharing by documenting data provenance, quality checks, and transformation steps.
  - Use the scaled metrics to compare sub-colonies and identify management priorities or policy impacts.
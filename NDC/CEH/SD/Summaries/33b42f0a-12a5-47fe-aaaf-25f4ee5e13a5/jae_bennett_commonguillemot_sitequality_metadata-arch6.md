# JAE_Bennett_CommonGuillemot Site Quality Data Files

- Purpose and scope
  - A set of data files describing site quality and dynamics for Common Guillemots, enabling exploration of occupancy, breeding success, colonisation and recolonisation dynamics, and subcolony/colony trends across years.
  - Data are designed to be combined and analyzed to produce insights and self-serve outputs (dashboards, pivot tables, reports).

- Data conventions
  - Null values are indicated by NA.
  - Key identifiers: Subcolony (sub-colony ID) and Year; many metrics are centered and scaled per sub-colony for comparability.

- Datasets and their key contents
  - JAE_Bennett_CommonGuillemot_sitequality_occupancy.csv
    - Core fields: Site.number, Subcolony, Year, Subcolony.size, Wholecolony.size, Occupancy.status (1/0), Quality (average breeding success excluding current year), Trend.phase (Positive/Neutral/Negative), Trend.slope (change in sub-colony size per year), Colonisation.phase (Colonisation/Decline/Recolonisation).
    - Derived/scaling fields: Mean.size.scale, Mean.trend.scale, Mean.whole.colony.size.scale, Mean.whole.colony.trend.scale.
  - JAE_Bennett_CommonGuillemot_sitequality_averagequality-and-success.csv
    - Core fields: Subcolony, Year, Quality, Successful.breeding, Unsuccessful.breeding.
    - Derived/scaling fields: Mean.size.scale, Mean.trend.scale, Mean.whole.colony.size.scale, Mean.whole.colony.trend.scale.
  - JAE_Bennett_CommonGuillemot_sitequality_newsites.csv
    - Core fields: Subcolony, Year, Colonisation.phase, No.new.sites, No.not.new.sites.
    - Derived/scaling field: Mean.size.scale.
  - JAE_Bennett_CommonGuillemot_sitequality_phases.csv
    - Core fields: Subcolony, Year, Subcolony.size, Colonisation.phase, Reocc.new (New vs Reoccupied), Prop.sites (proportion of sites in Reocc.new established that year), No.established, No.not.established, Pop.trend.phase, Mean.quality.
  
- How the data relate
  - Subcolony and Year serve as linking keys across all files.
  - Columns indicate per-subcolony and per-year measures of size, occupancy, quality, breeding outcomes, and colony-level trends.
  - Derived scales (Mean.*.scale) support cross-subcolony comparisons and trend analyses.

- Potential analyses and data products
  - Occupancy dynamics by subcolony and year, with associated site quality and breeding success.
  - Analysis of colonisation and recolonisation periods, including numbers of new vs not-new sites.
  - Subcolony and whole-colony size and trend scaling to compare growth patterns across subcolonies.
  - Proportions and counts of established sites in Reocc.new categories, informing understanding of colonisation success.
  - Visual dashboards or pivot reports showing relationships between size, trend, quality, and breeding outcomes over time.

- Data quality and preparation considerations
  - Expect missing values represented as NA; plan for imputation or exclusion as appropriate.
  - Ensure consistent Subcolony IDs and Year alignment when merging datasets.
  - Be mindful of interpretation of derived scales (mean-centred and scaled per subcolony) when comparing across subcolonies.

- Practical tips for Data Support
  - Start by verifying data sufficiency and consistency across the four files for the years and subcolonies of interest.
  - Clean and harmonize identifiers, then join datasets on Subcolony and Year to enable comprehensive analyses.
  - Use the self-serve-ready metrics and scaled fields to build dashboards and reports that communicate occupancy, quality, and colonial dynamics clearly.
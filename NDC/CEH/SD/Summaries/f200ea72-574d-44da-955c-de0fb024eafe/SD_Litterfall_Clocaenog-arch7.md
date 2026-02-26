# Details of data structure for 'Litterfall_Clocaenog.csv'

- Purpose and scope
  - Supplement to the supporting documentation for data series related to Clocaenog litterfall data.
  - Provides the data structure for the Litterfall_Clocaenog.csv dataset, intended for GIS usage and map-based analysis.

-Dataset overview
  - One spreadsheet containing 48 columns.
  - 28 columns cover litterfall data at the level of individual sample quadrats; 1 column is date, 27 columns contain experimental details (Plot, Block, Treatment, and sampling quadrat details).
  - 10 columns cover plot-level mean litterfall data (dates plus means for plots 1–9).
  - 10 columns cover plot-level mean litterfall per unit area (dates plus means per area).

-Column breakdown
  - Columns 1-28: Litterfall data in grams per sample quadrat
    - Column 1: Sampling date (range: 10/11/1999 to 14/06/2011)
    - Columns 2-28: Experimental details and quadrat-specific data (Plot, Block, Treatment, sampling quadrats)
  - Columns 29-38: Plot-level mean litterfall data
    - Column 29: Date (same range)
    - Columns 30-38: Mean litterfall mass per plot for plots 1–9
  - Columns 39-48: Plot-level mean litterfall per unit area
    - Column 39: Date (same range)
    - Columns 40-48: Mean litterfall mass per area

- Temporal and data completeness
  - Sampling spans 1999-2011.
  - Empty cells indicate no data for that specific day.

- GIS-related considerations
  - Data are tied to spatial identifiers: Plot, Block, Treatment, and sampling quadrats, enabling joins to spatial layers representing plots and quadrats.
  - Can be used to create time-enabled maps of litterfall, either per quadrat, per plot, or per unit area.
  - Requires careful handling of missing data during spatial analyses and time-series visualizations.

- Data quality and integration notes
  - Ensure consistent use of identifiers (Plot, Quadrats, Blocks) when joining to spatial features.
  - Be mindful of varying data resolutions: quadrat-level data vs. plot-level averages.
  - Data units are grams of litter per quadrat or per area; maintain unit consistency when aggregating or comparing.

- Useful for GIS workflows
  - Map-based visualization of litterfall across space and time.
  - Aggregation by plot or by area to compare treatments or blocks.
  - Integration with other spatial datasets (e.g., treatment plots, experimental blocks) for contextual mapping.
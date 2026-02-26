# Details of data structure for 'Litterfall_Clocaenog.csv'

- Purpose and provenance
  - Supplement to the supporting documentation for data series documented in 'Clocaenog_supporting documentation_Data series.rtf'.
  - Describes the data structure of the dataset 'Litterfall_Clocaenog.csv'.

- Dataset composition
  - Single spreadsheet containing 48 columns.
  - Columns 1–28: raw litterfall data (in grams per litter sample quadrat).
  - Columns 29–38: plot-level mean litterfall data.
  - Columns 39–48: plot-level mean litterfall data per unit area.

- Time frame and sampling details
  - Sampling date (Column 1): from 10/11/1999 to 14/06/2011.
  - Column 29 and Column 39 series both use dating aligned with the raw data period (10/11/1999 to 14/06/2011).

- Data structure specifics
  - Columns 2–28 provide experimental details for each litterfall measurement: Plot, Block, Treatment, and sampling quadrats.
  - Columns 30–38 present mean litterfall mass per plot for plots 1–9.
  - Columns 40–48 present mean litterfall mass per area for corresponding plots/units.
  - Empty cells indicate no data available for that date.

- Metadata and documentation considerations for data stewards
  - Ensure metadata clearly specifies:
    - Units (g litter per sample quadrat; mean mass per plot; mean per area).
    - Definitions of Plot, Block, Treatment, and sampling quadrats.
    - Date format and range, with explicit interpretation (dd/mm/yyyy as used here).
    - Handling of missing data (empty cells) and any imputation policies if applicable.
  - Maintain linkage to the supporting documentation and provenance (Clocaenog data series documentation).
  - Catalogue the dataset to support discoverability and reproducibility, including the data’s temporal span (1999–2011) and structure.

- Data governance and accessibility notes
  - Ensure data quality through validation of column integrity, consistent naming, and clear description of each column’s contents.
  - Document data updates or corrections and maintain versioning.
  - Prepare for potential data transfers across systems by providing clear mappings for raw vs. aggregated (mean) data columns.
  - Assess data availability and limitations (e.g., periods with missing data) for users and data users’ needs.

- Key considerations for use
  - Researchers relying on the dataset need clarity on how raw measurements translate to plot-level means and area-normalized values.
  - Full traceability from raw quadrat measurements to aggregated outputs is essential for reuse and replication.
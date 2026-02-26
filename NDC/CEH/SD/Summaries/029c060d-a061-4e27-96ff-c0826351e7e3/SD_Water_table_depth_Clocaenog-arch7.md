# Details of data structure for 'Water table depth_Clocaenog.csv

- Overview
  - A single spreadsheet with 10 columns.
  - Column 1 contains dates; Columns 2–10 contain water table depth measurements for experimental plots 1–9.
  - Values for depths are in centimetres (cm) from the soil surface.
  - Entries of 'below detectable limit' indicate water below the water table.

- Temporal coverage
  - Dates range from 13/05/1999 to 30/06/2015.

- Spatial scope
  - 9 experimental plots (plots 1–9) at the Clocaenog site.
  - No explicit coordinates provided in this document; intended for integration with site-level GIS layers.

- Data types and encoding
  - Column 1: Date (temporal field).
  - Columns 2–10: numeric depth values (cm) or the sentinel text 'below detectable limit' for non-detects.

- GIS-ready considerations
  - Prepare for time-enabled analyses by maintaining a date key and per-plot depth values.
  - Handle 'below detectable limit' as a non-numeric flag (e.g., null with an accompanying flag field or coded value).
  - If needed for mapping, reshape from wide to long format (date, plot_id, depth) or create per-plot layers with time dimension.
  - Align with related Clocaenog data series documentation for consistency and quality assurance.

- Data quality and preparation notes
  - Supplementary to the main documentation; ensure cross-reference with Clocaenog_supporting documentation_Data series.rtf.
  - Potential data gaps due to missing dates or non-detect values must be addressed in GIS workflows.
# Details of data structure for 'Fortnightly soil respiration_Clocaenog.csv'

- This document is a supplement to the supporting documentation for data series titled 'Clocaenog_supporting documentation_Data series.rtf'.
- Purpose: Describe the data structure of the Fortnightly soil respiration dataset from Clocaenog for data stewardship and reuse.

## Dataset structure

- Format: One spreadsheet.
- Columns: 11 total, with the data described as Date, Method, and Soil respiration for 1-9 plots.
- Row/content layout as described:
  - The first row contains the plot numbers 1–9.
  - The second row contains the climate treatment.
  - The method column contains the measurement method.
- Time span: Data entries range from 30/03/1999 to 30/06/2015.
- Missing data: Empty cells indicate no data available for that date.

## Data conventions and interpretation

- Date: Records use the specific dates listed; check for consistency in date format across the dataset.
- Plot data: Columns for soil respiration correspond to plots 1–9; plot-specific values are stored under these columns.
- Climate treatment: Indicated in the second row as part of the dataset structure (per the document’s description); ensure metadata clarifies how this treatment applies to rows/dates.
- Measurement method: Stored in the Method column; metadata should specify the units and technique.

## Data quality, provenance, and metadata

- Provenance: Supplement to existing Clocaenog supporting documentation; linkage to the main data series documentation should be maintained.
- Quality considerations:
  -Presence of missing data (empty cells) for certain dates.
  - Clarity needed on units, measurement method details, and any changes in methodology over time.
  - Need for consistent metadata to explain the layout (plot headers, climate treatment row, and method column) to users.

## Data governance and stewardship actions

- Metadata alignment: Ensure clear definitions for Date, Method, climate treatment, plot respiration values, and units in the dataset’s metadata.
- Data integrity: Validate date range, confirm plot column mappings, and document how missing data are represented.
- Versioning and updates: Establish a process for updating the Fortnightly soil respiration dataset and recording changes, with references to the Clocaenog supporting documentation.
- Storage and access: Store in a centralized repository with linkage to the supporting documentation; ensure discoverability and appropriate access controls.
- Documentation needs: If not already present, create a data dictionary detailing column meanings, row structure, and any anomalies; include data handling steps for missing values.
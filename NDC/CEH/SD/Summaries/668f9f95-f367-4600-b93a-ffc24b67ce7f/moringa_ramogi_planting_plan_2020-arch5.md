# Key to cell colours and replacement trees

- Purpose and scope
  - Defines how different cell colours represent tree status in the dataset and describes the replacements table used to track changes due to tree deaths or gaps.
  - Primarily relevant for forestry data but applicable to any dataset where status, replacements, and provenance must be tracked.

- Color/marker meanings
  - White cells: measured trees; the number corresponds to a Family ID in the data tables.
  - Dark grey cells: measured trees; the number corresponds to a Family ID in the data tables.
  - Red cells: additional planted trees to replace those that have died; refer to the Replacements Table for the new Family ID.
  - Yellow cells: planted as guard trees; not included in measurements or resulting data.
  - Additional note: trees planted to fill gaps were not measured.

- Replacements Table (structure and purpose)
  - Records replacements by planting row (PR No.) and maps Original Tree (O.Tree) to Replaced Tree (R.Tree) IDs.
  - Used to link pre-death trees to their replacements, enabling traceability of changes to the dataset.
  - Examples are provided in the table (PR No., O.Tree, R.Tree), illustrating how replacements are recorded across entries.

- Data quality and governance considerations for Data Stewards
  - Metadata needs to clearly define color codes, what constitutes a measured tree, and when a tree is excluded (guard trees).
  - Maintain a separate and up-to-date Replacements Table to preserve provenance and lineage of trees that have died and been replaced.
  - Exclude guard trees from measurements and final data outputs to avoid skewing analyses.
  - Ensure consistent formatting across entries (PR No., O.Tree, R.Tree) to support interoperability and reuse.
  - Document any gaps where planted trees were not measured to avoid misinterpretation of data completeness.

- Implications for data sharing and updates
  - Sharing datasets should include both the color-coding scheme and the Replacements Table so users can reconstruct the history of replacements.
  - Update processes should preserve historical relationships (Original to Replaced Tree mappings) and clearly indicate any new replacements or status changes.

- Practical notes
  - The document provides concrete, row-level mappings (PR No., O.Tree, R.Tree) that illustrate how replacements are recorded and linked to original measurements.
  - Highlights the importance of differentiating between measured trees (with IDs) and non-measured or excluded elements (guard trees).
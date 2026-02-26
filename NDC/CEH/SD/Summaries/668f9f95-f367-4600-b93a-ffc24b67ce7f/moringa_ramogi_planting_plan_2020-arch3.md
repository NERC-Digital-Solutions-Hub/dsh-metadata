# Key to cell colours and replacement trees

- Overview
  - Defines a legend for a plantation dataset showing statuses of trees across planting rows, including original trees, replacements, and planted guards.
  - Describes a Replacements Table that links original trees (O.Tree) to their replacements (R.Tree) within each planting row (PR No.).

- Data structure and meanings
  - Abbreviations:
    - PR Planting Row
    - O.Tree Original Tree
    - R.Tree Replaced Tree
  - Color/entry semantics:
    - White: measured trees (Family ID matches data tables)
    - Dark Grey: measured trees (Family ID)
    - Red: additional planted trees to replace those that have died (new Family ID referenced in the Replacements Table)
    - Yellow: guard trees (planted but not included in measurements or data)
    - Note: Trees planted to fill gaps were not measured

- Replacements Table (examples of entries)
  - PR No. = 2, O.Tree = 12, R.Tree = 25
  - PR No. = 2, O.Tree = 69, R.Tree = 32
  - PR No. = 3, O.Tree = 3, R.Tree = 29
  - PR No. = 3, O.Tree = 29, R.Tree = 38
  - PR No. = 3, O.Tree = 38, R.Tree = 31
  - PR No. = 4, O.Tree = 3, R.Tree = 39
  - PR No. = 4, O.Tree = 4, R.Tree = 61
  - PR No. = 4, O.Tree = 27, R.Tree = 6
  - PR No. = 4, O.Tree = 60, R.Tree = 12
  - PR No. = 4, O.Tree = 75, R.Tree = 35
  - PR No. = 5, O.Tree = 78, R.Tree = 25
  - (Additional entries continue the same O.Tree to R.Tree mapping across PR Nos.)

- Implications for monitoring framework design
  - Necessitates explicit data lineage: track original trees and their replacements through a linked mapping (O.Tree to R.Tree) within each planting row.
  - Requires clear metadata and documentation to interpret color codes and statuses correctly.
  - Highlights the need to represent unmeasured or non-counted Planting Row elements (e.g., guard trees, gap-fillers) to avoid bias in analyses.

- Practical considerations for authors of monitoring frameworks
  - Incorporate a color/status legend and a dedicated Replacements Table in data models.
  - Ensure consistent ID management (Family IDs, O.Tree, R.Tree) and linkage between original and replacement records.
  - Include metadata requirements to support data quality, provenance, and future reuse (e.g., which trees were measured vs. not measured).
  - Provide guidance on data sharing while preserving the integrity of replacement lineage information.
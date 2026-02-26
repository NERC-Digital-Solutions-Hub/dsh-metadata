# Key to cell colours and replacement trees

- Purpose: Defines color coding and replacement mappings for a tree dataset used in GIS mapping, including how Original Trees are tracked and how Replaced Trees are recorded.
- Key columns:
  - PR No. = Planting Row
  - O.Tree = Original Tree
  - R.Tree = Replaced Tree

## Color coding and statuses
- White cells: measured trees corresponding to Family ID in the data tables
- Dark Grey cells: measured trees corresponding to Family ID in the data tables
- Red cells: additional trees planted to replace those that have died; refer to the Replacements Table for the new Family ID
- Trees planted to fill gaps: these were not measured
- Yellow cells: guard trees; not included in measurements or resulting data

## Replacements Table (structure and purpose)
- Lists replacement events by PR No., mapping Original Tree (O.Tree) to Replaced Tree (R.Tree)
- Example entries:
  - PR No. 2: O.Tree 12 -> R.Tree 25
  - PR No. 2: O.Tree 69 -> R.Tree 32
  - PR No. 3: O.Tree 3 -> R.Tree 29
  - PR No. 3: O.Tree 29 -> R.Tree 38
  - PR No. 3: O.Tree 38 -> R.Tree 31
  - PR No. 4: O.Tree 3 -> R.Tree 39
  - PR No. 4: O.Tree 4 -> R.Tree 61
  - PR No. 4: O.Tree 27 -> R.Tree 6
  - PR No. 4: O.Tree 60 -> R.Tree 12
  - PR No. 4: O.Tree 75 -> R.Tree 35
  - PR No. 5: O.Tree 78 -> R.Tree 25

## Practical implications for GIS work
- Use color codes to quickly identify measured vs. unmeasured trees and replacements in map visualizations
- Maintain lineage by linking Original Tree IDs to their Replaced Tree IDs for accurate temporal analyses
- Clearly separate guard/unaudited trees (yellow) from measurement data to avoid skewed statistics
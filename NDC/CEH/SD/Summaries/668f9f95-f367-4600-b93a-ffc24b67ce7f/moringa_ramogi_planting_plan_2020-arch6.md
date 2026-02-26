# Key to cell colours and replacement trees

## Overview
- Defines color-coding and data structure for a grid that tracks planted and measured trees, including replacements.
- Uses PR (Planting Row), Original Tree (O.Tree), and Replaced Tree (R.Tree) identifiers.
- White and dark grey cells represent measured trees identified by Family ID; red cells indicate additional planted trees to replace those that died; yellow cells are guard trees not included in measurements or resulting data.
- Replacements Table links original trees to their replacements, aiding lineage tracking and data consistency.

## Color coding and data roles
- White cells: measured trees with Family ID numbers.
- Dark grey cells: measured trees (also linked to Family IDs).
- Red cells: additional planted trees to replace dead ones (with new R.Tree IDs in the Replacements Table).
- Yellow cells: guard trees not included in measurements or outcomes.

## Replacements Table (PR No. → Original Tree → Replaced Tree)
- PR No. 2
  - O.Tree 8 → R.Tree 25
  - O.Tree 65 → R.Tree 32
- PR No. 3
  - O.Tree 56 → R.Tree 29
  - O.Tree 20 → R.Tree 38
  - O.Tree 69 → R.Tree 31
- PR No. 4
  - O.Tree 56 → R.Tree 39
  - O.Tree 11 → R.Tree 61
  - O.Tree 69 → R.Tree 6
  - O.Tree 50 → R.Tree 12
  - O.Tree 10 → R.Tree 35
- PR No. 5
  - O.Tree 56 → R.Tree 25

## Data handling considerations
- Some trees planted to fill gaps were not measured.
- The dataset supports tracking replacements and updating measurements with new Tree IDs for continuity.
- Family IDs associated with measured trees enable correlation across the dataset and replacement events.

## Potential data products for Data Support
- Dashboards showing replacements by PR No and by Original Tree, with links to Replacement Tree IDs.
- Validation reports to ensure all Original Tree IDs have corresponding Replaced Tree IDs where applicable.
- Self-serve explorer to filter by PR No, Original Tree, or Replaced Tree, and to view measurement status (measured vs. not measured).
- Analytical views to assess replacement frequency, trends over PRs, and impact of guard trees on measurement coverage.
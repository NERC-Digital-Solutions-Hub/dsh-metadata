# Key to cell colours and replacement trees

## Overview
- Defines color-coding and identifiers used in a tree-monitoring dataset to track original trees, replacements, and additional plantings.
- Distinguishes between measured trees, replacements, fills, and guard plantings to support consistent reporting.

## Data coding and meaning
- PR Planting Row: identifies the planting row or project segment.
- O.Tree Original Tree: the original tree identified in the dataset.
- R.Tree Replaced Tree: the tree that replaced the original tree.
- Color codes:
  - White cells: measured trees; number corresponds to Family ID in data tables.
  - Dark Grey cells: measured trees; number corresponds to Family ID in data tables.
  - Red cells: additional planted trees to replace trees that have died; see Replacements Table for new Family ID.
  - Yellow cells: guard trees; planted but not included in measurements or resulting data.
- Trees planted to fill gaps were not measured.

## Replacements Table (sample interpretation)
- The Replacements Table lists mappings of Original Trees to Replaced Trees within each PR No. (Planting Row).
- Example structure found in the text:
  - PR No. = 2, O.Tree = 8, R.Tree = 25
  - PR No. = 2, O.Tree = 69, R.Tree = 32
  - PR No. = 3, O.Tree = 3, R.Tree = 3
  - PR No. = 3, O.Tree = 29, R.Tree = 38
  - PR No. = 3, O.Tree = 38, R.Tree = 31
  - PR No. = 4, O.Tree = 3, R.Tree = 39
  - PR No. = 4, O.Tree = 4, R.Tree = 61
  - PR No. = 4, O.Tree = 27, R.Tree = 6
  - PR No. = 4, O.Tree = 60, R.Tree = 12
  - PR No. = 4, O.Tree = 75, R.Tree = 35
  - PR No. = 5, O.Tree = 78, R.Tree = 25
- These entries illustrate how original trees have been replaced and how replacements are tracked.

## Implications for environmental monitoring
- Supports consistent, auditable tracking of tree replacements over time.
- Enables understanding of replacement activity within planting rows and across original trees.
- Guard trees are excluded from measurements, ensuring data reflects only monitored trees.

## Data quality and access considerations for analysts
- Emphasizes the need to preserve traceability from original to replaced trees via clear IDs (O.Tree to R.Tree and Family IDs).
- Color-coding aids rapid interpretation and cross-dataset compatibility.
- Replacements data should be stored in appropriate data portals to ensure accessibility for scrutiny and longitudinal analysis.
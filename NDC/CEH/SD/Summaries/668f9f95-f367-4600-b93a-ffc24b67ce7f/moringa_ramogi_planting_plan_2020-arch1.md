# Key to cell colours and replacement trees

## Purpose
- Describe the color-coding and replacement-tracking scheme used in the dataset of planted trees across Planting Rows (PR).

## Legend and cell meanings
- PR = Planting Row
- O.Tree = Original Tree
- R.Tree = Replaced Tree
- White cells = measured trees; number corresponds to Family ID in data tables
- Dark Grey cells = measured trees; number corresponds to Family ID in data tables
- Red cells = additional planted trees to replace those that have died; see Replacements Table for new Family IDs
- Yellow cells = guard trees; not included in measurements or resulting data
- Trees planted to fill gaps = not measured

## Replacements Table
- Lists mappings from Planting Row (PR No.) and Original Tree (O.Tree) to Replaced Tree (R.Tree)
- Examples include:
  - PR No. 2, O.Tree 8 -> R.Tree 25
  - PR No. 2, O.Tree 65 -> R.Tree 32
  - PR No. 3, O.Tree 56 -> R.Tree 29
  - PR No. 3, O.Tree 20 -> R.Tree 38
  - PR No. 3, O.Tree 69 -> R.Tree 31
  - PR No. 4, O.Tree 56 -> R.Tree 39
  - PR No. 4, O.Tree 11 -> R.Tree 61
  - PR No. 4, O.Tree 69 -> R.Tree 6
  - PR No. 4, O.Tree 50 -> R.Tree 12
  - PR No. 4, O.Tree 10 -> R.Tree 35
  - PR No. 5, O.Tree 56 -> R.Tree 25

## Practical implications for analysts
- Use colour codes to distinguish measured vs replaced trees and to exclude guard trees from analyses.
- Use the Replacements Table to link original and replaced trees, ensuring consistency of Family IDs across datasets.
- Exclude guard trees (yellow) from measurements and final data analyses.
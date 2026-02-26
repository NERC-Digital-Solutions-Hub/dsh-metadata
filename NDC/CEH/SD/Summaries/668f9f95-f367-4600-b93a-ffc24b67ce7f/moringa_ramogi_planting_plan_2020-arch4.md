# Key to cell colours and replacement trees

## Overview
- Describes a dataset for tracking trees, cell colors, and replacements across planting rows.
- Connects measured trees, replacements, and guard trees, with a Replacements Table capturing how original trees were replaced.

## Data structure and key fields
- PR No. (Planting Row) identifies each planting row.
- O.Tree (Original Tree) indicates the original tree involved.
- R.Tree (Replaced Tree) indicates the tree that replaced the original.
- Colors indicate status:
  - White: measured trees with Family ID alignment in data tables.
  - Dark Grey: measured trees also aligned to Family ID.
  - Red: additional planted trees to replace those that died.
  - Yellow: guard trees, not included in measurements or resulting data.

## Replacements Table
- Lists replacement events with:
  - PR No. (planting row number)
  - O.Tree (original tree identifier)
  - R.Tree (replaced tree identifier)
- Contains multiple entries across PR No. 2, 3, 4, and 5, showing how original trees were replaced by new trees.

## Data governance and quality considerations
- Importance of clearly mapping Original Tree to Replaced Tree for traceability.
- Guard trees must be excluded from measurements and analysis.
- Color coding aids data verification and quick status assessment.
- Metadata and consistent naming (PR No., O.Tree, R.Tree) support discoverability and updates.

## Practical implications for Data Leaders
- Use the structure to monitor data completeness, track replacements, and fill gaps in planting records.
- Ensure accurate linkage between original and replacement trees for reliable analysis.
- Maintain clear metadata to support dissemination, user needs, and cross-team collaboration.
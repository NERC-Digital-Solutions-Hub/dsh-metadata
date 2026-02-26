# WildCrickets06C_DominanceSenescence

## Purpose and Content
- Dataset describes success per fight and individual male crickets, likely for studying dominance senescence.
- Per-fight observations include: Year, ID, Age, AgeDiff, SizeDiff, and Won (fight outcome).

## Data Model and Fields
- Year: integer; year when the cricket was alive or observed.
- ID: string; unique identifier for each cricket.
- Age: integer; age at the fight in days.
- AgeDiff: integer; age difference relative to the opponent in days.
- SizeDiff: numeric; size difference relative to the opponent in grams.
- Won: integer (0 or 1); whether the cricket won the fight.

## Metadata and Provenance
- Requires clear metadata: field definitions, data types, units (days, grams), and data collection methods.
- Documentation should specify provenance: who collected data, when, and any transformations or cleaning steps applied.
- Missing value policies and any imputation must be recorded.

## Quality Assurance and Validation
- Implement data quality checks:
  - Age and Year consistency (plausible lifespans and fight timing).
  - Reasonableness of AgeDiff and SizeDiff ranges.
  - Won ∈ {0,1}.
  - Unique row identifiers or a documented composite key (e.g., ID plus fight timestamp/year).
- Regularly validate intra-critter consistency across multiple fights (e.g., trend checks for aging).

## Governance, Access, and Sharing
- Versioning and change history to track updates and corrections.
- Storage and portal upload procedures; ensure dataset is discoverable and interoperable with other datasets.
- Clear licensing and usage terms; define data sharing embargoes if applicable.
- Maintain a data dictionary and data dictionary updates as the dataset evolves.

## Recommendations for Data Stewards
- Provide comprehensive metadata including definitions, units, data types, and collection methods.
- Document data provenance and any transformations; attach versioned data dictionaries.
- Establish and enforce data quality rules and validation routines; implement automated checks where possible.
- Align the dataset with user needs by including fields that support downstream analyses of dominance and aging; ensure interoperability with related datasets.
- Prepare guidance on data ingestion timelines and communication with data producers to address delays or standardization issues.
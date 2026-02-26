# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Woodland (VW)

## Overview
- Presents a comprehensive crosswalk of species codes used by the ECN VW dataset with their taxonomic names and aliases.
- Includes numerous mappings between internal numeric codes and Latin/scientific names, as well as alias identifiers (e.g., Vas_ numbers) used for cross-database consistency.
- Focuses on ensuring consistent species identification and alignment with external taxonomic databases across longitudinal vegetation data.

## Species codes crosswalk
- Contains extensive mappings where a single code (e.g., 1171, 3131, 1182) is linked to multiple taxonomic names and synonyms, such as Salix cinerea ssp oleifolia(c) equating to Salix herbacea or Salix repens.
- Includes numerous alias cross-references (e.g., Vas_1786, Vas_1794, Vas_1801) to maintain interoperability with other classification schemes.
- Covers a wide range of taxa beyond Salix, illustrating how codes map to alternative taxonomic treatments and common equivalents.

## Data structure and usage implications
- The crosswalk is intended to translate dataset codes into standardized species names for analysis and reporting.
- Analysts should apply the mappings to harmonize taxonomy across time series, while accounting for potential multiple synonym mappings.
- The presence of numerous alias codes underscores the need to track both internal codes and external identifiers for reproducibility.

## Quality and metadata considerations
- While the text primarily presents species-code mappings, it sits within the ECN framework that pairs data with quality codes (see Quality Codes section).
- Analysts should consult accompanying quality metadata to ensure correct interpretation of observations, especially when taxonomic reclassification or alias changes may influence comparability.

## Practical guidance for analysts
- Use the crosswalk to standardize species identifications before aggregating or comparing data over time or across sites.
- Resolve synonym conflicts by prioritizing a consistent taxonomic reference (Latin names) and applying the corresponding code mapping.
- Integrate quality codes from the ECN standard list to filter data or assess reliability, and pay attention to the final 999 code indicating unusual events with accompanying text.
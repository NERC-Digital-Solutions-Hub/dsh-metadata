# WildCrickets06B_SearchingActivitySenescence Description of content

## Overview
- A dataset describing per-period observations of individual male adult crickets.
- Each observation records whether the searching activity duration was short (≤ 77 minutes) or long (> 77 minutes).
- Associated metadata include temporal, environmental, and biological context to support downstream analyses and data sharing.

## Key variables and coding
- Year
  - Year when the cricket was alive (temporal anchor for the observation).
- Year alive (implied)
  - The specific year the individual cricket's life was observed.
- ID
  - Unique identifier for each individual cricket.
- Temp
  - Temperature during the observation period, in degrees Celsius (°C).
- Age
  - Age of the cricket at sampling, in days.
- Short
  - Binary indicator of duration class for the observation period.
  - 1 = duration classified as short (≤ 77 minutes); 0 = duration not short (i.e., long, > 77 minutes).

## Data quality and consistency considerations
- The 77-minute threshold for classifying duration should be consistently applied across all records.
- Temperature units must be Celsius; verify any datasets merged from different sources use the same unit.
- Age values should be checked for plausibility (e.g., non-negative, within the expected life stage range).
- Ensure the ID field uniquely identifies individuals across years and observations.
- Document any missing values and the reasons (e.g., failed observation, sensor loss).

## Governance and sharing considerations
- Metadata completeness: provide clear definitions for Year, ID, Temp, Age, and Short, plus data collection methods.
- Provenance: record data collection protocols, instruments used, and observers to enable reproducibility.
- Versioning: track dataset versions and changes to definitions (e.g., if the Short threshold is revised).
- Licensing and access: specify usage rights and any embargoes; ensure data can be discoverable and reusable.
- Interoperability: adopt consistent naming conventions and units to facilitate integration with other cricket or ecological datasets.

## Suggested actions for data stewards
- Create a detailed data dictionary including variable definitions, data types, units, and valid ranges.
- Pilot quality checks: validate ranges (e.g., plausible Temp values, Age ranges), check for missing or inconsistent IDs.
- Establish a data upload and validation workflow to ensure consistent metadata and formatting before sharing.
- Document data provenance, collection methods, and any transformations applied to the data.
- Prepare guidelines for data discovery, including keywords and tags (ecology, crickets, behavior, senescence, activity).

## Potential uses
- Analyzing patterns in searching activity duration relative to age, temperature, and life stage.
- Studying senescence effects on activity in male adult crickets.
- Supporting meta-analyses that compare activity duration classifications across individuals and years.
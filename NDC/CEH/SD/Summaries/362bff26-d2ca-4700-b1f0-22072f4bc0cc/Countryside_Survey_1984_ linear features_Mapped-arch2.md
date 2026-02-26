# Dataset Documentation

- Purpose and scope
  - National estimates of landscape linear feature stock for 1984 calculated using the 2007 ITE Land Classification.
  - Estimates expressed as total lengths (metres) per 1km square per Land Class.
  - Note: negative values may appear due to the statistical model; treat as zero.

- Data structure and key fields
  - FID: Feature ID (autonumber), Shape: Geometry.
  - LC2007: ITE Land Class (numeric); LC2007_COD: ITE Land Class (text code).
  - CSYEAR: Year of survey.
  - LCAREA: Total area of relevant Land Class (00s ha).
  - LF_1 to LF_7: lengths of linear features by type (metres per 1km square per land class).
    - LF_1: Hedges
    - LF_3: Wall
    - LF_4: Line of trees/shrubs/relict hedge/fence
    - LF_5: Line of trees/shrubs/relict hedge
    - LF_6: Bank/grass strip
    - LF_7: Fence
  - LFTOTAL: Total length of linear features.
  - TOTAL: Summary field; Shape_Length and Shape_Area provide geometric attributes.

- Feature types and reporting rules
  - Six major feature types reported; no double counting of multi-element features.
  - Hedge elements have reporting precedence over walls and fences when co-occurring with them.
  - A hedge-containing feature is counted as hedge; walls/fences included with a hedge are not double-counted in hedge totals.

- Use and purpose for analysts
  - Supports monitoring environmental health and policy performance over time via standardized reporting formats (maps, charts, reports).
  - Data is intended to be verified, quality-assured, and transformed from established sources, then stored/uploaded to appropriate portals.

- Use limitations and attribution
  - All CS data usage must include an acknowledgement:
    - “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Acknowledgement and copyright notices apply to copies, publications, reports, and presentations.

- References and further information
  - Key Countryside Survey outputs and methodologies (UK results from 2007; background to dataset and project).
  - Technical and methodological publications detailing how national estimates are derived from 1km survey squares and the ITE Land Classification.
  - Relevant datasets and vector classifications (ITE Land Classification 2007).

- Access and additional resources
  - Countryside Survey Website: overview and links to methodologies and documents (http://www.countrysidesurvey.org.uk/).
  - Technical reports and referenced literature detailing statistical and classification frameworks.
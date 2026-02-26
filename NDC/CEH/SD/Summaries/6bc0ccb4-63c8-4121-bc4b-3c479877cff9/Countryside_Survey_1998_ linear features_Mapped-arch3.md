# Dataset Documentation

- Purpose and scope
  - National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
  - Outputs are total lengths (in metres) for each linear feature type per 1 km square per Land Class.
  - Note: some columns may contain negative values due to the statistical model; treat negatives as zero.

- Data structure and key fields
  - FID: Feature ID (auto-number).
  - LC2007: ITE Land Class (numeric).
  - LC2007_COD: ITE Land Class (text code).
  - CSYEAR: Year of survey.
  - LCAREA: Total area of relevant Land Class.
  - LF_1 to LF_7: Length estimates of linear features by type per 1 km square per land class (metres).
    - _1: Hedges
    - _3: Wall
    - _4: Line of trees/shrubs/relict hedge/fence
    - _5: Line of trees/shrubs/relict hedge
    - _6: Bank/grass strip
    - _7: Fence
  - LFTOTAL: Total length of linear features.
  - Shape_Length, Shape_Area: Geometric metadata.

- Reporting and data interpretation
  - Six major feature types are reported in a hierarchical system; results avoid double counting of multi-element features.
  - Hedgerows (_1) are given precedence when co-occurring with other features.
  - Lengths for walls and fences do not include portions that are part of hedges.
  - The dataset records detailed codes during field surveys to enable multiple reporting formats.

- Use limitations and governance
  - All use of Countryside Survey data must be acknowledged.
  - Required attribution: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; copyright retained.
  - Data sharing and metadata quality considerations can pose barriers; issues include data access timeliness, siloed data, and the need for data transformation.
  - Dataset contains metadata and provenance that support data governance, quality assurance, cleaning, transformation, and clear presentation of findings.

- Data provenance and references
  - Core sources include:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007.
    - Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside.
    - Scott (2007) CS Technical Report No.4/07: Statistical reporting methods.
    - Bunce et al. (1996, 2007) ITE Land Classification of Great Britain.
  - Additional methodology and reporting references listed as background.

- Access and further information
  - Countryside Survey Website: general overview, project documentation, and methodologies.
  - Direct references to datasets, technical reports, and associated datasets are provided via linked sources.
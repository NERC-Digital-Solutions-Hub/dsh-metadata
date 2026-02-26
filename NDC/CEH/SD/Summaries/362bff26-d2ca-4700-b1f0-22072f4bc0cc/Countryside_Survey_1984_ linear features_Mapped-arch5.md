# Dataset Documentation

- Purpose and scope
  - National estimates of landscape linear feature stock for 1984 calculated using the 2007 ITE Land Classification (references: Scott 2007; Bunce et al. 2007).
  - Estimates are total lengths (metres) of each linear feature type per 1 km square per Land Class.
  - Note: LC2007 values may be negative due to the statistical model; treat negatives as zero.

- Data structure and metadata
  - Key fields:
    - FID: Object ID; Description = Feature ID (autonumber)
    - Shape: Geometry
    - LC2007: Double; ITE Land Class (numeric)
    - LC2007_COD: Text; ITE Land Class (text code)
    - CSYEAR: Number; Year of survey
    - LCAREA: Number; Total area of relevant Land Class (00s ha)
    - LF_1: Number; Hedges (metres per 1 km square per land class)
    - LF_3: Number; Wall (metres per 1 km square per land class)
    - LF_4: Number; Line of trees/shrubs/relict hedge/fence (metres)
    - LF_5: Number; Line of trees/shrubs/relict hedge (metres)
    - LF_6: Number; Bank/grass strip (metres)
    - LF_7: Number; Fence (metres)
    - LFTOTAL: Number; Total length of linear features (metres)
    - Shape_Length: Number; Length of Land Class shape
    - Shape_Area: Number; Area of Land Class
  - Feature types (with codes and descriptions):
    - _1: Hedges – managed hedgerows
    - _3: Wall – built walls possibly with fences/banks/lines of trees
    - _4: Line of trees/shrubs/relict hedge/fence
    - _5: Line of trees/shrubs/relict hedge
    - _6: Bank/grass strip
    - _7: Fence
    - TOTAL: Total length of linear features
  - Reporting design:
    - Hierarchical six major feature types
    - No double counting of multi-element features
    - Hedge features have precedence; hedge lengths exclude lengths already counted as walls/fences when co-located with hedges

- Methodology and reporting
  - Results are reported by combining codes according to a predefined hierarchy; hedges are ecologically prioritized in reporting when alongside other features.

- Data quality, limitations, and governance notes
  - Use limitation: All CS data usage must be acknowledged with the provided citation text.
  - Acknowledgement text to include on all copies, publications, and presentations:
    - “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Negative LC2007 values may occur due to the statistical model; treat as zero.
  - Data are tied to the Countryside Survey methodology and ITE Land Classification (2007) references; users should consult the linked publications for methodological details.

- Access, attribution, and resources
  - Countryside Survey Website provides general project overview and links to methodologies and publications.
  - Key references include:
    - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
    - CS Technical Report No. 4/07 Statistical Report (Scott, 2007)
    - ITE Land Classification of Great Britain (Bunce et al., 1996; 2007)
    - Various foundational handbooks and methodological documents (listed in the References)
  - Related dataset documentation and methodological papers provide context for interpretation and reuse.

- Practical governance considerations for data stewards
  - Ensure metadata completeness: field definitions, data types, units, and classification codes are clearly documented for future users.
  - Maintain data provenance: origin from Countryside Survey via CEH/NERC; cite appropriate publications when reusing.
  - Preserve data integrity across versions: adhere to reporting hierarchy to avoid double counting; clearly document any updates or corrections.
  - Facilitate discoverability: reference the Countryside Survey website and technical reports to assist data discovery and understanding.
  - Plan for interoperability: align with ITE Land Classification 2007 standards; document any deviations or preprocessing steps (e.g., handling negative LC2007 values).
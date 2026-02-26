# Dataset Documentation

- National estimates of landscape linear feature stock for 1984 calculated using the 2007 ITE Land Classification. Estimates are given as total lengths in metres for each linear feature type per 1km square per Land Class. Note: negative values in LC2007 may occur due to the statistical model; treat these as zero.

- Dataset structure and fields
  - FID: Object ID (Feature ID autoincrement)
  - LC2007: Double — ITE Land Class (numeric)
  - LC2007_COD: Text — ITE Land Class (text code)
  - CSYEAR: Number — Year of survey
  - LCAREA: Number — Total area of relevant Land Class (00s ha)
  - LF_1: Number — Hedges (metres per 1km square per land class)
  - LF_3: Number — Wall (metres per 1km square per land class)
  - LF_4: Number — Line of trees/shrubs/relict hedge/fence (metres per 1km square per land class)
  - LF_5: Number — Line of trees/shrubs/relict hedge (metres per 1km square per land class)
  - LF_6: Number — Bank/grass strip (metres per 1km square per land class)
  - LF_7: Number — Fence (metres per 1km square per land class)
  - LFTOTAL: Number — Total length of linear features (metres per 1km square per land class)
  - Shape_Length: Number — Length of the Land Class shape
  - Shape_Area: Number — Area of Land Class (square metres)

- Linear feature types and descriptions
  - _1 Hedge: A managed woody vegetation line; may co-occur with other features; hedges have ecological priority in reporting
  - _3 Wall: Built stone/man-made wall (may include walls with fences or banks/grass strips and/or lines of trees/shrubs)
  - _4 Line of trees/shrubs/relict hedge/fence: Trees/shrubs line with natural shape; may include banks/grass strips
  - _5 Line of trees/shrubs/relict hedge: Line of trees/shrubs with natural shape; may include avenues; may include banks/grass strips
  - _6 Bank/grass strip: Earth/stone-faced bank or grass strip with/without a fence
  - _7 Fence: Post/rail/wire/wooden/masonry fence with grass strip, ditch or stream nearby

- Reporting framework
  - Six major feature types are reported in a hierarchical system to avoid double counting of multi-element features
  - If hedges are present with walls or fences, hedge lengths are reported for hedges, and walls/fences are reported separately without double counting the hedge parts
  - Hedges are treated as ecologically more important and policy-relevant; hedges take precedence when co-occurring with other features

- Use limitations and acknowledgement
  - All use of Countryside Survey (CS) data must be acknowledged
  - Required acknowledgement text (to be used on copies, publications, and presentations): 
    “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Data use is governed by copyright and database rights

- Relevant publications and references
  - The Countryside Survey outputs and methodologies are documented in key reports and papers, including:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007
    - Scott (2007) CS Technical Report No.4/07 Statistical Report
    - Bunce et al. (1996, 2007) ITE Land Classification references
    - Additional background on the ITE Land Classification and related handbooks
  - All use of CS data should be acknowledged as above

- Countryside Survey website and resources
  - General overview and project documentation: http://www.countrysidesurvey.org.uk/
  - Related technical reports and datasets, including background on how national estimates are generated

- Practical notes for data use (Data Support perspective)
  - The dataset provides ready-to-use vector data with geometry to support mapping, aggregation by land class, and cross-dataset analyses
  - Useful for creating dashboards, pivot-type summaries, and self-serve analyses of linear landscape features across land classes
  - Data quality considerations include handling negative LC2007 values as zero and referring to the land-class hierarchy to avoid double counting when combining features
  - When integrating with other CS products, ensure consistent licensing and the required acknowledgement text is included in outputs
# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology National estimates of landscape linear feature stock (as listed below) for 2007 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007). Estimates are given as total lengths in '000s km for each linear feature type per Land Class including lower and upper confidence limit estimates.

- Purpose and scope
  - Provides national estimates of landscape linear feature stock for 2007, using the ITE Land Classification.
  - Estimates are total lengths (in 000s km) by Land Class and feature type, with 95% confidence intervals (lower, mean, upper).

- Data structure and key fields
  - YEAR: Year of Survey.
  - LAND_CLASS: ITE Land Class.
  - FEATURENO: Linear feature code (see below).
  - FEATURE: Linear feature description.
  - LOWER_ESTIMATE: Lower 95% CI of feature length for the relevant Land Class (000s km).
  - MEAN_ESTIMATE: Mean estimate of feature length for the relevant Land Class (000s km).
  - UPPER_ESTIMATE: Upper 95% CI of feature length for the relevant Land Class (000s km).
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha).

- Linear feature codes and definitions
  - _1 = Hedge: A line of woody vegetation managed to a non-natural shape; may be alongside other features.
  - _3 = Wall: Built structure of natural stone or blocks (dry stone, mortared, may include walls with fences/banks/grass strips and/or lines of trees/shrubs).
  - _4 = Line of trees/shrubs/relict hedge/fence: Line of trees/shrubs with natural shape; may include banks/grass strips.
  - _5 = Line of trees/shrubs/relict hedge: Line of trees/shrubs with natural shape; may include avenues and banks/grass strips.
  - _6 = Bank/grass strip: Earth or stone-faced bank or grass strip with/without a fence.
  - _7 = Fence: Permanent posts and wires/rails; may be with grass strip, ditch or stream.
  - TOTAL: Total length of linear features.
  - Note: There is a hierarchical reporting system; hedges are reported as a precedence feature when co-occurring with walls or fences.

- Special reporting rules
  - No double counting of multi-element features.
  - A hedge is any feature containing a hedge element, and may coincide with walls or fences.
  - Estimates for walls and fences do not include lengths that are found with a hedge.

- Data use and interpretation
  - Values may be negative in MEAN_ESTIMATE due to the statistical model; treat negative values as zero.
  - Units are 000s of kilometers; values are reported by Land Class and feature type with confidence intervals.

- Use limitations and attribution
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement text to use on copies, publications, and presentations:
    - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

- Access and references
  - Countryside Survey Website: general project overview and documents.
  - Key publications:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007.
    - Scott (2007) CS Technical Report No.4/07 (Statistical Report) – how national estimates are generated from 1km survey squares.
    - Bunce et al. (1996, 2007) ITE Land Classification references.
  - Related datasets and methodology documents:
    - ITE Land Classification 2007 vector dataset.
    - CS Technical Report No.1/07 Field Mapping Handbook.
  - Links provided in the document point to metadata and methodological resources for deeper detail.
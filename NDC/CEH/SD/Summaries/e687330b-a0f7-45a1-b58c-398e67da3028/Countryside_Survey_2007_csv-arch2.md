# Dataset Documentation

- Purpose and scope
  - National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
  - Reported as total lengths in 000s km for each linear feature type per Land Class, including 95% confidence intervals (lower and upper estimates) and land class area.

- Data structure and fields
  - YEAR: Year of Survey
  - LAND_CLASS: Land Class (ITE)
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of length (000s km)
  - MEAN_ESTIMATE: Mean length (000s km) 
  - UPPER_ESTIMATE: Upper 95% CI of length (000s km)
  - LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)
  - Feature codes and descriptions
    - _1: Hedge (managed hedgerows; may accompany other features)
    - _3: Wall (stone/masonry walls; may include fences/banks or lines of trees/shrubs)
    - _4: Line of trees/shrubs/relict hedge/fence
    - _5: Line of trees/shrubs/relict hedge
    - _6: Bank/grass strip
    - _7: Fence
    - TOTAL: Total length of linear features
  - Note on reporting: Results use a hierarchical system of classes; no double counting of multi-element features. Hedges take precedence in reporting when found with other features.

- Interpretation and data characteristics
  - Some negative MEAN_ESTIMATE values may occur due to the statistical model; treat these as zero.
  - Outputs enable analysis of ecological importance and policy relevance, particularly for hedges.

- Usage limitations and citation
  - All use of Countryside Survey data must include acknowledgment.
  - Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright statements.

- Provenance and references
  - Dataset: Countryside Survey data © NERC - Centre for Ecology & Hydrology
  - Related documentation and methodologies:
    - Scott, W.A. (2007) CS Technical Report No.4/07 (Statistical methods for national estimates)
    - Bunce et al. (1996, 2007) ITE Land Classification of Great Britain
    - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - Data and methodology sources available via the Countryside Survey website and related metadata pages.

- Related resources and context
  - Countryside Survey general overview and links to associated documents and methodologies
  - Field mapping and habitat methodologies (CS Technical Report No.1/07)

- How Analysts Monitoring the Environment would use this dataset
  - Validate and quality-assure data from established sources; apply standardized analysis methods
  - Produce outputs (reports, maps, charts) to monitor environmental health and policy performance over time
  - Store and facilitate access to datasets through appropriate portals; enable integration with other data for enhanced value
  - Acknowledge data properly in all publications and presentations

- Practical notes for users
  - Distinguishes hedges as ecologically important and policy-relevant, with precedence in reporting when combined with other features
  - Field data captured as codes enabling flexible reporting across multiple hierarchical classes
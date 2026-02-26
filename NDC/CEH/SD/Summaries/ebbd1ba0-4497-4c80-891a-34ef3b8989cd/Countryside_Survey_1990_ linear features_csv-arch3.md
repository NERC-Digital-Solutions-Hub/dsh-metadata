# Dataset Documentation

- Purpose and scope
  - National estimates of landscape linear feature stock for 1990.
  - Calculated using the 2007 ITE Land Classification.
  - Results reported as total lengths (in 000s km) for each linear feature type within each Land Class.
  - Includes lower and upper 95% confidence interval estimates and Land Class area.

- Data structure and key fields
  - YEAR: Year of Survey.
  - LAND_CLASS: ITE Land Class description.
  - FEATURENO: Linear feature code.
  - FEATURE: Linear feature description.
  - LOWER_ESTIMATE: Lower 95% confidence interval estimate (000s km).
  - MEAN_ESTIMATE: Mean estimate (000s km).
  - UPPER_ESTIMATE: Upper 95% confidence interval estimate (000s km).
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha).
  - Note: Some MEAN_ESTIMATE values may be negative due to the statistical model; treat as zero.

- Linear feature codes and reporting
  - _1: Hedges (managed hedgerows; may appear with other features).
  - _3: Wall.
  - _4: Line of trees/shrubs/relict hedge/fence.
  - _5: Line of trees/shrubs/relict hedge (including avenues).
  - _6: Bank/grass strip.
  - _7: Fence.
  - TOTAL: Total length of linear features.
  - Reporting uses a hierarchical class system; no double counting of multi-element features.
  - Hedge length is prioritized in reporting when co-occurring with walls or fences; walls/fences with hedges are not included in the hedge totals.

- Data provenance and methods
  - Source: Countryside Survey data ( © NERC - Centre for Ecology & Hydrology ).
  - Links to general project overview, key reports, and technical methodologies provided.
  - References include foundational texts on Countryside Survey results, the ITE Land Classification, and statistical methodology for national estimates.

- Use considerations and governance
  - Use limitations require proper acknowledgement of Countryside Survey data.
  - Data ownership: Countryside Survey ©, with copyright retained by NERC-CEH.
  - Metadata quality and transformation requirements are implicit in dataset preparation; users should assess compatibility with their own data standards.

- Relevance for monitoring frameworks
  - Provides standardized measures of landscape linear features (hedges, walls, fences, banks/grass strips) across land classes.
  - Enables assessment of habitat structure and ecological connectivity changes over time.
  - The hierarchical reporting and explicit handling of hedges ensure consistent, non-duplicated reporting of feature stocks.

- Access and further information
  - Countryside Survey Website available for project context and methodology.
  - Related technical reports and datasets cited (e.g., 1990 Countryside Survey reports, 2007 ITE Land Classification documents).
  - Use in publications and presentations requires the stated acknowledgment and rights notice.
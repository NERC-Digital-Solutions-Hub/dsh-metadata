# Dataset Documentation

- This dataset provides national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification. Results are presented as total lengths (in 000s of km) for each linear feature type within each Land Class, including lower and upper 95% confidence intervals and the land class area (in 00s ha).

- Source and scope:
  - Countryside Survey data © NERC - Centre for Ecology & Hydrology.
  - Based on field survey data recorded as detailed codes, enabling reporting across multiple combinations of features.
  - Emphasizes hedges as ecologically priority features when co-occurring with walls or fences; there is no double counting of multi-element features.

## Data Model

- YEAR: Year of Survey.
- LAND_CLASS: ITE Land Class (text); based on Bunce et al. references.
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha).
- FEATURENO: Linear feature code (text).
- FEATURE: Linear feature description (text).
- LOWER_ESTIMATE: Lower estimate (95% CI) of feature length for the Land Class (000s km).
- MEAN_ESTIMATE: Mean estimate of feature length for the Land Class (000s km).
  - Note: Negative values may occur due to the statistical model; treat as zero.
- UPPER_ESTIMATE: Upper estimate (95% CI) of feature length for the Land Class (000s km).
- TOTAL: Total length of linear features (for reporting) (description provided in dataset).

- Data type notes (as described in the dataset):
  - YEAR, Data type = number.
  - LAND_CLASS, DATA type = text; LAND_CLASS Description = ITE Land Class (Bunce et al., 2007; 1996).
  - FEATURENO, DATA type = text; FEATURE, Data type = text; with corresponding descriptions.
  - LOWER/MEAN/UPPER_ESTIMATE, Data type = number.

## Linear Feature Codes

- _1 = Hedge (management-altered line of woody vegetation; can co-occur with other features; hedges prioritized in reporting).
- _3 = Wall (stone or manufactured wall; may include fences or banks/grass strips associated with other features).
- _4 = Line of trees/shrubs/relict hedge/fence (trees/shrubs in natural shape; may include banks/grass strips).
- _5 = Line of trees/shrubs/relict hedge (including avenues of trees; may include banks/grass strips).
- _6 = Bank/grass strip (earth/stone-faced bank or grass strip; may have a fence).
- _7 = Fence (permanent post and wire/rail; may be alongside other features; fences like slate-threaded-on-wire in Wales included).
- TOTAL = Total length of linear features.

- Reporting approach:
  - Features are reported using a hierarchical class system for six major feature types.
  - No double counting of multi-element features; for example, hedge lengths are reported separately from walls/fences, and hedge lengths are not included in wall/fence totals when hedges are present.

## Reporting Rules and Data Integrity

- When hedges occur with walls or fences, hedge length takes precedence in reporting; wall and fence estimates exclude hedge portions.
- The results are reported per Land Class and feature type, enabling aggregated or disaggregated analyses without double counting.

## Use Constraints, Acknowledgement, and Access

- Use limitations:
  - All use of Countryside Survey data must be acknowledged.
  - Required acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

- Access and documentation:
  - Countryside Survey Website provides general project overview and links to relevant documents and methodologies.
  - Key references for methodology and background:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007.
    - Scott (2007) CS Technical Report No. 4/07 (Statistical Report) on deriving national estimates from 1 km survey squares.
    - Bunce et al. (1996, 2007) ITE Land Classification documentation.
    - Additional related handbooks and mapping methodology references.

## Governance, Provenance, and Stewardship Considerations

- Data stewards should ensure:
  - Complete, machine-readable metadata describing fields, codes, and units.
  - Clear provenance tracing from field survey codes to final aggregated estimates.
  - Documentation of the ITE Land Classification version used (2007) and any transformations applied (e.g., zeroing negative MEAN_ESTIMATE values).
  - Consistent handling of negative estimates (interpret as zero) in analyses and downstream sharing.
  - Compliance with the required acknowledgment in all uses and publications.
  - Awareness of the data’s scope (1984 national estimates) and limitations when integrating with newer datasets or updating methods.
  - Preservation of source references and enabling traceability to the primary methodology documents and reports.
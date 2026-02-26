# May Classification Metadata

## Purpose and Methods
- All classifications were carried out using a maximum likelihood algorithm.
- For full methods, refer to 'Methods_overview'.

## Key Definitions
- Edge pixels: Pixels at the edge of floral unit clusters or centers of small clusters where the pixel may be mixed with other features.
- Pinkest pixels: Pixels deeper in the center of floral unit clusters, less likely to be mixed with other features.
- Merged categories: Regions of interest for different classification categories are merged into one or more groups rather than kept separate.

## Classification Variants and Datasets

- 3cm imagery
  - May_3cm_classification1
    - Pinkest Silene dioica values only, using non-merged categories for S. dioica.
    - Crataegus monogyna values are pure, merged.
  - May_3cm_classification2
    - Pinkest Silene dioica values only, merged categories.
    - Crataegus monogyna values are pure, merged.
  - May_3cm_classification3
    - Silene dioica pinkest and edge values, merged categories.
    - Crataegus monogyna pure values, merged.
  - May_3cm_classification4
    - Pinkest Silene dioica values only, non-merged categories for Silene dioica.
    - Crataegus monogyna pure values, non-merged categories.

- 7cm classifications
  - May_7cm_classification
    - Trained with 3cm data using the 3cm training set variant that produced the highest overall accuracy for 3cm imagery.
  - May_7cm_class_trained_7cm
    - May 7cm classification trained with 7cm data.

## Data Governance and Stewardship Implications
- Maintain clear metadata for each variant, including:
  - imagery scale (3cm vs 7cm)
  - training set variant used
  - category merging strategy
  - target species and pixels involved (e.g., Silene dioica, Crataegus monogyna)
  - reported accuracy metrics and performance context
- Ensure dataset versioning and consistent naming conventions to support discoverability and reproducibility.
- Document methods and lineage (link to Methods_overview) and preserve provenance for future audits and reuse.
- Facilitate data sharing and interoperability across systems by standardizing terminology and category definitions.

## Challenges for Data Stewardship
- Incomplete picture of user needs and priorities.
- Timely acquisition of data from producers.
- Getting data creators to meet standards, including metadata.
- Working across many different systems and formats, including difficult ones.
- Handling large datasets that are hard to transfer.
- Dealing with outdated databases requiring bespoke, non-interoperable solutions.
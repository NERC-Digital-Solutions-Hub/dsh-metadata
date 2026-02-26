# May Classification Metadata

## Overview
- Classifications were carried out using a maximum likelihood algorithm.
- For full methods, see the document referenced as Methods_overview.

## Definitions
- Edge pixels: pixels at the edge of floral unit clusters or centers of small clusters where mixed with other features is likely.
- Pinkest pixels: deeper center pixels more likely to be pure (less mixed with other features).
- Merged categories: regions of interest for different classification categories are combined into one or more groups rather than kept separate.

## Classifications using different training set variants: 3cm imagery
- May_3cm_classification1: Pinkest Silene dioica values only, non-merged categories for S. dioica; Crataegus monogyna values are pure and merged.
- May_3cm_classification2: Pinkest Silene dioica values only, merged categories; Crataegus monogyna values are pure and merged.
- May_3cm_classification3: Silene dioica pinkest and edge values, merged categories; Crataegus monogyna values are pure and merged.
- May_3cm_classification4: Pinkest Silene dioica values only, non-merged for Silene dioica; Crataegus monogyna pure values, non-merged.

## Classifications using 7cm imagery
- May_7cm_classification: May 7cm classification trained with 3cm data using the 3cm training variant that yielded the highest overall accuracy for 3cm imagery.
- May_7cm_class_trained_7cm: May 7cm classification trained with 7cm data.

## Implications for Data Strategy and Governance
- Documented multiple training variants to assess how definitions (edge vs pinkest) and merging decisions affect classification accuracy.
- Emphasizes the importance of transparent labeling schemes and metadata to support reproducibility and auditability.
- Highlights the need to choose training data variants intentionally and record the rationale (e.g., highest 3cm accuracy) when transferring across resolutions.
- Underlines the role of method documentation (Methods_overview) to enable cross-team understanding and collaboration.
- Demonstrates consideration of different data scales (3cm vs 7cm) and how models trained at one scale may be adapted or re-trained for another.
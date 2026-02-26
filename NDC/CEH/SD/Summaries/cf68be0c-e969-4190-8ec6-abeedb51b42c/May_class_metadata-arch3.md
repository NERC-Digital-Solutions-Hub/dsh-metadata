# May Classification Metadata

## Key concepts and definitions
- Classifications were performed using a maximum likelihood algorithm (full methods available in Methods_overview).
- Pixel categories:
  - Edge: Pixels at the edge of floral unit clusters or within small clusters where mixing with other features occurs.
  - Pinkest: Pixels deeper inside floral unit clusters, less likely to be mixed with other features.
  - Merged: Regions of interest for different categories combined into one or more groups rather than kept separate.

## Classification variants (3 cm imagery)
- May_3cm_classification1
  - Pinkest Silene dioica values only
  - S. dioica categories non-merged
  - Crataegus monogyna pure values, merged
- May_3cm_classification2
  - Pinkest Silene dioica values only
  - S. dioica categories merged
  - Crataegus monogyna pure values, merged
- May_3cm_classification3
  - Silene dioica pinkest and edge values
  - S. dioica categories merged
  - Crataegus monogyna pure values, merged
- May_3cm_classification4
  - Pinkest Silene dioica values only
  - S. dioica categories non-merged
  - Crataegus monogyna pure values, non-merged

## Classification variants (7 cm imagery)
- May 7cm_classification
  - Trained with 3 cm data
  - Uses the 3 cm training set variant that yielded the highest overall 3 cm classification accuracy
- May_7cm_class_trained_7cm
  - May 7 cm classification trained with 7 cm data

## Implications for monitoring and data handling
- The approach supports multi-scale analysis by projecting 3 cm training outcomes onto 7 cm imagery.
- Provides a framework for assessing how pixel-level definitions (edge, pinkest, merged) affect classification outcomes.
- Highlights the importance of selecting training variants based on known accuracy to inform reliable monitoring outputs.
- References to full methodological details in Methods_overview indicate emphasis on reproducibility and transparency in the monitoring workflow.
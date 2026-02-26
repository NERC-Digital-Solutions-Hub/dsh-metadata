# May Classification Metadata

## Overview
- Classifications were carried out using a maximum likelihood algorithm.
- Full methods for carrying out classifications are described in Methods_overview.
- Key terms:
  - Edge pixels: pixels at the edge of floral unit clusters or centers of small clusters where the pixel appears mixed with other features.
  - Pinkest pixels: pixels deeper in the center of floral unit clusters that are less likely to be mixed.
  - Merged categories: regions of interest for different classification categories are merged into one or more groups rather than kept separate.

## Classification variants (3 cm imagery)
- May_3cm_classification1: Pinkest Silene dioica values only, non-merged categories for S. dioica; Crataegus monogyna pure values, merged.
- May_3cm_classification2: Pinkest Silene dioica values only, merged categories; Crataegus monogyna pure values, merged.
- May_3cm_classification3: Silene dioica pinkest and edge values, merged categories; Crataegus monogyna pure values, merged.
- May_3cm_classification4: Pinkest Silene dioica values only, non-merged categories for S. dioica; Crataegus monogyna pure values, non-merged.

## Classification variants (7 cm imagery)
- May_7cm_classification: May 7 cm classification trained with 3 cm data and using the 3 cm training set variant that yielded the highest overall classification accuracy for 3 cm imagery: May_7cm_class_trained_7cm.
- May_7cm_class_trained_7cm: May 7 cm classification trained with 7 cm data.
# May Classification Metadata

- Overview: All classifications were performed using a maximum likelihood algorithm; full methodological details are available in 'Methods_overview'.

- Key definitions:
  - Edge pixels: Pixels at the edge of floral unit clusters or within small clusters where mixing with other features occurs.
  - Pinkest pixels: Pixels deeper in the centre of floral unit clusters, less likely to be mixed.
  - Merged categories: Regions of interest for different classification categories are combined into one or more groups rather than kept separate.

- Classifications using 3 cm imagery:
  - May_3cm_classification1: Pinkest Silene dioica values only, non-merged categories for S. dioica; Crataegus monogyna values kept pure and merged.
  - May_3cm_classification2: Pinkest Silene dioica values only, merged categories for S. dioica; Crataegus monogyna pure values, merged.
  - May_3cm_classification3: Silene dioica pinkest and edge values, merged categories; Crataegus monogyna pure values, merged.
  - May_3cm_classification4: Pinkest Silene dioica values only, non-merged categories for S. dioica; Crataegus monogyna pure values, non-merged.

- Classifications using 7 cm imagery:
  - May_7cm_classification: May 7 cm classification trained with 3 cm data, using the 3 cm training set variant that yielded the highest overall accuracy for 3 cm imagery.
  - May_7cm_class_trained_7cm: May 7 cm classification trained with 7 cm data.
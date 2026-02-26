# May Classification Metadata

- Method basis
  - All classifications were carried out using a maximum likelihood algorithm.
  - Full methods are documented in 'Methods_overview'.

- Key definitions
  - Edge pixels: Pixels at the edge of floral unit clusters or centers of small clusters where the pixel appears mixed with other features.
  - Pinkest pixels: Pixels deeper into the centre of floral unit clusters, less likely to be mixed with other features.
  - Merged categories: Regions of interest for different classification categories are merged into one or multiple groups rather than left separate.

- Classification variants (3 cm imagery)
  - May_3cm_classification1
    - Pinkest Silene dioica values only
    - Non-merged categories for Silene dioica
    - Crataegus monogyna: pure values, merged
  - May_3cm_classification2
    - Pinkest Silene dioica values only
    - Silene dioica: merged
    - Crataegus monogyna: pure values, merged
  - May_3cm_classification3
    - Silene dioica pinkest and edge values
    - Silene dioica: merged
    - Crataegus monogyna: pure values, merged
  - May_3cm_classification4
    - Pinkest Silene dioica values only
    - Silene dioica: non-merged categories
    - Crataegus monogyna: pure values, non-merged

- Classification variants (7 cm imagery)
  - May_7cm_classification
    - May 7 cm classification trained with 3 cm data
    - Uses the 3 cm training set variant that yielded the highest overall classification accuracy for 3 cm imagery
  - May_7cm_class_trained_7cm
    - May 7 cm classification trained with 7 cm data
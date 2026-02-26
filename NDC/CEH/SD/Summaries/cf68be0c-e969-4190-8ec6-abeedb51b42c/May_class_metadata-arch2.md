# May Classification Metadata

- Purpose and approach
  - Classifications were performed using a maximum likelihood algorithm.
  - The document outlines methods and variants for classifying floral unit features in imagery, at 3 cm and 7 cm resolutions.
  - Focus species/regions include Silene dioica (pinkest, edge values) and Crataegus monogyna (pure values).

- Key definitions
  - Edge pixels: pixels at the edge of floral unit clusters or centers of small clusters where features mix.
  - Pinkest pixels: pixels deeper in the center of clusters, less likely to be mixed with other features.
  - Merged categories: classification categories that are combined into one or more groups rather than kept separate.

- 3 cm imagery classifications
  - May_3cm_classification1
    - Pinkest Silene dioica values only
    - S. dioica categories non-merged
    - Crataegus monogyna pure values merged
  - May_3cm_classification2
    - Pinkest Silene dioica values only
    - S. dioica categories merged
    - Crataegus monogyna pure values merged
  - May_3cm_classification3
    - Silene dioica pinkest and edge values
    - Categories merged for both species
    - Crataegus monogyna pure values merged
  - May_3cm_classification4
    - Pinkest Silene dioica values only
    - Silene dioica categories non-merged
    - Crataegus monogyna pure values non-merged

- 7 cm imagery classifications
  - May_7cm_classification
    - Trained with 3 cm data
    - Uses the 3 cm training variant that yielded the highest overall 3 cm accuracy
  - May_7cm_class_trained_7cm
    - Specific trained variant name for 7 cm workflow
  - May_7cm_classification trained with 7 cm data
    - Classification adapted to 7 cm imagery

- Implications for environmental monitoring practice
  - Provides standardized, reproducible methods to classify imagery for plant feature detection.
  - Multiple variants allow assessment of how merging vs non-merging and edge vs pinkest distinctions affect outputs.
  - Outputs are designed to be stored and shared via appropriate data portals, supporting transparent monitoring over time.
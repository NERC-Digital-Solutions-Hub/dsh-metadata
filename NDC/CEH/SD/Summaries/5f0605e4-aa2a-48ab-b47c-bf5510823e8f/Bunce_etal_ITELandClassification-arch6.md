# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Purpose: classify every 1 km square in Great Britain into a land class, preserving the original ISA-based classifications to ensure continuity and compatibility with extensive existing datasets and studies.
- Why it matters for data work: enables a reproducible, machine-readable GB-wide land classification built from integrated, field- and map-derived data, suitable for policy analysis, remote sensing applications, and environmental planning.

## Data, datasets, and structure

- Data categories used to label squares:
  - COASTAL (coastal cliff, rock, sand, mud, shingle, tidal)
  - ALTITUDE (hill behind, distance to hill behind, gradient, mean altitude, etc.)
  - MAPDATA (distance to roads, water bodies, towns, railways, rivers, etc.)
  - DISTANCE (distance to south/west coasts)
  - ISLAND (island status)
  - CLIMATE (sunshine hours, snow days, Jan temp, etc.)
  - GEOLOGY (detailed rock/soil types)
  - DRIFT (drift/soil-deposit types)
- Data characteristics:
  - Based on existing datasets or automatically recordable features
  - Resolution and format aligned with automation for 1 km squares
  - Use of OS digital data (1:250,000) and ARC/INFO-derived maps
- Data integration goals:
  - Combine diverse attributes into consistent 1 km-square feature vectors
  - Retain relative distributions from sample squares used in the original ISA classification

## Classification approaches explored

- Baseline and context:
  - Original ISA-based classification using 1212 sample squares (1990s extension context)
- Multivariate methods tested:
  - Discriminant Function (DF)
  - Logistic Regression (LR) and combinations (Logistic/Discriminant)
  - Simulation ordination approaches (ISA-inspired)
  - Other multivariate techniques from phytosociology (experimental, exploratory)
- Evaluation criteria:
  - Geographic distribution of squares by class
  - Dispersion and variability of environmental variables within classes
  - Alignment with the original 1212-square classification
  - Proportional representation of class sizes
  - Relationship to the principal environmental gradient
  - Proportion of field-sampled squares retained
  - Practicality and error characteristics for GB-scale mapping
- Key challenges:
  - Differences in data balance, scale, and digitized data availability vs. original field data
  - Some methods produced substantial misallocations or boundary shifts (e.g., certain coastal or northern classes)

## Key findings from the analyses

- Correspondence with original classification:
  - Logistic/Discriminant approaches yielded higher correspondence with the original 1212-square classifications than alternatives, with better regional balance and lower errors.
  - Cross-tabulations showed the Logistic/Discriminant method produced a tighter diagonal alignment with fewer outliers.
- Environmental gradient and dispersion:
  - High correlation between environmental gradient positions for original vs. discriminant-based approaches (close to original axis alignment).
  - Standard errors for environmental gradients and class dispersion were generally lower for Logistic/Discriminant than the original, indicating more stable class positions.
- Land-cover estimation:
  - For 1978 land-cover estimates, both Discriminant Function and Logistic/Discriminant showed lower standard errors and coefficients of variation than the original classification.
- Ecological and vegetation alignment:
  - Moderate to strong correlations between the environmental gradient used for classification and vegetation quadrats, with Logistic/Discriminant performing comparably to the Original in some respects and slightly differently in others.
- Outputs and reproducibility:
  - Availability of multiple map products: original 32-class ISA-derived map (from 1212 squares), an expanded map including 4800 additional squares identified by 76 attributes, and a classification trained on the original 1212 squares via the Discriminant Function.
  - Emphasis on producing readable, end-user-ready maps and data layers for policy and planning contexts.

## Outputs, data products, and end-user benefits

- Maps and map layers:
  - Distribution maps for the selected classification method (Logistic/Discriminant)
  - Original 32-class ISA maps and expanded 32-class maps (1212 + 4800 squares)
  - Classification layers trained on the original sample
- Overlay and attribute integration:
  - Ability to overlay coastal features with other attributes (e.g., chalk coastal areas)
  - Area- and region-specific summaries (environmental means, geology frequencies)
- Data tables and summaries:
  - Environmental means by attribute, standard errors, and dispersion metrics
  - Summary comparisons of original vs. DF/LR classifications
  - Vegetation and soil-pH related summaries aligned with land classes
- Accessibility and reuse:
  - Outputs designed for self-serve use in GIS and data-analytic workflows
  - A reproducible methodology that can be applied to all GB squares

## Recommendations and conclusions

- Primary recommendation:
  - Use Logistic Regression combined with Discriminant Function (Logistic/Discriminant) for GB-wide land classification.
- Rationale:
  - DF alone struggles with coastal classes in the south and boundary shifts (e.g., class 7, 8, 25) that would require redefinition.
  - Logistic/Discriminant delivers better proportional representation of squares, closer alignment to the original classification, and generally lower standard errors and dispersion.
  - Both LR and DF alternatives offer improvements over the original classification; LR/DF (combined approach) provides the best overall performance and robustness for GB-scale mapping.
- Practical implications:
  - AGB-wide GB classification with LR/DF supports more reliable policy analysis, environmental planning, and remote-sensing applications.
  - Outputs should include multiple map options and trainable classifiers to accommodate future data updates and refinements.

## Appendices and references

- Appendix A: references to studies using the Merlewood Land Classification
- Appendix B: Multivariate discrimination (methods and technical details)
- Additional sections:
  - Field surveys and square sampling methodology
  - Coastal feature distribution and overlay examples
  - Environmental means and data tables for 2–6 data facets
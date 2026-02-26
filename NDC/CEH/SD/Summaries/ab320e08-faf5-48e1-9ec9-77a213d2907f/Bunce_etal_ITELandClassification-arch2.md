# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Objective and context
  - Aim: classify every 1 km square in Great Britain into a land class, using automated methods and machine-readable data.
  - Rationale for automation: original ISA-based classification would take about 20 man-years; existing classifications and databases needed to be preserved, and sample distributions needed to be retained.
  - Outcome sought: a reproducible classification that mirrors the original system while enabling large-scale, consistent outputs and comparisons over time.

- Data structure and inputs
  - Data domains used for classification:
    - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
    - ALTITUDE: hill/valley height, distances, gradients, aspect, slope
    - MAPDATA: OS-derived features (sea, woodland, roads, canals, water, towns, railways, etc.)
    - DISTANCE: distance to south/west coasts
    - ISLAND: island status
    - CLIMATE: sunshine hours, snow days, January temps
    - GEOLOGY: detailed rock/soil types
    - DRIFT: glacial and sedimentary deposits
  - Data were drawn from existing datasets or recorded automatically, prioritising data available for all squares.
  - Original intention: reuse the ISA framework with updated data, enabling full GB coverage on a computer.

- Classification procedures explored
  - Reproduction approach
    - Attempted to mirror the original ISA-based classification using the updated data; differences in data balance and spatial scale reduced exact replication.
  - Discriminant Function (DF)
    - Applied to divisions of land classes; evaluated against the original 1212-square ISA baseline.
    - Found to produce high correspondence for many classes but caused shifts in class sizes and some regional misallocations.
  - Logistic Regression / Discriminant Function (LR/DF)
    - Combined approach tested to improve correspondence with the original while stabilising class distributions.
    - Showed higher correspondence than either DF or LR alone in several metrics.
  - Other multivariate techniques
    - Explored additional algorithms (inspired by phytosociology and ordination concepts); many failed to keep the original classification intact geographically (e.g., Midlands classes dispersed into southern Scotland).
  - Indicators and simulation ordination
    - Used 76 indicator attributes to expand classification beyond the original 282 attributes; aimed to improve efficiency and regional coherence, but yielded substantial divergences in some cases.

- Evaluation criteria
  - Geographical distribution of squares within each land class
  - Dispersion of classes (means and standard errors of locational variables)
  - Allocation accuracy of the original 1212 squares between land classes
  - Proportional representation of squares per class across GB
  - Relationship between the principal environmental gradient and land classes
  - Proportion of field-sampled squares across dates (1978, 1984, 1990)
  - Efficiency in predicting areas and cover features
  - Relationship between environmental gradient and vegetation composition

- Key findings (comparative results)
  - Discriminant Function (DF) alone
    - Reasonable correspondence for several divisions but failed to identify coastal classes 7 and 8 in the south, implying redefining coastal classes would be required.
    - Regions such as class 25 extended into southern Britain, indicating regional misallocations.
  - Logistic Regression / Discriminant (LR/DF)
    - Best overall among tested approaches.
    - Maintained better proportional sampling (closer to stratum size) and higher retention of squares within the original classification.
    - Lower standard errors and less dispersion than the original for many classes, including coastal features.
    - Produced tighter clustering in distribution maps, with some divergence only in coastal classes 7 and 8 (which would necessitate redefinition).
    - Showed stronger alignment with environmental gradients and related vegetation patterns than the original and other methods.
  - Overall
    - The LR/DF approach offered substantial improvements over the original ISA-derived classifications and over other tested methods, particularly in maintaining coastal classifications and achieving more robust, scalable outputs.

- Outputs, maps, and data products
  - Distribution maps created using the LR/DF method (coastal and inland classes)
  - Available classifications and training data:
    - Original ISA 32-class map derived from 1212 squares (282 attributes)
    - Original 1212 squares plus 4800 squares identified from 76 key attributes
    - All squares classified using the Discriminant Function trained on the original 1212 squares
  - Additional outputs include altitude means, land cover estimates, and environmental gradient correlations; these are presented in figures and tables (e.g., correlations with the principal environmental gradient and vegetation data).

- Ecological interpretation and validation
  - Vegetation comparison: correlations between environmental gradients and vegetation quadrats indicate strong predictive alignment for LR/DF (and to a slightly lesser extent for DF and original classifications).
  - Soil and pH context: analyses of soil pits across sample squares show LR/DF classifications align well with observed soil properties and vegetation communities.

- Recommendations and conclusions
  - Primary recommendation: adopt the Logistic Regression / Discriminant Function (LR/DF) approach for the GB land classification.
  - Rationale
    - DF alone fails to capture southern coastal classes, potentially requiring redefinition.
    - LR/DF provides closer proportional representation, lower errors, and less dispersion than the original classification, and generally outperforms the Discriminant Function alone.
    - LR/DF maintains strong correspondence with the principal environmental gradient and with vegetation patterns, supporting its suitability for monitoring environmental health and policy performance.
  - Additional note
    - The improved method shows substantial gains over using indicator attributes alone for expansion (the 4800-square expansion) and is better suited for monitoring and reporting across time.

- Appendices and references
  - Appendix A lists studies using the Merlewood Land Classification
  - Appendix B outlines Multivariate Discrimination approaches
  - The document includes detailed tables, figures, and cross-tabulations supporting the comparisons and conclusions

- Implications for environmental monitoring
  - Provides a scalable, standardized GB-wide land classification aligned with environmental gradients and vegetation patterns.
  - Enables consistent monitoring of environmental health and policy performance over time, with data products suitable for integration into maps, reports, and portals.
  - Highlights the importance of preserving coastal-class definitions and achieving proportional sampling for reliable monitoring outputs.
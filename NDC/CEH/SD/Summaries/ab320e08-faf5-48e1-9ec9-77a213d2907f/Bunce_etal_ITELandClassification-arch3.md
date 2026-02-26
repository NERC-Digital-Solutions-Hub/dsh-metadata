# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- A project to assign every 1 km square in Great Britain to a land class, based on machine-readable data and automated methods, while seeking to reproduce the original ISA-based classification for continuity and usability in numerous studies.

## Overview and aims
- Classify all GB squares into land classes to support environmental monitoring and policy evaluation.
- Maintain consistency with the original ISA classification to preserve legacy study applications and databases.
- Develop an automated, scalable approach that can handle full GB coverage and future data updates.

## Data and dataset structure
- Data sources (Section 2):
  - COASTAL: coastal environments (cliff, rock, sand, mud, shingle, tidal)
  - ALTITUDE: hill/valley metrics (heights, distances, gradients, aspect)
  - MAPDATA: administrative and physical features (roads, towns, waterways, railways, etc.)
  - DISTANCE: distances to south and west coasts
  - ISLAND: island indicators
  - CLIMATE: sunshine, snow days, January temps
  - GEOLOGY: broad lithologies and formations
  - DRIFT: glacial and related deposits
  - Data from OS (MAPDATA), MOD 100 m DTM for altitude, ARC/INFO digitized climate contours
- Grid and sampling:
  - Initial 1 km square framework with over 240 detailed square-level measures; expanded dataset includes 4800 squares identified via 76 key attributes
  - Original ISA classification used as reference for comparison
  - Historical field data from 1978, 1984, and 1990
- Data governance notes:
  - Emphasis on using existing data where possible, with automation to handle full GB coverage
  - Highlighted need for metadata quality and sharing underlying data for transparency

## Methods explored and evaluation criteria
- Approaches tested (over ~15 months):
  - ISA/Indicator Analysis (replication approach)
  - Discriminant Function analyses
  - Logistic Regression (LR) and combinations with Discriminant Methods (LR/DF)
  - Other multivariate techniques (various clustering/ordination and regression-based methods)
  - Simulation ordination variants
- Evaluation criteria (Section 4 and 4.5):
  - Geographical distribution of squares within each class
  - Dispersion measures (means, standard errors) of variables
  - Allocation of original 1212 squares across new classes
  - Proportional representation of squares per class nationally
  - Relationship to the principal environmental gradient
  - Proportion of field-sampled squares across dates
  - Efficiency in predicting areas and cover features
  - Ecological characteristics of classes across data sets

## Key findings and comparisons
- Original vs new classifications:
  - The LR/Discriminant approach provided the best alignment with the original 1212-square classification and preserved key coastal classes, while the standalone Discriminant Function failed to identify coastal classes in the south (7 & 8) without redefining those classes.
  - Cross-tabulations showed LR/DF achieving closer correspondence to the original classification than other methods.
- Environmental gradient analysis:
  - Axis 1 (south/east lowlands to north/west uplands) served as a robust gradient for evaluating class relationships.
  - Correlations with the original environmental gradient: Discriminant Function ~0.995; LR/Discriminant ~0.997, indicating near-identical ordering of classes along the gradient.
- Proportional representation and dispersion:
  - LR/DF achieved the closest balance to proportional sampling relative to the class strata and generally lower standard errors than the original classification.
  - 4800 squares classified via indicator attributes showed notable divergences from the original, underscoring the LR/DF method’s improvement.
- Outputs and maps:
  - Distribution maps for land classes (from LR/DF) were produced and validated against coastal and inland dispersion patterns.
  - Altitude, coast-distance dispersion and environmental means were summarized to support interpretation and policy use.
- Ecological and vegetation validation:
  - Comparisons with vegetation quadrats and soil indicators showed that LR/DF classifications correlated strongly with observed vegetation patterns and soil/pH descriptors, supporting ecological validity.

## Recommendations and conclusions
- Primary recommendation: adopt the Logistic Regression with Discriminant Function (LR/DF) approach for GB land-classification.
  - Reasons:
    - LR/DF preserves coastal class definitions in southern Britain, avoiding the need to redefine coastal classes (7 & 8) and misplacement seen with the Discriminant Function alone.
    - Improved proportionality to class strata and generally lower standard errors than the original classification.
    - Demonstrated reduction in dispersion relative to the original, aiding policy development and monitoring consistency.
    - LR/DF provides a significant improvement over using indicator-attribute expansions alone (the 4800-squares with 76 attributes).

## Implications for monitoring frameworks
- Reproducibility and scalability:
  - Demonstrates a workflow that can be updated as new data become available, with automated processing over the entire GB grid.
- Data governance and openness:
  - Highlights the need for rigorous metadata, clear data provenance, and sharing underlying datasets to enable external validation and reuse.
- Communication of complex results:
  - Emphasizes producing clear outputs (maps, reports, dashboards) to convey classifications and their ecological implications to policymakers and stakeholders.
- Data integration and interoperability:
  - The methodology relies on integrating diverse data types (topography, climate, geology, infrastructure) into a single classification system, informing ongoing monitoring programs and policy evaluations.

## Additional outputs and resources
- Available outputs include:
  - Original 32-class ISA classification and subsequent LR/DF-derived classifications
  - Full classification of all GB squares trained on the original squares using Discriminant Function
  - Distribution maps and altitudinal/gradient analyses
  - Tables of environmental means by class and supporting ecological characteristics

## Summary of practical takeaways for monitoring authors
- For national-scale environmental monitoring frameworks, LR/DF offers a robust, transparent, and reproducible method to classify land areas while maintaining compatibility with established classifications.
- Ensuring good metadata, data provenance, and availability of underlying data is crucial to enable validation and policy relevance.
- Class definitions should carefully account for coastal and boundary regions to avoid misclassification and ensure stability across data updates.
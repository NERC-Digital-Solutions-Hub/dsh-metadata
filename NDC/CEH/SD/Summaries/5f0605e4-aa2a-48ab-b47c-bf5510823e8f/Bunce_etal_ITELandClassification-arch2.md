# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Aim
- Classify all 1 km squares in Great Britain into land classes.
- Use automated, machine-readable data to reproduce the original ISA-based classification while enabling scalable, repeatable analysis.
- Maintain confidence from the original classification and accommodate extensive existing datasets and applications.

## Structure of the data set and data used
- Data sources and features into the classification include:
  - COASTAL (coastal types), ALTITUDE (various height and distance metrics), CLIMATE (sunshine, snow, January temps), GEOLOGY (rock types), DRIFT (drift and deposits), MAPDATA (roads, water bodies, towns, etc.), DISTANCE (proximity to south/west coasts), ISLAND indicators, and related attributes.
- Data recorded at or derived from 1 km grid squares; originally many detailed field measurements, later digitised and combined with OS map data.
- Data volumes: initial aim to reuse the full original dataset; expanded to 76 key attributes from 240+ variables to enable automated classification across all GB squares.
- Data handling goals:
  - Ensure continuous (not discrete) data attributes where possible to reduce misclassification.
  - Preserve the relative distribution of field-sampled squares among land classes.
  - Enable cross-comparison with the original ISA-based 32-class scheme.

## Summary of the classification procedures explored
- Baseline approach: replicate original ISA classification for 1212 squares; assess feasibility with automated methods.
- Methods evaluated:
  - Discriminant Function analysis (early attempt to use continuous variables).
  - Logistic Regression and combinations with Discriminant Function (Logistic/Discriminant).
  - Other multivariate techniques (e.g., variants of TWINSPAN/ISA, various ordination-based simulations).
  - Simulation ordination approaches to mimic the original indicators’ progressive divisions.
- Evaluation criteria used to judge approaches:
  - Geographic distribution of squares across land classes.
  - Class dispersion (means, standard errors) of locational variables.
  - Allocation consistency for the original 1212 squares and movements of squares between classes.
  - Proportional representation of squares in each class across GB.
  - Relationship between principal environmental gradient and land classes with variability.
  - Proportion of field-sampled squares in 1978, 1984, 1990 per class.
  - Efficiency in predicting areas and cover features.
  - Ecological characteristics of classes across data sets.

## Comparison of results (original vs derived classifications)
- Discriminant Function vs Logistic/Discriminant:
  - Logistic/Discriminant approach produced better overall alignment with the original classification, with more cohesive class clustering and fewer misplacements in coastal classes.
  - Discriminant Function alone failed to identify certain coastal classes in the south (classes 7 & 8) without redefining coastal categories; class 25 (Scotland/northern England) extended into southern Britain if used alone.
- Cross-tabulations and environmental gradient analysis:
  - Logistic/Discriminant and Discriminant Function showed strong correspondence with the original classification across the principal environmental gradient axis.
  - Logistic/Discriminant had closer alignment (lower standard errors, better alignment in several coastal-related classes) than the original, with generally lower dispersion.
- Proportional representation and dispersion:
  - Logistic/Discriminant yielded sampling proportions closest to being proportional to class size; lower standard errors than the original, often on par with or better than other methods.
- Geographical dispersion and maps:
  - Distribution maps created for the Logistic/Discriminant method illustrate the geographic spread of the 32 original ISA classes and the refinements achievable with the automated approach.

## Key findings on environmental gradient, dispersion, and data compatibility
- Gradients: The first environmental gradient runs from the southern/eastern lowlands to the northern/western uplands, aligning with the expected ecological structuring of land classes.
- Correlations with vegetation data and soil attributes:
  - Correlations between environmental gradients and vegetation gradients were strong, indicating the derived classifications retain ecological relevance.
  - Comparisons with soil pit data (pH and related soil characteristics) showed reasonable consistency across original and LR/DF classifications.
- Field survey coverage and data richness:
  - The inclusion of 76 key indicator attributes improved classification performance over the original 1212-square dataset, revealing substantial divergences from the original patterns in the expanded dataset, underscoring the value of the automated approach.

## Recommendations and conclusions
- Primary recommendation: Use Logistic/Discriminant (LR/DF) for classification of all GB squares.
  - Reasons:
    - The Discriminant Function alone failed to identify coastal classes in the south, necessitating redefinition of coastal classes and risking misclassification in other regions.
    - LR/DF offered a closer overall match to the original classification with better coastal class integrity.
    - LR/DF produced sampling proportions closer to proportional to class size, with lower standard errors and less dispersion compared to the original.
    - The 4,800-square expansion using indicator attributes showed substantial improvements with LR/DF over the originals, indicating a robust, scalable approach.
- Additional notes:
  - The methodology provides lower errors and better stability for policy-relevant applications, while maintaining ecological interpretability via the environmental gradient.
  - The results include multiple outputs: original 32 ISA classes, original 1212 squares plus 4800 additional squares identified by 76 attributes, and a fully LR-trained classification of all squares.
  - Maps and data products related to the classification are available on request from ITE Merlewood.
- Practical implications for monitoring and policy:
  - A standardized, repeatable classification framework supports time-series analyses of environmental health and policy performance.
  - The LR/DF approach enables robust, comparable datasets across GB, supporting monitoring dashboards, maps, and reports.
  - Emphasis on proportional sampling and accessible underlying data aligns with value-adding data governance and transparency goals for environmental monitoring.

## Data access and further information
- The study notes that final outputs include distribution maps and original vs. derived classifications, with the following available on request:
  - The original 32 ISA-class classification derived from 1212 squares (and based on 282 attributes).
  - The original 1212 squares plus an expanded set of 4800 squares identified from the 76 attributes.
  - A full classification of all squares trained with the Discriminant Function (and cross-validated LR outputs).
- Appendix A/B contain references and methodological details for potential replication or extension.
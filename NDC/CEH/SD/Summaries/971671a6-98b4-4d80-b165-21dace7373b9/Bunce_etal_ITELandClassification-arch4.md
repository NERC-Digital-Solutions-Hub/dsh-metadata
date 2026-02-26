# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Executive overview
- Objective: classify every 1 km square in Great Britain into land classes, using automated methods that reproduce the original ISA classification for continuity and confidence.
- Approach: evaluated multiple multivariate methods (including discriminant analysis, logistic regression, and other techniques) against criteria such as geographic distribution, class dispersion, alignment with the original 1212-square classification, and relation to environmental gradients.
- Outcome: Logistic Regression combined with Discriminant Function (Logistic/Discriminant) is recommended as the primary method for GB-wide classification.
- Outputs: GB-wide land classification maps, dispersion statistics, coastal feature distributions, and environmental gradient analyses; estimates of land cover for GB based on 1978 samples; ecological characteristics linked to classification.

## Data and data architecture
- Data sources and features used (all machine-readable or automatically recordable):
  - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal zones.
  - ALTITUDE: hill behind, distance to hill, gradient, valley altitude, aspect, slope length.
  - MAPDATA: coded layers for sea, woodland, villages, roads (A, B roads), canals, water bodies, towns, motorways, railways, rivers; mapdata stored with 0.1 hectare units.
  - DISTANCE: distances to south and west coasts (km).
  - ISLAND: island presence/absence.
  - CLIMATE: sunshine hours, snow days, January minimum temperatures.
  - GEOLOGY: 15 lithologies (limestones, sandstones, clays, cherts, chalk, etc.).
  - DRIFT: glacial and related deposits (drift-free, alluvium, raised beach, etc.).
  - ALTITUDE data from MOD 100 m DTM; OS map data; climate contours digitized.
- Data strategy goals:
  - Use data that can be obtained from existing datasets or recorded automatically.
  - Ensure the GB-wide classification can be computed from datasets with broad coverage and consistent formats.
  - Maintain compatibility with the original ISA classification to preserve historical continuity and prior analyses.

## Methods evaluated (beginning to end)
- Baseline: attempt to reproduce the original ISA classification using the available datasets.
- Approached alternatives explored:
  - Discriminant Function (DF) analyses with various data transformations.
  - Logistic Regression (LR) approaches, used alone or with Discriminant comparisons.
  - Other multivariate techniques drawn from phytosociology (exploratory work), including distance-based measures and simulated ordination, with varied success.
  - Indicator Analysis and combinations (Indicator Attributes) to augment the data set.
- Key evaluation criteria:
  - Geographical distribution of squares within each class.
  - Dispersion of classes (means, standard errors) along environmental variables.
  - Agreement with the original 1212-square classification and reallocation patterns.
  - Proportional representation of squares per class across GB.
  - Relationship between principal environmental gradient and land classes; variability of gradient scores.
  - Field-sample coverage (1978, 1984, 1990) by class.
  - Efficiency in predicting area/cover features and ecological characteristics.

## Main findings
- Discriminant Function (DF) alone:
  - Reasonable alignment for high-level divisions but failed to identify southern coastal classes (7 and 8) and caused problematic expansion of class 25 into southern Britain.
  - Required redefinition of coastal classes and mid-latitude classes, undermining geographic coherence.
- Logistic Regression (LR) approaches:
  - When combined with Discriminant (LR), produced better alignment with the original classification at many levels, with more proportional sampling and generally lower standard errors than the original.
  - Cross-tabulations favored LR/Discriminant over the original and other methods, though some regional discrepancies remained for certain classes.
  - LR identified coastal patterns more reliably, reducing misclassifications in coastal zones.
- Overall environmental gradient alignment:
  - Correlations between environmental gradients and class assignments improved with the combined LR approach relative to the original, though LR had slightly lower gradient-correlation values than DF alone in some tests.
- Geographic dispersion:
  - LR and DF showed reduced dispersion compared with the original; LR offered more stable clusterings and more coherent geographic patterns, aside from a few coastal classes (7, 8) in some regions.
- Practical outputs and validation:
  - Land cover estimates for GB (using 1978 data) favored LR/Discriminant in terms of standard errors and coefficients of variation.
  - Validation included an ecological link to vegetation and soil properties (pH, soil pits) and showed improved predictiveness for vegetation gradients with LR.
- Final stance on data products:
  - The LR-based approach yields a robust, scalable, GB-wide land classification dataset with improved sampling balance and generally lower error metrics than the original or other tested methods.

## Recommendations and conclusions
- Primary recommendation: adopt the Logistic Regression combined with Discriminant Function (Logistic/Discriminant) as the preferred method for GB-wide classification.
- Rationale:
  - DF alone fails to capture coastal classes in the south and causes regional misallocations (e.g., class 25 extending too far north).
  - LR improves proportional sampling alignment to class sizes, reduces standard errors, and decreases dispersion relative to the original classification.
  - LR better handles the balance between sample coverage and class representation, particularly when using the larger set of indicator attributes (the 4,800-square expansion) for training.
- Additional considerations:
  - While LR shows overall improvements, the original classification still provides higher correspondence in some metrics; LR’s improvements are particularly notable for coastal patterns and regional balance.
  - The LR approach enables more reliable policy-relevant mapping and supports better downstream use for land-use planning and environmental assessments.
- Outputs for dissemination:
  - GB-wide LR-based land classification maps (32 classes) and distributions.
  - Distribution maps of coastal features and overlayed attributes to support integrated data use.
  - Value-added data products including vegetation correlations and ecological class descriptions.
  - Documentation of environmental means and standard errors for each class to support metadata and data governance.

## Implications for Data Leaders
- Data stewardship and governance:
  - A formal, GB-wide, automated land classification dataset demands robust metadata, versioning, and data provenance to ensure reproducibility across academic, governmental, and NGO networks.
  - Documentation should cover data sources, processing steps, model configurations (LR + DF), and validation results.
- Data standards and interoperability:
  - Harmonize data formats for coastal, altitude, geology, climate, and mapdata layers to streamline integration with external datasets and partner systems.
  - Maintain clear definitions for the 32 land classes and the environmental gradient axis to ensure consistent interpretation across networks.
- Data quality and accessibility:
  - Provide standard errors, sampling coverage metrics, and metadata on model performance per class to support risk assessment and decision-making.
  - Release maps and underlying data with appropriate licensing to enable reuse in policy analysis, planning, and environmental monitoring.
- Collaboration and scaling:
  - The methodology supports scalable updates as new data become available; establish processes for periodic reclassification and validation with partner organizations.
  - Align with broader data communities of practice to share best practices for automated land classification and environmental gradient modelling.

## Appendix / supporting context
- The study includes extensive cross-validation, comparisons against the original 1212-square classification and the larger 4,800-square set, and analyses of ecological characteristics (soil pH, vegetation cover) linked to class assignments.
- It provides a foundation for GB-wide land cover estimation and supports related environmental planning and policy work through a defensible, data-driven classification framework.
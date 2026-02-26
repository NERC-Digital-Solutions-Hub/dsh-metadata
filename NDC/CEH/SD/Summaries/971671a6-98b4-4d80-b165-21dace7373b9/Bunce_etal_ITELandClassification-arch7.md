# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Executive summary
- Objective: classify every 1 km square in Great Britain into land classes, using automated, machine-readable data to reproduce the original ISA-based system.
- Rationale: original 1km square classification was widely used; many related databases exist; field data distributions needed to be preserved; expanded classifications should be more efficient than new unsupervised methods.
- Approaches tested: Discriminant Function, Logistic Regression, a range of multivariate techniques, and simulation/ordination methods; assessments based on geographical distribution, class dispersion, concordance with original classifications, regional balance, and ecological relevance.
- Key finding: Logistic Regression combined with Discriminant Function (LR/DF) provided the best overall performance, addressing coastal class issues and improving sampling balance and error metrics.
- Final recommendation: adopt Logistic Regression/Discriminant (LR/DF) as the preferred method for classifying all GB squares, due to better alignment with the original classification, more proportional sampling, and lower standard errors.

## Data structure and inputs
- Grid: GB-wide 1 km square grid.
- Data types used (all machine-readable or automatically recorded):
  - COASTAL: coastal environments (cliffs, rock, sand, mud, shingle, tidal).
  - ALTITUDE: hill and valley-related metrics (height, distance to features, gradient, aspect, slope, mean altitude).
  - MAPDATA: land/water features and infrastructure (sea, woodland, villages, roads, canals, towns, railways, rivers) stored in 0.1 hectare units.
  - DISTANCE: proximity metrics to major coasts.
  - ISLAND: island status indicators.
  - CLIMATE: sunshine hours, snowfall, January temps.
  - GEOLOGY: rock type categories.
  - DRIFT: drift and surficial deposits categories.
- Data sources: OS digital map data, MOD 100 m DTM for altitude, Mapdata provider through a contractual arrangement; grid-based representation and 1 km scope.
- Data handling: aim to mirror the original data richness while ensuring broad coverage across all squares; remove zeros in some analyses to stabilize results.

## Classification approaches explored
- ISA-based approach reinstatement (using a detailed dataset) vs. updated automated approaches.
- Discriminant Function (DF): evaluated as a continuous-variable approach; initial expectations included faster computation and clear summaries of relationships between classes.
- Logistic Regression (LR) and its combination with Discriminant Function (LR/DF): applied to the first three divisions and final two levels; tested for correspondence with the original classification.
- Other multivariate techniques: explored several algorithms from phytosociology; issues with inter-regional class dispersal and distance measures limited applicability.
- Simulation ordination approaches: copied original ISA method via indicator axes; produced good results for many classes but misclassified northern-southern distributions (classes 25–26), leading to rejection.
- Key outcomes:
  - DF alone could reproduce many classes but struggled with coastal classifications in the south and some northern extensions (class 25).
  - LR/DF demonstrated better overall alignment with original distributions and produced more geographically coherent results.
  - Some methods yielded better alignment at high-level groupings but diverged at finer class levels.

## Results: comparisons and validation
- Cross-tabulations: LR/DF generally showed tighter correspondence to the original classification with fewer outliers; DF alone failed to identify southern coastal classes (7 & 8) without redefining coastal boundaries; LR/DF preserved coastal distinctions more effectively.
- Environmental gradient alignment: correlations between gradient axes and land classes were very high for both original and LR/DF approaches (original ~0.997, LR ~0.813, DF ~0.845 on the principal axis), indicating consistent capture of broad environmental gradients; LR/DF provided strong overall coherence with the environmental gradient.
- Proportional representation: LR/DF achieved closer proportional representation to stratum size, with the highest agreement with the original proportions among approaches tested.
- Land cover estimates (GB-wide): LR/DF and DF performed with lower standard errors and coefficients of variation than the original; LR/DF generally offered more efficient, stable estimates across the GB extent.
- Correlation with vegetation: LR/DF showed improved correlation with vegetation gradients relative to the original, indicating better ecological relevance of the classifications.
- Coastal features: distribution maps and coastal feature overlays demonstrated that LR/DF could better differentiate coastal environments and maintain coherent coastal class delineations.

## Ecological and vegetation characteristics
- Ecological characteristics and soil/vegetation relationships were evaluated by comparing soil properties (pH) and vegetation quadrat data across classifications.
- LR/DF classifications maintained comparable ecological summaries to the original while offering improved alignment with vegetation gradients and soil characteristics.

## Coastal features and attribute overlay
- Distribution of coastal features across 1 km squares was analyzed; LR/DF supported improved coastal feature mapping and enabled potential integration with more detailed coastal subdivisions in GIS workflows.
- Example overlays (as described) show how multiple attributes (e.g., sea cliffs with chalk) can be combined to define coastal areas, useful for GIS-based scenario analyses.

## Output products and practical implications for GIS work
- Output formats: 32 original ISA classes, original 1212-square setup, expanded 4800-square datasets, and LR/DF-trained classifications for all squares.
- Maps and datasets available on request; outputs include distribution maps per class, mean environmental gradients, and dispersion statistics.
- Practical GIS implications:
  - LR/DF provides more robust, spatially coherent classifications with lower error margins, suitable for policy analysis, land-use planning, and environmental assessments.
  - The coastal classes in the south (7 & 8) are better represented under LR/DF, reducing the risk of misclassification-driven policy errors.
  - For large-scale GIS projects, LR/DF outputs offer improved stability and interpretability across scales.

## Conclusions and recommendations
- Recommendation: adopt Logistic Regression with Discriminant Function (LR/DF) as the preferred classification method for all GB squares.
- Rationale:
  - Discriminant Function alone fails to capture southern coastal classes without redefining coastal boundaries, and class 25 (Scotland/north England) extends into southern Britain under some methods.
  - LR/DF yields better proportional sampling, lower standard errors, and less dispersion than the original classification, and shows clear improvements over the 4800-squares-indicator approach.
  - Both LR/DF and Discriminant Function outperform the original in key dispersion and error metrics, with LR/DF offering the best balance of accuracy, geographic coherence, and practical GIS utility.
- Additional notes:
  - The LR/DF approach provides a more proportional representation relative to stratified sampling and reduces misclassification risk for coastal areas.
  - Maps and related datasets are available on request for implementation and validation in GIS workflows.

## Additional context for GIS specialists
- The project emphasizes the need to balance fidelity to the original 32-class system with practical, scalable, and reproducible automated classification using nationwide, square-based datasets.
- Outputs are designed to support map-based data visualizations and spatial analyses for policy, planning, and public communication, aligning with the GIS specialist’s aims of accessible, explorable data products.
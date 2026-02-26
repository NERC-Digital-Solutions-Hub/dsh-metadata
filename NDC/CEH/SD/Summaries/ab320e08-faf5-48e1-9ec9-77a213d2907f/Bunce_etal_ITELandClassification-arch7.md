# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Overview
- Aims to classify every 1 km square in Great Britain into land classes, replicating the original ISA classification while enabling automated, map-ready GIS outputs.
- Evaluates multiple multivariate approaches to derive a consistent, scalable GB-wide land classification.

## Data and Input Structure
- Data categories used for classification (all mapped to 1 km grid):
  - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
  - ALTITUDE: hill behind, distance/gradient, valley behind, mean altitudes, aspect
  - MAPDATA: land features and infrastructure (sea, woodland, villages, roads, canals, inland water, towns, motorways, rails, rivers)
  - DISTANCE: distance to south and west coasts
  - ISLAND: island indicator
  - CLIMATE: sunshine hours, snow days, mean Jan temp
  - GEOLOGY: detailed rock types from various eras
  - DRIFT: drift types (glacial, alluvium, etc.)
- Data resolution and sources:
  - 1 km squares; map data at 0.1 ha units
  - MOD 100 m DTM for altitude, OS digital data via Mapdata contractors
  - Arc/INFO used for location of climate/geology contours
- Objective: use existing data sets or automatically recordable features to enable nationwide classification without prohibitive manual field work.

## Methods Explored
- Baseline: replicate original ISA classification using detailed, square-level data
  - ISA (Indicator Analysis) vs TwinSPAN: replication issues due to data balance and scale differences; results diverged
- Discriminant Function (DF)
  - Pros: continuous variables, fast, single output summarizing relationships
  - Cons: some lower-level misclassifications; regional balance issues; zeros in data problematic
  - Result: moderate correspondence with original (around 628/1212 for initial 3-level splits); regional balance concerns
- Logistic Regression (LR)
  - Applied to final levels; cross-tab comparisons show improved correspondence vs original
  - Generally better alignment with original classifications and more stable regionally
- Other multivariate approaches
  - Tests of various algorithms showed potential but issues with geography/region-specific distributions
  - Some approaches discarded due to dispersal of certain classes (e.g., Midlands into other regions)
- Evaluation criteria
  - Geographical distribution of squares per class
  - Class dispersion (means and SE of locational and environmental variables)
  - Match to original 1212-sq classification and reallocation movements
  - Overall class proportions GB-wide
  - Relationship to the principal environmental gradient and its variability
  - Field-sampling representation over time
  - Coverage of areas/features (e.g., land cover, coastal/vegetation indicators)

## Results and Comparisons
- Correspondence with original classifications
  - DF: 438/1212 correspondence when attempting close replication
  - LR: higher correspondence after optimization; generally closer to original
  - Cross-tab analyses show LR and DF have better diagonal patterns than original ISA in many cases
- Environmental gradient alignment
  - Correlation of gradient positions between original and DF/LR procedures: very high (original vs Discriminant ~0.995; original vs LR ~0.997)
- Proportional representation and dispersion
  - LR/DF methods exhibit better proportional representation and lower standard errors relative to the original scheme
  - Both LR and DF show less dispersion than the original, beneficial for policy/research use
- 4800 extra squares (from indicator attributes) versus original 1212
  - Indicator-based expansion diverged significantly from the original; LR/DF approaches offered a more coherent integration
- Coastal classes and regional agreement
  - Discriminant Function alone failed to identify southern coastal classes (7 & 8), necessitating redefinition if used alone
  - LR approach mitigates coastal misclassification risks and provides more stable regional coherence
- Ecological validation
  - Correlations between environmental gradients and vegetation data (5 quadrats across 256 squares) indicate moderate-to-strong ecological relevance (original ~0.827; LR ~0.845)
- Land cover estimates
  - LR/DF approaches yield lower SEs and CVs for land-cover estimates at 1978 baseline; generally outperform original ISA in error terms

## Outputs and GIS Products
- Classification outputs
  - DF-based classification of all GB squares
  - LR-based classification maps and cross-validated results
  - Original ISA 32-class maps (from ISA and 282 attributes)
  - Original 1212 squares plus 4800 additional squares with 76 key attributes
  - Classification results for all squares trained from the original 1212 squares via Discriminant Function
- Maps and overlays
  - Distribution maps by land class (LR/DF method)
  - Overlay demonstrations (example: coastal features such as sea cliffs and chalk in Kent/Sussex)
- Environmental summaries
  - Means and standard errors for altitude, drift, etc.
  - Environmental gradient scores by class
- Accessibility notes
  - Several maps and data products available from ITE Merlewood on request

## Conclusions and Recommendations
- Recommended method: Logistic Regression combined with Discriminant Function (LR/DF)
  - Primary reason: Discriminant Function alone misses coastal southern classes (7 & 8) and implies redefinition; LR avoids this issue
  - LR/DF combination offers:
    - Proportional sampling closer to stratum size
    - Highest correspondence with the original classification
    - Generally lower standard errors and dispersion than the original
    - Clear improvement over the 4800-indicator attribute approach in reproducing the original structure
- Implications for GB land classification work
  - Adopt LR/DF approach for GB-wide, map-ready land classification
  - Retain coarser coastal classifications where appropriate; avoid over-fragmentation that misrepresents regional patterns
  - Provide multiple data products for GIS use: original ISA-based maps, LR/DF maps, and combined-squares maps for scalable analysis

## Recommendations for GIS Practitioners
- Build seamless GIS layers for all GB 1 km squares using LR/DF classifications
- Include both the original ISA-derived 32-class map and the LR/DF-produced maps for comparative analysis
- Maintain metadata on data sources (MOD 100 m DTM, OS Mapdata, climate/geology attributes) and the data fusion process
- Enable overlays of coastal features, altitude, drift, and environmental gradient values to support policy, planning, and ecological studies
- Consider providing downloadable shapefiles or geodatabases with accompanying attribute tables summarizing class means and gradients

## Appendices and Related Work
- Appendix B: Multivariate discrimination methods and their testing results
- Appendix A: References to external studies using the Merlewood Land Classification
- Additional supporting figures and tables detailing environmental means, standard errors, and cross-validation results
# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Aim
- Classify every 1 km square in Great Britain into land classes using automated methods, while reproducing the original ISA-based classification to maintain continuity with prior studies and databases.
- Develop scalable, machine-readable classifications across GB with robust data provenance and interpretability for policy and research use.

## Data and data structure
- Data required to classify squares drawn from existing datasets or automatically recorded features.
- Key data types used:
  - COASTAL (coastal cliff, rock, sand, mud, shingle, tidal)
  - ALTITUDE (hill/valley height, distance, gradient, aspect, slope)
  - MAPDATA (OS-derived layers: seas, woods, villages, roads, towns, waterways, railways, etc.)
  - DISTANCE to south/west coasts
  - ISLAND presence and CLIMATE (sunshine, snow days, Jan temps)
  - GEOLOGY and DRIFT (drift types, sedimentary/ice-age deposits)
  - Altitude data from MOD 100 m DTM; map data digitised at 1:250,000
- Originally many variables (over 240 per square in some approaches); practical automation relied on a reduced set (76 key attributes).
- Target: align with the original 1212-squares ISA framework while enabling full-squares classification.

## Classification procedures explored
- Reproduction of original ISA with available data; evaluated against original classifications.
- Multivariate approaches tested:
  - Discriminant Function (DF)
  - Logistic Regression
  - Logistic/Discriminant (combined approach)
  - Other multivariate techniques (e.g., TWINSPAN/ISA, simulated ordination)
  - Use of indicator attributes (76 attributes) to train classifications
- Evaluation against multiple criteria, including geographical distribution, class dispersion, alignment with the original 1212 squares, and relationship to environmental gradients.

## Evaluation criteria
- Geographical distribution of squares within each land class
- Dispersion and variability of classes
- Match between new classifications and the original 1212-squares allocations
- Proportional representation of classes across GB
- Relationship to the principal environmental gradient and variability
- Correspondence with field sampling dates and cover features
- Predictive efficiency for areas and cover features
- Ecological characterisation of classes across data sets

## Key results
- Discriminant Function (DF)
  - Reasonable correspondence with the original for higher-level divisions but failed to identify coastal classes 7 & 8 in the south; some northern extension of class 25 into the south; issues with balance and regional allocations.
  - Cross-tabulations and environmental-gradient alignment indicated improvements over some methods but notable misclassifications at coastal boundaries.
- Logistic Regression and Logistic/Discriminant
  - Superior overall alignment with the original classification across scales
  - Better proportional balance to reflect GB strata
  - Generally lower standard errors and dispersion than the original, with robust clustering
  - More faithful retention of coastal class structure and regional patterns
- Other methods (e.g., ISA-based simulations, indicator-based approaches)
  - Produced inconsistent regional patterns or dispersed class allocations (e.g., Midlands/Southern Scotland issues)
  - Often degraded when applied to full GB squares or when extrapolated beyond sample squares

## Conclusion and recommendations
- Recommend adopting the Logistic/Discriminant approach as the primary method for GB-wide land classification.
- Rationale:
  - DF failed to capture coastal classes in the south and produced problematic regional extensions (e.g., class 25)
  - Logistic/Discriminant achieved closer overall correspondence to the original, better proportional representation, and lower standard errors
  - Both methods reduced dispersion relative to the original classification, with Logistic/Discriminant showing stronger practical performance and more reliable mapping outputs
  - The approach aligns with existing data structures and improves suitability for policy-relevant land-cover estimation and reporting

## Outputs and implementation notes
- Distribution maps of land classes derived from the Logistic/Discriminant method (GB-wide)
- Cross-tabulations and standard error analyses illustrating agreement with the original 1212-square classification and to the 4800-squares-expanded framework
- Consideration of overlaying attributes (e.g., coastal features, climate, geology) for potential refinement
- Availability of original and alternative-class maps and documentation on request

## Data provenance and reproducibility
- Data sources and processing steps documented; datasets and classifications can be uploaded with metadata to ensure discoverability and reuse
- Appendix references and external studies provide context for the methodology and potential applications in related environmental and land-use research
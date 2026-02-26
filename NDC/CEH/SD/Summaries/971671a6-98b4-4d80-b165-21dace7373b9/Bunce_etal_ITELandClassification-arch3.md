# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Executive goal: classify every 1 km square in Great Britain into land classes using automated, machine-readable data; aim to reproduce the original ISA classification to preserve its use in numerous studies and existing databases.

## Aim and Context for Monitoring Frameworks

- Provide a stable, scalable framework for environmental monitoring by mapping GB land into defined classes to support policy scrutiny and decision-making.
- Ensure classifications are reproducible, transparent, and comparable over time and across datasets.
- Balance detail with data availability and computational efficiency; prefer methods that maintain the integrity of the original classification while improving consistency and coverage.

## Data Sources and Metadata Considerations

- Data structure categories used for classification:
  - COASTAL (coastal environments)
  - ALTITUDE (hill/valley metrics, aspect, slope)
  - MAPDATA (OS-derived features: roads, towns, water bodies, railways, etc.)
  - DISTANCE (distance to south/west coasts)
  - ISLAND (island status)
  - CLIMATE (sunshine hours, snow days, January temps)
  - GEOLOGY (rock types)
  - DRIFT (glacial and geological drift)
  - ALTITUDE data from MOD 100 m DTM; coast/map data from OS digital sources
- Data scale and format: grid-based, units of 0.1 hectare; data intended to be machine-readable for automated classification.
- Metadata and data sharing: public sharing of underlying data is a barrier noted; data governance and provenance are critical to ensure quality, openness, and up-to-date datasets.
- Challenges: gaps in metadata, data quality concerns, data transformation requirements, and need for consistent data provenance across sources.

## Classification Approaches Explored

- Baseline: original ISA classification (manual/semiautomated) using detailed field data from 1 km squares.
- Alternative methods evaluated:
  - Discriminant Function (DF)
  - Logistic Regression / Discriminant Function (LR-DF, i.e., Logistic/Discriminant)
  - Simulation ordination approaches (to mimic ISA)
  - Other multivariate techniques drawn from phytosociology (exploratory)
- Evaluation criteria applied to compare methods:
  - Geographic distribution and dispersion of classes
  - Correspondence with original 1212-squares classification
  - Proportional representation of squares across classes
  - Relationship to the principal environmental gradient (ordination axis)
  - Consistency with vegetation sampling and ecological characteristics
  - Performance on both high- and low-level classifications, and integration with new indicator attributes
  - Stability when scaling from sample squares to all GB squares

## Key Findings from Comparisons

- Discriminant Function alone:
  - Good overall correspondence for some levels but failed to identify coastal classes 7 and 8 in the south; risk of redefining coastal classes and extending some northern classes into southern Britain.
  - Resulted in imbalanced class sizes and poorer regional balance.
- Logistic Regression / Discriminant Function (LR-DF) approach:
  - Provided better alignment with coastal classes and overall ecological gradient.
  - Produced closer-to-proportional sampling relative to class sizes.
  - Showed lower standard errors and less dispersion than the original ISA classification in many cases.
  - Cross-tabulations indicated LR-DF offered a tighter clustering around the environmental gradient than the original and was generally more consistent with the 1978–1990 vegetation data.
- Other multivariate approaches:
  - Some methods preserved the original classification but produced dispersed or regionally inconsistent results (e.g., Midlands England classes scattering into southern Scotland or southern England), or required redefinition of regional classes.
- Overall conclusion of comparisons:
  - The Logistic/Discriminant approach offered the best balance between maintaining key coastal classes, regional class balance, and lower error metrics, making it the preferred method for scaling the classification to all GB squares.

## Recommendations and Conclusions

- Primary recommendation: adopt the Logistic Regression / Discriminant Function (Logistic/Discriminant) approach for GB land classification.
  - Reason: preserves coastal classes (avoids needing to redefine coastal groups), maintains regional class balance, yields lower standard errors, and reduces dispersion versus the original classification.
  - Supported by: higher proportional representation to stratum size, lower error metrics, and improved performance relative to the original 1212-square ISA-based classification.
- Secondary notes:
  - Direct Discriminant Function alone is insufficient due to coastal misclassification and regional extension issues.
  - The LR-DF method demonstrates clear improvements over classifications based on indicator attributes alone (i.e., the 4800-square expansions), supporting its use for consistent, policy-relevant monitoring outputs.

## Outputs and Outputs-Related Considerations for Monitoring Frameworks

- Outputs produced and available:
  - Geographical distribution maps of GB land classes based on LR-DF
  - Cross-tabulations comparing Original, DF, and LR classifications
  - Tables of environmental means and standard errors (altitude, drift, etc.)
  - Distribution maps for the 32-class system (original ISA-derived 32 classes)
  - 4.7 Estimates of land cover for GB using 1978 data (with improved precision under LR-DF)
  - Overlay examples of combined attributes (e.g., sea cliffs with chalk) and potential areas for integrated monitoring
- Data governance implications:
  - Once LR-DF is adopted, maintain consistent metadata for all input datasets (coastal, altitude, map data, climate, geology, drift)
  - Ensure reproducibility by storing model parameters, class definitions, and the full set of squares with their LR-DF classifications
  - Consider public sharing of underlying data where possible, balancing data ownership and privacy with monitoring needs
- Monitoring readiness:
  - The approach supports scalable, repeatable updates as datasets are refreshed or expanded
  - Facilitates better communication of results to stakeholders through clearer, more accurate class boundaries and gradients

## Implications for Data Governance, Metadata, and Access

- Emphasizes the need for:
  - Robust metadata for each data source (origin, resolution, processing steps)
  - Open data policies where feasible to enable transparency and replication of monitoring outputs
  - Clear documentation of the chosen classification method (LR-DF), including rationale and implications for coastal and regional classifications
- Highlights governance challenges that monitoring bodies may face:
  - Data silos within and across organizations
  - Barriers to sharing foundational datasets publicly
  - Ensuring datasets remain up to date and are properly versioned
  - Managing the transformation and harmonization of disparate data sources for consistent monitoring outputs

## Outputs, Validation, and Ecological Interpretation

- Validation against vegetation and soil parameters:
  - Correlations between the environmental gradient and vegetation patterns show good alignment for LR-DF (and closely for original classifications), supporting ecological interpretability of the classes.
- Ecological characteristics and soil data:
  - Comparative analyses of pH and soil pit data across classifications provide evidence of the LR-DF approach maintaining ecological meaningfulness while improving statistical properties (lower standard errors, tighter clustering).

## Summary of Practical Implications for Monitoring Frameworks

- For monitoring frameworks aiming to scrutinize policy and inform decisions, adopting LR-DF classification provides a robust, scalable, and ecologically meaningful basis for land-class based monitoring across GB.
- The approach delivers improved statistical properties, better representation across regions, and maintains important coastal classifications, enabling clearer policy assessments and more reliable trend detection over time.
- Requires careful data governance: metadata management, data sharing policies, and transparent methodological documentation to support replication and stakeholder trust.
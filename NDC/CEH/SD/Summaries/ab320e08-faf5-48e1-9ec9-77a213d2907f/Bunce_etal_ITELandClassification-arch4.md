# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Purpose: classify every 1 km square in Great Britain into land classes, preserving compatibility with the original ISA-based 32-class framework while using automated, machine-readable data and datasets that cover all squares.

- Rationale for automation and data reuse:
  - Full GB classification would require about 20 man-years by hand; automation with existing data minimizes effort and enhances reproducibility.
  - Retain the relative distribution of the original sample and the confidence gained from the original classification.
  - Leverage extensive pre-existing databases built on the original classification and aim to reproduce its detail where possible.

- Data structure and inputs (Section 2):
  - Data categories used:
    - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
    - ALTITUDE: hill behind, distance behind, gradient, distance to valley, mean altitude, valley behind features, aspect, slope length
    - MAPDATA: coast, woodland, villages, roads (A, B, minor), canals, inland water, towns, railways, rivers; 0.1 ha resolution
    - DISTANCE: distance to south and west coasts (km)
    - ISLAND: island presence/absence
    - CLIMATE: hours of sunshine, snow days, mean Jan temp
    - GEOLOGY: detailed rock types (Calcareous, limestone, chalk, sandstone, etc.)
    - DRIFT: drift types (e.g., alluvium, glacial deposits, loess, etc.)
  - Additional data sources and processes:
    - Altitude data from MOD 100 m DTM
    - OS digital map data via Mapdata contract
  - Data requirements:
    - Data must be obtainable from existing datasets or recorded automatically
    - Emphasis on machine-readability, discovery, and the ability to update

- Classification approaches explored (Section 3):
  - Replication of original ISA approach vs extended classification
  - Discriminant Function (DF) trials
  - Logistic Regression (LR) trials, including a combined Logistic/Discriminant approach
  - Other multivariate techniques (e.g., simulations and distance-based methods)
  - Evaluation criteria across methods:
    - Geographical distribution of squares within each class
    - Dispersion and variability of environmental variables by class
    - Agreement with the original 1212-square classification
    - Overall class proportions across GB
    - Relationship to the principal environmental gradient and its variability
    - Sampling coverage across dates (1978, 1984, 1990)
    - Ecological characteristics inferred from vegetation and soils

- Key findings from method comparisons (Section 4):
  - Discriminant Function (DF) limitations:
    - Failed to identify southern coastal classes 7 & 8
    - Would require redefining coastal classes; also some northern extension of class 25
  - Logistic Regression (LR) and Logistic/Discriminant (LR-DF) advantages:
    - Higher correspondence with the original 1212-square classification
    - Better preservation of coastal classes and overall class balance
    - More proportional sampling and lower standard errors compared with the original
    - Reduced dispersion relative to the original classification
    - Strong alignment with the principal environmental gradient (Correlation with original gradient: very high; LR and original nearly identical)
  - Cross-tabulations and gradient alignment:
    - LR-based classifications yielded tighter clustering with fewer outliers than the original in most classes
    - LR showed strong coherence with the environmental gradient and vegetation associations
  - Data expansion impact:
    - Including 4800 squares identified by 76 indicator attributes improved coverage and demonstrated the LR approach’s improvement over other patterns
  - Output and visualization:
    - Distribution maps produced for LR-based classifications
    - Altitude means and standard errors, and other environmental means summarized to compare Original vs LR vs DF

- Recommendations and conclusions (Section 5):
  - Endorsement: Logistic Regression with Discriminant techniques (LR/DF) is recommended over Discriminant Function alone.
  - Rationale:
    - DF alone fails to identify important coastal classes in the south; LR/DF mitigates this and maintains coastal class integrity
    - LR/DF achieves closer correspondence to the original classification and better proportioning across strata
    - Lower standard errors and reduced dispersion compared with the original classification
    - The LR approach performs well across coastal, inland, and gradient-related metrics
  - Additional observations:
    - The LR method provides a more robust basis for the GB land classification and supports future expansion and updates
    - Output products include multiple maps and data views, enabling cross-compatibility with the original ISA-based framework

- Data governance and reuse implications (operational perspective for Data Leaders):
  - Reproducibility: explicit documentation of data inputs, processing steps, and model configurations enables repeatable classifications across updates.
  - Data lineage: clear trace from original ISA classification to LR-based outputs, ensuring traceability for policy and research use.
  - Metadata and discoverability: the work emphasizes making rich attribute data (including 76 key indicators) discoverable and linkable to GB 1 km squares.
  - Consistency vs. innovation balance: aims to preserve the validity and utility of the original classification while enabling scalable, automated updates.
  - User and stakeholder alignment: the methodology is designed to maintain compatibility with decades of studies that used the original classification, supporting ongoing policy and environmental analyses.

- Outputs and data products (operational deliverables):
  - LR-based classification maps for all 1 km squares
  - Cross-classification comparisons with the Original (1212-square ISA) and LR/DF methods
  - Altitude and environmental gradient means and associated standard errors
  - Coastal feature distributions and overlaying of individual attributes
  - Documentation and references to the original ISA-derived classes and subsequent 4800-square expansions

- Overall takeaway for data strategy:
  - Use LR/DF as the primary automated classification framework to classify all GB 1 km squares, preserving compatibility with the original ISA framework while achieving improved accuracy, proportionate sampling, and lower uncertainty.
  - Maintain rich metadata and attribute datasets (including 76 indicators) to support future refinements, validation, and integration with other GB environmental datasets.
# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Objective: classify every 1 km square in Great Britain into land classes, using automated methods based on machine-readable data to reproduce the original ISA-based classification while enabling scalable updates and broader application.

- Rationale for automation: the original manual approach would take about 20 man-years; automation needed to handle nationwide coverage and to work with existing, widely used datasets.

- Compatibility goal: any automated method should reproduce the original classifications for continuity and to leverage existing databases and studies that relied on the original system.

## Data Used and Structure

- Data categories used for classification (each square 1 km):
  - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
  - ALTITUDE: hill behind, distance to hill, gradient, mean altitude, valley behind, aspect, slope length
  - MAPDATA: Sea, Woodland, Villages, major/minor roads, canals, inland water, towns, motorways, railways, rivers (OS digital data, 0.1 hectare units)
  - DISTANCE: distance to south and west coasts
  - ISLAND: island indicator
  - CLIMATE: mean sunshine hours, mean snow days, mean Jan temp
  - GEOLOGY: detailed rock/soil types (e.g., calcareous/sandstone/limestone variety)
  - DRIFT: drift types (drift-free, alluvium, raised beach/marine deposits, glacial deposits, etc.)
- Data sources and scale:
  - Altitude data from 100 m MOD DTM
  - Mapdata and coast from OS digital data (1:250,000) via Readers Digest contract with Mapdata
  - Environmental variables digitized as described and used for broad environmental gradient analysis
- Sample and coverage:
  - Original aim compared to an initial ISA-based 1212-square set
  - Expanded dataset included about 4800 additional squares identified by 76 key attributes
- Data characteristics:
  - Variables used either from existing datasets or recorded automatically
  - Emphasis on continuous data over discrete attributes to improve classification robustness

## Methodologies Explored

- Approaches considered:
  - Reproducing original ISA classification using dataset-driven iterations (including TWINSPAN and ISA-based steps)
  - Discriminant Function analysis (DF) using continuous variables
  - Logistic Regression (LR) and combinations with Discriminant Function (LR/DF)
  - Other multivariate techniques (exploratory): various algorithms from phytosociology studies
  - Simulation ordination and cross-tabulations to compare against the original classification
- Evaluation criteria:
  - Geographical distribution of squares per class
  - Dispersion and variability of environmental variables per class
  - Correspondence between original 1212-square classifications and new classifications
  - Proportional representation of squares per class
  - Relationship to the principal environmental gradient and variability
  - Proportion of field-sampled squares across dates
  - Efficiency in predicting land cover areas and ecological characteristics
- Key findings during evaluation:
  - Several methods achieved varying degrees of correspondence with the original classification
  - Some approaches (e.g., certain LR transformations or simulated ordinations) yielded close but regionally imbalanced results or misallocations of some classes
  - The combination of Logistic Regression with Discriminant Function (LR/DF) provided tighter clustering and better alignment with the original classifications in most respects, but still required caution for coastal classes

## Key Findings and Recommendations

- Primary conclusion: LR combined with DF (Logistic/Discriminant) should be recommended for GB land classification.
  - Reasons:
    - The Discriminant Function alone failed to identify coastal classes in southern Britain, risking substantial redefinition of coastal classes or misplacements
    - LR/DF achieved closer alignment to the original classification and maintained a balance more proportional to class size
    - Standard errors and dispersion were generally lower than the original classification, with improvements in coastal factors
    - The LR/DF approach showed better overall performance across multiple evaluation criteria, including class coherence on the main environmental gradient
- Additional outcomes:
  - The 32-class system based on the LR/DF method produced distribution maps and dispersion analyses that were more robust than the original and the alternative methods
  - Environmental gradient correlations between original and LR/DF classifications remained high, indicating preserved ecological structure
  - Estimates of land cover for GB using LR/DF had lower standard errors and coefficients of variation compared with the original
  - Overlaying and documentation of individual attributes demonstrated potential for more detailed, multi-attribute classifications (e.g., combining sea cliffs with chalk, or other attribute overlays)
- Documentation and accessibility:
  - Availability of multiple maps and classifications (original ISA 32 classes, original 1212 squares plus 4800 squares, full LR-trained 1212 squares) upon request
  - Tables and figures for mean environmental values, distribution, and gradient analyses were prepared to support interpretation and reuse

## Data Governance and Stewardship Considerations

- Data provenance and lineage:
  - Classification built on a combination of existing datasets (OS Mapdata, coastlines, climate, geology, drift) and newly digitized/environmental attributes
  - Original ISA classification (1212 squares) used as the anchor for comparison and validation
  - Derived classifications (Discriminant DF, LR, LR/DF) created to extend and generalize the original scheme
- Data quality and reproducibility:
  - A range of multivariate methods were tested to ensure reproducibility of results and to identify the most reliable approach
  - Zero-value data issues were identified and addressed during refinement to achieve acceptable classifications
  - Cross-validation and cross-tabulation analyses were used to assess correspondence with the original classifications
- Data management and sharing:
  - Results include multiple classification outputs (original ISA, DF, LR, LR/DF) to support continuity with past studies and new analyses
  - Maps and data tables are available on request; recommended to publish in a data catalog with clear metadata, data dictionaries, and lineage
- Versioning and updates:
  - The project anticipates ongoing updates by incorporating additional squares and attributes; governance should support versioning to preserve historical classifications and enable traceability
- Metadata and documentation:
  - Comprehensive documentation of variables (Coastal, Altitude, Mapdata, Distance, Island, Climate, Geology, Drift) and data sources is essential
  - Include methodology details, model parameters, evaluation criteria, and validation results to support reuse and auditability
- Implications for data stewards:
  - Ensure robust data dictionaries and crosswalks between original ISA classes and LR/DF-derived classes
  - Maintain reproducible workflows (e.g., scripts for data preparation, model training, and validation)
  - Preserve both the original classifications and derived outputs to support legacy studies and new analyses
  - Provide access controls and licensing information when sharing data publicly or within networks

## Endnotes and Further Considerations

- Future deliverables referenced:
  - Environmental means tables for section 2 data
  - Distribution maps for coastal features from the main data base
  - Overlaying of individual attributes to create refined composite classes
- Ecological context:
  - The study connected land classes to vegetation and soil characteristics, with correlations between the original and LR/DF classifications informing ecological interpretation
- Overall takeaway for Data Stewards:
  - The Logistic/Discriminant approach offers a pragmatic, scalable path to reproduce and extend GB land classifications with improved statistical properties and better representation of coastal environments, while maintaining compatibility with historical classifications for continuity and comparability.
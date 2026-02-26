# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

- Aim and purpose
  - Classify every 1 km square in Great Britain into land classes, preserving compatibility with the original Merlewood/ISA 32-class framework due to its widespread use and established databases.
  - Develop an automated, machine-readable classification approach that could cover all squares and reproduce the essential structure of the original system.

- Data and data structure
  - Data inputs sourced from coastal, altitude, map data, distance metrics, island status, climate, geology, and drift type; augmented with distance to south/west coasts and other environmental variables.
  - Original approach relied on detailed field data from over 240 squares; practical classification used data sets recording features for each 1 km square, with data digitised from OS maps and climate/soil datasets (e.g., MOD 100 m DEM for altitude, ARC/INFO for digitised climate contours).
  - Spatial scope: all 1 km squares in GB; three field-survey dates (1978, 1984, 1990) to inform ecological and soil characterisations; datasets include 282 attributes from the ISA framework and an expanded 76 indicator attributes set.
  - Output formats included maps and tabulated means for environmental variables; several versions of classification for comparison (original ISA 32-class map, 1212-squares baseline, 4800 additional squared identified by 76 attributes).

- Classification approaches explored (mid 1990s evaluation)
  - Replication of the original ISA/TWINSPAN approach
    - Attempted to reproduce the original classifications using expanded detail; found divergences due to differences in data balance, data scale, and availability of detailed square-level information from digitised sources.
  - Discriminant Function (DF) analyses
    - Early DF using continuous variables offered faster results and clearer relationships, but reallocation of original sites to new groups and regional imbalances limited its fidelity.
    - A wide range of transformations were tested; best regional correspondence achieved but still diverged in key areas, leading to unsatisfactory regional redefinitions.
  - Other multivariate techniques (unsupervised and exploratory)
    - Some methods could not maintain the integrity of the original classification across all regions (e.g., Midlands classes dispersed to southern Scotland; distance metrics showed some promise for inter-class relationships but overall performance was insufficient).
  - Logistic Regression and combinations (Logistic Regression with Discriminant Function)
    - Applied to the first three divisions (DF), and DF at final two levels (LR/DF) for cross-comparison.
    - Found substantial correspondence with the original for many classes, but some limitations continued at finer scales.
  - Indicator-based simulations and gradient analyses
    - Simulated ordination approaches copying the original method closely yielded good results for many classes but diverged for a few coastal/inland boundary cases.
  - Cross-tabulation and gradient assessment
    - Cross-tabulations between original classifications and LR/DF methods showed LR/DF provided tighter clustering and better diagonal alignment with fewer outliers than Discriminant Function alone or Logistic alone.
    - Correlations between environmental gradients and class assignments remained very high, indicating strong overall coherence with the principal environmental gradient (south/east lowlands to north/west uplands).

- Key results and validation
  - Correspondence with original 1212-squares classification
    - Logistic/Discriminant (LR/DF) approach produced the highest overall correspondence with the original classification, and fewer misclassifications on coastal classes.
  - Gradient alignment and ecological validation
    - Environmental gradient analyses showed near-identical ordering of classes between the original and LR/DF results (high correlation on the primary axis; values around 0.995 to 0.997).
  - Geographic dispersion and sampling representativeness
    - LR/DF yielded more proportional sampling relative to stratum size and reduced standard errors in many key coastal and environmental dimensions.
  - Data and metadata considerations
    - The study highlighted data gaps, the challenge of publicly sharing entire data sets, and the need for consistent metadata to ensure verifiability and reuse.
  - Ecological and soil context
    - Comparisons with soil pit data and vegetation quadrats showed that LR/DF retained stronger associations with land-class ecology and soil pH distributions across the GB landscape.

- Conclusions and recommendations
  - Primary recommendation: adopt Logistic Regression with Discriminant Function (LR/DF) as the preferred method for classifying all GB squares.
    - Reasons:
      - Discriminant Function alone failed to identify southern coastal classes (7 and 8) and allowed extension of class 25 into southern Britain, necessitating reevaluation of coastal and northern boundary definitions.
      - LR/DF provided closer alignment to provincial/class boundaries while maintaining better class balance and proportional sampling.
      - Generally lower standard errors and dispersion compared to the original and other alternative methods.
      - The LR/DF approach demonstrated clear improvements over indicator-based expansions (e.g., the 4800-square indicator-based classifications) in accuracy and policy-relevant stability.
  - Additional considerations
    - The LR/DF approach supports more stable policy development due to reduced dispersion and improved representation across GB.
    - The study emphasizes the importance of proportional sampling, metadata quality, and data governance to enable transparent, reproducible monitoring frameworks.
  - Outputs and dissemination
    - The report notes availability of multiple outputs, including:
      - The original 32 ISA-class maps derived from 1212 squares with 282 attributes
      - The original 1212 squares plus a set of 4800 squares identified via 76 indicator attributes
      - A full LR/DF-trained classification of all GB squares
    - Maps and data products are available on request to ITE Merlewood and associated study teams.

- Data sources, scope, and governance notes
  - The classification builds on a long-standing environmental land classification tradition (ITE Merlewood system) with extensive historical usage in policy and research.
  - Data sources include OS digital map data, climate contours, altitude models, and taxonomic/vegetation references tied to soil and land-class definitions.
  - The methodology highlights ongoing data-quality and data-management considerations, including the need for robust metadata, data openness, and governance structures to support transparent, repeatable monitoring and decision-making.
  - The study references a broad set of empirical and ecological validation exercises (cross-study appendices and field surveys) to anchor the classification in real-world vegetation and soil variability.

- Appendices and references (high level)
  - Appendix A: studies using the Merlewood Land Classification system
  - Appendix B: multivariate discrimination techniques and their applications
  - The document cites numerous external studies spanning environmental planning, land use, conservation, and ecological classification, illustrating the broad applicability and testing of the classification framework.

- Overall significance for monitoring frameworks
  - Demonstrates a rigorous, methodical approach to selecting a monitoring classification framework that balances fidelity to an established classification with scalability and policy relevance.
  - Provides a blueprint for evaluating monitoring classifications against original baselines, environmental gradients, and sampling strategies.
  - Illustrates how to navigate data availability, metadata, and governance considerations in developing an authoritative environmental health monitoring tool.
# Sex-differences and temporal consistency in stickleback fish boldness

- Overview
  - Study of boldness in 48 three-spined sticklebacks (30 female, 18 male), using VIE tagging for individual identification.
  - Aims to assess sex differences and temporal consistency in exploratory boldness, including a long-term retest nine months later via catch order.
  - Data derived from exploratory behavior tests conducted in standardized tanks with controlled environmental conditions.

- Data Collected and Structure
  - Datasets comprise 8 files detailing:
    - PropTimeOut_DAY3 and PropTimeOut_DAY4: proportion of time out of cover during two consecutive test days (1 hour each).
    - Ave_PropTimeOut with Catch#1: mean proportion time out of cover across two days, linked to catch order.
    - Ave_PropTimeOut for full sample: overall mean across all subjects.
    - Sex differences datasets: PropTimeOut by sex; sample sizes for males and females.
    - Sex differences for catch number: relationship between catch order and sex.
    - Catch#1 and Catch#2: sequence of net-catch events nine months apart.
  - Key variables include: Ave_PropTimeOut, PropTimeOut_DAY3, PropTimeOut_DAY4, Sex, catch#1, catch#2.
  - Data collection uses video-based measurements of exploratory behavior in structured test tanks.

- Data Collection Procedures and Provenance
  - Subjects and housing:
    - 48 fish initially; housed in shared tanks with standardized environmental conditions (16°C, 8L:16D photoperiod).
    - After experiments, sexing performed by temperature shift to induce breeding coloration.
  - Experimental setup:
    - Exploratory tests in opaque tanks with lanes, covers, and bloodworms behind a screen to motivate exploration.
    - Each 4-day data collection cycle: days 1–2 with bloodworms present; days 3–4 without bloodworms; one hour per day.
    - Video monitoring from above; bloodworms replaced if consumed.
  - Data linkage and timing:
    - Catch order recorded during initial netting (catch#1); a second netting nine months later (catch#2) enables assessment of temporal consistency.
    - Nine-month retest allows longitudinal analysis of individual behavior.

- Data Processing, Quality Assurance, and Handling
  - Behavioral metrics:
    - Primary measure: proportion of time out of cover across days 3–4.
    - Exclusions: fish that failed to locate food on the first two test days were excluded from main analyses (with parallel analyses conducted on full sample).
  - Data handling:
    - Clear subject IDs linked to catch order data and sex.
    - Data organized into distinct files reflecting different analytical focal points (sex comparisons, catch-order analyses, etc.).
  - Documentation:
    - Descriptions of each dataset and column meanings provided (as per the listed file descriptions and column metadata).

- Metadata, Documentation, and Governance
  - Ethics and approvals:
    - All procedures approved as nonregulatory by the Royal Veterinary College Ethics and Welfare Committee.
    - Species not endangered; no special permissions required for collection.
  - Provenance and reproducibility:
    - Detailed recording of housing, experimental conditions, and behavioral assay setup.
    - Data explicitly linked to experimental cycles, days, and retest timepoints for reproducibility.

- Challenges and Considerations for Data Stewards
  - Incomplete user need picture:
    - Potential gaps in metadata about additional variables (e.g., environmental fluctuations beyond controlled conditions).
  - Data collection timing and standards:
    - Longitudinal data across nine months require robust versioning and clear linkage between catch#1 and catch#2.
  - Formats and interoperability:
    - Multiple datasets with related but distinct schemas; ensure consistent naming, units, and documentation.
  - Handling missing or excluded data:
    - Exclusion of non-feeders affects analysis scope; provide clear flags and rationale in metadata.
  - Data volume and accessibility:
    - Video data referenced; ensure proper metadata and storageplan if sharing raw media alongside processed metrics.

- Recommendations for Data Stewardship
  - Implement a consolidated data dictionary capturing all variables, units, and definitions across files.
  - Preserve raw and processed data with clear versioning; maintain links between catch order, sex, and behavioral metrics.
  - Document experimental conditions (temperature, photoperiod, housing) as experiment-level metadata.
  - Include ethics approvals and organism details in metadata; provide citation guidance using the article DOI for reuse.
  - Provide analysis scripts or code snapshots to facilitate reproducibility of the behavioral metrics (PropTimeOut, Ave_PropTimeOut).
  - Consider storing video data with associated metadata (timestamps, subject IDs) or provide indices to processed video-derived metrics to aid reuse.
# Telomere heritability and parental age at conception effects in a wild avian population

- Overview
  - Long-term, population-wide study of the Seychelles warbler to investigate telomere dynamics, heritability, and parental age effects on telomere length (RTL).
  - RTL measured from blood samples collected since 1990, with comprehensive quality control and metadata to support analyses of genetic and parental influences.

- Data collection and generation
  - Population monitoring since 1985; entire population (~320 adults) on Cousin Island has been intensively tracked.
  - Blood sampling (~25 μl) taken since 1990 and stored for RTL measurement; samples selected from 1995–2014 for the most complete data.
  - Telomere length measured using qPCR; DNA integrity and purity checked prior to analysis; samples with degraded DNA excluded and re-extracted as needed.
  - Random assignment of samples to qPCR plates to minimize systematic bias related to age, sex, cohort, or environment.

- Measured variables and units
  - Relative telomere length (RTL) as the primary measured value.
  - Additional sample- and individual-level metadata (see data structure section).

- Quality control and validation
  - Within-plate repeatability: GAPDH ~0.74; RTL ~0.73.
  - Between-plate repeatability for RTL: ~0.68 across samples measured on different plates.
  - DNA quality thresholds: minimum DNA concentration (~15 ng/μl), 260/280 purity between 1.8–2.0, 260/230 > 1.8; visual DNA integrity check on agarose gel; degraded samples re-extracted or excluded.
  - Outlier handling: exclude samples with extreme cq values (e.g., RTL or GAPDH cq thresholds) and replicate differences; ensure RTL values are derived from high-quality extractions.
  - Data considered across multiple plates with replicates (n = 388) to account for plate-to-plate variability.

- Experimental design and fieldwork
  - Major breeding season: June–September; minor season: January–March.
  - Field sampling via mist nets during breeding seasons to maximize capture probability.
  - Fieldwork period IDs (FPID) used to contextualize data within annual cycles and cohorts.

- Field and laboratory instrumentation
  - DNA extraction with DNeasy kit; overnight lysis at 37°C; final elution volume 80 μl.
  - DNA concentration measured with NanoDrop 8000; quality verified by agarose gel electrophoresis with ethidium bromide.
  - qPCR assays performed with randomization to prevent biases; outlier samples removed based on cq criteria.

- Data structure and column descriptions
  - BirdID: unique individual identifier.
  - Sex: 0 = female, 1 = male.
  - AgeY: age in years at capture.
  - AgeClass: categorical life stage (e.g., A, CH, FL, J, OFL, SA).
  - BirthFPID: fieldwork period ID of birth.
  - U_PlateID: qPCR plate identifier for RTL measurements.
  - RTL: relative telomere length (outcome of interest).
  - Technician: QC/control variable for the technician performing the qPCR.
  - Terr: territory assignment during capture.
  - FPID: fieldwork period ID of capture.
  - mum/dad: parental IDs from genetic pedigree.
  - MAC: maternal age at conception (years).
  - PAC: paternal age at conception (years).
  - BrF/BrM: dominant female/male in natal territory.
  - Additional identifiers (e.g., birth, cohort) used to link longitudinal data.

- Data processing, transformation, and reporting
  - Data cleaning and quality control steps implemented prior to analysis; samples passing QC are retained for RTL calculation.
  - Plate effects treated as a random effect in models to account for technical variation across qPCR runs.
  - Random assignment and replication across plates help ensure unbiased estimation of heritability and parental age effects.

- Data governance, sharing, and reproducibility
  - The dataset is embedded in multiple publications, with detailed methodological transparency (collection, QC, and data processing documented in cited works).
  - Open data considerations include sharing underlying data and metadata to enable replication, while acknowledging potential barriers (e.g., complete metadata availability and data-sharing constraints).

- Relevance for monitoring frameworks
  - Demonstrates rigorous data collection, QC, and metadata standardization essential for environmental health monitoring.
  - Highlights handling of long-term, multi-source data with technical variation (plate effects) and how to structure data (columns, identifiers) to enable monitoring and policy-relevant analyses.
  - Illustrates governance considerations: data provenance, quality assurance, transparency in processing, and careful planning for data sharing and reproducibility.

- Key challenges and considerations for monitoring
  - Ensuring data are complete and of high quality across time and across laboratories.
  - Managing metadata completeness and standardization to support replication and cross-study comparisons.
  - Addressing data access barriers and maintaining up-to-date metadata to verify data suitability for new analyses.
  - Implementing robust data governance to store, share, and maintain datasets and their associated metadata over long timeframes.
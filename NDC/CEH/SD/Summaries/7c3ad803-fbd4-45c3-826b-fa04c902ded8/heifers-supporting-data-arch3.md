# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

## Overview
- Longitudinal dataset describing antibiotic use and antibiotic-resistant E. coli in individual dairy heifers across 37 farms in South-West England during 2018.
- Part of the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance), funded by the Antimicrobial Resistance Cross Council Initiative.
- Data are merged and cleaned from multiple sources to enable monitoring of antimicrobial stewardship and resistance trends at the farm and animal level.

## Data sources and measures
- Farm-level data: demographics collected via farmer questionnaires.
- Laboratory data: screening for E. coli resistant to chosen antibiotics and genetic analysis of selected isolates.
- Prescription data: antimicrobial prescriptions/sales from veterinary practices and farm records.
- Key measures:
  - Antibiotic usage on-farm expressed as mg/PCU (population corrected unit).
  - Presence of resistance in samples to amoxicillin, cefalexin, tetracycline (binary indicators: amoxR, cephR, tetR).
  - Genotypic resistance markers: detection of blaCTX-M groups among CTX-R E. coli; AmpC hyperexpression status.
  - Derived variables summarizing resistance at farm and animal levels over time (e.g., farm_amoxR_pc_ex, heif_tetR_pc_in, etc.).
- Data processing and structure:
  - Variables include sample_id, farm, collection_method, and coded resistance indicators.
  - Extensive data dictionaries and derived binary/continuous variables to support analysis.

## Sampling design and recruitment
- Recruitment: convenience sample of 53 dairy farms, using personal contacts, veterinarians, and milk processors.
- Follow-up: on 37 farms, a cohort of heifers was tracked from birth to 18 months/first pregnancy.
- Farm comparability: farms were broadly representative of UK dairy farms in key metrics (herd size, milk yield, somatic cell count).

## Data collection, laboratory methods
- Sample collection: milk/rectal or freshly voided fecal samples from individual heifers during 2018.
- Microbiology workflow:
  - Samples processed after refrigeration; TBX agar used to identify E. coli colonies.
  - Resistance testing included growth on TBX with and without antibiotics (amoxicillin, cefalexin, tetracycline, cefalexin-containing media, etc.).
  - Selected isolates subjected to CTX-R testing on CTX TBX plates; beta-lactamase gene screening by multiplex PCR.
  - AmpC hyperexpression inferred when no β-lactamase genes detected; validated in a subset.
- Data quality steps:
  - Standardized product naming and quantity calculations across multiple veterinary practices.
  - Veterinary researcher reviewed data to ensure consistency prior to analysis.

## Data processing, metadata and variable definitions
- Data cleaning:
  - Condensed multi-choice responses (e.g., water trough cleaning frequency) into standardized categories.
  - Created derived variables from categorical data (e.g., binary forage type).
- Metadata and coding:
  - Sample and farm identifiers standardized (sample_id, farm codes).
  - Collection methods categorized (C = freshly voided, R = rectal).
  - Resistance indicators coded as binary (1 = yes, 0 = no) for amoxR, cephR, tetR.
  - MG/PCU and time-window based resistance metrics (e.g., farm_amoxR_pc_ex, heif_tetR_pc_ex, farm_amoxR_pc_ex_3m, etc.) defined for various lookback periods (1m, 2m, 3m, 4m).
- Data availability and governance:
  - Data are consolidated and cleaned for dissemination; linkage to a farm-level catalogue is provided.
  - Methodology and data sources are described to support scrutiny, replication, and policy-relevant reporting.

## Data governance and accessibility
- Data are drawn from farm records, veterinary practices, and laboratory analyses, with a clear audit trail of data provenance.
- Data cleaning and standardization are performed to enhance interoperability and comparability across farms and time.
- The dataset is associated with a referenced methodology and a project-related data catalogue link for access to farm-level data.

## Implications for monitoring frameworks
- Provides concrete, standardized AMU (mg/PCU) and AMR (binary resistance indicators; CTX-M and AmpC context) measures suitable for policy evaluation and monitoring dashboards.
- Demonstrates integration of multi-source data (demographics, prescriptions, lab results) to produce surveillance-ready variables.
- Highlights the value of derived time-window metrics (1–4 months, 3-month rolling) to monitor short- and medium-term resistance trends at farm and heifer levels.
- Illustrates rigorous data cleaning, metadata tagging, and cross-source harmonization steps essential for transparency and governance in monitoring frameworks.

## Limitations and considerations
- Convenience sampling may limit generalizability to all UK dairy farms.
- Data complexity and transformations require careful documentation to maintain transparency for monitoring outputs.
- Longitudinal follow-up coverage is limited to 37 farms; extrapolation to broader populations should consider potential biases.

## References
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20.
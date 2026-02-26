# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

- Purpose and context
  - Provides longitudinal data to monitor environmental health indicators related to antibiotic use and antibiotic-resistant E. coli in dairy farms.
  - Part of OH-STAR (One Health Selection and Transmission of Antimicrobial Resistance) project, funded by the Antimicrobial Resistance Cross Council Initiative.

- Data sources and scope
  - Farm demographic data from farmer questionnaires.
  - Biological samples and lab results: E. coli isolation and antibiotic resistance testing.
  - Prescription records from veterinary practices and farm records.
  - Coverage: 37 dairy farms in South-West England (2018); follow-up of a cohort of heifers from birth to 18 months/first pregnancy on these farms.
  - Recruitment: Convenience sample of 53 farms (37 followed); data include farm-level comparability metrics to UK farms (herd size, milk yield, somatic cell count).

- Antibiotic usage data
  - Metric: mg per population correction unit (mg/PCU) to quantify antibiotic use.
  - Data sources for usage: veterinary practices (51 farms) and on-farm records (2 farms); period spanned at least one year before enrolment to project end.
  - Herd size: calculated as average of start/end counts during sampling period.
  - Aimed to standardise naming and quantification across diverse product names and units.

- Sample collection and microbiology
  - Samples: from individual heifers collected during 2018; prioritised during routine pregnancy examinations when possible.
  - Collection protocol: sterile handling, fresh gloves per animal, and fresh faeces collection when needed.
  - Processing: samples stored at -80°C after preparation; cultured on TBX media with and without antibiotics (amoxicillin, ciprofloxacin, cephalexin, etc.) to detect resistance.
  - Resistance testing: isolates screened for β-lactamase genes (blaCTX-M groups) via multiplex PCR; CTX-R isolates further tested on CTX-containing TBX plates.
  - Hyperexpression: defined for AmpC when no β-lactamase genes detected; validation through independent checks.

- Data cleaning and variable creation
  - Standardisation: condensed multiple-choice responses (e.g., water trough cleaning frequency) into unified categories (e.g., daily vs. less often).
  - Derived variables: binary indicators for resistance (amoxR, cephR, tetR), continuous metrics for mg/PCU by antibiotic class, and proportion-based measures (ex/in,3m,1m,2m,4m windows).
  - Data dictionary elements: sample_id, farm, collection_method, and numerous antibiotic-resistance and usage variables (e.g., ceph_3_4, amox, tet, strep, cefalexin, fq, pen), plus proportion metrics at farm and heifer levels (ex, in, 3m/1m/2m/4m look-back periods).
  - Quality checks: veterinary researcher reconciled product names and quantities to ensure consistency across sources.

- Outputs and accessibility
  - Outputs include farm-level and sample-level indicators of antibiotic usage (mg/PCU) and presence of antibiotic resistance in E. coli isolates (amoxicillin, cephalexin, tetracycline; CTX resistance; β-lactamase genes).
  - Data intended for storage and upload to appropriate data portals; farm-level data accessible via CEH catalogue entry (URL provided in the dataset description).
  - Key reference for methodology: Schubert et al. 2021 (on reduced resistance and blaCTX-M gene carriage under certain conditions).

- Relevance to environmental monitoring and policy performance
  - Demonstrates longitudinal environmental monitoring of AMR dynamics tied to antibiotic usage on farms.
  - Standardised, QA'ed dataset suitable for integration with other environmental data to assess health outcomes and policy impact over time.
  - Addresses challenges of data value and access by providing harmonised usage metrics and resistance indicators derived from multiple sources.

- Limitations and considerations
  - Convenience sample may limit generalisability to UK dairy farms.
  - Not all recruited farms raised heifers; variability in sampling across farms.
  - Derived metrics depend on accurate cross-source standardisation of antibiotic products and units.
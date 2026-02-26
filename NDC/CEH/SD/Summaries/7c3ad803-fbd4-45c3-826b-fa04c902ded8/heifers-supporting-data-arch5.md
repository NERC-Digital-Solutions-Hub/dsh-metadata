# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

## Overview
- OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol; funded by the Antimicrobial Resistance Cross Council Initiative.
- Study collected farm-level data, samples, and laboratory results from 37 dairy farms in South-West England in 2018.
- A cleaned, merged dataset is provided, drawing from farm demographics, in-situ sampling, lab results for E. coli antibiotic resistance, and veterinary-prescription records.

## Data components and provenance
- Datasets merged into a cleaned version:
  - Farm demographic data (from farmer questionnaires).
  - Sample data collected at the time of sampling.
  - Laboratory results for E. coli resistance to selected antibiotics and genetic analyses of isolates.
  - Prescription/usage records from veterinary practices and farm records.
- Data sources are documented and linked to a farm-level catalog entry for the full farm dataset.

## Recruitment and study population
- Convenience sample of 53 dairy farms recruited through personal contacts, local veterinary practices, and milk processors.
- On 37 farms, a cohort of heifers was followed from birth to 18 months or first pregnancy; not all farms raised heifers.
- Farm-level context and comparisons to UK benchmarks are provided (herd size, milk yield, somatic cell count, and national antibiotic usage metrics).

## Data collection and sampling
- Farm demographics and antibiotic usage data collected for at least one year prior to enrolment through the project end.
- Sample collection in 2018 from individual heifers; pregnancy-diagnosis events targeted when available; otherwise direct sampling of freshly voided feces.
- Sample handling included refrigeration, sterile processing, and storage at -80°C for later analysis.

## Microbiology and laboratory methods
- E. coli detection via TBX agar with and without antibiotics; blue colonies counted as presumptive E. coli.
- Isolates from cephalexin TBX plates screened on CTX-TBX agar for resistance; beta-lactamase genes screened by multiplex PCR to categorize CTX-M groups.
- Hyperexpression of AmpC determined when no beta-lactamase genes detected, with independent checks confirming hyperexpression.
- Methodology aligns with established protocols (Schubert et al., 2021).

## Data cleaning, structure, and metadata
- Data cleaning included condensing multi-response items (e.g., water trough cleaning frequency) into standardized categories (e.g., daily vs. less often).
- Derived variables created (binary indicators, continuous metrics) for consistent analysis.
- Key identifiers and data coding:
  - sample_id and farm identifiers (unique codes per sample/farm).
  - collection_method (e.g., freshly voided vs. rectal) with corresponding codes.
  - Derived resistance indicators (e.g., amoxR, cephR, tetR) and continuous usage metrics (total_mg_pcu, specific antibiotic classes).
  - A comprehensive set of derived variables captures environmental and heifer-specific resistance measures (e.g., farm_amoxR_pc_ex, heif_tetR_pc_ex, and time-windowed measures like farm_amoxR_pc_ex_3m, _1m, _2m, _4m, etc.).
- Data are organized to support cross-linking across farm, sample, and laboratory results, with clear documentation for each variable.

## Antibiotic usage metrics and exposure variables
- Farm-level antibiotic usage quantified as mg/PCU (population corrected unit) with breakdowns by antibiotic classes and generations (e.g., amoxicillin, cephalosporins, tetracyclines, fluoroquinolones, penicillins, etc.).
- Temporal exposure metrics include proportions of environmental samples resistant to specific antibiotics across the project period and within defined windows prior to sample collection (1, 2, 3, 4 months).
- Proportions calculated for both environmental samples (exposed from environment) and heifer-specific samples, with distinctions for samples where E. coli was found or not.

## Data governance, access, and limitations
- Data are structured with coded farm and sample identifiers to support data governance and privacy.
- Access details for the broader farm-level dataset are provided via the CEH catalogue (link included in the data description).
- Limitations to note:
  - Convenience sampling may affect generalizability to UK farms.
  - Data come from multiple sources with potential naming and format variations requiring harmonization.
  - Some farms did not raise heifers; not all data are uniform across all farms.
  - Complex time-window variables (3-month, 1-month, 2-month, 4-month pre-sampling periods) require careful handling in analyses.

## Reference
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology. 2021;87:e01468-20
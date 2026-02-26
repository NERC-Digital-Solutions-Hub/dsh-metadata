# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018.

## Overview
- Datasets collected as part of the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol.
- Scope: farm management, longitudinal antibiotic use, and antibiotic-resistant E. coli in individual heifers across 37 dairy farms in SW England in 2018.
- Objective: enable analysis of relationships between farm practices, antibiotic usage, and antimicrobial resistance patterns.

## Data sources and contents
- Farm demographics: questionnaire-derived data describing farm characteristics.
- Microbiology: lab results screening for E. coli resistance to selected antibiotics; genetic analysis of isolates.
- Prescription and usage: antimicrobial prescription records from veterinary practices and in-farm records.
- Data merged and cleaned to produce a unified dataset for analysis.

## Recruitment and sampling
- Recruitment: convenience sample of 53 dairy farms (via personal contacts, local vets, milk processors).
- Cohort: on 37 farms, a cohort of heifers followed from birth to 18 months/first pregnancy; not all farms raised heifers.
- Farm-level context: data for all farms available via a provided CEH catalogue link; UK farm comparators cited (e.g., median herd size, milk yield, somatic cell counts).

## Data content and structure
- Sample identifiers and taxonomy:
  - sample_id, farm (unique farm code), collection_method (freshly voided vs rectal), Type/Coding (categorical).
- Antibiotic resistance outcomes (sample-level):
  - amoxR (amoxicillin resistance: yes/no), cephR (cephalexin resistance: yes/no), tetR (tetracycline resistance: yes/no).
- Antibiotic usage metrics (farm-level and per-antibiotic):
  - total_mg_pcu: total antibiotic usage in mg/PCU.
  - per-antibiotic usage: ceph_3_4, ceph_1, co_amox, tet, amox, fq, novobiocin, pen, cefalexin, strep, etc. (both binary indicators and continuous mg/PCU values).
- Derived/environmental resistance metrics:
  - farm_amoxR_pc_ex, farm_cephR_pc_ex, farm_tetR_pc_ex: proportion of environmental samples resistant to each antibiotic (excluding samples with no E. coli found).
  - heif_tetR_pc_ex, heif_cephR_pc_ex, heif_amoxR_pc_ex: proportion of environmental samples from dairy heifers with resistance.
  - farm_amoxR_pc_in, farm_cephR_pc_in, farm_tetR_pc_in: similar proportions including samples with E. coli found.
- Temporal windows before sampling:
  - farm_amoxR_pc_ex_3m, farm_cephR_pc_ex_3m, farm_tetR_pc_ex_3m: resistance proportions in the three months prior to a given heifer sample.
  - farm_amoxR_pc_ex_1m, farm_cephR_pc_ex_1m, farm_tetR_pc_ex_1m: one month prior.
  - farm_amoxR_pc_ex_2m, farm_cephR_pc_ex_2m, farm_tetR_pc_ex_2m: two months prior.
  - farm_amoxR_pc_ex_4m, farm_cephR_pc_ex_4m, farm_tetR_pc_ex_4m: four months prior.
  - Corresponding 3m/1m/2m/4m timepoints also defined for heifers and other groupings.
- Data cleaning transformations:
  - condensing multiple-choice responses (e.g., water trough cleaning frequency).
  - creation of binary and continuous derived variables for multi-category fields.
  - standardised coding for sample and farm identifiers.

## Microbiology and lab methods (summary)
- Sample handling: refrigerated post-collection; suspensions in PBS; mixed with glycerol; stored at -80°C.
- E. coli detection: TBX agar; blue colony counting indicates E. coli presence.
- Resistance testing: TBX plates with various antibiotic conditions; concentrations aligned with clinically relevant human resistance per EUCAST.
- Genetic screening: multiplex PCR for β-lactamase genes (CTX-M groups) on CTX-R E. coli; AmpC hyperexpression inferred when no β-lactamase genes detected, with independent checks confirming hyperexpression.

## Data quality and limitations
- Design: convenience sample; may limit generalisability beyond similar UK dairy operations.
- Not all recruited farms raised heifers; only a subset followed longitudinally.
- Data harmonisation: extensive QA steps to align product names and dosages across veterinary practices.
- Derived variables rely on reported farm activity and timing; temporal analyses depend on accurate recording of sampling dates and prior-period data.

## Access and references
- Farm-level data and associated materials available via the CEH catalogue link provided in the data description.
- Reference for methodology: Schubert et al. 2021 on antimicrobial resistance and blaCTX-M gene carriage in cattle-associated E. coli.

## Potential uses and data products
- Cross-farm comparisons of antibiotic usage (mg/PCU) and resistance prevalence in E. coli isolates.
- Time-series analyses of resistance proportions in environmental samples relative to prior antibiotic exposure.
- Self-serve dashboards or pivot-table style summaries enabling policy-makers or farm managers to explore links between management practices, antimicrobial usage, and resistance outcomes.
- Integration with other datasets to explore transmission dynamics and risk factors for resistance within dairy operations.
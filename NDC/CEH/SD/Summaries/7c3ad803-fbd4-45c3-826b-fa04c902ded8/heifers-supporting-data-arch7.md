# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

## Overview
- Longitudinal dataset from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance), University of Bristol, 2018.
- Focus on antibiotic use and antibiotic-resistant E. coli in individual dairy heifers across 37 farms in South-West England.
- Intended for analysis and mapping of spatial and temporal patterns of antimicrobial resistance and related farm-level factors.

## Data sources and cohort
- Data merged from:
  - Farm demographic questionnaires
  - Sample collection records
  - Microbiology results (E. coli presence and antibiotic resistance)
  - Genetic analysis of selected isolates
  - Veterinary prescription records and on-farm records
- Farm-level data for all farms available via the CEH catalogue (link provided in the source).

## Recruitment and farms
- Recruitment: convenience sample of 53 dairy farms (through personal contacts, local vets, milk processors).
- On 37 farms, a cohort of heifers was followed from birth to 18 months/first pregnancy.
- Farms representative of UK dairy sector with published comparative metrics (herd size, milk yield, somatic cell count).
- Antibiotic usage context provided with UK baseline mg/PCU estimates.

## Data collection and laboratory methods
- Sample collection (2018): from individual heifers; during routine pregnancy checks when possible; otherwise collected directly by researchers using gloved methods.
- Microbiology:
  - Sample processing with TBX media to detect E. coli; resistance screening using TBX with antibiotics (amoxicillin, cephalexin, tetracycline, ciprofloxacin, etc.).
  - Isolation of up to five E. coli per plate; cefotaxime-resistant isolates screened for β-lactamase genes via multiplex PCR.
  - Hyperexpression of AmpC determined when no β-lactamase gene detected; verification performed.
- Data handling: samples refrigerated and processed with standardized methods, including storage in glycerol and -80°C.

## Data cleaning and derived variables
- Recode and condense multi-response items (e.g., water trough cleaning frequency to daily vs less often).
- Derived variables created (binary and continuous) for consistent analysis, including:
  - Sample identifiers, animal/farm metadata
  - Collection method (freshly voided vs rectal)
  - Resistance indicators (amoxR, cephR, tetR)
  - Total antibiotic usage (total_mg_pcu) and breakdown by drug classes (e.g., amox, ceph_3_4, ceph_1, co_amox, tet, fq, pen, cefalexin, strep, etc.)
  - Proportions of resistant samples at farm level and within environmental samples for defined periods (ex and in), with sub-variables for short windows (1m, 2m, 3m, 4m) and prior-period windows (ex_3m, ex_1m, ex_2m, ex_4m)
  - Environmental vs all samples (ex = environmental-only; in = including all samples)
  - Temporal windows relative to individual heifer sampling (1–4 months prior, 3-month period prior, etc.)
- Reference coding and labels specified for interpretability in GIS contexts.

## Key measurements and variables relevant to GIS analysis
- Farm-level metrics:
  - total_mg_pcu: total antibiotic usage per farm (mg/PCU)
  - amoxR, cephR, tetR: resistance status per sample
  - Drug-class specific usage metrics (e.g., amox, cephalexin, tet, fq, pen, etc.)
- Resistance proportions:
  - farm_amoxR_pc_ex, farm_cephR_pc_ex, farm_tetR_pc_ex: proportion of environmental samples resistant (excluding empty E. coli)
  - heif_amoxR_pc_ex, heif_cephR_pc_ex, heif_tetR_pc_ex: proportion of environmental samples from dairy heifers resistant
- Temporal granularity:
  - ex_3m, ex_1m, ex_2m, ex_4m: environmental sample resistance proportions in specified windows before sampling
  - farm_amoxR_pc_in, farm_cephR_pc_in, farm_tetR_pc_in: proportions including samples where E. coli was not found
- Sample and farm identifiers:
  - sample_id, farm, collection_method, etc., enabling spatial joins with farm coordinates and mapping across time

## Access, references, and context
- Data availability: farm-level data for all participating farms accessible via the CEH catalogue (link in source).
- Reference: Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, et al., 2021.

## Potential for GIS products
- Mapping spatial distribution of antibiotic usage intensity (mg/PCU) and AMR proportions across farms.
- Temporal mapping to show changes in resistance proportions over defined windows (1–4 months, 3-month periods, etc.).
- Linking AMR data to farm demographics and management variables (herd size, milk yield, SCC) for spatial analyses of drivers.
- Visualization of environmental vs herd-level resistance patterns to support One Health analyses.
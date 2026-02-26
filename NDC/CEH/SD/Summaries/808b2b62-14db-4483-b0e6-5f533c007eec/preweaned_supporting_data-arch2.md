# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018

- A collaborative dataset from the OH-STAR (One Health Selection and Transmission of Antimicrobial Resistance) project at the University of Bristol, funded by the Antimicrobial Resistance Cross Council Initiative.
- Focuses on management data and E. coli resistant to certain antibiotics detected in pre-weaned calves across 51 dairy farms in South-West England during 2017–2018.
- Data are collected and merged from multiple sources to support environmental health and antimicrobial resistance surveillance in cattle.

## Purpose and scope

- Provide a cleaned, integrated dataset to monitor environmental health indicators and antimicrobial resistance in dairy farm settings.
- Enable assessment of how farm management, antibiotic usage, and environmental factors relate to resistance patterns in E. coli from pre-weaned calves.
- Align with a One Health perspective by linking farm practices, antimicrobial use, and microbial resistance data.

## Data sources and contents

- Farm demographics and management data from farmer questionnaires.
- Sample-level data collected at the time of each sample.
- Microbiology data: isolation of E. coli from environmental samples, antibiotic susceptibility testing, and CTX-R isolates.
- Genetic analysis: PCR screening for β-lactamase genes (blaCTX-M groups) in CTX-R isolates.
- Prescription records from veterinary practices and on-farm records.
- The dataset is a cleaned merge of these sources and structured for standardized analysis.

## Recruitment and sampling design

- Recruitment: convenience sample of 53 dairy farms; 51 farms had preweaned calves during the study.
- Farm comparability: similar to UK farms on several metrics (herd size, milk yield, somatic cell count, antibiotic usage levels).
- Sampling: monthly visits from Jan 2017 to Dec 2018; environmental samples collected from areas contaminated by pre-weaned calves using sterile overshoes or direct ground sampling.
- Sample handling: samples refrigerated during processing; aliquots stored at -80°C after processing.

## Laboratory methods

- Pasteurization and preparation: samples suspended in phosphate buffered saline, mixed, and stored with glycerol for preservation.
- Cultural methods: TBX agar used to identify E. coli (blue colonies); selective plates with antibiotics to screen for resistance (e.g., CTX, amoxicillin, ciprofloxacin, streptomycin, cephalexin).
- Confirmation: up to five E. coli isolates per plate transferred to CTX-TBX agar to identify cefotaxime resistance.
- Genotyping: multiplex PCR to detect β-lactamase genes in CTX-R isolates, focusing on blaCTX-M groups.
- Methodology aligns with Schubert et al. (2021).

## Data cleaning and variable construction

- Data condensed for multi-response questions where appropriate (e.g., water trough cleaning frequency categorized as daily or less often).
- Derived variables created (e.g., binary indicators for antibiotic usage components).
- Standardization of product names and quantities across different veterinary practices for consistent mg/PCU calculations.
- Averaged farm counts (e.g., total cattle, herd size) over the study period to generate representative metrics.

## Key data fields and variables

- Sample-level: sample_id, farm, visit_number, date_collected, ctx_m (CTX-M detected), amp_c (Amp-C detected), ct_pos (cefotaxime resistance detected), amoxR (amoxicillin resistance), tetR (tetracycline resistance), cephR (cephalexin resistance), strepR (streptomycin resistance), cipR (ciprofloxacin resistance), plain_undiluted (E. coli count).
- Farm-level: anything_waste (feeding waste milk), heifers_waste, whichclinresp (most common pneumonia antibiotic), pneum_vacc, diarrvacc, various calf health and management practices (e.g., time_dam, give_col, wean, calving_group, housing type, water source).
- Antibiotic usage: mg/PCU for multiple antibiotic classes (cephalosporins, amoxicillin-clavulanic acid, tetracyclines, fluoroquinolones, penicillins, cephalexin, streptomycin, etc.), including third- and fourth-generation cephalosporins (ceph_3_4) and other specific drugs (amox, co_amox, fq, pen, etc.).
- Other farm management variables: trough_clean frequency, calving pattern, housing, vaccination practices, water source, and groupings relevant to calf rearing.

## Data governance, access, and references

- The dataset represents a cleaned integration of farm demographics, sampling data, laboratory results, and prescription data, designed for consistent environmental health analyses.
- References the methodology and context described in Schubert H, Morley K, Puddy EF et al. (2021) on reduced antibacterial resistance and blaCTX-M distribution in cattle-associated E. coli.
- Data are intended to support cross-dataset analyses and, where possible, linking to other environmental and health datasets to enhance surveillance value.
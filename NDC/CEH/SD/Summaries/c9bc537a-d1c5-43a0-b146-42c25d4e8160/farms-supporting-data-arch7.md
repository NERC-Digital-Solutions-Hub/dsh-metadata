# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019

## Overview
- Longitudinal dataset from 53 dairy farms in South-West England (Jan 2017 – Dec 2019) as part of OH-STAR (One Health Selection and Transmission of Antimicrobial Resistance).
- Combines farm management data, sampling during the study, laboratory results, and antibiotic prescription records to study antibiotic use and resistance in Escherichia coli.

## Data and sources
- Cleaned dataset merged from:
  - Farm demographics and management data via farmer questionnaires
  - In-study samples collected at time of sampling
  - Laboratory results for E. coli resistance to selected antibiotics
  - Prescription records from veterinary practices and on-farm sources
- Data describe antibiotic usage with mg/PCU metrics and farm-level characteristics; include environmental sampling and genotypic resistance data.

## Recruitment and study scope
- Convenience sample of 53 dairy farms; recruited through personal contacts, local veterinarians, and milk processors.
- Farms broadly comparable to UK averages in herd size, milk yield, and somatic cell count (SCC).
- Antibiotic purchasing context provided (mg/PCU for UK dairy industry).

## Farm demographics and management data
- Four questionnaires administered across the study (enrolment and at follow-ups ~6–9, 12–16 months, and near final visit).
- Data include: herd size, milk yield, SCC, on-farm cattle movements, vaccination practices, housing, calving practices, feeding, waste milk use, grazing, farm infrastructure, and various management practices.
- Derived and binary variables created to simplify analysis (e.g., binary indicators for certain housing, grazing, or management practices).

## Farm antibiotic usage data
- Antibiotic usage computed for 51 farms (from veterinary practices) and 2 farms (on-farm records).
- Data standardized to mg/PCU, with herd size averages used to compute population-adjusted metrics.
- Timeframe covers at least one year before enrolment through the end of the project.

## Sampling design and sample types
- Monthly farm visits (Jan 2017 – Dec 2018); sterile sampling methods used.
- Sample types and targets (spanning adult milking cows, dry cows, replacement heifers, pre-weaned calves, and public footpaths crossing farms) with counts:
  - Adult milking cow environment: 1,963 samples
  - Dry cow environment: 321 samples
  - Replacement heifers environment: follow ~10 per herd from birth to 18 months
  - Pre-weaned calves environment (milk-fed cohort): samples
  - Footpath samples: 547 samples
- Sampling conducted using sterile overshoes or direct ground sampling; samples processed for E. coli isolation.

## Microbiology, resistance testing, and genotyping
- Samples refrigerated and processed to enumerate E. coli on TBX agar, with and without antibiotics (e.g., tetracycline, amoxicillin, ciprofloxacin, cephalexin).
- Up to five E. coli isolates per cephalexin plate transferred to CTX-TBX agar to assess cefotaxime resistance (CTX-R).
- Antibiotic resistance screening by multiplex PCR for β-lactamase genes (blaCTX-M groups) and AmpC hyperexpression (lab details pending).
- Resistance data linked to sample metadata for downstream spatial/temporal analyses.

## Data cleaning and structure
- Data cleaning included condensing multiple-choice responses (e.g., water trough cleaning frequency) and creating derived binary/categorical variables.
- A broad set of variables defined with clear data types (sample_id, farm, visit_number, date_collected, resistance flags, animal presence in sampling sites, farm practices, vaccination, housing, etc.).
- Dataset structure supports joinable records across samples, farms, and questionnaire time points.

## Key variables and data dictionary highlights
- Sample and farm identifiers: sample_id, farm
- Temporal markers: visit_number, date_collected
- Microbiology and resistance: ctx_m (CTX-M detected), amp_c (AmpC detected), ct_pos (cefotaxime resistance), cipR, tetR, cephR, strepR, amoxR
- Environment and animal presence indicators: adult, dry, weaned_heifer, footpath, etc.
- Management and farm practices: water source, bedding materials, calving practices, housing, grazing, vaccination programs, mastitis treatment patterns, dry cow therapy, antibiotic usage indicators (mg/PCU, total_mg_pcu), manure management, external collaborations
- Derived/derived binary variables: e.g., trough_clean, time_dam, wean, calving_group, calf_housing_type, organic status, etc.
- Environmental and facility factors: hectares, premises, milkgraze, predip, ACF, cleancluster, manure management features, external antibiotic usage

## Reference
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20

## Potential GIS applications
- Map farm locations and aggregate farm-level antibiotic usage (mg/PCU) and resistance indicators (CTX-M presence, CTX-R isolates) over time.
- Visualize sampling site distribution within farms (adult environment, dry cow areas, calves, footpaths) to identify spatial patterns of contamination.
- Combine farm demographics, management practices, and environmental sampling to identify spatial determinants of antibiotic resistance.
- Temporal GIS analysis: track changes in resistance markers and antibiotic usage across visits and years (2017–2019).

## Limitations and cautions for spatial analysis
- Convenience sample limits generalizability to broader UK dairy population.
- Data integrate multiple sources with potential inconsistencies in naming/units; standardization efforts are described but require careful QA when mapping.
- Some laboratory details (AmpC hyperexpression assay specifics) noted as awaiting details from the lab.
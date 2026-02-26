# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019.

## Overview
- Longitudinal dataset from 53 dairy farms in South-West England (2017–2019) as part of the OH-STAR project, funded by the Antimicrobial Resistance Cross Council Initiative.
- Data collected and merged from multiple sources to study antibiotic use and E. coli resistance patterns.
- Recruitment: convenience sample; farms broadly comparable to UK metrics in herd size, milk yield, somatic cell count, and antibiotic purchasing.

## Data scope and content
- Farm demographics and management data from farmer questionnaires.
- On-farm sampling data collected at the time of sampling.
- Laboratory results for E. coli presence and antibiotic resistance from collected samples.
- Prescription records from veterinary practices and farm records.
- Cleaned dataset with standardized naming and derived variables; antibiotic usage expressed as mg/PCU.

## Sampling and data collection design
- Monthly farm visits from January 2017 to December 2018 (except one farm that was youngstock-only for adult sampling).
- Sample environments:
  - Adult milking cow environment (e.g., collecting yard, housing shed, or field) – 1963 samples.
  - Dry cow environment – 321 samples.
  - Replacement dairy heifers environment – monthly sampling of ~10 heifers on 41 farms.
  - Pre-weaned calves environment and later calf cohorts.
  - Public footpaths crossing farms – 547 samples.
- Antibiotic usage data: collected from farms’ veterinary practices and on-farm records for at least one year prior to enrolment through to project end; standardized to mg/PCU.

## Laboratory methods
- Sample processing: refrigerated, suspended in PBS, mixed, and stored (glycerol at -80°C).
- Microbiology: TBX agar with and without antibiotics to detect E. coli; colonies counted.
- Resistance testing: up to five E. coli isolates per cephalexin TBX plate transferred to CTX-TBX plates to assess cefotaxime resistance (CTX-R); EUCAST-based concentrations used.
- Molecular screening: multiplex PCR for β-lactamase genes (blaCTX-M groups); AmpC hyperexpression detection (lab details pending).
- Methodology aligned with Schubert et al. (2021).

## Data cleaning and metadata
- Condensed multiple-choice questions to simpler categories (e.g., water trough cleaning frequency to daily vs less often).
- Created derived variables (e.g., binary forage type indicators, mg/PCU metrics).
- Standardized variable coding and ensured consistent naming across practices and farms.

## Data structure and key variables
- Sample-level variables:
  - sample_id, farm, visit_number, date_collected, context flags (adult, dry, weaned_heifer, etc.), environmental type (footpath, pasture, housed).
  - Resistance results: ctx_m (CTX-M detected), amp_c (AmpC detected), cipR, tetR, cephR, strepR, amoxR.
  - Bacterial load: plain_undiluted (total E. coli count on non-selective agar).
  - Other sample attributes: footpath presence, dam-related variables, pre-weaned calf indicators, etc.
- Farm-level and management variables (selected examples):
  - Total cattle on farm ( herd_size categories ), yield (305-day milk), scc baseline, bought_pre (cattle bought in last 12 months), hectares, pasture access, housing types, calving patterns (seasonal vs all-year), calving group housing, calving_now (recent calving).
  - Veterinary and farm management practices: water trough cleanliness, colostrum timing, calf-dip/spray, predip usage, mastitis therapy practices, NSAIDs usage in calves and mastitis, dry cow therapies, antibiotic classes used (amoxicillin-clavulanic acid, cephalosporins, tetracyclines, fluoroquinolones, etc.), total mg/PCU usage, third/fourth generation cephalosporins, and other antibiotic blocks.
  - Welfare and environmental variables: grazing vs housing, presence of other animals (poultry, equine), farm shows, market activities, external contractors, and manure management practices.
  - Housing and bedding: bedding types, shared machinery, lime use, automatic cluster flushing, milking hygiene practices, and cluster cleaning frequency.
  - External factors: presence of wildlife or pests (starlings, deer, badgers, rooks, pigeons, foxes, pheasants, rats), shoots or hunts crossing land, outsourcing rearing, and other farm characteristics.

## Quality, limitations, and governance
- Data derived from a convenience sample; comparisons to national UK metrics provided but generalizability may be limited.
- Some laboratory details noted as pending (AmpC detection method descriptor), indicating evolving metadata.
- Data organized to support discovery and analysis of antimicrobial resistance in cattle, with explicit cross-reference to the Schubert et al. 2021 methodology.

## Reference
- Schubert H, Morley K, Puddy EF, et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology. 2021;87:e01468-20.
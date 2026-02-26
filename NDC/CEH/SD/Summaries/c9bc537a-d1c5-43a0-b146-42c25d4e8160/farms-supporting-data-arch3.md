# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019

- A longitudinal dataset from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol, funded by the Antimicrobial Resistance Cross Council Initiative.
- Covers 53 dairy farms in South-West England from January 2017 to December 2019.
- Integrates farm demographics, management practices, antibiotic usage, sample-level microbiology, and laboratory resistance data.

## Data sources and structure

- Merged dataset from four primary sources:
  - Farm demographics and management data collected via farmer questionnaires.
  - In-field data collected at the time of sampling.
  - Laboratory results for E. coli resistance to several antibiotics, and genetic analysis of selected isolates.
  - Veterinary practice and on-farm prescription records.
- Data organization includes sample-level and farm-level variables with a detailed data dictionary.

## Recruitment and sampling

- Convenience sample of 53 dairy farms recruited through personal contacts, local vets, and milk processors.
- Farms are broadly representative of UK dairy farming metrics (median herd size, milk yield, somatic cell counts, antibiotic purchasing levels).

## Data collection timeline and management

- Four questionnaires administered across the project: at enrolment and at ~6–9 months, ~12–16 months, and near project end.
- Antibiotic usage quantified as mg/PCU using records from veterinary practices or on-farm sources; herd size and animal counts calculated as averages across the study period.
- Data cleaning included condensing multi-choice items and creation of derived variables (e.g., binary indicators from categorical data).

## Sample collection and microbiology

- Monthly farm visits (Jan 2017–Dec 2018). Samples collected via sterile methods from multiple environmental and animal-related sites:
  - Adult milking cow environments (faecally contaminated) across 52 farms.
  - Dry cow environments (46 farms).
  - Replacement dairy heifer environments (41 farms; ~10 heifers per cohort followed to 18 months).
  - Pre-weaned calves (milk-fed cohort environments).
  - Public footpaths across farms (40 farms).
- Processing:
  - Samples suspended in PBS, mixed, and stored at -80°C.
  - TBX agar used to screen for E. coli; antibiotics included in selective plates (e.g., cefotaxime, amoxicillin, ciprofloxacin, streptomycin, cephalexin) to detect resistant colonies.
  - Up to five E. coli isolates per plate transferred to CTX-R TBX for cefotaxime resistance testing.
  - PCR screening for β-lactamase genes (blaCTX-M groups) on CTX-R isolates; AmpC hyperexpression detected (method detail pending).
- Methodological notes reference Schubert et al. for dataset and lab workflow details.

## Data management and metadata

- Comprehensive data dictionary with explicit variable definitions (sample_id, farm, visit_number, date_collected, resistance indicators, management covariates, and numerous farm-level measures).
- Variables cover presence/absence of specific resistances (ctx_m, amp_c, and various antibiotic resistance phenotypes), on-farm practices, animal demographics, water and waste practices, vaccination schedules, housing, calving, calving management, biosecurity, and environmental interactions.
- Data cleaning steps include normalization of product names, codification of practices, and derivation of binary/ordinal indicators from categorical responses.
- Dataset explicitly notes that the described methodology follows Schubert et al. (1).

## Data governance, sharing and quality

- Data integration from diverse sources with attention to data quality (standardization, cleaning, and clear metadata).
- Metadata and a detailed data dictionary support reproducibility and transparency for monitoring frameworks.
- Underlying data sharing is framed within governance and openness expectations; outputs are designed to be shareable with stakeholders while maintaining appropriate data standards.

## Key measures and outcomes

- Antibiotic usage metrics at the farm level (mg/PCU) linked to farm demographics and management.
- Environmental and animal-associated E. coli monitoring, including:
  - Presence of E. coli resistant to cefotaxime, tetracycline, ciprofloxacin, cephalexin, streptomycin, amoxicillin, etc.
  - blaCTX-M β-lactamase gene carriage; AmpC detection pending detailed methodology.
- Linkages between management practices, vaccination, housing, calving, and antimicrobial resistance patterns over time.
- Data suitable for surveillance dashboards, trend analyses, and policy-oriented monitoring of antimicrobial use and resistance in dairy systems.

## Limitations and considerations for use

- Convenience sampling may limit generalizability to all UK dairy farms.
- AmpC detection details are noted as awaiting lab details (potential gaps in resistance characterization).
- Temporal scope is 2017–2019; users should consider temporal shifts in antibiotic practices and resistance patterns when extrapolating.

## Relevance for monitoring frameworks

- Demonstrates effective integration of farm-level management data with longitudinal environmental and microbiological surveillance.
- Highlights the importance of:
  - Clear data provenance and metadata for trustworthy monitoring outputs.
  - Standardized measures of antibiotic use (mg/PCU) and consistent resistance testing across sites.
  - Data cleaning and derived variables to facilitate clear, policy-relevant indicators.
  - Governance considerations for data sharing and transparency while maintaining data quality.
- Provides a rich dataset to inform policy decisions on antimicrobial stewardship, farm biosecurity, and AMR surveillance in agricultural settings. 

References
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20
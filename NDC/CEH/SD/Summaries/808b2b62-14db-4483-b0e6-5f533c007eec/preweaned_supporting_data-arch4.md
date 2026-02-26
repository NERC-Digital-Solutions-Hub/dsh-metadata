# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018..

- Purpose and scope
  - Describes a cleaned, integrated dataset from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol.
  - Focuses on management data and antibiotic resistance in Escherichia coli detected in pre-weaned calves on 51 dairy farms in South-West England, 2017–2018.
  - Funded by the Antimicrobial Resistance Cross Council Initiative; aligns with UK veterinary antimicrobial surveillance efforts.

- Data sources and contents
  - Farm demographics and management data from farmer questionnaires.
  - Sample-level data collected at the time of sampling.
  - Microbiology results from screening samples for E. coli resistant to selected antibiotics; genetic analysis of selected isolates.
  - Veterinary practice and on-farm prescription records for antibiotic usage.

- Recruitment and population context
  - Convenience sample: 53 dairy farms recruited; 51 had pre-weaned calves during the study.
  - Farms are broadly comparable to UK farms in herd size, milk yield, and somatic cell count (SCC).
  - Antibiotic usage data expressed as mg/PCU (per EU Surveillance of Veterinary Antimicrobial Consumption).

- Data collection and sampling design
  - Four farm visits per farm over the study period (enrolment, ~6–9 months, ~12–16 months, and near final visit).
  - Monthly visits (Jan 2017–Dec 2018); samples collected from faecally contaminated environments of pre-weaned calves using sterile methods.
  - Inclusion criteria: samples yielding E. coli on antibiotic-free TBX agar; otherwise excluded.
  - Up to five E. coli isolates per cefotaxime-challenged plate (CTX-R) used for further analysis.

- Microbiology and resistance profiling
  - Isolation and culture on TBX media with and without antibiotics (including tetracycline, amoxicillin, ciprofloxacin, streptomycin, cephalexin).
  - CTX-R isolates subjected to cefotaxime TBX, with detection of β-lactamase genes via multiplex PCR (blaCTX-M groups).
  - AmpC detection by PCR; resistance phenotypes recorded for multiple antibiotics (CTX-M, AmpC, amoxicillin, tetracycline, cephalexin, streptomycin, ciprofloxacin).
  - Data reference methodology described in Schubert et al. (2021).

- Data structure and variables
  - Sample-level: sample_id, farm, visit_number, date_collected, and a set of resistance indicators (ctx_m, amp_c, ct_pos, amoxR, tetR, cephR, strepR, cipR), as well as bacterial load (plain_undiluted).
  - Farm-level: many management and housing variables (e.g., water trough cleaning frequency, dam-calf contact time, calving_group, housing types, vaccination practices, antibiotic usage, and other management practices).
  - Antibiotic usage metrics: mg/PCU for specific drug classes and individual products (e.g., cephalosporins, amox/clav, tetracyclines, fluoroquinolones, penicillins, cefalexin, etc.).
  - Derived/derived-like variables: binary indicators for antibiotic usage, cleaned/condensed multi-response answers (e.g., water trough cleaning frequency), and categorical encodings for herd size, milk yield, and other farm characteristics.

- Data cleaning and standardization
  - Condensed multiple-choice responses to simpler categories (e.g., cleaning frequency to daily vs less often).
  - Created binary and continuous variables from categorical data; harmonized product names and quantified equivalents across practices.

- Data quality and standards
  - Uses EUCAST-referenced resistance interpretations to define clinically relevant resistance.
  - Standardized data across four data sources to ensure consistency in naming and quantification.
  - Ensured discoverability through a detailed variable dictionary and explicit data descriptions.

- Governance, access, and references
  - Dataset integrates laboratory results, farm management data, and prescription records to support surveillance and research on antimicrobial resistance.
  - Comprehensive metadata and a data dictionary accompany the dataset (variable names, descriptions, types, and coding).
  - Methodology and data handling align with the Schubert et al. (2021) framework for resistance surveillance.

- Limitations and considerations for users
  - Convenience sample may limit generalizability to all UK dairy farms.
  - Exclusion of samples without E. coli on antibiotic-free agar may bias prevalence estimates.
  - Data reflect pre-weaned calves in SW England during 2017–2018; temporal and geographic scope should be considered when extrapolating.

- Potential value for Data Leaders
  - Demonstrates end-to-end data integration across farm demographics, sampling, laboratory results, and antibiotic usage.
  - Provides a rich, well-documented data asset with a clear data dictionary, standardization approach, and transparent data cleaning processes.
  - Supports development of data products and analytics pipelines for antimicrobial resistance surveillance, risk factor analysis, and policy-relevant insights.
  - Highlights practical challenges in data harmonization (variable naming, product codes) and how to address them for larger, multi-source data ecosystems.

- Related literature
  - Data methodology described in Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli... (Applied and Environmental Microbiology, 2021).
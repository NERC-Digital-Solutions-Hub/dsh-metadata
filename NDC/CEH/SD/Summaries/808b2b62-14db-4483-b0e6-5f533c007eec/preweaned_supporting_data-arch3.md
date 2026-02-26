# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018..

- Aim and scope
  - Describes a dataset from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) aimed at monitoring antibiotic resistance in Escherichia coli from pre-weaned calves to inform policy and future decisions.
  - Data collected across 51 dairy farms in the South-West of England (2017–2018) to understand resistance patterns and associated factors.

- Data sources and content
  - Farm demographic and management data from farmer questionnaires.
  - On-farm sample collection data recording each sample event.
  - Microbiological results from screening for E. coli resistance and genetic analysis of selected isolates.
  - Veterinary-prescribed and on-farm antibiotic usage data.

- Recruitment and study design
  - Convenience sample of 53 dairy farms; 51 farms had pre-weaned calves during the study.
  - Farms broadly comparable to UK averages in herd size, milk yield, and somatic cell count.
  - Antibiotic purchasing data drawn for at least one year before enrolment through the study end; usage expressed as mg/PCU.

- Farm demographics and management data
  - Four questionnaires administered at enrolment and at ~6–9, 12–16 months, and near study end to capture management practices and changes.
  - Variables cover stock numbers, vaccination practices, housing, feeding, calving and management routines, water sources, biosecurity, and antibiotic-related practices.

- Antibiotic usage data
  - Data triangulated from veterinary practices and on-farm records.
  - Standardized naming and quantification of antimicrobial products to enable mg/PCU calculations.
  - Farm-level metrics include total antibiotic use, animal counts, and exposure indicators over the study period.

- Sample collection and microbiology
  - Monthly farm visits (Jan 2017–Dec 2018); samples collected from faecally contaminated environments around pre-weaned calves.
  - Laboratory processing involved enrichment and selective culture on TBX and antibiotic-containing TBX plates (including cefotaxime, amoxicillin, ciprofloxacin, etc.).
  - Isolation of up to five E. coli per cefotaxime-containing plate; PCR used to screen for β-lactamase genes (blaCTX-M groups) and resistance determinants (CTX-M, AmpC, and others).
  - Data aligned with Schubert et al. methods.

- Data cleaning and transformation
  - Condensed multiple-choice items to harmonize responses (e.g., water trough cleaning frequency).
  - Created derived variables (e.g., binary indicators for antibiotic usage).
  - Standardized variable formats and ensured consistent naming across sources.

- Variables and data structure (examples)
  - Sample-level: sample_id, farm, visit_number, date_collected, ctx_m, amp_c, ct_pos, amoxR, tetR, cephR, strepR, cipR, plain_undiluted.
  - Farm-level: total_cattle, yield, herd_size, bought_pre, pneum_vacc, diarrvacc, antimicrobial usage metrics (ceph_3_4, ceph_1, co_amox, amox, fq, pen, cefalexin, strep, novobiocin, etc.).
  - Intervention and management indicators: trough_clean, time_dam, um_spray, give_col, wean, calving_group, calf_housing_type, water, calving and housing practices.
  - Outcome indicators: presence of CTX-M, AmpC, cefotaxime resistance, and other resistance markers by PCR.

- Data governance, access and transparency
  - Merges data from farmer questionnaires, sample records, lab results, and prescription data, requiring careful data management and provenance.
  - Metadata and variable descriptions provided (as in the accompanying dataset dictionary within the study).
  - Public sharing of underlying data is noted as a potential barrier for some datasets; highlights governance considerations for openness and data quality.

- Relevance for monitoring frameworks
  - Demonstrates integration of environmental health monitoring components: exposure (antibiotic usage), biological response (resistant E. coli), and farm-management covariates.
  - Provides a rich, standardized data dictionary and processing pipeline suitable for evaluating surveillance systems and informing policy on antimicrobial resistance in livestock.
  - Illustrates practical challenges for monitoring frameworks: data access across sources, metadata quality, data transformation needs, and governance requirements to ensure timely, accurate, and shareable data.

- Funding and references
  - Funded by the Antimicrobial Resistance Cross Council Initiative (UK research councils) as part of the OH-STAR project.
  - Reference: Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021.
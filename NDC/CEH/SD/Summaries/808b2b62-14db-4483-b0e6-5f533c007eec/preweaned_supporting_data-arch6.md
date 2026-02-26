# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018.

## Overview
- Data from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol, funded by UK research councils.
- Scope: management data, sample data, and lab results for antibiotic-resistant E. coli from pre-weaned calves across 51 dairy farms in SW England, collected in 2017–2018.
- A cleaned, merged dataset drawing from farm demographics, in-situ sample collection, microbiology results, and veterinary prescription records.

## Data sources and components
- Farm demographics and management data from farmer questionnaires.
- Sample data collected at the time of sampling.
- Microbiology results for E. coli resistance to selected antibiotics; genetic analysis of selected isolates (blaCTX-M groups).
- Prescription records from veterinary practices and on-farm records.
- Dataset and methodology align with Schubert et al. (2021).

## Recruitment and context
- Convenience sample: 53 dairy farms invited; 51 farms had preweaned calves during the study.
- Farm comparability to UK norms ( herd size, milk yield, somatic cell count, and antibiotic usage metrics mg/PCU) to situate generalisability.

## Farm demographics and management data
- Four questionnaires administered over the study (enrolment and approximately 6–9 months, 12–16 months, and near final visit) to reduce farmer burden.
- Data include broad management practices, housing, vaccination, feeding, calving patterns, and antibiotic usage practices.

## Farm antibiotic usage data
- Antibiotic usage quantified as mg/PCU using records from veterinary practices and on-farm data.
- Data cover at least one year prior to enrolment through the study end.
- Herd and sampling period animal counts used to compute per-farm usage metrics.

## Sample collection
- Monthly farm visits (Jan 2017–Dec 2018).
- Samples taken from the faecally contaminated environments around pre-weaned calves using sterile methods (overshoes or direct ground collection where access limited).

## Microbiology and lab methods
- Samples refrigerated post-collection; prepared in PBS and glycerol; stored at -80°C.
- TBX agar used to detect E. coli; antibiotic-containing TBX plates used to screen for resistance to specific antibiotics (tetracycline, amoxicillin, ciprofloxacin, streptomycin, cephalexin).
- Up to five E. coli isolates per plate subjected to cefotaxime (CTX) TBX to identify CTX-R isolates; EUCAST-relevant concentrations used.
- Multiplex PCRs performed to detect β-lactamase genes (blaCTX-M groups) in CTX-R E. coli.
- Data collection mirrors the methodology described in Schubert et al. (2021).

## Data cleaning and variable construction
- Consolidation of multiple-choice responses (e.g., water trough cleaning frequency) into unified categories (e.g., daily vs less often).
- Derived binary variables created from categorical data (e.g., antibiotic usage indicators).
- Data cleaning steps applied to ensure consistency across diverse data sources and formats.

## Variables and data structure
- Sample-level variables: sample_id, farm, visit_number, date_collected, ctx_m, amp_c, ct_pos, amoxR, tetR, cephR, strepR, cipR, plain_undiluted, and various other resistance-related indicators.
- Farm-level variables: total_cattle, herd_size, yield, bought_pre, pneum_vacc, diarrvacc, anticocc, trough_clean, time_dam, um_spray, give_col, wean, calving_group, calf_housing_type, water source, and numerous antibiotic usage metrics (ceph_3_4, ceph_1, co_amox, amox, fq, novobiocin, pen, cefalexin, strep, etc.).
- Many binary indicators for presence/absence of resistance markers, and continuous variables for counts and antibiotic usage (mg/PCU).
- The dataset integrates farm leadership information, calf management practices, and lab-derived resistance profiles.

## Data provenance and quality considerations
- Exclusion criterion: samples with no E. coli colonies on antibiotic-free agar were excluded from analysis.
- Variation in product naming and quantity denominators necessitated normalization of antibiotic data across practices.
- Large, multi-source dataset with extensive variable lists; missing values and heterogeneity should be accounted for in analyses.

## Potential applications for data support
- Build dashboards and self-serve tools to explore relationships between farm management practices, antibiotic usage (mg/PCU), and observed E. coli resistance markers.
- Analyze associations between CTX-M β-lactamase genes and phenotypic resistance across antibiotics.
- Compare on-farm antibiotic usage patterns with environmental and isolate-level resistance data.
- Integrate with other systems to promote data sharing, re-use, and proactive policy or farming improvements in antimicrobial stewardship.

## Reference
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20
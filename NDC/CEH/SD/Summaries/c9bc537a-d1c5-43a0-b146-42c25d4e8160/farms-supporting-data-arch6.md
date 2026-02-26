# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019

## Overview
- Longitudinal dataset from OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol.
- 53 dairy farms in the South-West of England, Jan 2017 – Dec 2019.
- Integrates farm demographics, management data, longitudinal environmental and animal samples, laboratory antimicrobial resistance results, and veterinary prescription records.

## Data sources and contents
- Farm demographics and management data from farmer questionnaires.
- Sample-level data collected at time of sampling (date, location, environment).
- Laboratory results:
  - Screening for E. coli resistant to selected antibiotics.
  - Genetic analysis of selected E. coli isolates (beta-lactamase genes: blaCTX-M groups; AmpC hyperexpression).
- Prescription and farm-level data:
  - Antimicrobial prescriptions/sales from veterinary practices and farm records.
  - mg/PCU metrics for antibiotic usage; animal counts used to compute mg/PCU.

## Recruitment and comparators
- Convenience sample of 53 dairy farms recruited via personal contacts, local veterinary practices, and milk processors.
- Farms broadly representative of UK dairy sector on several metrics:
  - Median herd size 193 (UK median ~178)
  - Median 305-day milk yield 7488 L (UK median ~8967 L)
  - Median somatic cell count 167,000 cells/mL (UK median 178,000)
- 2016 antibiotic purchases reported as context (mg/PCU: UK ~26; represented farms ~21).

## Sampling design and timeline
- Monthly farm visits from Jan 2017 to Dec 2018.
- Samples collected from multiple farm environments and animal groups:
  - Adult milking cattle environment (collecting yard, housing shed, or field) – 52 farms; total 1963 samples.
  - Dry cow environment – 46 farms; total 321 samples.
  - Replacement dairy heifers – 41 farms; monthly around birth to 18 months.
  - Pre-weaned calves – environment sampling across a later cohort.
  - Public footpaths crossing the farm – 40 farms; 547 samples.
- Sterile collection methods using overboots; samples processed with PBS and glycerol, stored at -80°C.

## Microbiology and molecular methods
- Processing:
  - Samples diluted and plated on TBX (E. coli indicator) with and without antibiotics (e.g., tetracycline, amoxicillin, ciprofloxacin, cephalexin).
  - Count blue colonies indicating E. coli.
  - Up to five E. coli isolates per sample on cephalexin TBX plate transferred to CTX-TBX agar to screen for cefotaxime resistance.
- Resistance testing:
  - CLR/CTX-R isolates screened via multiplex PCR for β-lactamase genes (blaCTX-M groups).
  - AmpC hyperexpression detected via additional methods (details pending lab confirmation).
- Reference method: Schubert et al. (cited).

## Data cleaning and preparation
- Data merged from multiple sources; cleaned for consistency.
- Multiple-choice responses condensed (e.g., water trough cleaning frequency standardized to daily or less often).
- Derived variables created (binary indicators from categorical variables; aggregated farm-level indicators).

## Key variables and data structure
- Sample-level:
  - sample_id, farm, visit_number, date_collected, location/type (adult, dry, calf, footpath, etc.), animals_present (adult/dry/heifers/pw calves), presence of weaned calves, presence of adults, footpath flag.
  - ctx_m (CTX-M detected), antibiotic resistance indicators (amp_c, ct_pos, cipR, tetR, cephR, strepR, amoxR, etc.).
  - plain_undiluted (E. coli count on non-antibiotic agar), other derived metrics (anything_waste, heifers_waste).
  - management-related indicators (whichclinresp, firstmastitis, poultry/equine presence, total_cattle, yield, herd_size, bought_pre, scc, pneum_vacc, diarrvacc, anticocc, halocur, nsaiddiarr, trough_clean, time_dam, um_spray, give_col, wean, pattern, calving_group, calf_housing_type, calf_housing_older, hectares, othergraze, various vaccination statuses, housing and equipment variables, water source).
- Farm-level:
  - Total cattle, milk yield categories, herd size, pasture and housing details, antibiotic usage summary (total_mg_pcu, ceph_3_4, ceph_1, co_amox, tet, amox, fq, novobiocin, pen, cefalexin, strep; ranges provided).
  - Calving and calving management (calving_now, calving_group, calving pattern), housing/workflow (premises, shows, market, hostfarmwalk).
  - Slurry and manure management (manure_*), water access (water).

## Reference and related work
- Primary reference: Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology. 2021; 87: e01468-20.

## Practical considerations for Data Support use
- Opportunities:
  - Integrate farm management with resistance and antibiotic usage data to explore drivers of AMR in dairy settings.
  - Create self-serve dashboards linking mg/PCU with resistance markers (CTX-M presence, AmpC) across farm types and environments.
  - Cross-tab analyses of management practices (e.g., calf housing, trough cleaning, colostrum practices) with resistance outcomes.
- Challenges and cautions:
  - Convenience sample may limit generalizability to all UK dairy farms.
  - Some laboratory variables are pending (e.g., AmpC assay details), and certain PCR targets may be incomplete.
  - Data are longitudinal but span 2017-2019; interpret in the context of temporal changes in farming practices and antibiotic guidelines.
- Data use considerations:
  - Data are a cleaned, merged version of farm demographics, sampling, lab results, and prescriptions, suitable for exploratory analyses and dashboard development.
  - Alignment with Schubert et al. methodology for comparability with published results.
# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018..

- Study context
  - OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol
  - Funded by the Antimicrobial Resistance Cross Council Initiative; supported by seven UK research councils
  - Data collected on 51 dairy farms in South-West England during 2017–2018; samples and data merged from multiple sources

- Data sources and dataset composition
  - Farm demographic and management data from farmer questionnaires
  - Data recorded at the time of each calf sample collection
  - Laboratory results for E. coli resistance to selected antibiotics and genetic analysis of isolates
  - Veterinary practice and on-farm prescription records
  - Dataset is a cleaned, merged version from these four sources

- Study population and recruitment
  - Convenience sample of 53 dairy farms; 51 had pre-weaned calves during the study
  - Farms broadly comparable to UK farms (median herd size, milk yield, somatic cell count, and 2016 antibiotic usage mg/PCU)

- Sampling framework and laboratory methods
  - Monthly farm visits (Jan 2017–Dec 2018)
  - Sample type: fecal/environmental samples from pre-weaned calves using sterile overshoes or direct collection
  - Microbiology workflow:
    - Samples refrigerated, suspended in PBS, stored with glycerol at -80°C
    - TBX agar used to detect E. coli; antibiotic-supplemented TBX plates (tetracycline, amoxicillin, ciprofloxacin, streptomycin, cephalexin) for resistance screening
    - Up to five E. coli isolates from cephalexin TBX plates tested on cefotaxime (CTX) TBX to assess CTX resistance
    - CTX-resistant isolates screened by multiplex PCR for β-lactamase genes (blaCTX-M groups)
  - Data interpretation follows the methods described by Schubert et al. (2021)

- Data cleaning and variable structure
  - Multi-response questions condensed (e.g., water trough cleaning frequency)
  - Derived binary variables created from categorical responses
  - Variables cover sample and farm identifiers, collection dates, resistance phenotypes, and a wide range of farm management and antibiotic usage metrics

- Key variables and descriptions (highlights)
  - Sample and farm identifiers: sample_id, farm, visit_number, date_collected
  - Resistance and gene markers: ctx_m (CTX-M detected), amp_c (Amp-C detected), ct_pos (cefotaxime resistance), amoxR, tetR, cephR, strepR, cipR
  - Quantitative microbiology: plain_undiluted (total E. coli count)
  - Farm management and practices: anything_waste, heifers_waste, pneum_vacc, diarrvacc, trough_clean, give_col, wean, calving_group, calf_housing_type, water source, time_dam, um_spray, etc.
  - Antibiotic usage (mg/PCU) by antibiotic class and specific drugs (ceph_3_4, ceph_1, co_amox, amox, fq, novobiocin, pen, cefalexin, strep)
  - Herd and production metrics: total_cattle, yield (305-day milk yield), herd_size, bought_pre
  - Dry cow and six-month usage indicators: cefq_dct_6m, ceph_dct_6m, clox_dct_6m, fram_dct_6m
  - Other management details: calving_group (group vs. individual), calf_housing_older (presence of older animals nearby), water source details

- Analytical implications for data-driven questions
  - Enables exploration of correlations between antibiotic usage patterns and presence of resistant E. coli
  - Allows assessment of management practices (housing, calving, weaning, vaccination, water trough hygiene) as potential predictors of resistance
  - Supports modeling of temporal patterns across visits and farms, with linkage between on-farm prescriptions and resistance findings

- Limitations and context for interpretation
  - Convenience sampling limits generalizability beyond the study set
  - Complex, multi-source dataset requiring careful harmonization and consideration of missing data
  - Local-scale focus (South-West England); applicability to broader UK or international settings may be limited

- Reference to methodology
  - Data and methodology described in Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20

- Overall aim alignment
  - The dataset is designed to support analysis of correlations between farm practices, antibiotic usage, and antibiotic-resistant E. coli in pre-weaned calves, with potential to inform interventions and policy decisions in antimicrobial resistance surveillance and farm management.
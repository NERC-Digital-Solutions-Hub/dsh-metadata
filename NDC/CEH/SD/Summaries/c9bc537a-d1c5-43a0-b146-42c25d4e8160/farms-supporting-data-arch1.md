# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019

## Overview
- Dataset from OH-STAR project (University of Bristol) on antibiotic use and antibiotic-resistant E. coli in 53 dairy farms in South-West England, 2017–2019.
- Cleaned, merged dataset from multiple sources covering farm demographics, management data, sampling data, lab results, and prescription records.
- Aimed at analyzing correlations between management/antibiotic use and antimicrobial resistance patterns; provides a basis for modeling and inference on likely impacts of actions.

## Data sources and content
- Farm demographic and management data from farmer questionnaires.
- Per-sample data collected at the time of sampling.
- Microbiology results, including screening for E. coli resistant to specified antibiotics and genetic analysis of selected isolates.
- Veterinary prescription records and farm records for antibiotic usage.

## Recruitment and comparability
- Convenience sample of 53 dairy farms recruited via personal contacts, local veterinary practices, and milk processors.
- Farms broadly comparable to UK baselines (e.g., median herd size, milk yield, somatic cell count).
- Antibiotic usage quantified as mg/PCU (population corrected unit) per EU guidelines; herd size and other metrics derived accordingly.

## Farm demographics and management data collection
- Four questionnaires administered across the study (enrolment and approximately 6–9, 12–16 months, and near final visit).
- Data included both consent/sampling timing and follow-up management information, with responses combined to reduce burden.

## Farm-level antibiotic usage data
- Antibiotic quantity calculated from veterinary practice records (51 farms) and on-farm data (2 farms) for at least one year pre-enrolment through project end.
- Data validated for consistent product naming and quantification.
- Metrics standardized to mg/PCU; dairy cattle counts averaged over the study period.

## Sample collection (sampling design and types)
- Monthly farm visits (Jan 2017–Dec 2018).
- Sample types (with counts where provided):
  - Adult milking cow environment (collecting yard, housing, or field): 1963 samples from 52 farms.
  - Dry cow environment: 321 samples from 46 farms.
  - Replacement dairy heifers: longitudinal sampling of ~10 heifers per farm from birth to 18 months.
  - Pre-weaned calves (young calves still drinking milk): environment samples.
  - Footpaths/rights of way crossing farms: 547 samples from 40 farms.
- Sampling executed with sterile methods; standardized storage and transport to microbiology facilities.

## Microbiology methods
- Samples processed after refrigeration; suspension in PBS and incorporation into glycerol for storage at -80°C.
- TBX agar used to enumerate total E. coli and screened against antibiotics (including control and antibiotic-containing plates).
- Up to five E. coli isolates per CTX (cefotaxime) plate transferred to CTX-TBX for resistance testing.
- Resistance genes screened by multiplex PCR (β-lactamase genes, specifically blaCTX-M groups); AmpC hyperexpression detection described (lab details partially pending).
- Methodology aligned with Schubert et al. (reference provided).

## Data cleaning and variable construction
- Condensed multiple-choice responses to simplify interpretation (e.g., water trough cleaning frequency).
- Derived variables created (e.g., binary indicators from categorical variables, standardised encodings).
- Comprehensive variable descriptions provided, including:
  - Sample-level variables (sample_id, date_collected, ct_pos, ctx_m, resistance phenotypes like amoxR, cephR, cipR, tetR, etc.; plain_undiluted E. coli counts; presence of animals in sampled environment).
  - Farm-level variables (household practices, housing, welfare, vaccination, calving practices, stocking, forage types, manure management, milking practices, biosecurity, external contacts, etc.).
  - Management and production indicators (herd_size, yield, total_mg_pcu, percentdryoff, calving_group, housing type, feed sourcing, etc.).
- The dataset includes a wide range of binary, ordinal, categorical, and continuous variables capturing management, health, and antimicrobial use context.

## Data characteristics and usefulness
- Rich longitudinal design enabling analysis of correlations between antibiotic usage patterns, farm management practices, and presence of antimicrobial resistance determinants in E. coli.
- Enables descriptive summaries (e.g., prevalence of resistance genes, resistance phenotypes by farm/period) and modeling (e.g., predictors of CTX-M carriage, impact of dry cow therapy, antibiotic choices for mastitis).
- Provides cross-sectional and time-series potential across multiple sampling sites (adult environment, dry cows, heifers, preweaned calves, and footpaths).

## References
- Primary methodology and context for the dataset: Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20.
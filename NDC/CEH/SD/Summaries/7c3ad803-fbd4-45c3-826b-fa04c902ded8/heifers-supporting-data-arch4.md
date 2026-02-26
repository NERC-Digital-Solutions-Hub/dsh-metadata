# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

- A longitudinal dataset from 37 dairy farms in South-West England (2018) focusing on farm management, antibiotic use, and antibiotic resistance in E. coli from individual heifers.
- Part of the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) funded by the Antimicrobial Resistance Cross Council Initiative.

## Data sources and composition

- Cleaned dataset merged from multiple sources:
  - Farm demographic data collected via farmer questionnaires.
  - Microbiology results from screening E. coli for antibiotic resistance and β-lactamase genes.
  - Genetic analysis of selected E. coli isolates.
  - Prescription records from veterinary practices and farm records.
- Data include both farm-level and sample-level information with extensive metadata and derived variables.

## Recruitment and cohort

- Recruitment: convenience sample of 53 dairy farms via personal contacts, local veterinary practices, and milk processors.
- Cohort: on 37 farms, a set of heifers was followed from birth to 18 months or first pregnancy; not all farms raised heifers.
- Farm-level context: farms in the dataset are broadly comparable to UK farms (e.g., median herd size, milk yield, and somatic cell count proximate to national medians; 2016 antibiotic usage around 21–26 mg/PCU for UK dairy).
- Data availability: farm-level data for all recruited farms available at the CEH catalogue (link provided in documentation).

## Data collection and antibiotic usage

- Farm-level antibiotic usage:
  - Calculated from veterinary practice records for 51 farms and on-farm records for the remaining 2 farms.
  - Data spanned at least one year before enrolment to project end.
  - Usage quantified as mg/PCU (per European Surveillance of Veterinary Antimicrobial Consumption method).
  - Animal counts used to compute mg/PCU based on average herd size over the sampling period.
- Sample collection timing:
  - Samples collected from individual heifers during 2018, mostly during routine pregnancy diagnosis.
  - Fresh gloves used per animal; gloves collected when pregnancy checks occurred.
  - When pregnancy checks were not conducted, fresh faecal samples were collected by researchers.

## Microbiology and laboratory methods

- Sample processing and storage:
  - Samples refrigerated from collection to processing; stored at -80°C after glycerol stabilization.
- E. coli isolation and resistance testing:
  - TBX agar used to enumerate E. coli; specific antibiotic-containing TBX plates for resistance screening (including cephalexin-containing plates).
  - Up to five E. coli isolates per cephalexin TBX plate transferred to cefotaxime (CTX) TBX agar to identify CTX-resistant strains.
- Genetic analysis:
  - Multiplex PCRs to screen for β-lactamase genes (blaCTX-M groups) in CTX-resistant E. coli.
  - Hyperexpression of AmpC determined when no β-lactamase genes detected; independent checks confirm hyperexpression in those isolates.
- Methodology references:
  - Described as per Schubert et al. (2021).

## Data cleaning, coding, and derived variables

- Data harmonisation:
  - Condensed multiple-choice responses (e.g., water trough cleaning frequency) into standardized categories.
  - Created derived binary and continuous variables from categorical inputs (e.g., forage types, antibiotic resistance outcomes).
- Example variable structure:
  - Sample and farm identifiers (sample_id, farm) with descriptive coding.
  - Collection method (freshly voided vs rectal) with coded categories.
  - Antibiotic resistance indicators (amoxR, cephR, tetR) as binary flags.
  - Farm-level antibiotic usage metrics (total_mg_pcu) and antibiotic-class-specific usage (e.g., amox, ceph_3_4, tet, fq, pen, etc.).
  - Proportions of resistant environmental samples at various aggregation levels and time windows (e.g., farm_amoxR_pc_ex, heif_cephR_pc_ex, etc.), including short-term windows (1m, 2m, 3m, 4m) and pre-sampling periods (ex_3m, ex_1m, ex_2m, ex_4m).
- Data organization:
  - Clear separation of sample-level and farm-level data with consistent coding schemes to enable cross-linking and longitudinal analyses.

## Data availability and references

- Data availability note:
  - Farm-level data for all recruited farms available via the CEH catalogue (link provided in the dataset documentation).
- Reference for methodology:
  - Schubert H, Morley K, Puddy EF, et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated E. coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology. 2021;87:e01468-20.

## Relevance for Data Leaders

- Demonstrates end-to-end data integration across multiple sources (demographics, microbiology, prescription data) to build a longitudinal dataset.
- Highlights practical data governance considerations:
  - Provenance and merging of heterogeneous data sources with consistent naming conventions and derived variables.
  - Standardized usage metrics (mg/PCU) and careful handling of veterinary prescription data.
- Provides a rich, typified example of managing and quality-checking complex biological surveillance data at farm and sample levels.
- Illustrates challenges and mitigations relevant to data strategy:
  - Heterogeneity in data sources and product naming requiring careful standardization.
  - Longitudinal design with time-windowed exposure/outcome measures and derived epidemiological indicators.
  - Explicit documentation of laboratory methods, resistance definitions, and data cleaning steps to support reproducibility and reuse.
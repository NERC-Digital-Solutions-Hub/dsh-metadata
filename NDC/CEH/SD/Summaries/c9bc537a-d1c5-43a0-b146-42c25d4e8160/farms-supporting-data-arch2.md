# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019

## Overview
- Longitudinal dataset on antibiotic use and antibiotic-resistant E. coli from 53 dairy farms in South-West England (2017–2019).
- Part of OH-STAR (One Health Selection and Transmission of Antimicrobial Resistance) project at the University of Bristol, funded by the Antimicrobial Resistance Cross Council Initiative.
- Data are merged from farm demographics/management questionnaires, on-farm sampling data, laboratory results, and veterinary prescription records.

## Study scope, recruitment, and context
- Recruitment: convenience sample via personal contacts, local veterinary practices, and milk processors.
- Representativeness: farms comparable to UK averages (median herd size 193 vs 178; median 305-day yield 7488 L vs 8967 L; median SCC 167k vs 178k cells/mL).
- Antibiotic usage context: 2016 UK dairy antibiotic purchasing was 26 mg/PCU; study farms 21 mg/PCU.
- Sampling window: January 2017–December 2019; monthly farm visits (2017–2018).

## Data and data sources
- Merged dataset includes:
  - Farm demographics and management data from farmer questionnaires (4 time points).
  - Sample-level data collected at each sampling event.
  - Microbiology results from screening environmental and animal samples for E. coli resistance.
  - Genetic analysis of selected E. coli isolates (β-lactamase genes) and antibiotic resistance profiles.
  - Farm-level antibiotic prescription/sales data from veterinary practices and on-farm records.

## Sampling and microbiology
- Sample collection: monthly on 52 farms (one was a youngstock unit) with sterile methods; additional sampling for other herd groups and environments, including public footpaths.
  - Adult milking cow environment samples: ~1963 total.
  - Dry cow environment samples: ~321 total.
  - Replacement heifer environments: longitudinal sampling (~41 farms).
  - Pre-weaned calf environments: additional cohort sampling.
  - Footpath samples: ~547 total.
- Microbiology and resistance testing:
  - Samples processed and cultured on TBX media; antibiotic-containing and control media used to detect E. coli and resistance.
  - Up to five E. coli isolates per cephalexin TBX plate selected for further testing.
  - Cefotaxime (CTX) resistance tested; CTX-R isolates screened by multiplex PCR for blaCTX-M groups (β-lactamase genes).
  - AmpC hyperexpression screening performed (details pending lab reporting).
  - Methodology aligned with Schubert et al. (2021).

## Data management, cleaning, and structure
- Cleaning and harmonisation:
  - Condensed multiple-choice responses (e.g., water trough cleaning frequency).
  - Created derived variables (e.g., binary/ordinal variables for management practices and exposures).
- Metadata and variables:
  - Sample-level keys: sample_id, farm, visit_number, date_collected, ctx_m (CTX-M detected), antibiotic resistance flags (amp_c, ct_pos, cipR, tetR, cephR, strepR, amoxR), counts (plain_undiluted), and various location descriptors (adult/dry cattle, heifers, calves, footpath).
  - Farm-level variables cover housing, management practices, vaccination, calving, housing, water, waste/muck management, forage and feed, antibiotic usage indicators, biosecurity, and environmental interactions.
  - Data dictionary-style descriptions and coding schemes provided to support standard analysis.

## Antibiotic usage and resistance data
- Antibiotic usage quantified as mg/PCU (per European Surveillance of Veterinary Antimicrobial Consumption standard) using farm prescriptions and on-farm records; animal counts averaged over the study period.
- Environmental and animal sampling linked to antibiotic exposure and resistance outcomes (CTX resistance and β-lactamase gene carriage).

## Outputs, analyses, and environmental monitoring relevance
- Enables time-series and cross-sectional analyses of antibiotic use, management factors, and environmental reservoirs of resistant E. coli.
- Facilitates monitoring of environmental health indicators related to AMR in farm settings and the effectiveness of management practices.
- Provides a standardized data foundation suitable for reporting environmental health performance and policy impacts over time.

## Challenges and considerations for data use
- Convenience sample limits generalizability; comparisons to national UK metrics should be contextualised.
- Lab details for AmpC detection were awaiting final reporting, indicating potential gaps in resistance characterization.
- Large, highly detailed variable set requires careful data management and consistent definitions when combining with other datasets.

## References
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20.
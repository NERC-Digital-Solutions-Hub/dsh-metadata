# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for individual heifers on 37 dairy farms in the South-West of England in 2018

## Overview
- A data-rich descriptor from the OH-STAR project, collecting longitudinal information on antibiotic use and antibiotic-resistant E. coli in individual heifers across 37 dairy farms in South-West England during 2018.
- Dataset combines farm demographics, per-sample laboratory results, and veterinary prescription records to enable analysis of associations between management practices, antibiotic usage, and resistance patterns.

## Data sources
- Farm demographic data collected from farmer questionnaires.
- Per-sample microbiology results from screening for E. coli resistance to specified antibiotics and genetic analyses of selected isolates.
- Prescription data obtained from veterinary practices and farm records.
- Cleaned dataset merges these sources for analysis.

## Recruitment and sampling
- Convenience sampling of 53 dairy farms recruited via personal contacts, local veterinary practices, and milk processors.
- On 37 farms, a cohort of heifers was followed from birth to 18 months/first pregnancy; not all farms raised heifers.
- Farm-level data for all farms is available in the CEH catalogue.
- Compared farm characteristics to UK benchmarks (median herd size, milk yield, somatic cell count) to provide context for representativeness.
- Antibiotic purchasing usage metrics reference UK data from the European Surveillance of Veterinary Antimicrobial Consumption (mg/PCU).

## Data collection and laboratory methods
- Sample collection: during 2018, with emphasis on routine pregnancy diagnosis when possible; otherwise collected fresh fecal samples by researchers using gloves.
- Microbiology:
  - Samples refrigerated and processed, then cultured on TBX media to identify E. coli.
  - Antibiotic exposure tested by plating on TBX with/without antibiotics (including third/fourth-generation cephalosporins, amoxicillin, ciprofloxacin, streptomycin, cephalexin).
  - Up to five CTX-resistant E. coli isolates per cephalexin TBX plate moved to CTX-TBX for further testing.
  - β-lactamase gene screening via multiplex PCR to detect blaCTX-M groups; hyperexpression AmpC indicated when no β-lactamase genes were detected.
- Data handling: standardized naming and quantification across practices to harmonize product names and units.

## Data processing, variables, and metrics
- Antibiotic usage: calculated from farm veterinary practices and on-farm records; expressed as mg/PCU (per the European standardized metric). Animal counts on farms were averaged across the sampling period to derive population sizes for mg/PCU calculations.
- Derived variables: created from categorical data (e.g., forage type) and collapsed multi-option responses (e.g., water trough cleaning frequency into daily vs. less often).
- Sample and farm identifiers: standardized formats (e.g., sample_id, farm) with descriptive labels for analytical clarity.
- Example resistance variables:
  - amoxR, cephR, tetR: binary indicators of resistance to amoxicillin, cephalexin, and tetracycline in samples.
  - farm and heif_r*_pc_ex/in: proportions of resistant samples at farm level or within specific subgroups (environmental samples or heifer-derived samples) across the project period, with distinctions for exclude/include cases where E. coli was not found.
  - Time-windowed resistance metrics (e.g., 1m, 2m, 3m, 4m prior to sampling) to study temporal relationships between prior resistance prevalence and current isolates.

## Key variables (structure and coding)
- Core identifiers: sample_id, farm, heifer-level identifiers.
- Resistance indicators: amoxR, cephR, tetR (binary).
- Usage metrics: total_mg_pcu; additional breakdowns by antibiotic class (e.g., amox, cephalosporins, tet, fq).
- Derived farm/heifer resistance proportions: farm_amoxR_pc_ex/in, farm_cephR_pc_ex/in, farm_tetR_pc_ex/in, and similar metrics for heifer-level and three- or four-month windows prior to sampling.

## Access, provenance, and references
- Farm-level data for all enrolled farms accessible via the CEH catalogue (specific document link provided in the dataset description).
- Methodological references include Schubert et al. (2021) for AmpC hyperexpression interpretation.

## Potential analyses and uses
- Investigate associations between on-farm antibiotic usage (mg/PCU) and presence of resistant E. coli in heifers.
- Assess cross-farm variation in resistance prevalence and its relation to management practices captured in farm demographics.
- Examine temporal relationships between prior environmental resistances and current isolates using windowed prior-period metrics (1–4 months, 3 months prior for ex/out measures).
- Explore genotype-level resistance patterns (CTX-M groups) alongside phenotypic resistance data.
- Inform surveillance or intervention strategies in similar dairy-farming contexts.

## Limitations and challenges
- Convenience sample: possible biases and limited generalizability to wider UK dairy farms.
- Data scale and scope: 2018 data from a specific region; may not reflect current practices or regional differences elsewhere.
- Data integration challenges: harmonizing diverse data sources (farm records, lab results, prescriptions) requires careful curation and consistent nomenclature.
- Access and IT considerations: as with many such datasets, ensuring discoverability and interoperability of derived datasets is important for reuse.

## References
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20
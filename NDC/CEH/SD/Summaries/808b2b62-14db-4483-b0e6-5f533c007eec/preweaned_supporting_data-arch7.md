# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018..

- A cleaned, merged dataset from the OH-STAR project (One Health Selection and Transmission of Antimicrobial Resistance) at the University of Bristol, funded by the Antimicrobial Resistance Cross Council Initiative.
- Focuses on management data, sampling, laboratory results for antibiotic resistance in E. coli, and farm-level antibiotic prescription records from 51 dairy farms in South-West England (2017–2018).

## Data sources and structure

- Four embedded data streams:
  - Farm demographics and management data from farmer questionnaires.
  - Sample collection data (timing and context of each sample).
  - Microbiology results (E. coli presence, resistance markers, beta-lactamase genes).
  - Prescription/antibiotic usage records from veterinary practices and on-farm records.
- Data were cleaned and merged to form a single dataset suitable for analysis and visualization.

## Recruitment and sampling

- Convenience sample of 53 dairy farms; 51 farms had pre-weaned calves during the study.
- Farms were broadly comparable to UK dairy industry metrics (herd size, milk yield, somatic cell counts).
- Antibiotic purchasing metrics calculated as mg/PCU (European Surveillance of Veterinary Antimicrobial Consumption) for baseline context.

## Data collection and sampling timeline

- Farms visited monthly from January 2017 to December 2018.
- Samples collected from the faecally contaminated environments of pre-weaned calves (milk-fed) using sterile overshoes or direct collection from ground when access was limited.

## Microbiology workflow

- Samples refrigerated from collection to processing; prepared in PBS and glycerol, stored at -80°C.
- E. coli quantified on TBX agar with and without select antibiotics (tetracycline, amoxicillin, ciprofloxacin, streptomycin, cephalexin).
- Up to five E. coli isolates per cephalexin plate tested on CTX-TBX agar to identify cefotaxime resistance (CTX-R).
- Multiplex PCR to screen for blaCTX-M beta-lactamase gene groups in CTX-R isolates.
- Methodology aligned with Schubert et al. (2021).

## Data cleaning and derived variables

- Condensed multi-response questions (e.g., water trough cleaning frequency) into unified categories (e.g., daily vs. less often).
- Created derived variables (binary indicators) from categorical responses (e.g., antibiotic usage indicators).
- Standardized and documented variable definitions to support mapping and analysis.

## Variables and descriptions (highlights)

- Sample and farm identifiers:
  - sample_id: unique sample reference; farm: farm code; visit_number: visit sequence; date_collected.
- Microbiological outcomes (sample-level):
  - ctx_m: CTX-M detected in any isolates from the sample.
  - amp_c: AmpC detected by PCR.
  - ct_pos: cefotaxime resistance detected in the sample.
  - amoxR, tetR, cephR, strepR, cipR: resistance detected to amoxicillin, tetracycline, cephalexin, streptomycin, and ciprofloxacin, respectively.
  - plain_undiluted: total E. coli count in the sample.
  - other binary PCR-derived indicators for specific resistances.
- Farm management and demographics:
  - water source, trough cleaning frequency, dam time with calves, colostrum practices, vaccination regimes, housing type, calving group, weaning age, farm patterns.
  - herd_size, total_cattle, yield (305-day milk), scc (somatic cell count), bought_pre (cattle purchases in the prior year).
  - antibiotic usage indicators and detailed mg/PCU metrics by antibiotic class (e.g., cephalosporins, amoxicillin-clavulanic acid, tetracyclines, fluoroquinolones, penicillins, cefalexin, strep, novobiocin, etc.).
- Temporal and spatial context (potential for GIS mapping):
  - date_collected and visit_number enable temporal trend analysis.
  - farm identifiers can be linked to geographic locations for spatial visualization once geospatial coordinates are available.

## Antibiotic usage and resistance metrics

- mg/PCU-based antibiotic usage metrics derived from veterinary practice records and on-farm data.
- Detailed per-antibiotic class usage (e.g., 1st/3rd-4th generation cephalosporins, tetracyclines, fluoroquinolones) preserved for correlational mapping with resistance patterns.
- Resistance outcomes include both gene-level (blaCTX-M groups) and phenotype-level (CTX-R, amoxR, tetR, etc.).

## Potential GIS applications

- Farm-level mapping of resistance prevalence and patterns across the 51 farms in South-West England.
- Spatial analysis of resistance markers (CTX-M presence, AmpC, CTX-R) in relation to farm demographics, antibiotic usage, and management practices.
- Temporal mapping of resistance emergence across monthly visits (2017–2018) to identify hotspots or trends.
- Integration with environmental or regional factors (e.g., farm density, vaccination programs, water sources) to examine spatial associations.

## Limitations and considerations

- Convenience sample; findings may not be fully generalizable to all UK dairy farms.
- Data are limited to pre-weaned calves in the South-West region during 2017–2018.
- Spatial analysis requires geolocation data for farms (coordinates or shapefiles) not provided in the dataset description.
- Temporal resolution is monthly sampling within the two-year window; longer-term trends would require extended data.

## References

- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87: e01468-20
# Management data and antibiotic resistant E. coli detected for pre-weaned calves on 51 dairy farms in the South-West of England during 2017-2018..

## Overview
- A dataset from the OH-STAR (One Health Selection and Transmission of Antimicrobial Resistance) project (University of Bristol) covering 2017–2018.
- Scope: 51 dairy farms in South-West England; pre-weaned calves; data collected from farm management, samples, lab results, and veterinary prescriptions.
- Purpose: support surveillance of management practices and antimicrobial resistance in Escherichia coli from calves.
- Data are cleaned and merged from multiple sources; methodology described and linked to Schubert et al. (2021).

## Data provenance and sources
- Merged from four main sources:
  - Farm demographic and management data from farmer questionnaires.
  - Data recorded at the time of sample collection.
  - Lab results for E. coli resistance and β-lactamase genes (blaCTX-M) via PCR.
  - Prescription records from veterinary practices and farm records.
- Dataset and methodology align with prior work (Schubert et al., 2021).

## Population and recruitment
- Recruitment: convenience sample of 53 dairy farms; 51 farms had pre-weaned calves during the study.
- Farm comparability to UK averages (median herd size, milk yield, somatic cell count, and antibiotic purchasing) noted to contextualize representativeness.
- Antibiotic usage quantified using mg/PCU (European Surveillance of Veterinary Antimicrobial Consumption).

## Data content and structure
- Data types:
  - Farm-level demographics and management variables (housing, vaccination, calving practices, water sources, waste milk use, etc.).
  - Sample-level data: visit timing, sampling method, date collected, and E. coli presence.
  - Laboratory results: CTX-M β-lactamase presence, AmpC, cefotaxime resistance, and other antibiotic resistances (amoxicillin, tetracycline, cephalexin, streptomycin, ciprofloxacin).
  - Molecular data: PCR-based detection of resistance genes.
  - Derived metrics: mg/PCU antibiotic usage by class, house-keeping counts (e.g., total cattle, herd size), and other categorical or continuous farm metrics.
- Variable descriptions include:
  - sample_id, farm, visit_number, date_collected.
  - Binary markers for resistance (ctx_m, amp_c, ct_pos, amoxR, tetR, cephR, strepR, cipR).
  - Many farm-level indicators (water trough cleaning, housing type, calf stay with dam, vaccination routines, weaning age, calving group, etc.).
  - Antibiotic usage metrics by drug class (mg/PCU) and specific drugs (amox, pen, tetracycline, fluoroquinolones, cephalosporins, etc.).
- Data dictionary style entries indicate coding (binary 1/0, ordinal categories, continuous measures) and the sampling framework (monthly visits, four-point questionnaire schedule).

## Data processing, cleaning, and quality assurance
- Data cleaning:
  - Condensed multiple-choice responses (e.g., water trough cleaning frequency consolidated to “daily” or “less often”).
  - Created derived binary variables from categorical responses.
- Standardization:
  - Harmonization of antibiotic product names and quantities to ensure consistent mg/PCU calculations.
- Laboratory methodology:
  - Samples processed via TBX agar with and without specific antibiotics; resistance definitions aligned with EUCAST thresholds.
  - Selection of up to five E. coli isolates per plate for further screening; blaCTX-M groups detected via multiplex PCR.
- Documentation:
  - Methodology and data structure align with the described prior work (Schubert et al., 2021).

## Metadata and documentation
- Comprehensive variable-level descriptions included to support reuse and reproducibility.
- Lab and sampling methods are explicitly described, enabling alignment with similar datasets.
- Reference to the primary methodological publication for context and replication.

## Governance, access, and reuse considerations
- Data governance aims mentioned (respect sharing limitations and have systems for updates), though explicit access terms are not stated in this document.
- Practical considerations for stewarding:
  - Maintain a detailed data dictionary and consistent coding across versions.
  - Link dataset to raw data sources and laboratory records.
  - Provide clear versioning and, if possible, data access controls or licensing information.
  - Ensure reproducibility of mg/PCU calculations and derived metrics.

## Use cases, limitations, and cautions
- Use cases:
  - Surveillance of antibiotic resistance patterns and associations with farm management and antibiotic usage.
  - Analyses exploring relationships between management practices and presence of resistant E. coli in calves.
- Limitations:
  - Convenience sample may affect generalizability to the broader UK dairy sector.
  - Temporal scope is 2017–2018; methods reflect that period.
  - Data rely on self-reported management data and on-farm records, which may introduce reporting biases.
- Methodological notes:
  - Results and interpretations should reference the underlying lab protocols and EUCAST-based resistance definitions.

## References
- Schubert H, Morley K, Puddy EF et al. Reduced Antibacterial Drug Resistance and bla CTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology 2021; 87 : e01468-20.
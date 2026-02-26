# Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

## Purpose and scope
- Investigates adaptive phenotypic plasticity in a bacterial pathogen by testing how Mycoplasma gallisepticum isolates (from epidemic periods) affect host infection dynamics and pathogen traits.
- Uses a unique repository of isolates to examine plasticity in replication and transmission in response to host defences, contributing to understanding pathogen–environment interactions.

## Data access and citation
- Available under the Open Government Licence.
- Access: https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d
- Primary citation for reuse: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

## Study design and ethics
- Subjects: Wild house finches captured in Arizona (AZ) and Alabama (AL); initial screening to confirm absence of prior infection.
- Ethics and approvals: IACUC at Auburn University (PRN 2015-2721) and ASU (15-1438R); institutional authorizations at Auburn (BUA 500) and Exeter ethics approval.
- Inoculation: Birds randomly inoculated with one of 56 M. gallisepticum isolates collected over epidemic years; isolates prepared and stored, then grown before inoculation.
- Housing: Inoculated birds housed in pairs (AZ birds); quarantine and transfer logistics described.
- Experimental stopping rule: Birds euthanized at 35 days post-inoculation per licensing.

## Data collected and measured outcomes
- Clinical phenotype
  - Eye lesion severity scored for each eye on a 0–5 scale at multiple time points (days 3, 6, 8, 14, 21, 25, 28, 34 post-inoculation).
  - Scoring performed blinded to treatment.
- Host condition
  - Body mass recorded at days −7, 0, 3, 8, 14, 21, 28, 34 post-inoculation.
- Pathogen detection and load
  - Pathogen clearance: detection of M. gallisepticum DNA in conjunctival and tracheal swabs at days 8, 14, 21, 28.
  - Quantitative pathogen load (MG load) recorded for days 8, 14, 21, 28.
  - Additional PCR data for non-infected birds across multiple days (2–35 days) to monitor environmental exposure or background signals.
- Molecular assays
  - qPCR conducted with Mgc110-F/R and Rag1 primers; Mgc110-JOE and Rag1-FAM probes; specific cycling conditions and reaction composition detailed.
  - Presence/absence and load measurements recorded as numeric or binary outcomes (e.g., MG_PCR_d8/d14/d21/d28, PCR_2t…PCR_35t for non-infected birds).

## Data structure and variables
- Core identifiers: Bird unique ID; Sex (f/m); Population of origin (AO = Auburn/Opelika; GT = Greater Tempe); Pathogen Year.
- Phenotypic measurements by day post-inoculation:
  - Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34.
  - Eye scores by day for right and left eyes (RE_score and LE_score across days: d3, d6, d8, d13, d14, d21, d25, d28, d34).
  - MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (MG DNA detection in inoculated birds).
  - Pload_d8, Pload_d14, Pload_d21, Pload_d28 (MG load in cells).
  - PCR_2t through PCR_35t (MG DNA detection in non-infected birds across days 2–35).
- Data completeness: N/A notes indicate missing measurements or assay failures; comprehensive variable list covers clinical, physiological, and molecular data.

## Data quality, provenance and usage notes
- Data collected under controlled experimental conditions with standardized protocols to enable cross-isolate and time-series comparisons.
- Protocols for antibody screening (SPA) and current infection verification (endpoint PCR) documented.
- Culture and isolation methods, growth media composition, and storage conditions described to support reproducibility of pathogen preparations.
- The dataset is designed for integration into environmental monitoring of pathogen dynamics, enabling broad comparisons across isolates, hosts, and time points.

## Repositories and references
- Data repository: NERC Environmental Information Data Centre (EIDC).
- Key references detailing background and methods:
  - Field and laboratory references on M. gallisepticum and house finch infections.
  - Protocols for eye lesion scoring and infection confirmation.
- Direct data citation provided in the data access section above.
# Supporting Information CHEMPOP Sparrowhawks SGARs

## Description of dataset
- Concentrations of second generation anticoagulant rodenticides (SGARs) in livers of Eurasian sparrowhawks found dead in Great Britain, 1995–2015.
- Includes bird age (adult/juvenile), sex, and location where found.

## Associated datasets and funding acknowledgement
- Collected, examined, and archived under the Predatory Bird Monitoring Scheme (PBMS), part of UK Centre for Ecology & Hydrology.
- Funding: Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.
- Contaminants and data analysis funded under the CHEMPOP project (NE/S000100/1).
- Author contributions span study concept, sampling, analysis, QA, and manuscript preparation.

## Author list and contributions
- Lee A. Walker: study concept, sample selection, manuscript preparation
- Richard K. Broughton: study concept, manuscript preparation
- Kate R. Searle: quality assurance
- Heather Carter: SGAR analysis
- M. Gloria Pereira: SGAR analysis, manuscript preparation
- Elaine D. Potter: bird necropsies and tissue sampling
- Darren Sleep: SGAR analysis

## Bird sampling
- Study period: 1995–2015; Sparrowhawk population in Britain had recovered from organochlorine pesticides by this time.
- Sample: 259 dead Sparrowhawks submitted by the public to PBMS.
- Demographics: 134 adults, 125 juveniles; 146 females, 113 males. Juveniles defined as birds hatched in the current or previous calendar year; adults are in their third calendar year or older.

## SGAR analysis
- Analytes: five UK-licensed SGARs — bromadiolone, difenacoum, brodifacoum, flocoumafen, difethialone.
- Sample processing: ~0.25 g liver dried, ground, extracted with chloroform:acetone (1:1), cleanup via size-exclusion chromatography and solid-phase extraction.
- Instrumentation: LCMS-MS with APCI in negative mode; data processed with Xcalibur.
- Method specifics: gradient elution with ammonium acetate in water/methanol; matrix-matched standards; batch analysis of 12 samples with blanks and spiked recovery standards.
- Performance: recoveries for spiked chicken liver ranged 68–110%; mean recoveries by compound: bromadiolone 82.9%, difenacoum 92.2%, flocoumafen 91.7%, brodifacoum 96.75%, difethialone 87.8%.
- Sensitivity: limits of detection (LoD) ~2.3 ng/g wet weight for all SGARs, except difethialone at 3.0 ng/g.
- Regionally grouped samples: Scotland (58), northern England (46), western England with Wales (65), eastern England (90).

## Regional grouping
- Four geographic regions intended to reflect differing land-use and Sparrowhawk dispersal patterns in Britain:
  - Scotland
  - Northern England
  - Western England with Wales
  - Eastern England

## Quality control
- Analyses performed in UKAS-accredited ISO 17025:2017 laboratories.
- Data quality checked by two or more people to identify anomalies.

## Data structure (availability)
- Data file: ChemPop_Sparrowhawks_SGARs.csv
- Columns include:
  - BIRD: unique bird identifier
  - REGION: geographic region found
  - AGE: juvenile or adult
  - SEX: female or male
  - Bromadiolone, Difenacoum, Brodifacoum, Difethialone, Flocoumafen: SGAR concentrations (ng/g wet weight)
  - Sum_SGAR: total SGAR concentration (ng/g wet weight)
  - Units: ng/g wet weight
- Year found is captured in the regional dataset and metadata for each entry.

## References
- Related literature and data sources cited, including PBMS, PBMS methodology, and prior Sparrowhawk and land-cover studies.
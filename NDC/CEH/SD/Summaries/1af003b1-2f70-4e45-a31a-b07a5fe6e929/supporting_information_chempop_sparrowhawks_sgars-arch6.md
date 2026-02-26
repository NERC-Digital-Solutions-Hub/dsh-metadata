# Supporting Information CHEMPOP Sparrowhawks SGARs

- Dataset documenting concentrations of second generation anticoagulant rodenticides (SGARs) in livers of Eurasian sparrowhawks (Accipiter nisus) found dead in Great Britain from 1995 to 2015.
- Includes demographic information (age and sex) and location where each bird was found.
- Associated with the Predatory Bird Monitoring Scheme (PBMS) and the CHEMPOP project.

## What the dataset contains

- Total of 259 sparrowhawks:
  - 134 adults and 125 juveniles
  - 146 females and 113 males
- SGARs measured (ng/g wet weight):
  - bromadiolone
  - difenacoum
  - brodifacoum
  - difethialone
  - flocoumafen
  - Sum_SGAR (sum of the five compounds)
- Each record includes region of discovery and year found, along with age and sex.

## Sampling and context

- Birds submitted by the public to PBMS during 1995–2015.
- Sparrowhawk population had recovered from earlier pesticide impacts by the mid-1990s.
- Ageing based on plumage/morphology; juveniles are from the current or previous calendar year; adults are third calendar year or older.
- Regional grouping into four areas to reflect potential differences in exposure: Scotland; northern England; western England with Wales; eastern England.

## SGAR analysis (methods and quality)

- Liver tissue processed from archived PBMS samples.
- Analytical workflow:
  - Extraction with chloroform:acetone (1:1), followed by cleanup via automated size-exclusion chromatography and solid-phase extraction.
  - Final analysis by LC-MS/MS with an APCI source in negative mode.
- Calibration and QA:
  - Matrix-matched standards; batch analysis of 12 samples with blank and spiked recovery controls.
  - Recovery ranges: bromadiolone 82.9%, difenacoum 92.2%, flocoumafen 91.7%, brodifacoum 96.75%, difethialone 87.8%.
  - Limits of detection (LoD): 2.3 ng/g for most compounds; 3.0 ng/g for difethialone.
- Instrumentation details: LC-MS/MS with Ultimate 3000 HPLC and Quantum Ultra TSQ mass spectrometer (APCI, negative polarity).

## Regional grouping

- Four geographic regions:
  - Scotland
  - Northern England
  - Western England with Wales
  - Eastern England
- Regions chosen to reflect Sparrowhawk dispersal and land-use exposure differences.

## Data quality and provenance

- Analyses conducted in UKAS-accredited laboratories (ISO 17025:2017).
- Datasets reviewed by at least two individuals to identify anomalies.
- Data and methods linked to established monitoring and contaminant programs.

## Data structure and file format

- Single CSV file: ChemPop_Sparrowhawks_SGARs.csv
- Column definitions:
  - BIRD: Bird identifier (numeric)
  - REGION: Geographic region in Britain in which the bird was found
  - AGE: General age category (juvenile or adult)
  - SEX: Sex of the bird (female or male)
  - Bromadiolone: Concentration in ng/g (wet weight)
  - Difenacoum: Concentration in ng/g
  - Brodifacoum: Concentration in ng/g
  - Difethialone: Concentration in ng/g
  - Flocoumafen: Concentration in ng/g
  - Sum_SGAR: Sum of the SGAR concentrations in ng/g
  - Units: Measurement units (ng/g wet weight)

## Metadata, access, and acknowledgments

- Data collection and analysis supported by:
  - Predatory Bird Monitoring Scheme (PBMS)
  - CHEMPOP project (NERC grant NE/S000100/1)
  - PBMS and associated institutions acknowledged in the study
- Funding acknowledgment: NERC grant NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability
- References and related datasets provided to contextualize methods and data quality

## Authors and contributions

- Lee A. Walker — study concept, sample selection, manuscript preparation
- Richard K. Broughton — study concept, manuscript preparation
- Kate R. Searle — quality assurance
- Heather Carter — SGAR analysis
- M. Gloria Pereira — SGAR analysis, manuscript preparation
- Elaine D. Potter — bird necropsies and tissue sampling
- Darren Sleep — SGAR analysis
# Supporting Information CHEMPOP Sparrowhawks SGARs

- Concentrations of five second generation anticoagulant rodenticides (SGARs) in livers from Eurasian sparrowhawks (Accipiter nisus) found dead in Great Britain, 1995–2015; includes bird age, sex, and location.

## Data sources, purpose, and funding
- Collected under the Predatory Bird Monitoring Scheme (PBMS), part of the UK Centre for Ecology & Hydrology’s long-term contaminant monitoring.
- Analyzed within the CHEMPOP project (NERC grant NE/S000100/1) and supported by UK-SCAPE/NERC awards (NE/R016429/1).
- Aimed at monitoring environmental contamination by SGARs to inform policy and future decision-making.

## Authors and contributions
- Lee A. Walker: study concept, sample selection, manuscript preparation
- Richard K. Broughton: study concept, manuscript preparation
- Kate R. Searle: quality assurance
- Heather Carter: SGAR analysis
- M. Gloria Pereira: SGAR analysis, manuscript preparation
- Elaine D. Potter: bird necropsies and tissue sampling
- Darren Sleep: SGAR analysis

## Bird sampling
- Timeframe: 1995–2015; 259 dead Sparrowhawks submitted by the public to PBMS.
- Demographics: 134 adults, 125 juveniles; 146 females, 113 males. Juveniles defined as birds hatched in the current or previous calendar year; adults as third calendar year or older.
- Rationale: Sparrowhawk population recovery from organochlorine pesticides during the study period.

## SGAR analysis (analytical methods)
- Target compounds: bromadiolone, difenacoum, brodifacoum, difethialone, flocoumafen.
- Sample processing: ~0.25 g liver ground and extracted with chloroform:acetone (1:1); cleanup via size-exclusion chromatography and solid-phase extraction; final reconstitution in LCMS-MS mobile phase.
- Instrumentation: LC-MS/MS (Ultimate 3000 HPLC with TSQ Quantum Ultra mass spectrometer; APCI negative mode) with Xcalibur software.
- Quality controls: matrix-matched standards; batches of 12 with blanks and spiked recovery standards (chicken liver); recoveries ranged 68–110% (compound-specific means: bromadiolone 82.9%, difenacoum 92.2%, flocoumafen 91.7%, brodifacoum 96.75%, difethialone 87.8%); limits of detection (LoD) 2.3 ng/g wet weight (2–3 ng/g for difethialone).
- Outcome: Quantified concentrations of each SGAR in liver tissue.

## Regional grouping and geography
- Four geographic regions in Britain: Scotland (58 birds), northern England (46), western England with Wales (65), eastern England (90).
- Purpose: to reflect potential differences in SGAR exposure related to land use and sparrowhawk dispersal distances.

## Data quality, governance, and structure
- Quality control: UKAS-accredited laboratories (ISO 17025:2017); datasets reviewed by at least two people to identify anomalies.
- Data structure: single CSV file (ChemPop_Sparrowhawks_SGARs.csv) containing:
  - BIRD identifier
  - REGION (geographic region found)
  - AGE (juvenile or adult)
  - SEX (male or female)
  - Bromadiolone, Difenacoum, Brodifacoum, Difethialone, Flocoumafen concentrations (ng/g wet weight)
  - Sum_SGAR (sum of SGAR concentrations; ng/g wet weight)
  - Units and Year found
- Data provenance and sharing: dataset maintained with metadata; underlying data generated under established monitoring schemes and funded projects.

## References and context
- Includes methodological and contextual references for PBMS, SGARs, and sparrowhawk ecology and monitoring frameworks.
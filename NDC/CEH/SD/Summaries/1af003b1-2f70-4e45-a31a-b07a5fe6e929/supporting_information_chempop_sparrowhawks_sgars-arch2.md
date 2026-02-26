# Supporting Information CHEMPOP Sparrowhawks SGARs

## Overview
- Description of dataset: concentrations of second generation anticoagulant rodenticides (SGARs) in livers of Eurasian sparrowhawks found dead in Great Britain (GB) from 1995 to 2015.
- Includes demographic data (age, sex) and location of finding.

## Dataset content and scope
- Number of birds: 259 dead sparrowhawks submitted via the Predatory Bird Monitoring Scheme (PBMS).
- Demographics: 134 adults / 125 juveniles; 146 females / 113 males.
- Geographic regions: Scotland (58), northern England (46), western England with Wales (65), eastern England (90).
- SGARs measured: bromadiolone, difenacoum, brodifacoum, difethialone, flocoumafen.
- Output metric: Sum_SGAR (total SGAR concentration per liver); units are ng/g wet weight.

## Sampling, analysis and methods
- PBMS sampling context: long-term contaminant monitoring of avian predators; carcasses sexed and aged by plumage/m morphology.
- Tissue processing: ~0.25 g liver, dried and ground; solvent extraction (chloroform:acetone), centrifugation, repeat extraction; combined extracts.
- Cleanup: automated size exclusion chromatography; solid-phase extraction.
- Instrumentation: LC-MS-MS (Ultimate 3000 HPLC + Quantum Ultra TSQ) with APCI negative mode; Xcalibur software.
- Mobile phases and gradient: ammonium acetate in water/methanol with defined gradient program.
- Calibration and QA: matrix-matched standards; spiked recovery standards (chicken liver); recoveries 68–110% across compounds.
- Detection limits: 2.3 ng/g ww for all SGARs, except difethialone at 3.0 ng/g ww.

## Quality assurance and data integrity
- Laboratories: UKAS-accredited ISO 17025:2017.
- Data validation: datasets assessed by two or more individuals to identify anomalies.

## Data structure and accessibility
- Data file: ChemPop_Sparrowhawks_SGARs.csv.
- Key columns: Bird ID; Region; Year found (YYYY); Age; Sex; Bromadiolone; Difenacoum; Brodifacoum; Difethialone; Flocoumafen; Sum_SGAR; Units.
- Units: ng/g wet weight for SGAR concentrations and Sum_SGAR.

## Regional grouping rationale
- Four geographic regions designed to reflect Sparrowhawk dispersal and land-use exposure differences: Scotland; northern England; western England with Wales; eastern England.

## Associated data, funding and collaboration
- Data collection: Predatory Bird Monitoring Scheme (PBMS).
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 as part of UK-SCAPE; CHEMPOP project (NE/S000100/1).
- Author contributions: study concept, sampling, SGAR analysis, QA, manuscript preparation.

## Context and implications for monitoring
- Context: Sparrowhawk population had recovered by 1995–2015 after organochlorine pesticide impacts in the mid-20th century.
- Purpose: provides standardized, QA'd SGAR exposure data for environmental health monitoring and policy assessment, with emphasis on data accessibility and comparability.

## References (illustrative)
- Baker 2016; Morton et al. 2014; Newton 1986; Newton & Wyllie 1992; Shore et al. 2005; Walker & Newton 1998 (and related PBMS and CHEMPOP references).
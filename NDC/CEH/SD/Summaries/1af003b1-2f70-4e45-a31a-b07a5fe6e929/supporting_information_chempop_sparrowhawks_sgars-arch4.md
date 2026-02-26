# Supporting Information CHEMPOP Sparrowhawks SGARs

## Overview
- Dataset of concentrations of second generation anticoagulant rodenticides (SGARs) in livers of Eurasian sparrowhawks found dead in Great Britain, 1995–2015.
- Includes bird demographic data (age and sex) and the location where each bird was found.
- Part of CHEMPOP project and UK-SCAPE programme; funding from NERC.
- Data collected under the Predatory Bird Monitoring Scheme (PBMS); long-term archival by PBMS.

## Sampling and dataset scope
- Sample: 259 dead Sparrowhawks submitted by the public to PBMS.
- Demographics: 134 adults, 125 juveniles; 146 females, 113 males.
- Time frame: 1995–2015 (period used to contextualise Sparrowhawk population recovery after pesticide-related declines).
- Geographic grouping: four regions in Britain for exposure assessment - Scotland, northern England, western England with Wales, and eastern England.
- Purpose: assess SGAR exposure in Sparrowhawks and provide data for contaminant monitoring and risk assessment.

## SGAR analysis methods
- Target compounds: bromadiolone, bromadiacone? (bromadiolone), difenacoum, brodifacoum, difethialone, flocoumafen (five SGARs analyzed).
- Sample preparation: ~0.25 g liver, dried and ground; extraction with chloroform:acetone (1:1); cleanup via automated size exclusion chromatography and solid-phase extraction; final reconstituted in LCMS-MS mobile phase.
- Instrumentation: LC-MS/MS with Ultimate 3000 HPLC and Thermo TSQ Quantum Ultra TSQ; APCI negative mode; Xcalibur software.
- Quantification: matrix-matched standards; recoveries 68–110% across compounds; mean recoveries per compound ~ bromadiolone 82.9%, difenacoum 92.2%, flocoumafen 91.7%, brodifacoum 96.75%, difethialone 87.8%.
- Sensitivity: limits of detection (LoD) 2.3 ng/g wet weight for all compounds except difethialone at 3.0 ng/g.
- Quality control: samples analyzed in UKAS-accredited ISO 17025:2017 labs; data validated by two or more people; batch QA included blanks and spiked recovery standards.

## Data structure and accessibility
- Data file: ChemPop_Sparrowhawks_SGARs.csv (single CSV).
- Columns (example structure):
  - BIRD: bird identifier
  - REGION: geographical region (Scotland, northern England, western England with Wales, eastern England)
  - Year found: year bird was found
  - AGE: juvenile or adult
  - SEX: female or male
  - Bromadiolone: concentration (ng/g wet weight)
  - Difenacoum: concentration (ng/g ww)
  - Brodifacoum: concentration (ng/g ww)
  - Difethialone: concentration (ng/g ww)
  - Flocoumafen: concentration (ng/g ww)
  - Sum_SGAR: sum of SGAR concentrations (ng/g ww)
  - Units: ng/g wet weight
- Data structure notes: includes region-specific grouping to reflect potential exposure differences; year, age, sex, and all compound concentrations are recorded per bird.

## Provenance, governance, and funding
- Sample collection and archiving: PBMS; long-term storage by PBMS.
- Data analysis and project: CHEMPOP; part of UK-SCAPE National Capability.
- Funding: Natural Environment Research Council (NERC) award NE/S000100/1; PBMS and CHEMPOP collaboration.
- Authors: Lee A. Walker (concept, sample selection, manuscript), Richard K. Broughton (concept, manuscript), Kate R. Searle (QA), Heather Carter (SGAR analysis), M. Gloria Pereira (SGAR analysis, manuscript), Elaine D. Potter (necropsies and tissue sampling), Darren Sleep (SGAR analysis).

## Usage, limitations, and context
- Enables assessment of temporal and spatial patterns of SGAR exposure in Sparrowhawks and supports broader contaminant monitoring efforts.
- Regional grouping aids interpretation of land-use-related exposure differences.
- Limitations: reliance on birds submitted by the public (potential sampling bias); SGAR detection and recovery rates may influence concentration estimates; LoD varies slightly between compounds.
- Data is suitable for informing ecological risk assessments, trends over time, and cross-project data integration within wildlife contaminant research.

## References and related information
- Associated references for background and methodology include works on Sparrowhawk recovery, PBMS framework, and SGAR analytical methods (e.g., Baker 2016; Newton & Wyllie; Shore et al.; Walker & Newton).
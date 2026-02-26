# Supporting Information CHEMPOP Sparrowhawks SGARs

## Overview
- Describes concentrations of second generation anticoagulant rodenticides (SGARs) in Eurasian sparrowhawk livers found dead in Great Britain from 1995 to 2015.
- Includes bird demographics (age and sex) and the location where each bird was found.

## Context and Funding
- Data collected under the Predatory Bird Monitoring Scheme (PBMS) and UK-SCAPE National Capability.
- Contaminants and data analysis conducted under the CHEMPOP project (NERC grants NE/S000100/1 and related support).

## Sampling and Population
- 259 Sparrowhawks available for study; birds submitted by the public to PBMS.
- Demographic breakdown: 134 adults, 125 juveniles; 146 females, 113 males.
- Juvenile definition: hatched in the current or previous calendar year; adults: third calendar year or older.
- PBMS provides long-term contaminant monitoring for avian predators.

## SGAR Analysis Methods
- Analyzed five SGARs licensed for UK use: bromadiolone, difenacoum, brodifacoum, difethialone, flocoumafen.
- Laboratory workflow: liver ~0.25 g dried and ground; solvent extraction; automated size-exclusion chromatography cleanup; solid-phase extraction; LC-MS/MS analysis (APCI, negative mode).
- Quantification: matrix-matched standards; batch analysis with chicken liver blanks and spiked recoveries.
- Performance: recovery ranges ~69–111% across compounds; limit of detection (LoD) 2.3 ng/g wet weight for all except difethialone at 3.0 ng/g.

## Regional Grouping
- Four geographic regions in Britain to reflect potential exposure differences and Sparrowhawk dispersal:
  - Scotland
  - Northern England
  - Western England with Wales
  - Eastern England
- Region-based grouping helps account for varying land use and SGAR exposure.

## Data Quality and Standards
- Analyses conducted in UKAS-accredited laboratories (ISO 17025:2017).
- Datasets quality-assessed by at least two individuals to identify anomalies.

## Data Structure and Format
- Single CSV file: ChemPop_Sparrowhawks_SGARs.csv.
- Key columns (example contents):
  - BIRD: Bird identifier
  - REGION: Region found (geography) and year found (YYYY)
  - AGE: Juvenile or Adult (year of finding)
  - SEX: Female or Male (year of finding)
  - Bromadiolone, Difenacoum, Brodifacoum, Difethialone, Flocoumafen: SGAR concentrations (ng/g wet weight)
  - Sum_SGAR: Sum of SGAR concentrations (ng/g wet weight)
  - Units: ng/g wet weight
- Data provide region-level spatial context (not precise coordinates) suitable for regional mapping and aggregation.

## Practical GIS Use and Considerations
- Ideal for creating region-based maps of SGAR exposure across Britain and temporal trends by year.
- Can be joined with regional land-cover data to explore associations between exposure and land use.
- Useful for identifying regional hotspots and informing wildlife health assessments or policy discussions.
- Consider limitations: samples represent birds found dead (potential sampling bias) and geographic resolution is regional rather than precise point locations.

## Limitations and Considerations
- Spatial resolution limited to four regions; no fine-scale coordinates.
- Temporal span covers 1995–2015; potential changes in SGAR usage and regulations over time.
- Data reflect exposure in sparrowhawks that died (not necessarily habitat-wide exposure).

## References
- Supporting literature and methodological references included in the document (e.g., prior PBMS reports and related ecological and methodological studies).
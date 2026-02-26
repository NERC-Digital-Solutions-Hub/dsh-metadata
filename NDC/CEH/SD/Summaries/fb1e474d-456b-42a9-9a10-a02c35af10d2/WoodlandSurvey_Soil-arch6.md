# Woodlands Survey soil data 1971-2001

## Overview
- A long-term soil data resource from 103 broadleaved woodlands across Britain, surveyed in 1971 with detailed plot-level data and revisited over the growing seasons of 2000, 2002, and 2003 (referred to as 2001).
- Data collected at site level and on 16 randomized 200 m² plots per site, including plant species information, soil pH, soil organic matter (SOM), habitat management, and other plot- and site-level descriptors.
- Analyses aimed to identify ecological changes over time and to estimate drivers of change (atmospheric S and N deposition, climate, canopy structure changes, woodland management).
- Key publications for methods and results: Kirby et al. (2005) and Corney et al. (2004). Users should consult these for detailed methods and analytical findings.

## Data collection design and provenance
- Survey design: Stratified sampling across the study area using Bunce & Shaw’s 1973 standardized survey methods; field handbook provided.
- Data originators (time of surveys): 1971 – Bunce & Shaw; 2001–2003 – Smart, Black, Kirby, Corney, and colleagues.
- Related datasets and context: Countryside Survey; historical and methodological references listed.

## Data structure and contents
- Primary data structure: Site and Plot metadata plus multiple measured variables per plot.
- Core fields (examples):
  - Site: numeric code (1–103)
  - Plot: numeric code (1–16)
  - pH1971, pH2003: soil pH in 1971 and in the 2000s
  - pH1971_QA_repeats: repeat pH measurements from 2000 on archived 1971 samples
  - SOM1971, SOM2003: soil organic matter percentage in 1971 and in the 2000s
  - SOM1971_QArepeats: repeat SOM measurements on archived samples
  - MSG: Major Soil Group code (Avery 1973)
  - SG: Soil Group code (Avery 1973)
  - SSG: Soil Sub-group code (Avery 1973)
  - Major_Soil_Group, Soil_Group, Soil_subgroup: textual descriptions of soil classifications
- Data types: numeric codes and descriptive text
- Coverage: site- and plot-level data with longitudinal measurements over the baseline and follow-up surveys

## Data usage and interpretation
- Intended use: Assess long-term ecological change in British woodlands; examine relationships between soil properties and environmental/management drivers.
- Analytical guidance: Refer to Kirby et al. (2005) and Corney et al. (2004) for detailed methods and results on drivers of change and spatial factors.
- Data products: Outputs suitable for dashboards, pivot-style analyses, or self-serve exploration of soil parameters across sites and time.

## Accessibility and references
- Data access: DOI link provided for the dataset (Woodlands Survey soil data 1971-2001).
- Related datasets: Countryside Survey and historical woodland surveys (e.g., Steele 1968).
- References for methods and context:
  - Avery, B.W. 1973. Soil Classification in the Soil Survey of England and Wales
  - Corney et al. 2004; Haines-Young et al. 2003; Kirby et al. 2005

## Origin and contact points
- Originators (time of surveys): 1971 – Bunce & Shaw; 2001–2003 – Smart, Black, Kirby, Corney, and colleagues at CEH and associated institutions.
- Institutional context: CEH Merlewood and CEH Lancaster, English Nature, University of Liverpool, among others.

## Key considerations for data support
- Quality assurance: pH and SOM repeats (QA repeats) are included for certain samples; data require careful alignment of 1971 baseline with 2000s resurvey metrics.
- Data harmonization: Uses standardized soil classification codes (MSG, SG, SSG) aligned with Avery (1973) classifications.
- Integration with external drivers: data designed to be combined with atmospheric deposition, climate, canopy structure, and management variables to model drivers of ecological change.
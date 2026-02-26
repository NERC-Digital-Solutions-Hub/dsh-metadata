# Soil bacterial cell counts and moisture content from a water stress experiment [NERC Soil Biodiversity Programme] -Supporting Information

## Background
- The NERC Soil Biodiversity Thematic Programme (established 1999) studied a large field experiment at Sourhope to understand soil biota diversity and their functional roles in key ecological processes.
- 24 projects investigated soil structure, soil processes (carbon and nitrogen cycles), and roles of microfauna, flora, meso- and macro-fauna.
- Primary aim of the bacterial component: monitor activity and diversity of soil bacterial communities in response to perturbation (drying and rewetting) and examine culture-dependent and culture-independent aspects of microbial function.

## Experimental set-up and sampling
- Location: Sourhope field site, unimproved grazed pasture with organic-rich brown forest soil (pH 4.5–5.0); dominant grasses Agrostis and Festuca.
- Method: intact grassland monoliths (~15 cm depth) placed in plastic pots (45 cm diameter) to standardize conditions; nine microcosms total (3 replicates × 3 treatments).
- Treatments: A – continual wetting, B – drying, C – drying and rewetting; duration July–October 2001.
- Sampling timeline: 11 time points (S1–S11); S1–S3 had natural rainfall, then rainfall exclusion started on 14 August; drying began after S3; rewetting on 18 September (approx. 1 month without water) with regimens matching treatment A.
- Procedures: four 1-cm-diameter cores per pot (to ~7 cm) pooled for analyses; samples processed to determine soil moisture and bacterial activity.
- Soil description: organic-rich soil with edge effects minimized; litter layer level with pot rim.

## Culturability and total cell count of bacterial community
- Culturable counts: soil (0.5 g wet weight) dispersed in PBS with glass beads, decimally diluted, plated on:
  - full-strength TSBA
  - 1/10-strength TSBA
  - pseudomonad-selective agar (PSA)
  - all media with cycloheximide to suppress fungi
- Incubation: 10 days at 18°C; colonies counted to determine culturability; biomass from plates used for nucleic acid extraction.
- Total cells: extracted from soil via Nycodenz density cushion; fixed with 1% paraformaldehyde; stained with SYBR Green II; counted by flow cytometry (FACSCalibur) after preparation.

## Data Structure
- Two CSV datasets:
  - Drought experiment. Microcosm culturable cell counts (P2136_Culturable_cells.csv)
    - Fields: MICROCOSM_ID, TREATMENT (wet/dry/rewet), SAMPLING_DATE, MEDIA_USED (psa, tsba, 1/10 tsba), CELL_COUNT (per gram dry weight soil)
  - Drought experiment. Microcosm moisture contents of soil samples (P2136_Microcosm_Soil_Moisture.csv)
    - Fields: MICROCOSM_ID, TREATMENT, SAMPLING_DATE, MOISTURE_CONTENT (%)
- Data notes: MICROCOSM_ID identifiers; dates as date type; media and treatment as text; counts as numeric; moisture as numeric.

## Related information and references
- Whiteley, A. S., Griffiths, R. I., & Bailey, M. J. (2003). Analysis of microbial functional diversity via flow cytometry and cell sorting.
- Griffiths, R. I., Whiteley, A. S., O'Donnell, A. G., & Bailey, M. J. (2003). Physiological and community responses of soil bacteria to water stress.
- Sourhope Field Data Handbook (2003) and related UK soil biodiversity literature for context and data handling.
- Access notes: Data cited are QA’d but not guaranteed by NERC; no liability for data use; data sharing may be subject to openness and governance constraints; data available via linked catalogues (e.g., EIDC).

## Site and data governance notes
- Site reference: Sourhope field site (grid NT8545019630).
- Soil type and conditions described to support interpretation of microbial responses to moisture perturbations.
- Data management: underlying datasets require metadata from originators; data sharing may face barriers and governance considerations.
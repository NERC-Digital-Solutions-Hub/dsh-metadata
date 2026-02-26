# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview
- Datasets from a Hedgerow management experiment (2006–2014) investigating the effects of hedgerow cutting timing and frequency on wildlife habitat, resource provision, and associated moth and parasitoid communities.
- Includes moth larva data and parasitoid associations, hedgerow architecture, foliar quality, and derived measurements.
- Related publication: Facey et al. 2014, Insect Conservation and Diversity.
- Funded by Defra (BD2114); managed by UKCEH; data later uploaded to an Oracle database after QA.

## Experimental design and scope
- Location: Monks Wood, Cambridgeshire, UK; hedgerows planted in 1961 on former arable land.
- Experimental setup: randomized factorial design with four hedgerows, 32 plots (15 m length) plus 2 unmanaged controls.
- Treatments (applied to plots in factorial combinations):
  - Cutting frequency: annual, biennial, triennial
  - Cutting timing: autumn or winter
  - A control (unmanaged)
- Years: 2005–2014 (data described from 2011 sampling); cutting conducted with tractor-mounted flail cutter; autumn cuts in Sep; winter cuts in Jan/Feb.
- Replication: 8 repeats for annual plots; 4 repeats for 2- and 3-year plots (per treatment combination).
- Experimental outputs measured: hawthorn flowering/berry production, hedgerow structure, and resource provisioning for wildlife.

## Data collection methods and content
- Moth sampling and rearing (2011):
  - Timed search and hedgerow beating to collect larvae.
  - Identification of adult moths from reared larvae; recording parasitism when parasitoids emerged.
  - Photographs of leaf mines for ID; rearing details and emergence records stored.
  - Data file: MResMothLarvaeParasitoids.csv (individual larvae, parasitoid records, sample metadata, emergence dates).
- Hedgerow architecture and resource availability:
  - Measurements of hedge height, width, branching density, and leaf biomass/biomass weight at multiple plot locations.
  - Methods include quadrats and range poles; leaf samples dried and weighed; branching metrics calculated.
  - Data files: MResDimensions.csv (height/width per replicate), MResLeaves.csv (leaves counts and dry weight), MResBranches.csv (total branches per quadrat), MResBranchTips.csv (branch tip measurements, growing and thorn tips).
- Foliar quality analysis:
  - Foliar carbon and nitrogen concentrations from leaves collected along plots; analyzed via dry combustion after freeze-drying and milling.
  - Data file: MResCN.csv (foliar C% and N% per plot/visit).
- Data columns and structure:
  - MResMothLarvaeParasitoids.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, COLLECTION_METHOD, SAMPLE_NO, MOTH_NAME, PARASITISED, PARASITOID, PARASITOID_FAMILY/SUBFAMILY, PARASITOID_NOTES, DATE_EMERGED.
  - MResDimensions.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, REPLICATE, HEIGHT, WIDTH.
  - MResLeaves.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, REPLICATE, LEAVES_COUNT, LEAF_SAMPLE_WEIGHT.
  - MResBranches.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, QUADRAT_NO, TOTAL_BRANCHES.
  - MResBranchTips.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, QUADRAT_NO, REPLICATE, BRANCH_LENGTH, GROWING_TIPS, GROWING_TIPS_2YEAR, GROWING_TIPS_3YEAR, THORN_TIPS_1YEAR, THORN_TIPS_2YEAR.
  - MResCN.csv includes: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, FOLIAR_C_PERCENT, R FOLIAR_N_PERCENT.
- Quality control:
  - Standard protocol followed; identifications verified by experts; data checked for anomalies; missing values attributed to survey error.
  - Post-upload QA performed on Oracle database.

## Data governance and stewardship considerations
- Standardized data schema across multiple related files to support interoperability and integration with other hedgerow/biodiversity datasets.
- Units and measurement protocols explicitly documented (e.g., heights in cm, biomass in grams, carbon/nitrogen percentages, branch lengths in cm).
- Clear treatment coding (1–13) with accompanying design description; ensure mapping between treatment codes and their definitions is maintained for reuse.
- Provenance and linkage to publications and funding: data derived from long-running Defra-funded experiments; publication enabling traceability of analyses.
- Site coordinates and site metadata provided (Monks Wood reference), enabling spatial analyses and data discovery.
- Data licensing, access conditions, and reuse rights are implied by repository practices; for stewardship, consider publishing a data usage license and DOI/landing page to improve findability and reusability.

## Usage and references
- Primary publication: Facey SL, Botham MS, Heard MS, Pywell RF, Staley JT (2014) Moth communities and agrienvironment schemes: Examining the effects of hedgerow cutting regime on diversity, abundance, and parasitism. Insect Conservation and Diversity, 7: 543-552. doi: 10.1111/icad.12077
- Experimental report underpinning design: Defra BD2114; related methodological notes in Defra report (2018) on hedgerow management effects on biodiversity.
- Data files provide a comprehensive dataset for analyses on hedgerow management, habitat quality, moth and parasitoid dynamics, and foliar resource relationships.

## Funding and governance
- Defra project BD2114; UK Centre for Ecology & Hydrology (UKCEH) management.
- Data publication and sharing aligned with Defra-funded long-running hedgerow experiments; dataset supports future biodiversity and land-management research.

## Stewardship recommendations
- Maintain a detailed data dictionary and data dictionary updates for any schema changes; ensure the treatment code mapping is preserved and accessible.
- Preserve site-level metadata (e.g., precise coordinates, plot layout, replicate design) for reproducibility and spatial analyses.
- Provide licensing and citation guidance to facilitate reuse; assign a DOI and a stable data repository landing page.
- Facilitate data discoverability by linking to related publications, reports, and project metadata.
- Consider exposing data quality flags and lineage notes in the metadata to assist data users in assessing reliability and context.
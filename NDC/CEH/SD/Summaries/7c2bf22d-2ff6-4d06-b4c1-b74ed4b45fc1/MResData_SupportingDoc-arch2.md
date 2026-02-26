# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview
- Dataset of hawthorn moth species, parasitoids, and associated hedgerow architecture/resource data from a long-running hedgerow experiment in Cambridgeshire, UK.
- Connected to the 2014 publication: Facey et al. Moth communities and agrienvironment schemes: Examining the effects of hedgerow cutting regime on diversity, abundance, and parasitism.
- Centered on Experiment 1 (2006–2014) assessing how cutting timing/frequency influences wildlife habitat quality, food resources, and potential restoration options under agri-environment schemes (ELS/HLS).

## Experimental design and scope
- Location: Monks Wood, Cambridgeshire (four hedgerows planted in 1961 on former arable land).
- Design: Randomised, factorial plot experiment (2005–2014) with cutting frequency (annual, biennial, triennial) and cutting timing (autumn, winter) plus unmanaged controls.
- Replication: Each treatment combination replicated across plots; annual plots had eight replicates, two- and three-year plots had four replicates.
- Objectives (Experiment 1): Long-term effects of cutting on hawthorn flowers, berry provision for overwintering wildlife, and hedge structure; evaluate low-cost restoration/management options.

## Data collected and variables
- Moth sampling and parasitism data (2011)
  - Methods: Timed search and hedgerow beating to collect moth larvae; rearing to determine parasitism; species-level identification where possible.
  - Variables: Moth species/larvae, emergence dates, parasitism status, parasitoid identity/family, sampling method, plot treatment, replicate, and sample metadata.
  - File: MResMothLarvaeParasitoids.csv (detailed metadata per sample).
- Hedge architecture and resource availability
  - Measurements: Hedge height, width, leaf abundance/biomass, branching density and structure (tips, nodes, branch lengths).
  - Timing: June measurements and multiple quadrat-based leaf/branch assessments per plot.
  - Files: MResDimensions.csv, MResLeaves.csv, MResBranches.csv, MResBranchTips.csv (per-plot, per-quadrat and replicate data).
- Foliar quality
  - Analysis: Foliar carbon and nitrogen concentration to probe links between moth metrics and leaf chemistry.
  - Sampling: Three growing tips/leaves per plot per sampling period; leaves freeze-dried, milled, and analyzed by dry combustion.
  - File: MResCN.csv (FOLIAR_C_PERCENT, R FOLIAR_N_PERCENT).
- Data structure and units
  - Datasets include precise field identifiers: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE/YEAR, REPLICATE, and derived fields for specific measurements.
  - Example description for key files:
    - MResMothLarvaeParasitoids.csv: sample-level moth/parasitoid data with fields for treatment, plot, sampling method, dates, sample IDs, and parasitism status.
    - MResDimensions.csv: hedge height/width measurements with replicate info.
    - MResLeaves.csv: leaf counts and dried leaf weights.
    - MResBranches.csv: total branches per quadrat.
    - MResBranchTips.csv: branch length and counts of growing tips and thorn tips by age category.
    - MResCN.csv: foliar carbon and nitrogen percentages.

## Data quality, provenance, and methodology
- Protocols: Standardised field methods and identification procedures; expert verification of species IDs.
- Quality checks: Anomaly checks, missing value handling, and post-upload validation in the Oracle database.
- Data provenance: Linked to Defra project BD2114 and managed by UKCEH; methods and experimental design described in related Defra reports (2018) and literature cited.
- Documentation: Detailed file-level metadata provided for each dataset, ensuring traceability from field collection to final data products.

## Usage and outputs
- Analysts can use the dataset to assess how hedgerow cutting regimes influence:
  - Moth diversity, community composition, and parasitism rates.
  - Resource provisioning metrics such as hawthorn flowering, berry yields, and hedgerow structure.
  - Relationships between foliar chemistry and moth community metrics.
- Potential outputs include time-series style assessments by treatment, standardized biodiversity indicators, and maps/charts illustrating habitat quality across treatments.
- The data are suitable for integration with other hedgerow management datasets to enhance cross-study comparability and long-term monitoring efforts.

## References and funding
- Publication: Facey SL, Botham MS, Heard MS, Pywell RF, Staley JT (2014). Moth communities and agrienvironment schemes: Examining the effects of hedgerow cutting regime on diversity, abundance, and parasitism. Insect Conservation and Diversity, 7: 543-552.
- Supporting sources: Bremner & Tabatabai (1971); Croxton et al. (2004); Kimber (2013); Maudsley et al. (2002); Sparks & Croxton (2007); Waring & Townsend (2009).
- Funding: Defra project BD2114; UK Centre for Ecology & Hydrology (UKCEH).
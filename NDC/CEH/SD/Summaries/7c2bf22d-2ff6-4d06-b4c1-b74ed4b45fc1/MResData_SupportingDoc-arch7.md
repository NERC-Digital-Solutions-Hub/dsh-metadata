# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview
- A multi-file dataset from long-running hedgerow experiments examining how hedgerow cutting regime affects moth communities, parasitoids, and hedgerow resources.
- Includes moth larvae and parasitoid data, hedgerow architecture measurements, leaf quality metrics, and foliar carbon and nitrogen data.
- Data linked to a controlled, randomised field experiment at Monks Wood, Cambridgeshire (coordinates 52.4026°N, -0.2357°W).

## Experimental design and study site
- Randomised plot experiment conducted 2006–2014 to test timing (autumn vs winter) and frequency (annual, biennial, triennial) of hedgerow cutting.
- Four hedgerows planted in 1961 on former arable land; adjacent unmanaged controls observed.
- Experimental layout: 32 plots per hedge in factorial combination of treatments, with eight replicates for annual plots and four replicates for biennial/triennial plots; cutting occurred with a tractor-mounted flail cutter.
- Annual autumn cuts and winter cuts documented; the scheme aimed to maintain and restore hedgerow habitat quality and food resources for wildlife.
- Experimental design is tied to Defra project BD2114 and related methodology reports.

## Data collected and files
- Files containing data collected from Experiment 1 (Monks Wood MW-Monks Wood site), year 2011:
  - MResMothLarvaeParasitoids.csv: moth larvae species data and associated parasitoid data per sample.
  - MResDimensions.csv: hedgerow height and width measurements per plot/replicate.
  - MResLeaves.csv: leaf counts and leaf weights per plot/replicate.
  - MResBranches.csv: total number of branches in two quadrats per plot.
  - MResBranchTips.csv: growing tip and thorn tip data along sampled branches (replicates, quadrats).
  - MResCN.csv: foliar carbon and nitrogen concentrations per plot.
- All datasets include location and treatment identifiers (Experiment, Site, Block_No, Plot_No, Treatment), sampling dates (Visit_Date, Visit_Year), and replicate information.

## Data structure and key columns (highlights)
- MResMothLarvaeParasitoids.csv:
  - Columns include EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, COLLECTION_METHOD, SAMPLE_NO, MOTH_NAME, PARASITISED, PARASITOID, PARASITOID_FAMILY, PARASITOID_SUBFAMILY, PARASITOID_NOTES, DATE_EMERGED.
- MResDimensions.csv:
  - Includes EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, REPLICATE, HEIGHT (cm), WIDTH (cm).
- MResLeaves.csv:
  - Includes EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, REPLICATE, LEAVES_COUNT, LEAF_SAMPLE_WEIGHT.
- MResBranches.csv:
  - Includes EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, QUADRAT_NO, TOTAL_BRANCHES.
- MResBranchTips.csv:
  - Includes EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, QUADRAT_NO, REPLICATE, BRANCH_LENGTH, GROWING_TIPS, GROWING_TIPS_2YEAR, GROWING_TIPS_3YEAR, THORN_TIPS_1YEAR, THORN_TIPS_2YEAR.
- MResCN.csv:
  - Includes EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, FOLIAR_C_PERCENT, RFOLIAR_N_PERCENT.

## Methods summary
- Moth sampling and rearing (2011):
  - Timed search within 1 m x 0.5 m quadrats at 1.5 m height; 3 minutes per location.
  - Hedgerow beating to dislodge larvae; leaves and mines photographed for identification.
  - Larvae reared to pupation to determine parasitism; adults identified to species level or via established references.
- Hedgerow architecture and resource availability:
  - Height and width measured along hedge at five points per plot.
  - Leaf biomass measured via quadrats at multiple positions; leaves dried and weighed.
  - Branching density and length recorded using 1 m x 0.5 m quadrats; branching structure and tips counted and classified.
- Foliar quality analysis:
  - Foliar carbon and nitrogen concentrations measured from dried leaf samples using dry combustion after grinding.
- Quality controls:
  - Standard protocols, expert identifications, data checks for anomalies, and post-upload completeness checks in Oracle database.

## Data quality and provenance
- Data collected by experienced field surveyors; identifications checked by experts.
- Missing values are due to survey error (not system gaps) and are noted as such.
- Quality assurance steps include standard protocols and post-upload data verification.

## GIS relevance and potential uses
- Spatial representation of hedgerow management regimes and biodiversity responses:
  - Map plots by hedge, treatment type, and replication.
  - Visualize relationships between cutting regime (frequency and timing) and moth/parasitism metrics.
  - Integrate architectural metrics (height, width, leaf biomass, branching) with moth and CN data to explore habitat quality drivers.
- Temporal scope:
  - Treatments implemented 2005–2014 with data collection focused on 2011; supports cross-sectional and longitudinal GIS analyses when combined with other years.
- Coordinate reference:
  - Site coordinates provided; data supports spatial analyses at plot and quadrat scales within hedgerows.

## References and funding
- References include methodological and taxonomic sources for moth identification and hedgerow management effects.
- Funding: Defra BD2114; UK Centre for Ecology & Hydrology (UKCEH).
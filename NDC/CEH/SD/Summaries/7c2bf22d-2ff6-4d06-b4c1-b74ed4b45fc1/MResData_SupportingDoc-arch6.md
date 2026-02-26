# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview
- Dataset of hawthorn moth larvae and parasitoids, with hedgerow architecture and resource availability data.
- Derived from a long-running hedgerow experiment and used to study effects of hedgerow cutting regimes on moth diversity, abundance, and parasitism.
- Associated publication: Facey et al. 2014, Insect Conservation and Diversity.

## Experimental Design and Scope
- Period: 2006–2014, randomised plot experiment at Monks Wood, Cambridgeshire, UK (site coordinates provided).
- Aim: Assess long-term effects of hedgerow management on wildlife habitat quality and food resources; explore restoration/restoration options at scale under ELS and HLS.
- Setup:
  - Four hedgerows planted in 1961 on former arable land.
  - Each hedge divided into 32 contiguous plots (15 m long) with factorial combinations of:
    - Cutting frequency: annual, biennial, triennial
    - Cutting timing: autumn, winter
  - Two unmanaged control plots (no cutting for 15+ years prior to current experiment)
  - Experimental replication: eight replicates for annual plots, four replicates for two-/three-year plots.
- Experiment 1 focused on timing and frequency of cutting and resulting resource provision (flowers, berries) and habitat structure.

## Data Files Included
- MResMothLarvaeParasitoids.csv — moth larva species data and associated parasitoid data per sample.
- MResDimensions.csv — hedgerow height and width measurements for each plot.
- MResLeaves.csv — leaf count and dry weight per plot.
- MResBranches.csv — total number of branches within two quadrats per plot.
- MResBranchTips.csv — tip data per sampled branch (branch length, growing tips, thorn tips across replicates).
- MResCN.csv — foliar carbon and nitrogen concentrations per plot.
- References andFunding sections provide provenance and support details.

## Data Collection Methods
- Moth sampling and rearing (2011:
  - Timed search: 1 m x 0.5 m quadrat at 1.5 m height, sampled at 5 and 10 m along each plot for 3 minutes.
  - Hedgerow beating: plastic gutter method at two locations per plot to dislodge larvae; collected material reared to pupation to assess parasitism.
  - Larvae identified to species; parasitoid status recorded; adults euthanized and identified.
- Hedgerow architecture and resource availability (June measurements):
  - Height and width measured along plots.
  - Leaves: number, total biomass, mean leaf biomass measured using 0.5 m x 0.25 m quadrats; leaves dried and weighed.
  - Branching: density and length measured within 1 m x 0.5 m quadrats; random sampling of five branches per quadrat with measurements of growth tips and thorn tips.
- Foliar quality (CN analysis):
  - Sampling of leaves along plots; leaves freeze-dried, milled, and analyzed for carbon and nitrogen content via dry combustion.

## Variables and Data Structure
- Common fields across datasets:
  - EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, VISIT_YEAR, REPLICATE (where applicable).
- Dataset-specific variables:
  - MResMothLarvaeParasitoids.csv: MOTH_NAME, PARASITISED, PARASITOID, PARASITOID_FAMILY, PARASITOID_SUBFAMILY, NOTES, DATE_EMERGED, SAMPLE_NO.
  - MResDimensions.csv: HEIGHT, WIDTH, REPLICATE.
  - MResLeaves.csv: LEAVES_COUNT, LEAF_SAMPLE_WEIGHT.
  - MResBranches.csv: QUADRAT_NO, TOTAL_BRANCHES.
  - MResBranchTips.csv: BRANCH_LENGTH, GROWING_TIPS, GROWING_TIPS_2YEAR, GROWING_TIPS_3YEAR, THORN_TIPS_1YEAR, THORN_TIPS_2YEAR.
  - MResCN.csv: FOLIAR_C_PERCENT, FOLIAR_N_PERCENT.
- Data linkage:
  - All datasets share core fields to enable integration by Experiment, Site, Block, Plot, Treatment, Visit, and Quadrat/Replicate identifiers.
  - Species and parasitoid identifications linked to moth samples; temporal aspects connect sampling events with treatments.

## Quality Control and Provenance
- Standard protocol followed; species data collected by experienced surveyors and verified by experts.
- Data checks for anomalous values; missing values attributed to survey error (e.g., missed measurements) rather than systematic gaps.
- Data were uploaded to an Oracle database with subsequent missing value input as needed.
- Funding and management acknowledged (Defra BD2114; UK CEH).

## Usage and Related Publication
- Data enabling analyses of:
  - How hedgerow cutting timing and frequency affect hawthorn moth communities and parasitism rates.
  - Relationships between hedgerow structure (height, width, branching) and resource availability (leaves, flowers, berries) with moth abundance and diversity.
  - Foliar quality (carbon and nitrogen) associations with moth community metrics.
- Publication linkage: Facey SL et al. 2014 (Insect Conservation and Diversity) examines effects of hedgerow cutting regimes on diversity, abundance, and parasitism.
- Suitable for data products such as dashboards, self-serve queries, and comparative analyses across hedgerow management treatments.

## References, Funding, and Access
- Methodological and taxonomic references for moth and parasitoid identification, hedgerow measurements, and CN analyses are provided within the dataset documentation.
- Funding: Defra project BD2114; managed by UK Centre for Ecology & Hydrology (UKCEH).
# Moth community and parasitoid data from a hedgerow cutting regime experiment in Cambridgeshire, England, 2011

## Overview
- Dataset from a long-running hedgerow experiment examining how hedgerow cutting timing and frequency affect wildlife habitat quality, resources, and associated moth communities and their parasitoids.
- Data collected as part of an MRes project and linked to a 2014 publication: Facey et al. (Insect Conservation and Diversity).
- Focuses on Experiment 1, which investigates long-term effects of cutting regimes on resource provision for wildlife.
- Components include moth larvae and parasitoid data, hedgerow architecture, and foliar resource quality.

## Experimental design
- Randomised plot experiment conducted 2006–2014 at Monks Wood, Cambridgeshire, UK (four hedgerows planted in 1961 on former arable land).
- Treatments (factorial):
  - Cutting frequency: annual, biennial, triennial
  - Cutting timing: autumn, winter
- Two unmanaged control plots were monitored (not cut in the current experiment).
- Each treatment combination replicated either eight times (annual plots) or four times (two- and three-year plots).
- Experimental timeline and cutting cycles summarized from 2005–2014, with winter cuts in January/February and autumn cuts in September.

## Data files and schema
- MResMothLarvaeParasitoids.csv
  - Fields include: EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, TREATMENT, VISIT_DATE, SAMPLE_NO, MOTH_NAME, PARASITISED, PARASITOID, PARASITOID_FAMILY, PARASITOID_SUBFAMILY, DATE_EMERGED, and related notes.
  - Contains moth larva data and associated parasitoid information identified during rearing.
- MResDimensions.csv
  - Contains hedgerow height and width measurements with REPLICATE, HEIGHT, WIDTH.
- MResLeaves.csv
  - Contains leaf counts and weights per plot: LEAVES_COUNT, LEAF_SAMPLE_WEIGHT, with REPLICATE.
- MResBranches.csv
  - Contains branch counts per quadrat: QUADRAT_NO, TOTAL_BRANCHES, with REPLICATE.
- MResBranchTips.csv
  - Contains branch tip data by quadrat: BRANCH_LENGTH, GROWING_TIPS, GROWING_TIPS_2YEAR, GROWING_TIPS_3YEAR, THORN_TIPS_1YEAR, THORN_TIPS_2YEAR.
- MResCN.csv
  - Contains foliar carbon and nitrogen percentages: FOLIAR_C_PERCENT, FOLIAR_N_PERCENT (R FOLIAR_N_PERCENT).

## Data collection and processing methods
- Moth sampling and rearing (2011)
  - Timed search within a 1 m x 0.5 m quadrat at 1.5 m height (5 m and 10 m along each plot) for three minutes.
  - Hedgerow beating: 2 m section disrupted to dislodge larvae/material; larvae reared to pupation to determine parasitism.
  - Species identified from larvae or reared adults; parasitoids documented with emergence dates and taxonomy where possible.
- Hedgerow architecture and resource measurements
  - Architectural measurements: height and width taken at five points per plot.
  - Resource measurements: leaf biomass and count taken at three points per plot; leaves dried, weighed, and mean leaf biomass computed.
  - Branching metrics: density and length measured via 1 m x 0.5 m quadrats; branching tips recorded and categorized by age (year) where applicable.
- Foliar quality analysis
  - Foliar carbon and nitrogen concentrations measured from freeze-dried leaf samples using dry combustion (Elementar Vario EL CHNS analyzer).
- Quality control
  - Standardised protocols, experienced field surveyors, expert verifications of species identifications, anomaly checks, and handling of missing values due to field error.

## Data interpretation and linking
- Data are structured to be joined by EXPERIMENT, SITE, BLOCK_NO, and PLOT_NO to analyse treatment effects on:
  - Moth communities and parasitoid associations
  - Habitat resource provision (flowering/berry yield proxies, leaves, biomass)
  - Hedgerow structure (height, width, branching)
  - Foliar quality (C and N content)

## Key considerations for analysts
- Experimental design and replication
  - Factorial design with distinct treatment combinations; replication varies by frequency (eight for annual, four for biennial/triennial).
  - Two unmanaged controls provide baseline comparisons.
- Temporal scope
  - Cutting regime spans 2005–2014, but the released data and sampling detailed here focus on 2011 for moths and parasitoids; other files capture structural and foliar metrics that may reflect cumulative effects.
- Data integration
  - Cross-file analyses require careful keying by EXPERIMENT, SITE, BLOCK_NO, PLOT_NO, and sometimes QUADRAT_NO (for branch data).
- Potential analyses
  - Effects of cutting regime on moth abundance, species richness, and parasitism rates.
  - Relationships between hedgerow architectural metrics (height, width, leaf biomass, branching density) and moth/parasitoid metrics.
  - Links between foliar quality (C and N) and herbivore pressure or predator/parasitoid activity.
  - Mixed-effects models with plot or block as random effects and treatment factors as fixed effects; Year as a repeated measure if data permit.
- Limitations and caveats
  - Data availability for 2011 sampling; broader temporal trends may be inferred only from architectural/foliar metrics unless additional years are integrated.
  - Some taxa identifications may be uncertain (micro moths) and rely on larval or limited morphological data.
  - Data quality notes indicate potential missing measurements due to surveyor omission, though overall quality controls are in place.

## References and funding
- Key references supporting methodology and context (e.g., methods for carbon/nitrogen analysis, hedgerow restoration studies, moth identification guides).
- Funding: Defra project BD2114; management by UK Centre for Ecology & Hydrology (UKCEH).
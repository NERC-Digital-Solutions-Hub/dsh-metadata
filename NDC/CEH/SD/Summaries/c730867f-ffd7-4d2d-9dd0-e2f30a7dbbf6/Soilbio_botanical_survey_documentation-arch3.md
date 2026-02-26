# Background

- Context and aims
  - The NERC Soil Biodiversity Thematic Programme (established 1999) conducted intensive study of a large field experiment at Sourhope, Scottish Borders.
  - Primary aims: understand soil biota biodiversity and the functional roles of soil organisms in key ecological processes.
  - Funded 24 research projects studying soil structure, soil processes (carbon and nitrogen cycles), and the roles of micro-, meso-, and macro-fauna.

- Sampling methods and timeline
  - Baseline vegetation (1998): 50 x 50 cm point quadrats, sampled in five subplots per main plot; 25 points per quadrat; presence/absence with potential abundance data.
  - Subplot selection and sampling layout referenced to Scott et al., 2003.
  - Point quadrat surveys (2000–2002): larger scale sampling using a 0.5 m² cell within subplots S, T, U, V; 100-hole grid with a pin dropped through 25 holes per sample to record touched species.
  - Bryophyte identification improved in 2002 (to species level) compared with earlier years.
  - Additional data from 2000 collected as part of joint sampling; separate data release forthcoming.

- Structure of data (datasets and fields)
  - Baseline vegetation (1998): P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
    - Key fields: MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT, BASE_DATE, SPECIES_CODE, SPECIES_NAME, ABUNDANCE
  - Point quadrat data (2000–2002): P2109_BOTANICAL_SURVEY_2000_2002.csv
    - Key fields: YEAR, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT_NO, TREATMENT, SPECIES, SPECIES_COUNT
  - Data coding references: block/plot/sub-plot codes align with Scott et al., 2003; species codes align with Stace, 1997.

- Quality control and data governance
  - Quality checks performed: numeric range checks, formatting conformity, and logical integrity checks.
  - Data are subject to QA procedures, but NERC does not warrant accuracy or fitness for purpose; no liability for loss or damage from use.
  - Metadata and data stewardship considerations noted; some data (e.g., bryophyte identifications) were enhanced in 2002.
  - Additional data from 2000 may be released separately; data provenance and references provided (Scott et al., 2003; Stace, 1997).
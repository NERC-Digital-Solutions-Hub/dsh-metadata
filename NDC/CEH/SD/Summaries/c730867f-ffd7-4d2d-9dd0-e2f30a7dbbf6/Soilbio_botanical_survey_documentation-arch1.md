# Background

- The NERC Soil Biodiversity Thematic Programme (established in 1999) focused on intensive study of a large field experiment at Sourhope (Macaulay/James Hutton Institute) to understand soil biota biodiversity and the functional roles of soil organisms in key ecological processes. Twenty-four projects investigated soil structure, soil processes (e.g., carbon and nitrogen cycles), and the roles of micro-, meso-, and macro-fauna.

- Sampling methods and data collection
  - Baseline vegetation survey (1998): 
    - Method: 50 x 50 cm point quadrats, 25 points per sub-quadrat within selected subplots, presence/absence with potential abundance information.
    - Coverage: Baseline data for subplots within main plots and blocks as defined by the study design.
  - Point quadrat surveys (2000-2002):
    - Method: 0.5 m^2 cell in subplots S, T, U, V; a 100-hole frame with a pin dropped through 25 holes each time to record species touches along the vegetation profile.
    - Years: 2000, 2001, 2002; annual data collection.
    - Bryophyte identification: In 2002, bryophytes identified to species level (improved resolution from earlier years).
    - Subplots: Data collected across subplots with treatments applied (denoted by TREATMENT_NO and TREATMENT).
  - Survey team: S. Buckland, W. Walker, and G. Burt-Smith.

- Structure of data and files
  - Baseline vegetation data (1998): P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
    - Key fields: MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT, BASE_DATE, SPECIES_CODE, SPECIES_NAME, ABUNDANCE
    - Notes: Abundance summarized to sub-plot level; species names follow Stace (1997).
  - Point quadrat data (2000-2002): P2109_BOTANICAL_SURVEY_2000_2002.csv
    - Key fields: YEAR, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT_NO, TREATMENT, SPECIES, SPECIES_COUNT
    - Notes: Data cover years 2000–2002; includes treatment information.
  - Taxonomic reference: Scott et al. (2003) Sourhope Field Data Handbook; Stace (1997) New Flora of the British Isles.

- Quality control and limitations
  - Quality assurance steps included numeric range checks, formatting conformity, and logical integrity checks.
  - Limitations and disclaimers:
    - NERC cannot warrant the accuracy of the data or its fitness for a user’s intended purpose.
    - No liability for loss, damage, injury, or other outcomes arising from use of the data.
  - These cautions imply analysts should validate applicability to their specific questions and consider data provenance and quality when modelling or drawing conclusions.
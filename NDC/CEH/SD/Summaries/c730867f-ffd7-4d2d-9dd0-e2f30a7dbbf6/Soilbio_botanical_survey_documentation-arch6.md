# Background

- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of a large field experiment at Sourhope, Scottish Borders, to understand soil biodiversity and the functional roles of soil organisms in key ecological processes. Twenty-four research projects studied soil structure, soil processes (e.g., carbon and nitrogen cycles), micro-/meso-/macro-fauna and flora.

- Sampling timeline and methods:
  - Baseline vegetation assessment in 1998 using 50 x 50 cm point quadrats across selected subplots to record presence/absence and approximate abundance of species.
  - Subsequent vegetation surveys (2000–2002) used a more extensive point quadrat approach: a 0.5 m² cell within subplots S, T, U, V, with a 100-hole frame and 25-pin drops to generate a detailed vegetation profile, including improved bryophyte identification in 2002.
  - Subplots and blocks were organized within main plots (A–F) and numbered blocks (1–5); specific sampling and treatment contexts were recorded.

- Data products and structure:
  - Two CSV data files are provided:
    - P2109_BOTANICAL_SURVEY_BASELINE_1998.csv (Baseline vegetation data)
      - Key fields: MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT, BASE_DATE, SPECIES_CODE, SPECIES_NAME (Stace, 1997), ABUNDANCE.
    - P2109_BOTANICAL_SURVEY_2000_2002.csv (Point quadrat data)
      - Key fields: YEAR, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT_NO, TREATMENT, SPECIES, SPECIES_COUNT.
  - Data describe abundance per sub-plot for baseline and yearly counts per species per sub-plot for 2000–2002, with bryophyte species identified to species level in 2002.

- Coding, references, and data context:
  - Species nomenclature references: Stace (1997) for plant names.
  - Main structural reference: Scott et al., 2003 (Sourhope Field Data Handbook 2003).
  - Additional data collected in 2000 were part of a joint sampling event and are noted as available separately.

- Quality control and data usage notes:
  - Verification included numeric range checks, formatting conformity, and logical integrity checks.
  - The data are subject to quality assurance procedures, but the NERC cannot warrant accuracy or fitness for a particular use and disclaims liability for any results or outcomes arising from their use.

- Practical implications for data use:
  - Enables analysis of plant community composition and abundance across blocks and treatments.
  - Supports exploration of temporal changes from 1998 baseline to 2000–2002 point quadrat data.
  - Suitable for constructing summaries, dashboards, or reports that compare species counts by plot, block, and treatment, while accounting for data limitations and provenance.
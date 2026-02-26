# SOURHOPE FIELD DATA HANDBOOK 2003

## Aim and context
- NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biota diversity and functional ecological roles.
- The Sourhope field site (Scottish Borders) supported 24 projects on soil structure, processes (C/N cycles), micro- to macro-fauna, and root-feeding invertebrates.
- Primary data described here cover above-ground biomass production and soil/plant mineral nutrients.

## Data collected and methods
- Above-ground biomass (vegetation) measurements:
  - Collected 5 times per growing season (1999–2002) from 50 x 50 cm cells within main plots.
  - Biomass harvested, sorted by species, dried at 80°C, weighed.
  - July 1999 mineral analyses conducted on grass cuttings.
- Experimental treatments:
  - Treatments included nitrogen and lime additions; comparisons between improved (N and/or lime) vs non-improved plots.
  - Observed year-to-year variation, with notable 2001 biomass increase linked to personnel changes and switch to mechanical cutting.

## Data structure and files
- Two CSV data files are provided:
  - Biomass values, 1999-2001: P2109_VEG_BIOMASS_1999_2002.csv
    - Key fields: MEASID, BLOCK (1-5), MAIN_PLOT (A-F), SUB_PLOT, CELL_X, CELL_Y, TREATMENT, MEAS_DATE, BIOMASS (g per 50 x 50 cm cell).
  - Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
    - Key fields: VEG_ID, CUT_DATE, TREATMENT, BLOCK, MAIN_PLOT, NITROGEN (N), CALCIUM (Ca), POTASSIUM (K), MAGNESIUM (Mg), PHOSPHORUS (P), ALUMINIUM (Al); includes limits of detection and analytical methods.

## Findings and interpretation
- Biomass displayed a consistent hierarchy across treatments with peak production in July/August each year.
- 2001 showed a substantial biomass increase, attributed to methodological changes (personnel and mechanical cutting).
- Normalisation to a control (C1) year-by-year recommended to identify true effects of nitrogen and lime.
- Statistical analysis (ln-transformed biomass) indicated:
  - Significant differences between improved and non-improved plots.
  - Significant interaction between treatment and year.
  - No significant differences between blocks.

## Data quality and provenance
- Quality control included numeric range checks, formatting checks, and logical integrity checks.
- Laboratory analyses followed internal MLURI QA procedures.
- NERC disclaims liability for data accuracy or fitness for a given use; data provided without warranty.

## Access and references
- Source: Scott, Bell, Kenny, Jeffers, Buckland, Burt-Smith (2003) SourHope Field Data Handbook.
- Available as Supporting Information via the EIDC catalogue (reference provided in the document).
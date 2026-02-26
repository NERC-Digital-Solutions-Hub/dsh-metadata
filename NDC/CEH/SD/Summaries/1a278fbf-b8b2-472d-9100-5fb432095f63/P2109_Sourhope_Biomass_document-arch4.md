# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview
- Describes the NERC Soil Biodiversity Thematic Programme (established 1999) and the Sourhope field experiment in the Scottish Borders, which studied soil biota diversity and the functional roles of soil organisms.
- The programme funded 24 projects examining soil structure, soil processes (e.g., carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna and flora.

## Data Content
- Two CSV datasets are provided:
  - Biomass values, 1999-2001 (P2109_VEG_BIOMASS_1999_2002.csv)
  - Mineral nutrient analysis, 1999 (P2109_BASELINE_99_VEG_MIN_ANAL.csv)
- Biomass dataset captures above-ground vegetation productivity and diversity measures from 50 x 50 cm cells within main plots across 1999–2002 seasons, including:
  - Field identifiers: MEASID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y
  - Treatments and timing: TREATMENT, MEAS_DATE
  - Outcome: BIOMASS (dry weight per cell)
- Baseline mineral analysis dataset captures vegetation nutrient content (N, Ca, K, Mg, P, Al) with:
  - Sample identifiers: VEG_ID, CUT_DATE
  - Field identifiers: BLOCK, MAIN_PLOT, NITROGEN, CALCIUM, POTASSIUM, MAGNESIUM, PHOSPHORUS, ALUMINIUM
  - Notes on detection limits and units

## Data Structure and Metadata
- Biomass file fields and descriptions referenced to Scott et al., 2003.
- Metadata concepts include:
  - Block and plot structure (BLOCK, MAIN_PLOT, SUB_PLOT)
  - Spatial grid within plots (CELL_X, CELL_Y)
  - Treatment codes (TREATMENT)
  - Date of measurement (MEAS_DATE)
  - Biomass measurement (BIOMASS in grams per 50 x 50 cm cell)
- Nutrient dataset fields and descriptions include sample identifiers (VEG_ID), cut date, treatment, block/plot, and nutrient contents with units in g/100 g (%), plus detection limits.

## Data Quality and Provenance
- Quality control steps included:
  - Numeric range checks
  - Data formatting checks
  - Logical integrity assessments
  - Laboratory analyses subjected to internal MLURI quality procedures
- Important caveat from NERC:
  - Data are subject to quality assurance, but no warranty or liability for accuracy or fitness for purpose is provided by NERC or the Soil Biodiversity Programme.

## Data Processing and Analysis Notes
- Biomass results showed a consistent biomass hierarchy across treatments, with peak production in July/August each year.
- A notable rise in 2001 biomass likely due to personnel changes and a switch from manual cutting to mechanical shears.
- Normalisation against a reference (C1) per year is recommended to compare productivity trends (to account for year-specific changes).
- Analyses (ln-transform of biomass, ANOVA) indicated:
  - Significant differences between improved (N and/or L added) versus non-improved plots
  - Significant treatment-by-year interaction
  - No significant differences between blocks

## Implications for Data Leaders (Usage and Governance)
- Demonstrates the importance of:
  - Clear data structure and lineage (how plots, cells, and treatments map to outcomes)
  - Rich metadata to support cross-study comparability (e.g., plot design, treatment codes)
  - Documentation of data collection changes over time (e.g., switch to mechanical shears) and the need for normalisation when comparing years
  - Transparent quality assurance and clear liability statements to manage user expectations
- Data discoverability and reuse facilitated by linking to the Sourhope Field Data Handbook (Supporting Information) and formal data handbooks.
- The datasets are best used in conjunction with the Scott et al. 2003 reference for interpretation of methods and context.

## Sources and References
- R. Scott, J. Bell, C. Kenny, J. Jeffers, S. Buckland and G. Burt-Smith (2003) SOURHOPE FIELD DATA HANDBOOK 2003. Available as Supporting Information via EIDC catalogue record.
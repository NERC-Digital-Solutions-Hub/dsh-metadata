# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview and aims
- NERC Soil Biodiversity Thematic Programme (1999) studied soil biota diversity and functional roles at Sourhope, with 24 projects on soil structure, processes, and various soil-dwelling organisms.
- Primary data themes include above-ground biomass production, species composition, and related soil processes, collected from a long-term field experiment.

## Data collected and purpose
- Above-ground biomass (grass) measurements:
  - Collected 5 times per growing season across 1999–2002 from 50 x 50 cm cells within main plots and sub-plots.
  - Biomass samples were dried (80°C) and weighed; July biomass data also lie in the dataset.
- Mineral nutrient analyses (baseline 1999):
  - Analyzed vegetation for N, Ca, K, Mg, P, and Al; patterns linked to soil treatments.
  - Lab analyses conducted by Macaulay Land Use Research Institute (MLURI).

## Data structure and format
- Two CSV data files (as provided):
  - Biomass values, 1999-2001: P2109_VEG_BIOMASS_1999_2002.csv
    - Key fields: MEASID, BLOCK (1–5), MAIN_PLOT (A–F), SUB_PLOT, CELL_X, CELL_Y, TREATMENT, MEAS_DATE, BIOMASS (g per 50 x 50 cm cell)
  - Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
    - Key fields: VEG_ID, CUT_DATE, TREATMENT, BLOCK, MAIN_PLOT, NITROGEN (N), CALCIUM (Ca), POTASSIUM (K), MAGNESIUM (Mg), PHOSPHORUS (P), ALUMINIUM (Al)
    - Includes method details and detection limits for each element
- Data context notes:
  - Descriptions and units are provided for each field; references to Scott et al., 2003
  - Some fields include measurement methods and detection limits

## Data provenance and quality control
- Quality checks:
  - Numeric range checks, formatting conformity, and logical integrity checks
  - Internal MLURI quality procedures for laboratory analyses
- Documentation and liability:
  - NERC does not warrant data accuracy or fitness for a specific use; no liability for any outcomes from data use
- Documentation references:
  - Source: SOURHOPE FIELD DATA HANDBOOK 2003 (Scott et al.)

## Temporal changes and interpretation notes
- Observed 2001 biomass increase attributed to staff changes and switch from manual cutting to mechanical shears
- Analyses suggest normalizing treatment effects against a control (C1) to identify lasting impacts of nitrogen and lime
- Statistical notes:
  - Biomass data were ln-transformed for ANOVA
  - Significant differences between improved (N and/or L) vs non-improved plots; year-by-treatment interaction significant; block effects not significant

## Access, citation, and reuse
- Primary citation: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003)
- Availability: Supporting Information via the EIDC catalogue
- File references for datasets provided above; methods and results documented in the handbook

## Governance, metadata, and sustainability considerations for Data Stewards
- Metadata alignment:
  - Ensure consistent field names, descriptions, units, and measurement methods are captured in metadata
  - Link datasets to the Scott et al. (2003) handbook for provenance and scope
- Data provenance and lineage:
  - Track lab analyses, data collection dates, plot configurations (BLOCK, MAIN_PLOT, SUB_PLOT), and treatment details
- Data quality and liability:
  - Maintain QA steps (range checks, formatting, logic) and note the liability disclaimer from NERC
- Data updates and interoperability:
  - Plan for versioning and updates given potential changes (e.g., personnel or protocol shifts)
  - Be prepared to normalise across years or datasets to enable cross-year comparability
- Access and sharing considerations:
  - Document any access restrictions or embargoes; ensure proper citation and attribution
  - Maintain cross-references to the field handbook and supporting information for users

## Practical implications and recommendations
- For data stewards handling these datasets:
  - Preserve the two-file structure but ensure clear cross-references between biomass and nutrient analyses
  - Maintain robust metadata, including units, measurement methods, and data curation steps
  - Document any year-specific changes (e.g., measurement methodology) that affect comparability
  - Provide guidance on normalisation and analysis approaches to account for temporal changes
  - Include the disclaimer and liability statements for users who might apply the data to new contexts

## Challenges highlighted for stewarding these data
- Incomplete understanding of user needs and priorities
- Timely access to data from multiple sources and formats
- Achieving consistent metadata and metadata quality across datasets
- Handling large datasets and potentially outdated databases requiring bespoke solutions
- Ensuring updates are captured and shared while respecting sharing limitations and provenance
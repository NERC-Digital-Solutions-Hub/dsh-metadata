# Background The NERC Soil Biodiversity Thematic Programme

## Overview and aims
- Established in 1999; centered on intensive study of a large field experiment at Sourhope (Scottish Borders) to understand soil biodiversity and the functional roles of soil organisms in key ecological processes.
- Funded 24 projects covering soil structure, processes (carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna and flora.

## Study site and data context
- Site: Sourhope Field (Macaulay Land Use Research Institute, now James Hutton Institute), grid NT8545019630.
- Focus areas include aboveground biomass production, species composition, and relative abundance within the soil-biota context.

## Sampling methods and design
- Baseline vegetation (1998): 50 x 50 cm point quadrats across randomly selected subplots; 25 points per quadrat recorded for presence/absence with potential abundance data; multiple sub-sections per main plot mapped.
- Longitudinal sampling (2000–2002): Point quadrat method within 0.5 m^2 cells per sub-plot; 100-hole grid with a pin dropped through 25 holes to record species touched; annual data for years 2000, 2001, 2002.
- Bryophyte identification progressed to species level in 2002.
- Researchers: S. Buckland, W. Walker, G. Burt-Smith.

## Data structure and files
- Two CSV files:
  - P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
    - Columns: MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT, BASE_DATE, SPECIES_CODE, SPECIES_NAME, ABUNDANCE
  - P2109_BOTANICAL_SURVEY_2000_2002.csv
    - Columns: YEAR, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT_NO, TREATMENT, SPECIES, SPECIES_COUNT
- Taxonomic references: Stace (1997) for species names; validation aligns with Scott et al. (2003) Sourhope Field Data Handbook.

## Quality control and governance
- QA procedures include numeric range checks, formatting conformity, and logical integrity checks.
- Data provided with no warranty or liability from NERC regarding accuracy or fitness for a user’s purpose.

## Accessibility and references
- Data (and related materials) available as Supporting Information via the EIDC catalogue (Sourhope Field Data Handbook 2003).
- Key references:
  - Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK)
  - Stace, 1997 (New flora of the British Isles)

## Implications for data leadership
- Demonstrates the importance of clearly defined data collection methods, longitudinal data structure, and explicit metadata (plot codes, dates, treatments).
- Highlights need for robust data quality checks and clear disclaimers on data usability and liability.
- Illustrates discoverability and reusability through standardized file naming, documented data fields, and external catalog references.
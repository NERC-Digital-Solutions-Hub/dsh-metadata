# NERC Soil Biodiversity Thematic Programme

## Overview
- Initiated in 1999, centered on a large field experiment at Sourhope, Scottish Borders, to study changes in aboveground biomass, species composition, and diversity of soil biota.
- Aimed to understand soil biodiversity and the functional roles of soil organisms (across bacteria, nematodes, protozoa, fungi, micro- to macro-fauna) and their roles in key ecological processes.
- Funded 24 separate projects examining soil structure, soil processes (e.g., carbon and nitrogen cycles), and the roles of various soil organisms.

## Data Collection and Methods

- Baseline vegetation survey (1998)
  - Method: 50 x 50 cm point quadrats in randomly selected subplots within main plots; 25 points per quadrat.
  - Data: presence/absence with an implied abundance record (based on number of hits per species).
  - Subsections for vegetation survey detailed across multiple plots.

- Point quadrat surveys (2000–2002)
  - Method: Within subplots S, T, U, V, a separate 0.5 m² cell was surveyed each year.
  - Procedure: 100-hole grid with a large pin dropped through 25 holes each time; record every occurrence a species is touched by the pin.
  - 2002 enhancement: bryophyte identification to species level (improved resolution compared with earlier years).

- Survey governance
  - Lead surveyors: S. Buckland, W. Walker, and G. Burt-Smith.

## Data Structure and Files

- Baseline vegetation from 1998
  - File: P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
  - Key fields: MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT, BASE_DATE, SPECIES_CODE, SPECIES_NAME, ABUNDANCE.

- Point quadrat data (2000–2002)
  - File: P2109_BOTANICAL_SURVEY_2000_2002.csv
  - Key fields: YEAR, SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT_NO, TREATMENT, SPECIES, SPECIES_COUNT.

- References for taxonomy and protocol
  - Scott et al., 2003. SOURHOPE FIELD DATA HANDBOOK 2003 (Supporting Information via EIDC catalogue).
  - Stace, C. (1997). New flora of the British Isles.

## Quality Control and Limitations

- Quality assurance processes
  - Numeric range checks, formatting conformity, and logical integrity checks.

- Limitations and liability
  - Data are subject to QA procedures, but NERC does not warrant accuracy or fitness for a particular use.
  - No liability for loss or damage arising from use of these data.

## Access, Provenance, and Related Resources

- Data availability
  - Datasets are provided as CSV files with documented fields and structure.
  - Related documentation and additional data (e.g., 2000 joint sampling data) referenced in accompanying materials.

- External access
  - Supporting information and catalogue entry available via the Environmental Information Data Centre (EIDC) and CEH catalogue records, including a link to the dataset documentation.